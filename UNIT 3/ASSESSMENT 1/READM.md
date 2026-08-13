# ============================================================
# ARTIFICIAL INTELLIGENCE - ASSESSMENT 2
# LOGICAL REASONING USING RESOLUTION ALGORITHM
# ============================================================
#
# Problems:
# 1. Rain and Wet Ground
# 2. Student Assignment Submission
# 3. Library Membership
# 4. Placement Eligibility
# 5. Access Control System
#
# ============================================================


# ------------------------------------------------------------
# RESOLUTION FUNCTION
# ------------------------------------------------------------

def resolve(clause1, clause2):

    for literal in clause1:

        # Find complementary literal
        if literal.startswith("NOT_"):
            opposite = literal[4:]
        else:
            opposite = "NOT_" + literal

        # Check whether complementary literal is present
        if opposite in clause2:

            # Remove complementary literals
            new_clause = (clause1 - {literal}) | \
                         (clause2 - {opposite})

            return new_clause

    return None


# ============================================================
# QUESTION 1
# RAIN AND WET GROUND
# ============================================================

print("\n" + "=" * 65)
print("QUESTION 1 - RAIN AND WET GROUND")
print("=" * 65)

print("\nKnowledge Base:")
print("1. If it rains, then the ground becomes wet.")
print("2. It is raining.")

print("\nPropositional Logic:")
print("R -> W")
print("R")

print("\nGoal: W")
print("Negated Goal: NOT_W")

# CNF Clauses
Q1_C1 = {"NOT_R", "W"}
Q1_C2 = {"R"}
Q1_C3 = {"NOT_W"}

print("\nCNF Clauses:")
print("C1 =", Q1_C1)
print("C2 =", Q1_C2)
print("C3 =", Q1_C3)

# Resolution Step 1
Q1_C4 = resolve(Q1_C1, Q1_C2)

print("\nResolution Step 1:")
print(Q1_C1, "+", Q1_C2, "=>", Q1_C4)

# Resolution Step 2
Q1_C5 = resolve(Q1_C4, Q1_C3)

print("\nResolution Step 2:")
print(Q1_C4, "+", Q1_C3, "=>", Q1_C5)

if len(Q1_C5) == 0:
    print("\nEmpty Clause obtained: {}")
    print("Conclusion: Ground is wet. GOAL PROVED.")
else:
    print("\nGoal cannot be proved.")


# ============================================================
# QUESTION 2
# STUDENT ASSIGNMENT SUBMISSION
# ============================================================

print("\n" + "=" * 65)
print("QUESTION 2 - STUDENT ASSIGNMENT SUBMISSION")
print("=" * 65)

print("\nKnowledge Base:")
print("1. If a student submits the assignment, then the student")
print("   receives internal marks.")
print("2. Rahul submitted the assignment.")

print("\nPropositional Logic:")
print("S -> M")
print("S")

print("\nGoal: M")
print("Negated Goal: NOT_M")

# CNF Clauses
Q2_C1 = {"NOT_S", "M"}
Q2_C2 = {"S"}
Q2_C3 = {"NOT_M"}

print("\nCNF Clauses:")
print("C1 =", Q2_C1)
print("C2 =", Q2_C2)
print("C3 =", Q2_C3)

# Resolution Step 1
Q2_C4 = resolve(Q2_C1, Q2_C2)

print("\nResolution Step 1:")
print(Q2_C1, "+", Q2_C2, "=>", Q2_C4)

# Resolution Step 2
Q2_C5 = resolve(Q2_C4, Q2_C3)

print("\nResolution Step 2:")
print(Q2_C4, "+", Q2_C3, "=>", Q2_C5)

if len(Q2_C5) == 0:
    print("\nEmpty Clause obtained: {}")
    print("Conclusion: Rahul receives internal marks. GOAL PROVED.")
else:
    print("\nGoal cannot be proved.")


# ============================================================
# QUESTION 3
# LIBRARY MEMBERSHIP
# ============================================================

print("\n" + "=" * 65)
print("QUESTION 3 - LIBRARY MEMBERSHIP")
print("=" * 65)

print("\nKnowledge Base:")
print("1. If a person is a library member, then the person")
print("   can borrow books.")
print("2. Priya is a library member.")

print("\nPropositional Logic:")
print("L -> B")
print("L")

print("\nGoal: B")
print("Negated Goal: NOT_B")

