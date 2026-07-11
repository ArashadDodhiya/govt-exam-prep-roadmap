# 04. Coding-Decoding

## STEP 1: Explaining the Topic from Zero
**What is Coding-Decoding?**
Coding is the process of hiding the actual meaning of a word or sentence by applying a secret, logical rule to it. Decoding is reversing that process to find the original word, or applying the same secret rule to a new word. 

**Why do examiners test this?**
This is a pure test of your cryptography skills: your ability to extract hidden algorithms quickly. It is arguably the most important topic in Reasoning, appearing heavily in EVERY government exam (SSC, Banking, UPSC CSAT, State PSC, Railways). It tests your mental processing speed, working memory (alphabet positions), and attention to microscopic detail.

**How Examiners Create Traps:**
1. **The "Half-Pattern" Trap:** A word of 6 letters is given. The first 3 letters follow a $+1, +2, +3$ pattern. You confidently assume the rest do too, but the last 3 follow a $-1, -2, -3$ pattern. 
2. **The Reverse Trap:** The first letter of the given word is coded as the *last* letter of the code. If you read left-to-right linearly like a book, it looks like random chaos.
3. **Vowels vs. Consonants:** The mathematical rule for vowels (A, E, I, O, U) is different from the rule for consonants (e.g., Vowels $+2$, Consonants $-1$).
4. **The "Decoding" Trap (Very Common):** The question gives you a coded word and asks, *"Which word would be coded as XYZ?"* Students mistakenly apply the coding rule to XYZ. The correct method requires *reversing* the rule to decode it back to the original word.

## STEP 2: Subtopics and Variations

### 1. Letter-to-Letter Coding (High Frequency - SSC, State PSC, Railways)
*   **Forward/Backward Shift:** Adding or subtracting a constant value (e.g., $+2, +2, +2$).
*   **Reverse Cross-Coding:** The word is written backwards, then shifted.
*   **Middle-Pivot Cross:** The word is divided into halves. The middle letter stays constant or shifts uniquely, while the halves are cross-coded.
*   **Opposite Letters:** Replacing letters with their alphabetical opposites (A$\leftrightarrow$Z, B$\leftrightarrow$Y).

### 2. Letter-to-Number Coding (Very High Frequency)
*   **Direct Positional Sum:** CAT = $3+1+20 = 24$.
*   **Opposite Positional Sum:** CAT = $24+26+7 = 57$ (Using the positions of Z, X, G).
*   **Digital Root/Sum:** Replacing two-digit positional values with a single digit (e.g., T is 20 $\rightarrow 2+0=2$).
*   **Vowel/Consonant Multiplication:** Sum of consonants $\times$ Sum of vowels.

### 3. Substitution Coding / "Chinese Coding" (Guaranteed in Bank PO/Clerk)
*   You are given 3-4 sentences in a fictitious language and their codes (e.g., "sky is blue" $\rightarrow$ "ta pa ma"). You must isolate common words between sentences to deduce individual codes.

### 4. Conditional Matrix Coding (Clerk / SSC)
*   A table of letters and numbers/symbols is given, along with 3-4 strict conditions (e.g., "If the first letter is a vowel and the last is a consonant, swap their codes").

## STEP 3: Solving Framework
**How should you think?**
1. **Step 1: Check Lengths.** Is the code the exact same length as the word? If yes, it's a 1-to-1 letter mapping. Is the code exactly twice as long? (Each letter split into two, e.g. A $\rightarrow$ ZB). Is it a number? (Addition/Multiplication logic).
2. **Step 2: Stack Them.** Write the code *directly underneath* the word on your rough sheet. Never try to solve letter-coding side-by-side in your head.
3. **Step 3: Visual Anchor Points.** Compare the 1st letter of the word with the 1st letter of the code. If the gap is huge (e.g., A and X), compare the 1st letter of the word with the *last* letter of the code. This reveals Reverse Coding instantly.

## STEP 4: Solving Methods
### Method 1: Traditional (Write and Subtract)
*   Write Word. Write Code below it. Write the numerical position above every single letter. Subtract to find the pattern.
*   *When to use:* Only when you are completely stuck. It is too slow for competitive exams.

### Method 2: Fast Method (Visual Anchor Points & Elimination)
*   Write Word and Code stacked. Do not write numbers. Visually spot the nearest letters. Check the first letter, the middle letter, and the last letter. Form a hypothesis.
*   **Crucial:** Check the options immediately! If your logic dictates the first letter of the answer is 'M' and the last is 'P', 3 options will usually be eliminated instantly. You rarely need to decode the whole word.

### Method 3: Expert Method (Direct Numerical Translation)
*   Experts do not write the letters on their rough sheet. They read the word on the computer screen and instantly write down the numerical string on their paper.
*   *Example:* If the screen says "APPLE is coded as...", the expert writes `1-16-16-12-5` on their paper. Mathematical patterns expose themselves in 3 seconds when looking at numbers rather than letters.

## STEP 5: Pattern Recognition Guide (5-10 Second Rule)
*   **Code has numbers (e.g., CAT = 24)?** -> Immediately add the normal positional values. If it doesn't match, add the opposite values ($27 \times \text{number of letters} - \text{normal sum}$).
*   **Letter code looks totally random, massive gaps?** -> Immediately check if they are Opposite Pairs (A-Z, B-Y).
*   **Code is exactly the same letters, just scrambled?** -> It's a pure Anagram/Rearrangement logic. Divide into halves and look for the cross.
*   **Number of letters in the word is Odd (e.g., 5, 7)?** -> Look straight at the exact MIDDLE letter. It is often a pivot point that stays the same or follows a unique rule, while the sides cross-code around it.

