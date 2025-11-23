# 🌳 Hierarchy Tree Editor

A powerful, standalone web-based tool for visualizing and editing hierarchical data from Excel files. Built for **LAMBDA TECHNOLOGIES** by **JM eAM Consulting LLC**.

![Version](https://img.shields.io/badge/version-1.0.0-green)
![License](https://img.shields.io/badge/license-MIT-blue)

## ✨ Features

### Core Functionality
- 📊 **Excel Import/Export**: Load `.xlsx` files, edit data, and export changes
- 🌲 **Interactive Tree View**: Visual hierarchy with expand/collapse functionality
- 🔍 **Dual Search System**: Independent search for tree and orphan nodes
- 🎯 **Drag & Drop**: Intuitive node reparenting with scroll preservation
- 🆕 **Create Records**: Add new nodes directly in the tool
- ✏️ **Live Editing**: Modify any field with instant updates
- 📊 **Data Quality Analysis**: Comprehensive validation and reporting

### Advanced Features
- **Auto-Mapping**: Automatically detects column mappings
- **Orphan Detection**: Identifies and manages disconnected nodes
- **Circular Reference Detection**: Prevents invalid parent-child relationships
- **Whitespace Cleanup**: Auto-fix formatting issues
- **Quality Scoring**: Real-time data quality metrics
- **Export Reports**: Generate detailed quality analysis reports

## 🚀 Quick Start

### Installation

No installation required! This is a standalone HTML file.

1. **Download** `hierarchy_tree_editor.html`
2. **Open** in any modern web browser
3. **Start** editing your hierarchical data

### Basic Usage

1. **Load Excel File**
   - Click "Load Excel" button
   - Select your `.xlsx` or `.xls` file
   - File should contain Node ID, Parent ID, and Label columns

2. **Map Columns**
   - Select which columns represent Node ID, Parent ID, and Label
   - Or click "Auto Map" for automatic detection

3. **Build Tree**
   - Click "Build Tree" to generate the hierarchy
   - View roots in the main tree panel
   - View orphans in the right panel

4. **Edit & Explore**
   - Click nodes to view/edit details
   - Drag & drop to reparent nodes
   - Use search to find specific nodes
   - Expand/collapse branches as needed

5. **Export Changes**
   - Click "Export Modified Excel" to save your changes

## 📖 User Guide

### Understanding the Interface

#### Left Panel - Controls
- **File Loading**: Import Excel files
- **Column Mapping**: Define data structure
- **Tree Building**: Generate hierarchy
- **Record Creation**: Add new nodes
- **Export**: Save modifications
- **Quality Analysis**: Run data validation
- **Help**: Built-in documentation

#### Middle Panel - Tree View
- **Tree Section**: Hierarchical view of connected nodes
- **Orphans Section**: Disconnected or invalid nodes
- **Search Bars**: Independent filtering for each section
- **Drop Zone**: Make nodes into root nodes

#### Right Panel - Details
- **Record Details**: Edit all fields for selected node
- **Live Updates**: Changes save automatically

### Data Structure Requirements

Your Excel file should contain at least three columns:

| Column Type | Description | Example |
|------------|-------------|---------|
| **Node ID** | Unique identifier | `ASSET001`, `PUMP-123` |
| **Parent ID** | References another Node ID | `FACILITY-A`, *(blank for roots)* |
| **Label** | Descriptive name | `Main Pump`, `Building A` |

### Node Categories

- **Root Nodes**: No parent ID, but have children
- **Child Nodes**: Have a valid parent ID reference
- **Orphan Nodes**: 
  - Have a parent ID that doesn't exist, OR
  - Are completely isolated (no parent, no children)

### Drag & Drop Operations

1. **Reparent a Node**
   - Drag any node to another node
   - Dropped node becomes child of target

2. **Make a Root**
   - Drag node to the "Drop here to make root" zone
   - Node's parent ID is cleared

3. **From Orphans**
   - Drag orphan nodes to tree to assign parents
   - Automatically removes from orphans list

### Search Features

#### Tree Search
- Searches: Node ID, Label, and all other fields
- Supports regex patterns (e.g., `^ABC`, `.*test.*`)
- Shows matching nodes and their ancestors
- Live results as you type (300ms delay)

#### Orphan Search
- Independent from tree search
- Same search capabilities
- Shows match count

**💡 Tip**: Use both searches simultaneously to find related nodes!

### Quality Analysis

Run "Data Quality Report" to check for:

#### Critical Issues 🔴
- **Duplicates**: Multiple nodes with same ID
- **Circular References**: Nodes referencing themselves
- **Empty IDs**: Rows without Node IDs

#### Warnings ⚠️
- **Orphans**: Invalid parent references
- **Whitespace**: Extra spaces in IDs (auto-fixable)
- **Empty Labels**: Missing descriptions

#### Statistics ℹ️
- Total records and valid nodes
- Root and orphan counts
- Max tree depth
- Average children per parent

## 🛠️ Technical Details

### Built With
- **HTML5**: Semantic structure
- **CSS3**: Modern styling with gradients and animations
- **Vanilla JavaScript**: No framework dependencies
- **SheetJS (xlsx.js)**: Excel file processing

### Browser Compatibility
- ✅ Chrome/Edge (Recommended)
- ✅ Firefox
- ✅ Safari
- ✅ Opera

### File Format Support
- `.xlsx` (Excel 2007+)
- `.xls` (Excel 97-2003)

## 📋 Best Practices

### Data Preparation
1. ✅ Use unique, meaningful Node IDs
2. ✅ Avoid spaces in IDs (use `_` or `-`)
3. ✅ Keep parent-child relationships simple
4. ✅ Ensure parent IDs exist before referencing
5. ✅ Add descriptive labels for all nodes

### Workflow Recommendations
1. **Load & Map**: Import file and verify column mappings
2. **Build**: Generate initial tree structure
3. **Analyze**: Run quality report to identify issues
4. **Fix Critical**: Address duplicates and circular refs first
5. **Clean**: Fix whitespace and empty labels
6. **Reorganize**: Use drag & drop to correct relationships
7. **Export**: Save your cleaned data

### Performance Tips
- Files with 1,000+ records may take a few seconds to process
- Collapse unused branches to improve rendering performance
- Use search to navigate large trees efficiently
- Export frequently to save progress

## 🔒 Privacy & Security

- ✅ **100% Client-Side**: All processing happens in your browser
- ✅ **No Data Upload**: Your files never leave your computer
- ✅ **No Internet Required**: Works completely offline
- ✅ **No Account Needed**: No login or registration

## 📧 Support & Contact

**JM eAM Consulting LLC**
- 📧 Email: [jmeamconsulting@gmail.com](mailto:jmeamconsulting@gmail.com)
- 📱 Mobile: 803.226.1039

## 📄 License

Copyright © 2025 JM eAM Consulting LLC. All Rights Reserved.

This tool is provided for use by LAMBDA TECHNOLOGIES.

---

**Built with ❤️ for LAMBDA TECHNOLOGIES**
