
# EgoText - Complete Text Manipulation Library for EgoLang

[![EgoLang Compatible](https://img.shields.io/badge/EgoLang-2.8%2B-00A4E0?style=flat&logo=expensify&logoColor=white)](https://github.com/isamytanaka/EgoLang)
[![Version](https://img.shields.io/badge/Version-1.2.0-FF4500?style=flat)](https://github.com/isamytanaka/EgoLang/releases)
[![License](https://img.shields.io/badge/License-MIT-9370DB?style=flat)](https://opensource.org/licenses/MIT)
[![Build Status](https://img.shields.io/badge/Build-Passing-4CAF50?style=flat)](https://github.com/isamytanaka/EgoLang/actions)
[![Coverage](https://img.shields.io/badge/Coverage-92%25-388E3C?style=flat)](https://github.com/isamytanaka/EgoLang/actions)

## Table of Contents
1. [Installation](#installation)
2. [Basic Usage](#basic-usage)
3. [API Reference](#api-reference)
4. [Advanced Examples](#advanced-examples)
5. [Performance Tips](#performance-tips)
6. [Support](#support)

## Installation

```bash
# Clone the EgoLang repository (if not already installed)
git clone https://github.com/isamytanaka/EgoLang.git

# Copy the EgoText library to your project
cp EgoLang/src/libraries/EgoText.ego ./your_project/
```

## Basic Usage

### Initialization
```ego
// Import the EgoText class (automatic in EgoLang)
public mutable EgoText text = @py: EgoText();

// Set initial content
text.content = "Hello World";
```

### Simple Operations
```ego
// Convert to uppercase
print(text.toUpper());  // Output: "HELLO WORLD"

// Get string length
print(text.length());   // Output: 11

// Check if empty
print(text.isEmpty());  // Output: false
```

## API Reference

### Core Methods

| Method | Parameters | Returns | Description |
|--------|------------|---------|-------------|
| `toUpper()` | None | `string` | Converts all characters to uppercase |
| `toLower()` | None | `string` | Converts all characters to lowercase |
| `length()` | None | `int` | Returns the number of characters |
| `reverse()` | None | `string` | Reverses the string |
| `isEmpty()` | None | `bool` | Returns true if string is empty |
| `capitalize()` | None | `string` | Capitalizes first character |

### Property

| Property | Type | Description |
|----------|------|-------------|
| `content` | `mutable string` | The underlying string storage |

## Advanced Examples

### Method Chaining
```ego
// Chain multiple operations
text.content = "  egoLang  ";
print(text.trim().toUpper().reverse());  
// Output: "GNALOGE"
```

### Text Processing Pipeline
```ego
public mutable EgoText processor = @py: EgoText();
processor.content = "   Text Processing Example   ";

// Normalization pipeline
processor.trim()
        .toLower()
        .capitalize();

print(processor.content); 
// Output: "Text processing example"
```

### Conditional Processing
```ego
text.content = "Important Message";

if (text.length() > 10) {
    text.toUpper();
    print(text.content);  // Output: "IMPORTANT MESSAGE"
}
```

## Performance Tips

1. **Reuse Instances**: Create one EgoText instance and reuse it
2. **Batch Operations**: Chain methods to reduce intermediate copies
3. **Length Checks**: Use `isEmpty()` before processing large strings
4. **Python Interop**: For complex operations, consider `@py:` directives

## Support

[![Issues](https://img.shields.io/badge/Support-GitHub_Issues-FFA500?style=flat&logo=github)](https://github.com/isamytanaka/EgoLang/issues)
[![Apoia.se](https://img.shields.io/badge/Apoia.se-Support_Isamy_Tanaka-D72638?style=flat&logo=buymeacoffee&logoColor=white)](https://apoia.se/isamytanaka)

Created by [Isamy Tanaka](https://github.com/isamytanaka)  
[![Follow](https://img.shields.io/github/followers/isamytanaka?style=social)](https://github.com/isamytanaka)  
![Profile Views](https://count.getloli.com/get/@isamytanaka.github.readme)
