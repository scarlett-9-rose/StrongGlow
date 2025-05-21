# StrongGlow
import matplotlib.pyplot as plt

# Define color palettes
palettes = {
    "Fresh Glow": {
        "Mint Green": "#A8E6CF",
        "Blush Pink": "#FFD3B6",
        "Warm White": "#FFF9F0",
        "Peach Coral": "#FF8B6A",
        "Soft Olive": "#B5CDA3"
    },
    "Empowered Radiance": {
        "Lavender": "#D4BBFF",
        "Soft Coral": "#FF9AA2",
        "Cream": "#FFF4F0",
        "Deep Orchid": "#8E44AD",
        "Sage Green": "#C9E4C5"
    },
    "Berry Bright": {
        "Raspberry Pink": "#FF4D6D",
        "Blueberry Purple": "#6A4C93",
        "Powder White": "#FAFAFA",
        "Pale Peach": "#FFE8E8",
        "Soft Green": "#D2F6C5"
    }
}

# Plotting the palettes
fig, axes = plt.subplots(len(palettes), 1, figsize=(10, 6))
fig.suptitle('Color Palettes for Teen Girls’ Health & Nutrition App', fontsize=14, fontweight='bold')

for ax, (palette_name, colors) in zip(axes, palettes.items()):
    ax.set_title(palette_name, fontsize=12, loc='left')
    for i, (color_name, hex_code) in enumerate(colors.items()):
        ax.add_patch(plt.Rectangle((i, 0), 1, 1, color=hex_code))
        ax.text(i + 0.5, -0.1, color_name, ha='center', va='top', fontsize=9, rotation=30)
    ax.set_xlim(0, len(colors))
    ax.set_ylim(0, 1)
    ax.axis('off')

plt.tight_layout(rect=[0, 0, 1, 0.96])
plt.show()
