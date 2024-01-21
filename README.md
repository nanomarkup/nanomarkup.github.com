# Nano Markup

Nano Markup is a minimalistic markup language crafted for simplicity and efficiency in document creation. With a focus on fundamental elements, it strives to provide a high-quality and efficient way of expressing information. NanoMarkup is tailored for scenarios where a lightweight and straightforward syntax is paramount.

## Language overview

### Key/Value Pair
The Key/Value Pair feature is a fundamental aspect of the language, defining a unique identifier (key) associated with a corresponding value. Each key is followed by a space, and the data following the key is considered its value. This structure ensures clear and unambiguous representation of information, where keys uniquely identify specific attributes or properties, and values hold the associated data.

The value can be empty to provide flexibility in data representation. Additionally, to maintain proper formatting and prevent ambiguity in key identification, the key itself cannot end with a dot, as the dot serves as a separator token for referenced data. This ensures consistent and reliable usage of the key/value pair structure while respecting the role of the dot as a separator.
```
name Ariana
age 12
```
   In this example, "name" and "age" are the keys, and "Ariana" and "12" are their corresponding values. The simplicity of this structure allows for straightforward representation of various data points in a concise manner.

### Array
The Array feature allows the assignment of a list of values to a key. Each value is placed on a new line, contributing to the clarity of the structure. Additionally, the array can include inline arrays or inline entities, enhancing flexibility. The use of square brackets "[]" encapsulates the array, providing a clear visual delineation. This design ensures a clean representation of ordered data associated with a specific key.
```
goods [
  bread
  salt
  milk
]
```
In this example, the key is "goods," and the associated array includes values like "bread," "salt," and "milk." The syntax promotes readability and organization, while the option for inline arrays or entities adds versatility to the representation of structured data.

### Inline Array
The Inline Array declaration mirrors that of a standard array. To extend an existing array, use its name followed by square braces. Alternatively, reference another inline array using a dot as a separator for names. The new array inherits data from the existing one, with appended values. 
```
goods [
  bread
  salt
  milk
]

buy [
  items goods [
    water
  ]
]
```
In this example, the "buy" array extends the "goods" array by appending the item "water".

### Entity
The "Entity" feature represents a structured collection of key/value pairs. The entity name is a single word without spaces, and the entity is denoted by a trailing colon ":". Each key/value pair within the entity is indented for clarity. This design ensures a well-defined and organized representation of related data within a distinct entity.

The name of the entity cannot be ended by a dot, as the dot serves as a separator token for referenced data. This rule ensures proper formatting and prevents ambiguity in distinguishing entity names from other elements in the language, maintaining a clear and organized structure.
```
student:
  name John
  age 20
```
In this example, "student" is the entity name, and it encapsulates key/value pairs like "name" with the value "John" and "age" with the value "20". The use of indentation and the ":" symbol provides a clear and structured way to represent entities in the language.

### Inline Entity
The "Inline Entity" feature serves as a value for a key, providing a compact and expressive way to represent structured data. It is declared using curly braces "{}" and includes key/value pairs as well as entities. This allows for the nesting of information within a single key, enhancing readability and organization.

You can overload an existing entity by using its name before curly braces or provide a full path to the inline entity using a dot as a separator. The overloaded entity must exist. In the case of an overload, all data is inherited, and the same key will be overridden by a new value provided in curly braces. This mechanism ensures flexibility and efficient organization of data within the language structure.
```
buy:
  mercedes {
    year 2023
    color black
  }
```
In this example, the "mercedes" key is assigned the value of an inline entity, which contains key/value pairs like "year" with the value "2023" and "color" with the value "black." The use of curly braces "{}" signifies the inline entity, creating a concise and visually clear representation of nested data.

### Comment 
The "Comment" feature allows for annotating code with additional information. Single-line comments start with "//" and are placed on a new line. Multi-line comments begin with "/*" and end with "*/". This feature enhances code readability and documentation.
```
// This is a single-line comment. It should start from a new line.

/* 
  This is a multiline comment.
  You can describe something here.
  It spans multiple lines and provides detailed information.
*/
```
Single-line comments provide brief annotations on a new line, while multi-line comments allow for more extensive descriptions spanning multiple lines.
