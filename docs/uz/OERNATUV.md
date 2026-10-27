# Örnatiş Qöllanmasi

**Latinga** dasturidan tayyor bajaruvçi fayllarni yuklab oliş yoki manba bitikdan yiğiş orqali foydalanişingiz mumkin.

## 1. Tayyor bajaruvçi fayllarni yuklab oliş
[Releases](https://github.com/yourusername/latinga/releases) sahifasiga öting va operatsion tizimingizga mos faylni tanlang:

### 🐧 Linux
1. `latinga-linux-amd64` faylini yuklab oling.
2. Unga ruxsat bering: `chmod +x latinga-linux-amd64`.
3. Tizimga joylang: `sudo mv latinga-linux-amd64 /usr/local/bin/latinga`.

### 🍎 macOS (Apple Silicon M1/M2/M3)
macOS xavfsizlik çoralari tufayli quyidagi amallarni bajaring:
1. `latinga-macos-arm64` faylini yuklab oling.
2. Terminalda buyruqni bering: `chmod +x latinga-macos-arm64`.
3. Faylni Finder orqali toping, **öng tugmani** bosing va **Open** tanlang.
4. Ogohlantiriş çiqsa, **Open** tugmasini bosing (bu faqat bir marta söraladi).
5. Tizimga joylang: `sudo mv latinga-macos-arm64 /usr/local/bin/latinga`.

### 🪟 Windows
1. `latinga-windows-amd64.exe` faylini yuklab oling.
2. (Ixtiyoriy) Nomini `latinga.exe` ga özgartirib, tizim PATH qismiga qöşişingiz mumkin.

## 2. Cargo orqali örnatiş
```baş
cargo install latinga --features cli