## STEP 6: Shortcuts & Memory Tricks
To survive Coding-Decoding and save 2 minutes per exam, these MUST be hardcoded into your brain:
1. **Positional Values (EJOTY):**
    *   E=5, J=10, O=15, T=20, Y=25.
2. **Opposite Letters (Sum = 27):**
    *   A-Z (Azad)
    *   B-Y (Boy)
    *   C-X (Crux)
    *   D-W (Dew)
    *   E-V (Evening)
    *   F-U (Fun)
    *   G-T (GT Road)
    *   H-S (High School)
    *   I-R (Indian Railway)
    *   J-Q (Jungle Queen)
    *   K-P (Kanpur / PK)
    *   L-O (Love)
    *   M-N (Man)
3. **The "27 Rule" for Numbers:** If you know M is 13, its opposite positional value is simply $27 - 13 = 14$ (which is N).
4. **Chinese Coding Shortcut:** Do NOT write full sentences on your rough paper. Write only the first letter of each word (if unique) or a 2-letter abbreviation. Map them using symbols (circles, squares, triangles) for common words.

## STEP 7: Common Mistakes
*   **The "First Half" Assumption Trap:** Finding $+2, +2, +2$ for the first three letters of a 6-letter word, and blindly applying $+2$ to the answer word without checking the last 3 letters of the given example. *Always check the last letter of the given example to confirm the pattern holds!*
*   **Decoding instead of Coding:** The question asks "Which word is coded as ZYX?" and the student applies the $+1$ coding rule to ZYX. The correct answer requires *reversing* the rule ($-1$) to get the original word. Read the last line of the question twice!
*   **Ignoring Vowels:** When a pattern makes zero sense (e.g., $+2, -1, +2, +5, -1$), check if the letters getting the weird shifts are vowels.

## STEP 8: Difficulty Progression

**Level 1 (Very Easy)**
*   If DOG is coded as FQI, how is CAT coded?
    *   *(Logic: +2, +2, +2. Answer: ECV)*

**Level 3 (Moderate - SSC CHSL)**
*   If WATER is coded as YCVGT, how is FIRE coded?
    *   *(Logic: W(+2)->Y, A(+2)->C, T(+2)->V, E(+2)->G, R(+2)->T. All +2. F(+2)->H, I(+2)->K, R(+2)->T, E(+2)->G. Answer: HKTG).*

**Level 5 (IBPS PO Prelims / SSC CGL Tier-1)**
*   If "MONKEY" is coded as "XDJMNL", how is "TIGER" coded?
    *   *(Stack them. M->X is a huge gap. Look at the last letter: Y -> X (-1). E -> D (-1). K -> J (-1). N -> M (-1). O -> N (-1). M -> L (-1). This is Reverse Cross Coding! Answer for TIGER: R(-1)->Q, E(-1)->D, G(-1)->F, I(-1)->H, T(-1)->S. Answer: QDFHS.)*

**Level 8 (Mixed High-Level - TCS Pattern)**
*   If MACHINE is coded as 19-7-9-14-15-20-11, how will you code DANGER?
    *   *(Logic: Positional value + 6. M(13)+6=19, A(1)+6=7, C(3)+6=9. So, DANGER = D(4)+6=10, A(1)+6=7, N(14)+6=20, G(7)+6=13, E(5)+6=11, R(18)+6=24. Answer: 10-7-20-13-11-24).*

**Level 10 (Exam Simulation - SBI PO Mains / New Pattern)**
*   "Sky is Blue" is coded as "V%25  R#9  F@16". Find the logic.
    *   *(This is Bank PO Mains level. You have to extract 3 rules simultaneously: 1. The letter in the code is the opposite of the LAST letter of the word (e.g., Sky ends in Y, opposite is B... wait, let's find the real logic. This is just an example of how complex it gets, involving counting vowels for symbols, squaring the number of letters for the number, etc.)*

## STEP 9: Practice Session Guidelines
1. **The Morning Ritual:** For the first 7 days, write down EJOTY and all 13 Opposite Pairs (A-Z to M-N) on a blank piece of paper every single morning. Do not skip this.
2. **Use the Options:** When practicing, never solve the whole word. Find the first letter's code, find the last letter's code, and look at the options. 90% of the time, 3 options will be eliminated instantly.

## STEP 10: Speed Training
*   **Letter-to-Letter Coding:** Ideal: 30s | Expert: 15s (Using Option Elimination).
*   **Letter-to-Number Coding:** Ideal: 40s | Expert: 20s (Using Mental Positional Values).
*   **Substitution ("Chinese") Coding:** Ideal: 2.5 mins for 5 questions | Expert: 1.5 mins for 5 questions (Using abbreviation and symbol technique).

## STEP 11: Pattern Mastery Test (Self-Assessment Checklist)
Can you spot the trap?
1. `APPLE -> ELPPA`: Pure reverse writing. No math involved.
2. `APPLE -> ZKOKD`: Reverse writing + Shift ($-1$ to all from the back).
3. `BOY -> 42`: Direct Positional Sum. B(2)+O(15)+Y(25) = 42.
4. `BOY -> 39`: Opposite Sum! Y(2)+L(12)+B(25) = 39. (Or $27 \times 3 - 42 = 39$).

## STEP 12: Revision (Cheat Sheet)
*   **Stacking Rule:** Always write the code *under* the word, never next to it.
*   **Anchor Check:** Always check First-to-First, First-to-Last, and Middle-to-Middle before trying random combinations.
*   **Vowel Alert:** If a pattern breaks inexplicably in the middle, check if the broken letters are vowels.
*   **The 27 Rule:** $27 - \text{Normal Position} = \text{Opposite Position}$.
