# Artificial Intelligence – Assessment 2
# Logical Reasoning and Automated Theorem Proving
# Using Resolution Algorithm
#
# Problems:
# 1. Rain and Wet Ground
# 2. Student Assignment Submission
# 3. Library Membership
# 4. Placement Eligibility
# 5. Access Control System


# ---------------------------------------------------------
# RESOLUTION FUNCTION
# ---------------------------------------------------------

def resolve(clause1, clause2):
    for literal in clause1:

        # Find the opposite literal
        if literal.startswith("¬"):
            opposite = literal[1:]
        else:
            opposite = "¬" + literal

        # If opposite literal exists in the second clause
        if opposite in clause2:

            # Remove the complementary literals
            new_clause = (clause1 - {literal}) | \
                         (clause2 - {opposite})

            return new_clause

    return None


# ---------------------------------------------------------
# QUESTION 1
# RAIN AND WET GROUND
# ---------------------------------------------------------

print("=" * 60)
print("QUESTION 1 - RAIN AND WET GROUND")
print("=" * 60)

print("\nKnowledge Base:")
print("1. If it rains, then the ground becomes wet.")
print("2. It is raining.")

print("\nPropositional Logic:")
print("R -> W")
print("R")

print("\nGoal: W")
print("Negated Goal: ¬W")

# CNF
C1 = {"¬R", "W"}
C2 = {"R"}
C3 = {"¬W"}

print("\nCNF Clauses:")
print("C1 =", C1)
print("C2 =", C2)
print("C3 =", C3)

# Resolution Step 1
C4 = resolve(C1, C2)

print("\nResolution Step 1:")
print(C1, "+", C2, "=>", C4)

# Resolution Step 2
C5 = resolve(C4, C3)

print("\nResolution Step 2:")
print(C4, "+", C3, "=>", C5)

if len(C5) == 0:
    print("\nEmpty Clause (□) obtained.")
    print("Conclusion: Ground is wet. GOAL PROVED.")
else:
    print("\nGoal cannot be proved.")


# ---------------------------------------------------------
# QUESTION 2
# STUDENT ASSIGNMENT SUBMISSION
# ---------------------------------------------------------

print("\n" + "=" * 60)
print("QUESTION 2 - STUDENT ASSIGNMENT SUBMISSION")
print("=" * 60)

print("\nKnowledge Base:")
print("1. If a student submits the assignment, then the student")
print("   receives internal marks.")
print("2. Rahul submitted the assignment.")

print("\nPropositional Logic:")
print("S -> M")
print("S")

print("\nGoal: M")
print("Negated Goal: ¬M")

# CNF
C1 = {"¬S", "M"}
C2 = {"S"}
C3 = {"¬M"}

print("\nCNF Clauses:")
print("C1 =", C1)
print("C2 =", C2)
print("C3 =", C3)

# Resolution Step 1
C4 = resolve(C1, C2)

print("\nResolution Step 1:")
print(C1, "+", C2, "=>", C4)

# Resolution Step 2
C5 = resolve(C4, C3)

print("\nResolution Step 2:")
print(C4, "+", C3, "=>", C5)

if len(C5) == 0:
    print("\nEmpty Clause (□) obtained.")
    print("Conclusion: Rahul receives internal marks. GOAL PROVED.")
else:
    print("\nGoal cannot be proved.")


# ---------------------------------------------------------
# QUESTION 3
# LIBRARY MEMBERSHIP
# ---------------------------------------------------------

print("\n" + "=" * 60)
print("QUESTION 3 - LIBRARY MEMBERSHIP")
print("=" * 60)

print("\nKnowledge Base:")
print("1. If a person is a library member, then the person")
print("   can borrow books.")
print("2. Priya is a library member.")

print("\nPropositional Logic:")
print("L -> B")
print("L")

print("\nGoal: B")
print("Negated Goal: ¬B")

# CNF
C1 = {"¬L", "B"}
C2 = {"L"}
C3 = {"¬B"}

print("\nCNF Clauses:")
print("C1 =", C1)
print("C2 =", C2)
print("C3 =", C3)

