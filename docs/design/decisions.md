# Design Decisions

## 1. Human review remains a distinct stage

**Benefit.** The final job profile can be checked and corrected by HR.

**Trade-off.** Draft generation and final approval need separate states and interactions.

## 2. Generation does not overwrite a newer human revision

**Benefit.** Concurrent drafting cannot silently replace editorial work.

**Trade-off.** A late result may need to be reviewed as a proposal.

## 3. PDF rendering is separate from AI generation

**Benefit.** The exported document corresponds to a defined content version.

**Trade-off.** Template changes and document history must be managed consistently.
