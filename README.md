# VTEX IO SNIPPETS

This project aims to have a set of Snippets and shortcuts for creating [VTEX IO Store Framework](https://developers.vtex.com/vtex-developer-docs/docs/overview-5).
<br>

## Requirements

The extension will be activated when working on .jsonc files

## Current snippets

|   Prefix | Method                        |
| -------: | ----------------------------- |
|   `vrl→` | `VTEX Responsive Layout`      |
|   `vfr→` | `VTEX Flex Layout Row`        |
|   `vfc→` | `VTEX Flex Layout Column`     |
|   `vrt→` | `VTEX Rich Text`              |
|   `vic→` | `VTEX Info Card`              |
|   `vsl→` | `VTEX Store Link`             |
|   `vml→` | `VTEX Modal Layout`           |
|   `vsf→` | `VTEX Store Form`             |
|   `vcl→` | `VTEX Condition Layout (2.x)` |
| `vlogo→` | `VTEX Logo`                   |
|  `vsld→` | `VTEX Slider Layout`          |
|  `vimg→` | `VTEX Image`                  |

<br>

## Snippets Description

### `vrl`

```jsonc
"store.custom#about-us": {
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
"flex-layout.row#": {
  "props": {
    "blockClass": "",
  },
  "children": []
}
```

### `vfc`

```jsonc
"flex-layout.col#": {
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
    "children": ["modal-trigger#example"]
  },
  "modal-trigger#example": {
    "children": ["rich-text#example", "modal-layout#example"]
  },
  "rich-text#example": {
    "props": {
      "text": "Click me"
    }
  },
  "modal-layout#example": {
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
<br>

## For more information

* [Write me an email](brendonguedes@icloud.com)
* [Buy me a Coffee](ko-fi.com/brendonguedes)
* [Report a problema or improvement](https://github.com/brendonguedes/vtex-snippets/issues)

<br>
Made with 💜 by [Brendon Guedes](https://www.linkedin.com/in/brendonguedes/)
<br>
Consider leaving a ⭐ in this project
<br>

**Thanks 😍**
