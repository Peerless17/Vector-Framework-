# Vector Framework Documentation

## File Structure

Below is a structured format for the Vector Framework documentation split into multiple Markdown files:

### README.md
This is the introduction page and contains the overview of the framework:
```markdown
# Vector Framework

Vector Framework is a comprehensive library designed to simplify and enhance your Windows Forms applications by providing extensive features for window management, customization, security, and utilities.

## Table of Contents

- [Getting Started](getting-started.md)
- [Window Controls](window-controls.md)
- [Appearance Customization](appearance-customization.md)
- [Security Features](security-features.md)
- [Utility Features](utility-features.md)
- [Bootstrapper](bootstrapper.md)
- [Effects](effects.md)
- [Design Features](design-features.md)
- [Contributing](contributing.md)
```

### getting-started.md
```markdown
# Getting Started

## Installation

1. Clone the repository.
2. Include the Vector Framework DLL in your project.
3. Add `using Vector_Builder;` in your C# files.

## Example Usage
```csharp
using Vector_Builder;

public partial class MainForm : Form
{
    public MainForm()
    {
        InitializeComponent();
        VectorBuilder.EnableFormDrag(this);
    }
}
```
```

### window-controls.md
```markdown
# Window Controls

## Features

- **Minimize:** Minimizes the form.
- **Maximize:** Maximizes the form.
- **Close:** Closes the form.

### Example
```csharp
VectorBuilder.Minimize(this);
VectorBuilder.Maximize(this);
VectorBuilder.Close(this);
```
```

### appearance-customization.md
```markdown
# Appearance Customization

## Features

- **Set Background Color**
- **Set Background Image**

### Example
```csharp
VectorBuilder.SetBackgroundColor(this, Color.Black);
VectorBuilder.SetBackgroundImage(this, "https://yourimageurl.com");
```
```

### security-features.md
```markdown
# Security Features

## Features

- **Anti-Debug**
- **Process Blacklist**
- **Keylogger Detection**
- **Integrity Check**

### Example
```csharp
VectorBuilder.EnableAntiDebug();
VectorBuilder.AddProcessToBlacklist("notepad.exe");
```
```

### utility-features.md
```markdown
# Utility Features

## Features

- **Restart Application**
- **Clear All TextBoxes**
- **Open URLs**

### Example
```csharp
VectorBuilder.Restart();
VectorBuilder.ClearTextBoxes(this);
VectorBuilder.OpenUrl("https://yourlink.com");
```
```

### bootstrapper.md
```markdown
# Bootstrapper

## Features

- Downloads and extracts files from a given URL.

### Example
```csharp
VectorBuilder.DownloadAndExtractZip("https://example.com/file.zip", "C:\\DestinationPath");
```
```

### effects.md
```markdown
# Effects

## Features

- **Fade Out and Close**

### Example
```csharp
VectorBuilder.FadeOutAndClose(this);
```
```

### design-features.md
```markdown
# Design Features

## Features

- **Themes**
- **Rounded Corners**
- **Shadow Effects**

### Example
```csharp
VectorBuilder.ApplyTheme(VectorBuilder.Themes.Dark);
```
```

### contributing.md
```markdown
# Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository.
2. Create a feature branch.
3. Commit your changes.
4. Open a pull request.

For major changes, please open an issue first to discuss what you would like to change.
```