# CNF Clauses
Q3_C1 = {"NOT_L", "B"}
Q3_C2 = {"L"}
Q3_C3 = {"NOT_B"}

print("\nCNF Clauses:")
print("C1 =", Q3_C1)
print("C2 =", Q3_C2)
print("C3 =", Q3_C3)

# Resolution Step 1
Q3_C4 = resolve(Q3_C1, Q3_C2)

print("\nResolution Step 1:")
print(Q3_C1, "+", Q3_C2, "=>", Q3_C4)

# Resolution Step 2
Q3_C5 = resolve(Q3_C4, Q3_C3)

print("\nResolution Step 2:")
print(Q3_C4, "+", Q3_C3, "=>", Q3_C5)

if len(Q3_C5) == 0:
    print("\nEmpty Clause obtained: {}")
    print("Conclusion: Priya can borrow books. GOAL PROVED.")
else:
    print("\nGoal cannot be proved.")


# ============================================================
# QUESTION 4
# PLACEMENT ELIGIBILITY
# ============================================================

print("\n" + "=" * 65)
print("QUESTION 4 - PLACEMENT ELIGIBILITY")
print("=" * 65)

print("\nKnowledge Base:")
print("1. If a student clears the aptitude test, then the student")
print("   is eligible for placement.")
print("2. Arun cleared the aptitude test.")

print("\nPropositional Logic:")
print("A -> E")
print("A")

print("\nGoal: E")
print("Negated Goal: NOT_E")

# CNF Clauses
Q4_C1 = {"NOT_A", "E"}
Q4_C2 = {"A"}
Q4_C3 = {"NOT_E"}

print("\nCNF Clauses:")
print("C1 =", Q4_C1)
print("C2 =", Q4_C2)
print("C3 =", Q4_C3)

# Resolution Step 1
Q4_C4 = resolve(Q4_C1, Q4_C2)

print("\nResolution Step 1:")
print(Q4_C1, "+", Q4_C2, "=>", Q4_C4)

# Resolution Step 2
Q4_C5 = resolve(Q4_C4, Q4_C3)

print("\nResolution Step 2:")
print(Q4_C4, "+", Q4_C3, "=>", Q4_C5)

if len(Q4_C5) == 0:
    print("\nEmpty Clause obtained: {}")
    print("Conclusion: Arun is eligible for placement. GOAL PROVED.")
else:
    print("\nGoal cannot be proved.")


# ============================================================
# QUESTION 5
# ACCESS CONTROL SYSTEM
# ============================================================

print("\n" + "=" * 65)
print("QUESTION 5 - ACCESS CONTROL SYSTEM")
print("=" * 65)

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
print("Negated Goal: NOT_G")

# CNF Clauses
Q5_C1 = {"NOT_P", "A"}
Q5_C2 = {"NOT_A", "G"}
Q5_C3 = {"P"}
Q5_C4 = {"NOT_G"}

print("\nCNF Clauses:")
print("C1 =", Q5_C1)
print("C2 =", Q5_C2)
print("C3 =", Q5_C3)
print("C4 =", Q5_C4)

# Resolution Step 1
Q5_C5 = resolve(Q5_C1, Q5_C3)

print("\nResolution Step 1:")
print(Q5_C1, "+", Q5_C3, "=>", Q5_C5)

# Resolution Step 2
Q5_C6 = resolve(Q5_C2, Q5_C5)

print("\nResolution Step 2:")
print(Q5_C2, "+", Q5_C5, "=>", Q5_C6)

# Resolution Step 3
Q5_C7 = resolve(Q5_C6, Q5_C4)

print("\nResolution Step 3:")
print(Q5_C6, "+", Q5_C4, "=>", Q5_C7)

if len(Q5_C7) == 0:
    print("\nEmpty Clause obtained: {}")
    print("Conclusion: User is granted access. GOAL PROVED.")
else:
    print("\nGoal cannot be proved.")


# ============================================================
# FINAL RESULTS
# ============================================================

print("\n" + "=" * 65)
print("FINAL RESULTS")
print("=" * 65)

print("\nQuestion 1: Ground is wet - PROVED")
print("Question 2: Rahul receives internal marks - PROVED")
print("Question 3: Priya can borrow books - PROVED")
print("Question 4: Arun is eligible for placement - PROVED")
print("Question 5: User is granted access - PROVED")

print("\nAll five problems were successfully solved")
print("using the Resolution Algorithm.")

print("=" * 65)
