# Nano Markup

Nano Markup is a minimalistic markup language crafted for simplicity and efficiency in document creation. With a focus on fundamental elements, it strives to provide a high-quality and efficient way of expressing information. NanoMarkup is tailored for scenarios where a lightweight and straightforward syntax is paramount.

**A Key/Value Pair** feature is a fundamental aspect of the language, defining a **unique** identifier (key) associated with a corresponding value. Each key is followed by a space, and the data following the key is considered its value. 

This structure ensures clear and unambiguous representation of information, where keys uniquely identify specific attributes or properties, and values hold the associated data.

## Key

A new key starts from a new line. Keys cannot include spaces or dots. The key can be an entity, an array, a single-line value, or a multi-line value. Also, it can be empty to provide flexibility in data representation.

### Entity
The "Entity" represents a structured collection of key/value pairs. Each key/value pair within the entity is indented for clarity. The use of curly braces "{}" encapsulates the entity, providing a clear visual delineation. This design ensures a well-defined and organized representation of related data within a distinct entity.
```
student {
  name John
  age 20
}
```
In this example, "student" is the entity, and it encapsulates key/value pairs like "name" with the value "John" and "age" with the value "20". The use of curly braces "{}" provides a clear and structured way to represent entities in the language.

**Inline Entity**

The Inline Entity declaration is the same as the entity. 
```
buy {
  mercedes {
    year 2023
    color black
  }
}
```
In this example, "mercedes" is the inlined entity. 

**Extended Entity**

The Extended Entity allows you to overload an existing entity by using its name before curly braces or provide a full name to the inline entity using a dot as a separator. All data is inherited and the same key will be overridden by a new value provided in curly braces. This mechanism ensures flexibility and efficient organization of data.
```
buy {
  mercedes {
    year 2023
    color black
  }
}

tomorrow {
  buy buy.mercedes {
    color red
  }
}
```
In this example, the "tomorrow.buy" entity is assigned the value of the extended entity, which contains key/value pairs like "color" with the value "red". The "color" key is replaced by a new value "red" for the "tomorrow.buy" entity only.

### Array
The Array allows the assignment of a list of values to a key. Each value is placed on a new line, contributing to the clarity of the structure. Additionally, the array can include inline arrays or inline entities, enhancing flexibility. The use of square brackets "[]" encapsulates the array, providing a clear visual delineation. This design ensures a clean representation of ordered data associated with a specific key.
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

The Extended Array allows you to extend the existing array effortlessly. To extend an existing array, simply use its full name followed by square braces. Alternatively, reference another inline array using a dot as a separator for names. The new array inherits data from the existing one, with appended values.
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

## Value

A **single-line value** is a data representation placed within the current line. It provides a streamlined way to express information without the need for additional formatting.

A **multi-line value** offers the flexibility to capture more extensive information by spanning across multiple lines. It is denoted by enclosing the content within triple quotes at both the beginning and the end. This feature allows for the expression of detailed and multiline data, facilitating a more comprehensive representation within the markup language.
```
name Ariana
age 12
description """
This is a multi-line value.
You can more than one line for data representation.
"""
```
In this example, "name" and "age" are the keys, and "Ariana" and "12" are their corresponding single-line values. The "description" key represents multi-line value. The simplicity of this structure allows for straightforward representation of various data points in a concise manner.

## Comment 
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
