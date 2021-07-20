<p align="center">
  <a href="https://marketplace.visualstudio.com/items?itemName=brendonguedes.vtex-snippets" rel="noopener" target="_blank"><img width="150" src="https://github.com/brendonguedes/vtex-snippets/blob/main/images/logo.png" alt="VTEX IO logo"></a>
</p>

<h1 align="center">VTEX IO SNIPPETS</h1>
<p align="center">A vscode <a href="https://marketplace.visualstudio.com/items?itemName=brendonguedes.vtex-snippets" target="_blank">extension</a> to create VTEX IO stores faster 🚀</p>

[![GitHub stars](https://img.shields.io/github/stars/brendonguedes/vtex-snippets?style=social&label=Star&maxAge=2592000)](https://github.com/brendonguedes/vtex-snippets/stargazers/)


## 💡 About the project

This project aims to have a set of Snippets and shortcuts for creating [VTEX IO Store Framework](https://developers.vtex.com/vtex-developer-docs/docs/overview-5).

## 🤷🏻‍♂️ CAUTION

Make sure you are writing to a .jsonc file, the extension is only enabled when using jsonc files.

## Installation

To install directly from the vscode extension manager, use:
```sh
brendonguedes.vtex-snippets
```

---

## Current snippets

|     Prefix | Method                        |
| ---------: | ----------------------------- |
|     `vrl→` | `VTEX Responsive Layout`      |
|     `vfr→` | `VTEX Flex Layout Row`        |
|     `vfc→` | `VTEX Flex Layout Column`     |
|     `vrt→` | `VTEX Rich Text`              |
|     `vic→` | `VTEX Info Card`              |
|     `vsl→` | `VTEX Store Link`             |
|     `vml→` | `VTEX Modal Layout`           |
|     `vsf→` | `VTEX Store Form`             |
|     `vcl→` | `VTEX Condition Layout (2.x)` |
|   `vlogo→` | `VTEX Logo`                   |
|    `vsld→` | `VTEX Slider Layout`          |
|    `vimg→` | `VTEX Image`                  |
|  `vshelf→` | `VTEX Shelf`                  |
|     `vcm→` | `VTEX Category Menu`          |
|   `vfcfr→` | `VTEX Flex Row into Flex Col` |
|   `vfrfc→` | `VTEX Flex Col into Flex Row` |
|     `vss→` | `VTEX SKU Selector`           |
|  `vvideo→` | `VTEX Video`                  |
| `viframe→` | `VTEX Iframe`                 |

## Snippets Description

### `vrl`

```jsonc
"store.custom#change-me": {
  "blocks": [
    "responsive-layout.desktop",
    "responsive-layout.tablet",
    "responsive-layout.phone"
  ]
},
"responsive-layout.desktop": {
  "children": []
},
"responsive-layout.tablet": {
  "children": []
},
"responsive-layout.phone": {
  "children": []
},
```

### `vfr`

```jsonc
"flex-layout.row#change-me": {
  "props": {
    "blockClass": "",
  },
  "children": []
}
```

### `vfc`

```jsonc
"flex-layout.col#change-me": {
  "props": {
    "blockClass": "",
  },
  "children": []
}
```

### `vrt`

```jsonc
"rich-text#": {
  "props": {
    "blockClass": "",
    "font": "t-body",
    "text": "",
    "textAlignment": "CENTER",
    "textColor": "c-on-base",
    "textPosition": "CENTER"
  }
}
```

### `vsl`

```jsonc
"link.product#product-page": {
    "props": {
      "href": "/{slug}/p",
      "label": "More details >"
    }
  },
```

### `vml`

```jsonc
{
  "store.home": {
    "children": ["modal-trigger#change-me"]
  },
  "modal-trigger#change-me": {
    "children": ["rich-text#change-me", "modal-layout#change-me"]
  },
  "rich-text#change-me": {
    "props": {
      "text": "Click me"
    }
  },
  "modal-layout#change-me": {
    "children": ["rich-text#modal-content"]
  },
  "rich-text#modal-content": {
    "props": {
      "text": "Hello"
    }
  }
}
```

### `vsf`

```jsonc
  "form": {
    "props": {
      "entity": "clients",
      "schema": "person"
    },
    "children": [
      "rich-text#formTitle",
      "form-input.text#firstName",
      "form-input.text#lastName",
      "form-field-group#address",
      "form-input.checkbox#agreement",
      "form-submit"
    ],
    "blocks": ["form-success"]
  },
  "form-success": {
    "children": [
      "rich-text#successSubmit"
    ]
  },
  "rich-text#successSubmit": {
    "props": {
      "text": "Succesfully submitted the data!",
      "textAlignment": "CENTER",
      "textPosition": "CENTER"
    }
  },
  "form-input.text#firstName": {
    "props": {
      "pointer": "#/properties/firstName"
    }
  },
  "form-input.text#lastName": {
    "props": {
      "pointer": "#/properties/lastName"
    }
  },
  "form-input.checkbox#agreement": {
    "props": {
      "pointer": "#/properties/agreement",
      "label": "Do you agree that this is the best form component in the whole wide world?"
    }
  },
  "form-field-group#address": {
    "props": {
      "pointer": "#/properties/address"
    }
  },
  "form-submit": {
    "props": {
      "label": "Submit"
    }
  }
```

### `vshelf`

```jsonc
{
  "product-summary.shelf#demo1": {
    "children": []
  },
  "list-context.product-list#demo1": {
    "blocks": ["product-summary.shelf#demo1"],
    "children": ["slider-layout#demo-products"]
  }
}
```

### `vsl`

```jsonc
"link.product#product-page": {
    "props": {
      "href": "/{slug}/p",
      "label": "More details >"
    }
  },
```

### `vcm`

```jsonc
{
  "category-menu": {
    "props": {
      "showAllDepartments": true,
      "showSubcategories": true,
      "menuDisposition": "center",
      "departments": [],
      "sortSubcategories": "name"
    }
  }
}
```

### `viframe`

```jsonc
  "iframe": {
    "props": {
      "src": ""
    }
  }
```

### `vvideo`

```jsonc
  "video#background": {
    "props": {
      "width": "100%",
      "height": "600px",
      "loop": false,
      "autoPlay": true,
      "muted": false,
      "src": "https://www.youtube.com/watch?v=wygFqZXMIco",
      "blockClass": "videoEl"
    }
  }
```

### `vss`

```jsonc
  "sku-selector#change-me": {
    "props": {
      "hideImpossibleCombinations": false
    }
  },
```

### `vfrfc`

```jsonc
  "flex-layout.row#change-me": {
    "children": [
      "flex-layout.col#change-me"
    ]
  },
  "flex-layout.col#change-me": {
    "children": []
  },
```

### `vfcfr`

```jsonc
  "flex-layout.col#change-me": {
    "children": [
      "flex-layout.row#change-me"
    ]
  },
  "flex-layout.row#change-me": {
    "children": []
  },
```

<br>

## 📝 Licence

This project is under MIT licence. See the archive [LICENSE](LICENSE) to more details.

---

## For more information

- [Write me an email](brendonguedes@icloud.com)
- [Buy me a Coffee](ko-fi.com/brendonguedes)
- [Report a problema or improvement](https://github.com/brendonguedes/vtex-snippets/issues)

<br>

Made with 💜 by [Brendon Guedes](https://www.linkedin.com/in/brendonguedes/)
<br>

Consider leaving a ⭐ in this project
<br>

**Thanks 😍**
