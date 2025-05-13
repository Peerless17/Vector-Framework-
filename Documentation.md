# Vector Framework Documentation

## Introduction

The Vector Framework is a comprehensive library for building Windows Forms applications with advanced security, design, and utility features. It provides a collection of methods for managing window behaviors, customizing application appearances, adding security features, and more. This framework helps developers easily integrate functionalities like anti-debugging, file integrity checks, and custom UI effects, among others.

---

## Table of Contents

* **Getting Started**
* **Window Controls**

  * Minimize
  * Maximize
  * Close
* **Appearance Customization**

  * Set Background Color
  * Set Background Image
  * Set Top Most
  * Apply Themes
* **Security Features**

  * Anti-Screenshot
  * Process Blacklist
  * Keylogger Detection
  * HWID Spoofing
  * Integrity Check
* **Utility Features**

  * Clear Textboxes
  * Open URL
  * Get Public IP
  * Bootstrapper

    * Download File
    * Extract Zip
    * Run Downloaded File
* **Effects**

  * FadeOutAndClose
* **Design Features**

  * Rounded Corners
  * Shadow Effects
* **Conclusion**

---

## Getting Started

### Installation

1. Download the Vector Framework source code from the repository.
2. Add the `VectorFramework` namespace to your Windows Forms project.
3. Start using the features by calling methods from the `VectorBuilder` class.

```csharp
using VectorFramework;
```

---

## Window Controls

The Window Controls allow you to manage the window's state, such as minimizing, maximizing, or closing the form.

### Minimize

Minimizes the window to the taskbar.

```csharp
VectorBuilder.Minimize(this);
```

### Maximize

Maximizes the window to fullscreen.

```csharp
VectorBuilder.Maximize(this);
```

### Close

Closes the application immediately.

```csharp
VectorBuilder.Close(this);
```

---

## Appearance Customization

Customize the window's appearance with several built-in functions.

### Set Background Color

Changes the background color of the form.

```csharp
VectorBuilder.SetBackgroundColor(this, Color.Black);
```

### Set Background Image

Sets a background image from a URL. The image is fetched asynchronously.

```csharp
await VectorBuilder.SetBackgroundImage(this, "https://yourimageurl.com");
```

### Set Top Most

Keeps the window on top of all other windows.

```csharp
VectorBuilder.SetTopMost(this, true);
```

### Apply Themes

Apply a custom theme to the form and its controls.

```csharp
VectorBuilder.ApplyTheme(this, Color.DarkSlateGray, Color.White);
```

---

## Security Features

### Anti-Screenshot

Detects and kills any known screenshot tools like Lightshot or Snipping Tool.

```csharp
VectorBuilder.AntiScreenshot();
```

### Process Blacklist

Kills any unauthorized processes running on the system.

```csharp
VectorBuilder.ProcessBlacklist(new[] { "maliciousProcess1", "maliciousProcess2" });
```

### Keylogger Detection

Detects and blocks common keylogging tools.

```csharp
VectorBuilder.KeyloggerDetection();
```

### HWID Spoofing

Detects if the system is using a hardware ID spoofer.

```csharp
string hwid = VectorBuilder.GetHWID();
bool isSpoofed = VectorBuilder.IsHWIDSpoofed(hwid);
```

### Integrity Check

Checks the integrity of a file using SHA-256 hashing.

```csharp
bool isValid = VectorBuilder.VerifyIntegrity("path/to/file.exe", "expectedSHA256Hash");
```

---

## Utility Features

### Clear Textboxes

Clears all textboxes within a form.

```csharp
VectorBuilder.ClearTextBoxes(this);
```

### Open URL

Opens a URL in the default browser.

```csharp
VectorBuilder.OpenUrl("https://yourlink.com");
```

### Get Public IP

Retrieves the public IP address of the machine.

```csharp
string ip = VectorBuilder.GetPublicIP();
```

### Bootstrapper

#### Download File

Downloads a file from a given URL to a specified path.

```csharp
await VectorBuilder.DownloadFile("https://example.com/file.zip", "path/to/save/file.zip");
```

#### Extract Zip

Extracts a ZIP file to a given directory.

```csharp
VectorBuilder.ExtractZip("path/to/file.zip", "path/to/extract/directory");
```

#### Run Downloaded File

Runs the downloaded executable.

```csharp
VectorBuilder.RunDownloadedFile("path/to/extracted/exe");
```

---

## Effects

### FadeOutAndClose

Fades out the form and closes it after the animation.

```csharp
await VectorBuilder.FadeOutAndClose(this);
```

---

## Design Features

### Rounded Corners

Applies rounded corners to the form.

```csharp
VectorBuilder.AddRoundedCorners(this);
```

### Shadow Effects

Adds a shadow effect around the form to give it a more professional look.

```csharp
VectorBuilder.AddShadow(this);
```

---

## Conclusion

The Vector Framework is designed to simplify application development by providing an easy-to-use set of tools for window management, appearance customization, security features, and more. You can easily integrate these features into your own Windows Forms projects and enhance the overall user experience, security, and functionality.

---

## Contributing

We welcome contributions to the Vector Framework! If you have any ideas, bug fixes, or new features you'd like to see, please feel free to submit a pull request or open an issue on our GitHub repository.
