# Nano Markup

Nano Markup is a minimalistic markup language meticulously designed for simplicity and efficiency in document creation. With a focus on fundamental elements, it strives to provide a high-quality and efficient means of expressing information. NanoMarkup is tailored for scenarios where a lightweight and straightforward syntax is paramount.

**The Key/Value Pair** feature is a fundamental aspect of the language, defining a unique identifier (key) associated with a corresponding value. Each key is followed by a space, and the data following the key is considered its value. This structure ensures a clear and unambiguous representation of information, where keys uniquely identify specific attributes or properties, and values hold the associated data.

## Key

A new key always starts on a new line. Keys, essential for identifying attributes or properties, cannot include spaces or dots, ensuring a straightforward and unambiguous structure.

A key in Nano Markup can take various forms, such as an entity, an array, a single-line value, or a multi-line value. This versatility allows for expressing diverse types of information within the markup language. Additionally, a key can be left empty, providing flexibility in data representation to accommodate various scenarios and enhance the language's adaptability.

### Entity
The "Entity" in Nano Markup signifies a structured collection of key/value pairs. Each key/value pair within the entity starts from a new line for clarity, enhancing readability and organization. The use of curly braces "{}" encapsulates the entity, offering a clear visual delineation and reinforcing the hierarchical structure of the data. This deliberate design ensures a well-defined and organized representation of related data within a distinct entity, promoting clarity and ease of interpretation.
```
student {
  name John
  age 20
}
```
In this example, "student" is the entity, and it encapsulates key/value pairs like "name" with the value "John" and "age" with the value "20". The use of curly braces "{}" provides a clear and structured way to represent entities in the language.

**Inline Entity**

The Inline Entity declaration mirrors the structure of a regular entity.  
```
buy {
  car {
    year 2023
    color black
  }
}
```
In this example, "car" is the inlined entity. 

**Extended Entity**

The Extended Entity introduces the ability to overload an existing entity by providing a full name to the inline entity before curly braces using a dot as a separator. This innovative feature allows for seamless data inheritance, where all data from the original entity is retained, and any overlapping keys are overridden by the new values. This mechanism ensures a high degree of flexibility and efficient organization of data, providing users with powerful tools for managing and extending entity structures within the markup language.
```
buy {
  car {
    year 2023
    color black
  }
}

tomorrow {
  buy buy.car {
    color red
  }
}
```
In this example, the "tomorrow.buy" entity is assigned the value of the extended entity, which contains key/value pairs like "color" with the value "red". The "color" key is replaced by a new value "red" for the "tomorrow.buy" entity only.

### Array
The Array feature facilitates the assignment of a list of values to a key. Each value is presented on a new line, contributing to the overall clarity of the structure. Furthermore, the array can include inline arrays or inline entities, adding an extra layer of flexibility to accommodate various data structures. The use of square brackets "[]" encapsulates the array, offering a distinct visual representation. This intentional design ensures a clean and organized portrayal of ordered data associated with a specific key, promoting clarity and facilitating the effective representation of structured information.
```
goods [
  bread
  salt
  milk
]
```
In this example, the key is "goods" and the associated array includes values like "bread", "salt" and "milk" The syntax promotes readability and organization, while the option for inline arrays or entities adds versatility to the representation of structured data.

**Inline Array**

The Inline Array declaration mirrors the structure of a regular array. 
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

The Extended Array feature facilitates the effortless extension of an existing array. To achieve this, simply use the full name of the existing array followed by square brackets. Alternatively, reference another inline array by using a dot as a separator for names. In this process, the new array inherits data from the existing one, with appended values. This mechanism ensures a straightforward means of expanding arrays while maintaining the integrity of existing data structures, providing users with a powerful tool for managing and extending array content within the markup language.
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
