# VSCode Audit Bookmarks Configuration

Custom configuration for the [Inline Bookmarks](https://marketplace.visualstudio.com/items?itemName=tintinweb.vscode-inline-bookmarks) VSCode extension, optimized for smart contract security audits.

## Setup
1. Install the "Inline Bookmarks" extension in VSCode
2. Open VSCode settings (Ctrl+,)
3. Click "Open Settings (JSON)" icon in the top right
4. Add the configuration below to your settings.json

## Configuration

```json
{
    "inline-bookmarks.expert.custom.words.mapping": {
        "blue": ["@audit\\-info[ \\t\\n]"],
        "purple": ["@todo[ \\t\\n]"],
        "green": ["@fp[ \\t\\n]", "@audit\\-low[ \\t\\n]"],
        "red": ["@audit\\-high[ \\t\\n]"],
        "darkred": ["@audit\\-critical[ \\t\\n]"],
        "orange": ["@audit\\-medium[ \\t\\n]"],
        "grey": ["@reported[ \\t\\n]"],
        "pink": ["@note[ \\t\\n]"],
        "darkorange": ["@audit[ \\t\\n]"]
    },
    "inline-bookmarks.expert.custom.styles": {
        "blue": {
            "gutterIconColor": "#157EFB",
            "overviewRulerColor": "#157EFBB0",
            "light": {
                "color": "#157EFB",
                "fontWeight": "bold"
            },
            "dark": {
                "color": "#157EFB",
                "fontWeight": "bold"
            }
        },
        "purple": {
            "gutterIconColor": "#C679E0",
            "overviewRulerColor": "#C679E0B0",
            "light": {
                "color": "#C679E0",
                "fontWeight": "bold"
            },
            "dark": {
                "color": "#C679E0",
                "fontWeight": "bold"
            }
        },
        "green": {
            "gutterIconColor": "#2E8B57",
            "overviewRulerColor": "#2E8B57B0",
            "light": {
                "color": "#2E8B57",
                "fontWeight": "bold"
            },
            "dark": {
                "color": "#3EA671",
                "fontWeight": "bold"
            }
        },
        "red": {
            "gutterIconColor": "#FF0000",
            "overviewRulerColor": "#FF0000B0",
            "light": {
                "color": "#FF0000",
                "fontWeight": "bold"
            },
            "dark": {
                "color": "#FF0000",
                "fontWeight": "bold"
            }
        },
        "darkred": {
            "gutterIconColor": "#800000",
            "overviewRulerColor": "#800000B0",
            "light": {
                "color": "#800000",
                "fontWeight": "bold"
            },
            "dark": {
                "color": "#8B0000",
                "fontWeight": "bold"
            }
        },
        "orange": {
            "gutterIconColor": "#FFA500",
            "overviewRulerColor": "#FFA500B0",
            "light": {
                "color": "#FFA500",
                "fontWeight": "bold"
            },
            "dark": {
                "color": "#FFA500",
                "fontWeight": "bold"
            }
        },
        "grey": {
            "gutterIconColor": "#666666",
            "overviewRulerColor": "#666666B0",
            "light": {
                "color": "#666666",
                "fontWeight": "bold"
            },
            "dark": {
                "color": "#888888",
                "fontWeight": "bold"
            }
        },
        "pink": {
            "gutterIconColor": "#FFB6C1",
            "overviewRulerColor": "#FFB6C1B0",
            "light": {
                "color": "#FFB6C1",
                "fontWeight": "bold"
            },
            "dark": {
                "color": "#FFB6C1",
                "fontWeight": "bold"
            }
        },
        "darkorange": {
            "gutterIconColor": "#FF531A",
            "overviewRulerColor": "#FF531AB0",
            "light": {
                "color": "#FF531A",
                "fontWeight": "bold"
            },
            "dark": {
                "color": "#FF531A",
                "fontWeight": "bold"
            }
        }
    }
}
```
# Available Bookmarks

| Bookmark | Color | Usage |
|----------|--------|-------|
| `@audit-critical` | Dark Red/Brown | Critical severity findings |
| `@audit-high` | Bright Red | High severity findings |
| `@audit-medium` | Orange | Medium severity findings |
| `@audit-low` | Green | Low severity findings |
| `@audit-info` | Blue | Informational findings |
| `@fp` | Green | False positives |
| `@reported` | Grey | Issues already reported |
| `@todo` | Purple | Tasks to be done |
| `@note` | Pink | General notes |

# Usage Example
```solidity
// @audit-critical Reentrancy in main withdrawal function
// @audit-high Incorrect slippage calculation
// @audit-medium Lack of input validation
// @audit-low Magic numbers in configuration
// @audit-info Consider adding events for better tracking
// @fp False positive: Safe delegate call pattern
// @reported Already submitted in previous audit
// @todo Need to check edge cases
// @note Architecture decision explained here
