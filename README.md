Royal Flying Doctor Service
------------
**Application Programming Interface Documentation**

Looking for the [docs](https://juanvillegas.github.io/rfds-docs/)?

## Collaborators Guide

### Executing Slate

See [slate docs](https://github.com/lord/slate)

### Formatting tables

Although in Markdown the alignment of rows and cells in a table is not required, for the sake of the 
rest of the contributors the documentation developer should make sure all the vertical pipes "|" are aligned:
 
 **BAD**
 
 ```
 ID | Type
  --|--|
  1|String
 ```
 
 **GOOD**
 
```
| ID | Type    |
| -- | ------- |
| 1  | String  |
```

If you are a **Phpstorm** user you may install the plugin Pipe Table Formatter to handle this automatically.
