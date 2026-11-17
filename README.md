# ExamBPPP Mobile – APK Build

1. Upload isi folder ini ke repo GitHub (branch `main`).
2. Tab **Actions** → **Build APK** → hasil di **Artifacts** / **Releases**.

Alur: `source/*.apk` → apktool decode → `app/` → `patch/patch_mod.py` (popup "Mod by Fikri Everly") → apktool build → zipalign → sign.
Edit kode/resource di `app/` (ambil dari artifact `*-decoded-source`, commit ke repo) lalu push untuk build ulang.

Signing sendiri (opsional): secrets `KEYSTORE_BASE64`, `KEYSTORE_PASS`, `KEY_ALIAS`.
