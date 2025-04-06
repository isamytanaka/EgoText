# EgoText - Text Manipulation Library for EgoLang

[![EgoLang](https://img.shields.io/badge/EgoLang-%E2%9A%96%20Powered-FFD700?style=flat&logo=expensify&logoColor=00274D&labelColor=0057B7&color=00A4E0&borderRadius=50)](https://github.com/isamytanaka/EgoLang)
![Version](https://img.shields.io/badge/Version-1.0.0-00CED1?style=flat&logo=semantic-release&logoColor=white&labelColor=008B8B&color=20B2AA)
[![License](https://img.shields.io/badge/License-MIT-9370DB?style=flat&logo=license&logoColor=white&labelColor=8A2BE2&borderRadius=20)](https://github.com/isamytanaka/EgoLang/blob/main/LICENSE)
![Open Source](https://img.shields.io/badge/Open_Source_Contributor-3DA639?style=flat&logo=github&logoColor=FFFFFF&labelColor=1E1E1E&color=006400)

*A robust text processing library for the EgoLang ecosystem*

## Support the Developer

[![Support on Apoia.se](https://img.shields.io/badge/Apoia.se-Support_Isamy_Tanaka-D72638?style=flat&logo=buymeacoffee&logoColor=white&labelColor=FF3D3D&color=D72638)](https://apoia.se/isamytanaka)

If you find this project valuable, consider supporting Isamy Tanaka's work through Apoia.se. Your contribution helps maintain and improve EgoLang and its ecosystem.

## Key Features

- Case conversion (upper/lower/capitalize)
- String reversal operations
- Length calculation utilities
- Empty string detection
- Simple and intuitive API design

## Installation

```bash
git clone https://github.com/isamytanaka/EgoText.git
```

## Usage Example

```ego
public mutable EgoText text = @py: EgoText();
text.content = "Hello EgoLang";
print(text.toUpper().reverse());  // Output: "GNALOGE OLLEH"
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

## Community

[![Issues](https://img.shields.io/badge/Support-GitHub_Issues-FFA500?style=flat&logo=github)](https://github.com/isamytanaka/EgoLang/issues)

Created by [Isamy Tanaka](https://github.com/isamytanaka)  
[![Follow](https://img.shields.io/github/followers/isamytanaka?style=social)](https://github.com/isamytanaka)  
![Profile Views](https://count.getloli.com/get/@isamytanaka.github.readme)
