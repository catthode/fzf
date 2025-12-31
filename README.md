# Catthode for fzf

> **From CRT to OLED.** Bringing warmth back to a world of cold themes. [cattho.de](https://cattho.de/)

Catthode is a high-contrast, retro-futuristic theme designed for prolonged shell sessions. It blends the crushed blacks of modern OLED displays with the comforting, warm glow of analog tungsten filaments.

## 🎨 Color Palette

### Surface
| Color | Hex | Role |
| :--- | :--- | :--- |
| **Base** | `#000000` | Background, Gutter |
| **Selection** | `#2d2d2d` | Selected background |
| **Border** | `#636363` | Borders, separators |

### Phosphor
| Color | Hex | Role |
| :--- | :--- | :--- |
| **Text** | `#ffffff` | Foreground (selected), Query |
| **Variable** | `#e8e8e8` | Foreground (normal) |
| **Label** | `#aeaeae` | Labels |

### Glow
| Color | Hex | Role |
| :--- | :--- | :--- |
| **Tan** | `#d9b98c` | Highlights (normal), Header |
| **Gold** | `#ffb86c` | Spinner |
| **Amber** | `#ff9e3b` | Highlights (selected), Pointer |
| **Clay** | `#f08d49` | Marker |

### Accents
| Color | Hex | Role |
| :--- | :--- | :--- |
| **Red** | `#ff6b6b` | Prompt |
| **Green** | `#b9d665` | Info |

## 📦 Installation

To use Catthode with fzf, you need to set the `FZF_DEFAULT_OPTS` environment variable.

### Bash / Zsh

Add the following to your `.bashrc` or `.zshrc`:

```bash
export FZF_DEFAULT_OPTS=$FZF_DEFAULT_OPTS'
  --color=fg:#e8e8e8,fg+:#ffffff,bg:#000000,bg+:#2d2d2d
  --color=hl:#d9b98c,hl+:#ff9e3b,info:#b9d665,marker:#f08d49
  --color=prompt:#ff6b6b,spinner:#ffb86c,pointer:#ff9e3b,header:#d9b98c
  --color=gutter:#000000,border:#636363,label:#aeaeae,query:#ffffff
  --border="bold" --border-label="" --preview-window="border-bold" --prompt="> "
  --marker=">" --pointer="◆" --separator="─" --scrollbar="│"
  --layout="reverse"'
```

### Fish

Add the following to your `config.fish`:

```fish
set -Ux FZF_DEFAULT_OPTS "$FZF_DEFAULT_OPTS
  --color=fg:#e8e8e8,fg+:#ffffff,bg:#000000,bg+:#2d2d2d
  --color=hl:#d9b98c,hl+:#ff9e3b,info:#b9d665,marker:#f08d49
  --color=prompt:#ff6b6b,spinner:#ffb86c,pointer:#ff9e3b,header:#d9b98c
  --color=gutter:#000000,border:#636363,label:#aeaeae,query:#ffffff
  --border='bold' --border-label='' --preview-window='border-bold' --prompt='> '
  --marker='>' --pointer='◆' --separator='─' --scrollbar='│'
  --layout='reverse'"
```

### Apply Changes

After editing your configuration file, restart your shell or source the file:

```bash
source ~/.zshrc  # or ~/.bashrc
```
