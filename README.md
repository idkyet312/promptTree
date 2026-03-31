![Prompt Tree Interface](image/promptTree_Version_1_0_23.jpg)

# **Prompt Tree v1.0.23**

## **Overview**

**Prompt Tree** is a specialized prompt-engineering application designed for Generative AI image and video production. It is built specifically for filmmakers to manage complex, multi-shot workflows by replacing monolithic text blocks with a structured, object-oriented asset framework. By using a hierarchical tree approach, every element—from characters to cameras—becomes a recyclable and easily editable asset.

## **The Four-Panel Interface**

The application uses a **4-Panel layout** to manage the workflow:

- **Asset Panel (Top-Left):** Your library of assets and core definitions (characters, cinematography, settings, etc.).

- **Tree Panel (Top-Right):** The project hierarchy where you build sequences and shots by dragging assets from the library.

- **Editor Panel (Bottom-Left):** A text editor for the prompt content of the currently selected node.

- **Prompt Panel (Bottom-Right):** A live concatenated preview of the final prompt, formatted with indentation and hierarchy.

## **Core Features**

### **1. Object-Oriented Asset Management**

- **Instancing:** Dragging an Asset Panel node into the Tree Panel creates a link to the source.

- **Global Updates:** Modifying a source asset automatically updates every linked instance in the Tree Panel.

- **Inheritance:** Shots inherit assets from their parent nodes.

### **2. Visibility**

- There are three node visibility states :

1. **None**  Inherits visibility of parent node. This is the default visibility state.

2. 👁  Visible. Included in prompt.

3.  —  Invisible. Excluded from prompt.

- The Asset Panel nodes and the Tree Panel nodes can have separate Visibility states.



### **3. Synchronization Buttons**

- **Sync Content:** Forces all linked node names and content in the Tree Panel to match the Asset Panel.

- **Sync Visible:** Forces all nodes in the Tree Panel to match the visibility of the Asset Panel.

## **Keyboard Shortcuts**

### **File Operations**

- **Ctrl+N**: New Project.

- **Ctrl+O**: Open Project.

- **Ctrl+I**: Import/Merge Project.

- **Ctrl+S**: Quick Save.

- **Ctrl+Shift+S**: Save Project As....

- **Ctrl+Alt+S**: Save Version Up (Auto-increments `v0000`).

- **Ctrl+Q**: Exit Application.

### **Node Operations**

- **Enter**: Add Sibling Node.

- **Insert / Ctrl+Enter**: Add Child Node.

- **F2**: Rename Node.

- **Ctrl+D**: Duplicate Node and all children.

- **- (Minus)**: Add visual separator line.

- **V**: Toggle Visibility.

- **Alt+V**: Clear all visibility overrides in active tree.

- **Delete / Backspace**: Delete Node and children.

### **Navigation & View**

- **Ctrl+Shift+X**: Expand/collapse ALL nodes in tree.

- **Shift+X / Alt+Click**: Expand/Collapse node and all descendants.

- **Ctrl+J**: Jump from linked instance to original source asset.

- **Ctrl+Z**: Undo.

- **Ctrl+Y / Ctrl+Shift+Z**: Redo.

### **Prompt Operations**

- **Ctrl+G**: Generate Prompt (Copy to clipboard).

- **Ctrl+C**: Copy preview text (when Tree Panel is active).

## **Drag & Drop Logic**

- **Top Third of Node**: Drops the item **before** the target node.

- **Middle Third of Node**: Drops the item **into** the target node as a child.

- **Bottom Third of Node**: Drops the item **after** the target node.

## **Exporting**

- **Copy Prompt:** Copies the current indented preview to the clipboard.

- **Save XML:** Exports the prompt as a hierarchically tagged XML file for AI digestibility.

- **Save TXT:** Exports the prompt as a standard plain text file.
