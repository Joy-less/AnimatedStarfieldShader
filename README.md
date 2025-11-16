# Animated Starfield Shader

Animated starry sky shader for Godot 4.

Based on [Starfield in the sky with scrolling effect](https://godotshaders.com/shader/2d-starfield-in-the-sky-with-scrolling-effect-ver-1-0) by xcv145336.

## Usage

Create a `ShaderMaterial` with the shader and assign it to your mesh.
- `background_color`: The color of the background.
- `aspect_ratio`: The amount to stretch stars inversely.
- `density`: The amount of stars.
- `layer_parascale`: The number of star layers.
- `star_speed`: The speed that stars move across the background.
- `star_wave`: The speed that stars move back-and-forth across the background.
- `star_rotate_speed`: The speed that stars rotate.
- `twinkle_effect`: The amount of star flickering.
- `twinkle_speed`: The speed of star flickering.
- `pixelate_enabled`: Whether to enable the pixelation effect.
- `pixelate_count`: How many pixels to round to in the pixelation effect.

## Canvas Item Shader

To use the shader on a canvas item:

Replace:
```gdshader
shader_type spatial;
render_mode depth_prepass_alpha;
render_mode diffuse_toon;
render_mode specular_toon;
```

With:
```gdshader
shader_type canvas_item;
```

Replace:
```gdshader
ALBEDO = color;
ALPHA = 1.0;
```

With:
```gdshader
COLOR = vec4(color, 1.0);
```