# FormLab safety boundary

FormLab is a source snapshot of Formwheel, not yet an executable sandbox. The sync workflow copies the upstream file tree and intentionally disables scripts in HTML entry points. This avoids accidental use of Formwheel's production Firebase data while a separate Firebase project is not configured.

The BETA LAB toggles are currently stored in localStorage on the Formwheel origin, so they **cannot** be read by FormLab on a different origin. Future implementation must use authenticated per-user storage with strict rules, and only then activate experiments. No cross-origin sync is claimed.

Run the **Sync Formwheel source into FormLab** workflow manually in Actions. Do not remove safe mode until sandbox authentication, database isolation, and tests are complete.
