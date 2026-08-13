# Resolution Algorithm for Propositional Logic
# Five Example Problems

def resolve(clause1, clause2):
    """
    Applies the resolution rule to two clauses.
    """
    resolvents = []

    for literal in clause1:
        opposite = "¬" + literal if not literal.startswith("¬") else literal[1:]

        if opposite in clause2:
            new_clause = (clause1 - {literal}) | (clause2 - {opposite})
            resolvents.append(new_clause)

    return resolvents


def resolution(clauses, goal):
    """
    Proves the goal using resolution by contradiction.
    """

    print("\nNegated Goal:", "¬" + goal)

    # Add negation of goal
    clauses = [set(c) for c in clauses]
    clauses.append({"¬" + goal})

    print("\nInitial Clauses:")
    for i, clause in enumerate(clauses, 1):
        print("C" + str(i), "=", clause)

    step = 1

    while True:
        new_clauses = []

        for i in range(len(clauses)):
            for j in range(i + 1, len(clauses)):

                resolvents = resolve(clauses[i], clauses[j])

                for result in resolvents:

                    print(
                        "\nResolution Step", step,
                        ":", clauses[i], "and", clauses[j],
                        "=>", result
                    )

                    step += 1

                    # Empty clause obtained
                    if len(result) == 0:
                        print("\nEmpty Clause (□) obtained!")
                        print("Goal is PROVED.")
                        return True

                    if result not in clauses and result not in new_clauses:
                        new_clauses.append(result)

        if not new_clauses:
            print("\nNo new clauses can be generated.")
            print("Goal cannot be proved.")
            return False

        clauses.extend(new_clauses)


# ---------------------------------------------------------
# QUESTION 1 - RAIN AND WET GROUND
# ---------------------------------------------------------

print("=" * 60)
print("QUESTION 1 - RAIN AND WET GROUND")
print("=" * 60)

# R -> W  becomes  ¬R OR W
clauses_q1 = [
    {"¬R", "W"},
    {"R"}
]

print("\nKnowledge Base:")
print("1. R -> W")
print("2. R")

print("\nGoal: W")

resolution(clauses_q1, "W")


# ---------------------------------------------------------
# QUESTION 2 - STUDENT ASSIGNMENT SUBMISSION
# ---------------------------------------------------------

print("\n" + "=" * 60)
print("QUESTION 2 - STUDENT ASSIGNMENT SUBMISSION")
print("=" * 60)

# S -> M becomes ¬S OR M
clauses_q2 = [
    {"¬S", "M"},
    {"S"}
]

print("\nKnowledge Base:")
print("1. S -> M")
print("2. S")

print("\nGoal: M")

resolution(clauses_q2, "M")


# ---------------------------------------------------------
# QUESTION 3 - LIBRARY MEMBERSHIP
# ---------------------------------------------------------

print("\n" + "=" * 60)
print("QUESTION 3 - LIBRARY MEMBERSHIP")
print("=" * 60)

# L -> B becomes ¬L OR B
clauses_q3 = [
    {"¬L", "B"},
    {"L"}
]

print("\nKnowledge Base:")
print("1. L -> B")
print("2. L")

print("\nGoal: B")

resolution(clauses_q3, "B")


# ---------------------------------------------------------
# QUESTION 4 - PLACEMENT ELIGIBILITY
# ---------------------------------------------------------

print("\n" + "=" * 60)
print("QUESTION 4 - PLACEMENT ELIGIBILITY")
print("=" * 60)

# A -> E becomes ¬A OR E
clauses_q4 = [
    {"¬A", "E"},
    {"A"}
]

print("\nKnowledge Base:")
print("1. A -> E")
print("2. A")

print("\nGoal: E")

resolution(clauses_q4, "E")


# ---------------------------------------------------------
# QUESTION 5 - ACCESS CONTROL SYSTEM
# ---------------------------------------------------------

print("\n" + "=" * 60)
print("QUESTION 5 - ACCESS CONTROL SYSTEM")
print("=" * 60)

# P -> A becomes ¬P OR A
# A -> G becomes ¬A OR G
clauses_q5 = [
    {"¬P", "A"},
    {"¬A", "G"},
    {"P"}
]

print("\nKnowledge Base:")
print("1. P -> A")
print("2. A -> G")
print("3. P")

print("\nGoal: G")

resolution(clauses_q5, "G")


print("\n" + "=" * 60)
print("ALL FIVE QUESTIONS COMPLETED")
print("=" * 60)