# Resolution Step 1
C4 = resolve(C1, C2)

print("\nResolution Step 1:")
print(C1, "+", C2, "=>", C4)

# Resolution Step 2
C5 = resolve(C4, C3)

print("\nResolution Step 2:")
print(C4, "+", C3, "=>", C5)

if len(C5) == 0:
    print("\nEmpty Clause (□) obtained.")
    print("Conclusion: Priya can borrow books. GOAL PROVED.")
else:
    print("\nGoal cannot be proved.")


# ---------------------------------------------------------
# QUESTION 4
# PLACEMENT ELIGIBILITY
# ---------------------------------------------------------

print("\n" + "=" * 60)
print("QUESTION 4 - PLACEMENT ELIGIBILITY")
print("=" * 60)

print("\nKnowledge Base:")
print("1. If a student clears the aptitude test, then the student")
print("   is eligible for placement.")
print("2. Arun cleared the aptitude test.")

print("\nPropositional Logic:")
print("A -> E")
print("A")

print("\nGoal: E")
print("Negated Goal: ¬E")

# CNF
C1 = {"¬A", "E"}
C2 = {"A"}
C3 = {"¬E"}

print("\nCNF Clauses:")
print("C1 =", C1)
print("C2 =", C2)
print("C3 =", C3)

# Resolution Step 1
C4 = resolve(C1, C2)

print("\nResolution Step 1:")
print(C1, "+", C2, "=>", C4)

# Resolution Step 2
C5 = resolve(C4, C3)

print("\nResolution Step 2:")
print(C4, "+", C3, "=>", C5)

if len(C5) == 0:
    print("\nEmpty Clause (□) obtained.")
    print("Conclusion: Arun is eligible for placement. GOAL PROVED.")
else:
    print("\nGoal cannot be proved.")


# ---------------------------------------------------------
# QUESTION 5
# ACCESS CONTROL SYSTEM
# ---------------------------------------------------------

print("\n" + "=" * 60)
print("QUESTION 5 - ACCESS CONTROL SYSTEM")
print("=" * 60)

print("\nKnowledge Base:")
print("1. If a user enters the correct password, then the user")
print("   is authenticated.")
print("2. If a user is authenticated, then the user is granted access.")
print("3. The user entered the correct password.")

print("\nPropositional Logic:")
print("P -> A")
print("A -> G")
print("P")

print("\nGoal: G")
print("Negated Goal: ¬G")

# CNF
C1 = {"¬P", "A"}
C2 = {"¬A", "G"}
C3 = {"P"}
C4 = {"¬G"}

print("\nCNF Clauses:")
print("C1 =", C1)
print("C2 =", C2)
print("C3 =", C3)
print("C4 =", C4)

# Resolution Step 1
C5 = resolve(C1, C3)

print("\nResolution Step 1:")
print(C1, "+", C3, "=>", C5)

# Resolution Step 2
C6 = resolve(C2, C5)

print("\nResolution Step 2:")
print(C2, "+", C5, "=>", C6)

# Resolution Step 3
C7 = resolve(C6, C4)

print("\nResolution Step 3:")
print(C6, "+", C4, "=>", C7)

if len(C7) == 0:
    print("\nEmpty Clause (□) obtained.")
    print("Conclusion: User is granted access. GOAL PROVED.")
else:
    print("\nGoal cannot be proved.")


# ---------------------------------------------------------
# FINAL RESULT
# ---------------------------------------------------------

print("\n" + "=" * 60)
print("FINAL RESULT")
print("=" * 60)

print("\n1. Rain and Wet Ground")
print("   Result: Ground is wet - PROVED")

print("\n2. Student Assignment Submission")
print("   Result: Rahul receives internal marks - PROVED")

print("\n3. Library Membership")
print("   Result: Priya can borrow books - PROVED")

print("\n4. Placement Eligibility")
print("   Result: Arun is eligible for placement - PROVED")

print("\n5. Access Control System")
print("   Result: User is granted access - PROVED")

print("\nAll five problems were successfully solved")
print("using the Resolution Algorithm.")
print("=" * 60)
