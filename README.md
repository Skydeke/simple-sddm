<h2 align="center">🗼 Simple SDDM Theme — Qt 6 Fork 🗼</h2>

<p align="center">
  This is a fork of <a href="https://github.com/JaKooLit/simple-sddm">JaKooLit/simple-sddm</a> (originally based on <a href="https://github.com/rototrash/tokyo-night-sddm">rototrash/tokyo-night-sddm</a>).<br>
  The original theme targets Qt 5. I forked it because I needed a Qt 6 compatible version for my setup.<br>
  All Qt 5 imports have been ported to Qt 6, and the login form is positioned on the right side of the screen.
</p>

<p align="center">
  Fork maintained at: <a href="https://github.com/Skydeke/simple-sddm">https://github.com/Skydeke/simple-sddm</a>
</p>

<h2 align="center">Preview</h2>
<p align="center">
<img src="./Previews/1.png" alt="preview-1">
</p>

---

## Dependencies

- `sddm`
- `qt6-declarative`
- `qt6-5compat` — required for blur, drop shadow, and colour overlay effects

Optional:
- `qt6-virtualkeyboard` — on-screen keyboard button

---

## Install

### Option 1 — PKGBUILD (Arch Linux)

A `PKGBUILD` is included in this repo. It pulls directly from the git repo.

```bash
git clone https://github.com/Skydeke/simple-sddm.git
cd simple-sddm
makepkg -si
```

### Option 2 — Manual

> Assumes SDDM is installed and configured. If not, see the [Arch Wiki](https://wiki.archlinux.org/title/SDDM).

```bash
git clone https://github.com/Skydeke/simple-sddm.git
sudo cp -r simple-sddm /usr/share/sddm/themes/simple-sddm-qt6
```

---

## Activate

Edit `/etc/sddm.conf.d/theme.conf` (create it if it doesn't exist):

```ini
[Theme]
Current=simple-sddm-qt6
```

---

## Testing without logging out

```bash
sddm-greeter-qt6 --test-mode --theme /usr/share/sddm/themes/simple-sddm-qt6
```

---

## Customisation

Edit `/usr/share/sddm/themes/simple-sddm-qt6/theme.conf` to change:

- `Background` — path to a background image inside `Backgrounds/`
- `FormPosition` — `left`, `center`, or `right`
- `HourFormat` — `HH:mm` for 24h, `hh:mm AP` for AM/PM
- `AccentColor` / `MainColor` — theme colours

---

## Credits

- Original Qt 5 theme by [JaKooLit](https://github.com/JaKooLit/simple-sddm)
- Based on [tokyo-night-sddm](https://github.com/rototrash/tokyo-night-sddm) by [rototrash](https://github.com/rototrash)
