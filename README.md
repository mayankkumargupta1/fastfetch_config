# 🐚 SoftShell — Fastfetch Configuration

The official [Fastfetch](https://github.com/fastfetch-cli/fastfetch) configuration for **SoftShell**, a modern desktop shell experience.

Designed with a clean, pastel aesthetic and responsive Kitty image protocol support that scales seamlessly with terminal font resizing.

---

## ✨ Features

- **Responsive Image Logo**: Uses the `kitty-direct` protocol with character-cell boundaries (`c=26, r=13`) so the SoftShell logo scales in real-time when zooming or shrinking the terminal font (`Ctrl + Shift + -` / `+`).
- **SoftShell Branding**: Custom icon logo located at `logo/softshell_icon.png`.
- **Minimalist Palette**: Cool pastel accents tailored for modern terminals and Wayland setups.
- **Automated Bootstrapping**: Automatically installed and configured when setting up the **SoftShell Zsh** environment.

---

## 📁 Structure

```
~/.config/fastfetch/
├── config.jsonc            # Main Fastfetch configuration
├── logo/
│   └── softshell_icon.png  # High-resolution SoftShell logo
└── README.md
```

---

## 🚀 Installation

### Automatic (Recommended with SoftShell Zsh)
If you are using the SoftShell Zsh configuration, this repository is automatically cloned to `~/.config/fastfetch` on first launch.

### Manual
```bash
git clone git@github.com:mayankkumargupta1/fastfetch_config.git ~/.config/fastfetch
```

Or via HTTPS:
```bash
git clone https://github.com/mayankkumargupta1/fastfetch_config.git ~/.config/fastfetch
```

---

## ⚙️ Configuration Highlights

```jsonc
"logo": {
  "source": "~/.config/fastfetch/logo/softshell_icon.png",
  "type": "kitty-direct",
  "width": 26,
  "height": 13,
  "padding": {
    "top": 1,
    "left": 2,
    "right": 3
  }
}
```

> [!TIP]
> If you ever run Fastfetch inside a terminal that does not support the Kitty graphics protocol (e.g., standard virtual console or Alacritty), change `"type": "kitty-direct"` to `"type": "chafa"` to render the logo as colored Unicode block art.
