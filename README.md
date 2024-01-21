# Nano Markup

Nano Markup is a minimalistic markup language crafted for simplicity and efficiency in document creation. With a focus on fundamental elements, it strives to provide a high-quality and efficient way of expressing information. NanoMarkup is tailored for scenarios where a lightweight and straightforward syntax is paramount.

## Language overview

### Key/Value Pair
The Key/Value Pair feature is a fundamental aspect of the language, defining a unique identifier (key) associated with a corresponding value. Each key is followed by a space, and the data following the key is considered its value. The value can be empty to provide flexibility in data representation. This structure ensures clear and unambiguous representation of information, where keys uniquely identify specific attributes or properties, and values hold the associated data.
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
In this example, the key is "goods" and the associated array includes values like "bread", "salt" and "milk" The syntax promotes readability and organization, while the option for inline arrays or entities adds versatility to the representation of structured data.

**Inline Array**

The Inline Array declaration is the same as the array. 
```
goods [
  bread
  salt
  milk
  vegetables [
    potato
    cucumber
  ]
]
```
In this example, the inline array is "vegetables" which includes values like "potato" and "cucumber".

**Extended Array**

The Extended Array allows you to extend the existing array effortlessly. To extend an existing array, simply use its name followed by square braces. Alternatively, reference another inline array using a dot as a separator for names. The new array inherits data from the existing one, with appended values.
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

tomorrow [
  buy buy.goods [
    butter
  ]
]
```
In this example, the "buy" array extends the "goods" array by adding the item "water" and the "tomorrow.buy" array extends the "buy.goods" array by adding the item "butter". Extended array simplifies array extension for seamless data manipulation.

### Entity
The "Entity" feature represents a structured collection of key/value pairs. The entity name is a single word without spaces, and the entity is denoted by a trailing colon ":". Each key/value pair within the entity is indented for clarity. This design ensures a well-defined and organized representation of related data within a distinct entity.

The name of the entity cannot be ended by a dot, as the dot serves as a separator in the entity path. This rule ensures proper formatting and prevents ambiguity in distinguishing entity names, maintaining a clear and organized structure.
```
student:
  name John
  age 20
```
In this example, "student" is the entity name, and it encapsulates key/value pairs like "name" with the value "John" and "age" with the value "20". The use of indentation and the ":" symbol provides a clear and structured way to represent entities in the language.

**Inline Entity**

The "Inline Entity" feature serves as a value for a key, providing a compact and expressive way to represent structured data. It is declared using curly braces "{}" and includes key/value pairs as well as entities. It enhances readability and data organization.
```
buy:
  mercedes {
    year 2023
    color black
  }
```
In this example, "mercedes" is the inlined entity. The use of curly braces "{}" signifies the inline entity, creating a concise and visually clear representation of nested data.

**Extended Entity**

The Extended Entity allows you to overload an existing entity by using its name before curly braces or provide a full path to the inline entity using a dot as a separator. All data is inherited and the same key will be overridden by a new value provided in curly braces. This mechanism ensures flexibility and efficient organization of data.
```
buy:
  mercedes {
    year 2023
    color black
  }

tomorrow:
  buy buy.mercedes {
    color red
  }
```
In this example, the "tomorrow.buy" key is assigned the value of the extended entity, which contains key/value pairs like "color" with the value "red". The "color" key is replaced by a new value "red".

### Comment 
The "Comment" feature allows for annotating data with additional information. Single-line comments start with "//" and are placed on a new line. Multi-line comments begin with "/*" and end with "*/". This feature enhances data readability and documentation.
```
// This is a single-line comment. It should start from a new line.

/* 
  This is a multiline comment.
  You can describe something here.
  It spans multiple lines and provides detailed information.
*/
```
Single-line comments provide brief annotations on a new line, while multi-line comments allow for more extensive descriptions spanning multiple lines.
