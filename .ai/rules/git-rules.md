# Git Rules

## 1. Purpose

These rules govern version control and engineering history in the ORNITHOPTER repository.

---

## 2. Engineering History

Git history is part of the engineering record.

Important engineering changes must remain traceable.

---

## 3. Commit Scope

Commits should represent coherent changes.

Prefer:

```text
Add wing structural sizing calculation
```

over:

```text
update stuff
```

---

## 4. Commit Messages

Commit messages should describe what changed.

Recommended structure:

```text
<area>: <change>
```

Examples:

```text
aero: add preliminary lift model
structures: update spar sizing
mechanism: add crank-rocker model
simulation: add CFD baseline case
verification: review wing load calculation
docs: document mass budget
```

---

## 5. Avoid Mixing Unrelated Changes

Do not combine unrelated engineering changes into a single commit when separation would improve traceability.

---

## 6. Never Hide Engineering Changes

Do not silently overwrite:

* requirements,
* calculations,
* assumptions,
* design decisions,
* test results,
* or validation records.

When changing them, preserve the reason for the change.

---

## 7. Experimental Data

Raw experimental data must not be modified to make results appear better.

If processing is required:

```text
raw data
→ processing
→ processed data
→ analysis
```

The raw data must remain preserved.

---

## 8. Generated Files

Avoid committing unnecessary generated files.

Generated results should only be committed when they are useful for:

* reproducibility,
* traceability,
* review,
* documentation,
* or validation.

---

## 9. Large Files

Large binary files such as:

* CAD assemblies,
* simulation outputs,
* videos,
* large datasets,

should be handled deliberately.

Do not commit large files simply because they exist locally.

---

## 10. Branches

Branches may be used for:

* experimental designs,
* major architecture changes,
* risky modifications,
* isolated development,
* or parallel engineering investigations.

The main branch should represent the current accepted project state.

---

## 11. Review

Important engineering changes should be reviewed before becoming part of the accepted system baseline.

---

## 12. Reproducibility

A repository checkout should provide enough information to understand the engineering state associated with that version.

---

## 13. Forbidden Behavior

Never:

* rewrite history to hide engineering mistakes,
* delete failed experiments merely because they failed,
* commit secrets or credentials,
* commit personal API keys,
* or remove traceability from important engineering changes.
