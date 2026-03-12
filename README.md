# Action Toolbar — egui Horizontal Layout

Episode 6 of the **Learn egui in Neovim** series.

A toolbar app with Add, Remove, and Reset buttons arranged horizontally, showing live status and count.

## What You'll Learn

- `ui.horizontal()` to arrange widgets side by side
- Placing multiple buttons in a single row
- Combining horizontal groups with labels for status displays
- Managing state updates from toolbar actions

## Run

```bash
cargo run
```

## Key Code

```rust
ui.horizontal(|ui| {
    if ui.button("Add").clicked() {
        self.count += 1;
        self.message = format!("Added! Count: {}", self.count);
    }
    if ui.button("Remove").clicked() {
        self.count -= 1;
        self.message = format!("Removed! Count: {}", self.count);
    }
    if ui.button("Reset").clicked() {
        self.count = 0;
        self.message = String::from("Reset!");
    }
});
```

## Series

This is part of the [Learn egui in Neovim](https://www.youtube.com/@CelesteAI) series, where we build Rust GUI apps step by step.
