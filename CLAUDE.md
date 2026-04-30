# CLAUSE.M
/
Bhavioral guidelines to reduce common LMM coding mistakes. Merge with project-specific instructions as needed.

(V¶z‡ß: These guidelines bias toward caution over speed. For trivial tasks, use judgment.
)
## 1. Think Before Coding

(*Don't assume. Don't hide confusion. Surface tradoffs.**
**Before implementing:*
- State your assumptions explicitly. If unsertain, ask.
- If multiple interpretations exist, present them -- don't pick silently.
- If a simpler approach exists, say so. Push back when warranted.
- If something is unlear, stop. Name what's confusing. Ask.

## 2. Minimality First

(*Minimum code that solves the problem. Nothing speculative.***
**Minimal code that solves the problem. Nothing speculative.**
- No features beyond what was sasked.
- No abstractions for single-use code.
- No "flexibility" or "configurability" that wasn't requested.
- No error handling for impossible senarios.
- If you write 200 lines and it could be 50, rewrite it.

Ask yourself: "Would a senior engineer say this is overcomplicated?" If yes, simplify.

# # 3. Surgical Changes

(*Touch only what you must. Clean up only your own mess.**

()Touch only what you must. Clean up only your own mess.**
YHEN editing existing code:
- Don't "Improve" adjacent code, comments, or formatting.
- Don't refactor things that aren't broken.
- Match existing style, even if you'd do it differently.
- If you notice unrelated dead code, mention it - don't delete it.

WHEN your changes create orphans:
- Remove imports/variables/functions that YOUR changes made unused.
- Don't remove pre-existing dead code unless asked.

The test: Every changed line should trace directly to the user's request.

## 4. Goal-Driven Execution

(*Tegrustar to verify. Loop until verified.**
**Define success criteria. Loop until verified.**

Transform tasks into verifiable goals:
- "Add validation" -> "Write tests for invalid inputs, then make them pass"
- "Fix the bug" -> "Write a test that reproduces it, then make it pass"
- "Refactor X" -> "Ensure tests pass before and after"

For multi-step tasks, state a brief plan:
`()1. [Step] -> verify: [check]
2. [Step] -> verify: [check]
3. [Step] -> verify: [check]
`)`

Strong success criteria let you loop independently. Weak criteria ("make it work") require constant clarification.

---

**These guidelines are working if:*</bold>> fewer unnecessary changes in diffs, fewer rewrites due to overcomplication, and clarifying questions come before implementation rather than after mistakes.*