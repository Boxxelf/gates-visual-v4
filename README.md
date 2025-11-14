# Gates Visual - Calculus Concept Map

An interactive visualization of calculus topics and their applications in Computer Science.

## Live Demo

**https://boxxelf.github.io/gates-visual-v4/**

## ✨ Features

- Interactive force-directed graph with drag-and-drop
- Filter by CS category or Calculus level
- Click nodes to view detailed CS applications
- Hierarchical course structure (Course → Core Idea → Topic)
- Course selection with disabled state for unselected courses
- Color-coded courses (Calculus I: Blue, Calculus II: Green)
- Smart zooming and auto-focus on selected nodes
- Node size scaling based on connection count when all courses are selected

## 🚀 Local Setup

```bash
git clone https://github.com/Boxxelf/gates-visual-v4.git
cd gates-visual-v4
python3 -m http.server 8000
```

Open http://localhost:8000 in your browser.

## 💡 How to Use

1. **Select CS Topics**: Click topics in the left sidebar to highlight related calculus nodes
2. **Browse Course Hierarchy**: Expand courses and core ideas to locate specific topics
3. **View Details**: Click any calculus node to view filtered rationales matching selected CS topics
4. **Course Selection**: Toggle course checkboxes to enable/disable course topics
5. **Navigate**: Drag nodes to rearrange, use mouse wheel to zoom, click background to reset

## Project Structure

```
gates_visual_v5/
├── index.html          # Main HTML page
├── style.css           # Styling and layout
├── app.js              # JavaScript logic and D3.js visualization
├── graph_data.json     # Calculus topics data with relationships
├── Calculus topic labeling scheme.csv  # Topic codes and hierarchy
├── ML_Alg_AI_CG_Rationales_081525(Rationales).csv  # CS topic rationales
└── README.md           # This file
```

## Data Structure

The `graph_data.json` file contains:

- **Nodes**: Each calculus topic with:
  - `id`: Short identifier
  - `topicCode`: Codified label (e.g., "Lim1", "Der2")
  - `label`: Full topic name
  - `calc_level`: "Calculus I" or "Calculus II"
  - `cs_categories`: Array of relevant CS fields
  - `rationales`: Detailed explanations of CS applications

- **Edges**: Prerequisites/follow-up relationships between topics

## Customization

### Adding New Topics

Edit `graph_data.json` and `Calculus topic labeling scheme.csv`:

1. Add topic to CSV with Course, Core Idea, Topic Code, and Topic Name
2. Add corresponding node to `graph_data.json`
3. Add edges to establish relationships

### Styling

Modify `style.css` to change colors, fonts, or layout.

## License

This project is open source and available for educational purposes.

## Contributing

Contributions are welcome! Feel free to:
- Add more calculus topics
- Enhance the visualizations
- Improve the UI/UX
- Fix bugs

## Contact

For questions or suggestions, please open an issue on GitHub.

---

Made with D3.js for Computer Science students learning Calculus
