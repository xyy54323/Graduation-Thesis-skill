# Chinese Thesis Functional Structure Diagram Layout

Use this reference when the user asks for `功能结构图`, `系统功能结构图`, `功能结构树`, or explicitly wants a thesis-style black-and-white functional hierarchy diagram.

## Default visual style

Treat this as the default pattern unless the user explicitly asks for a different layout.

- White background only.
- Black strokes only. No color, gradient, shadow, icons, or decorative fills.
- Top-down organizational-tree layout.
- Centered title at the top.
- One root module centered below the title.
- First-level modules arranged horizontally in one row.
- Second-level modules placed below each first-level module as narrow vertical rectangles.
- All connectors must be orthogonal right-angle connectors.
- Avoid diagonal edges, curved edges, overlapping edges, and crossed trunks.
- Keep generous horizontal spacing between first-level groups so each group reads independently.
- Use consistent stroke width around 1.5px to 2px.

## Shape rules

### Root module
- Use a larger rounded rectangle.
- Center it horizontally.
- Use horizontal Chinese text.

### First-level modules
- Use medium rounded rectangles.
- Arrange them evenly in a single horizontal row.
- Use horizontal Chinese text.

### Second-level modules
- Use plain rectangles, not rounded rectangles.
- Make them obviously taller than they are wide.
- Labels must be true vertical labels, matching the example image.
- For Chinese labels, place one character per line.
- For mixed labels like `OLED数据显示` or `数据上传APP`, also stack Latin letters vertically one line at a time, for example `O`, `L`, `E`, `D` on separate lines.
- Do not rely on automatic text wrapping; explicitly construct vertical labels.

## Connector rules

For each first-level group:
- Draw one vertical trunk from the first-level module downward.
- Draw one short horizontal branch line for that group only.
- Connect each second-level module to that branch line with vertical connectors.
- Do not share one large lower branch line across all groups.
- Do not let connectors overlap labels or boxes.

For root to first-level modules:
- Use one centered vertical connector from the root.
- Use one horizontal branch line across the first-level row.
- Drop vertical connectors from that branch line to each first-level module.

## Spacing guidance

- Keep the title, root, first-level row, and second-level row visually separated.
- Leave enough horizontal room between second-level boxes so vertical text stays readable.
- Keep module box sizes uniform within the same level.
- Prefer symmetry and alignment over compactness.

## Example asset

Use this bundled example as the canonical visual reference for future generations:
- `assets/functional-structure-cn-example.png`

If a request is ambiguous but clearly asks for a Chinese thesis functional structure diagram, follow this reference by default.
