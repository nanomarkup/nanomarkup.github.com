# Nano Markup

Nano Markup is a minimalistic markup language meticulously designed for simplicity and efficiency in document creation. With a focus on fundamental elements, it strives to provide a high-quality and efficient means of expressing information. NanoMarkup is tailored for scenarios where a lightweight and straightforward syntax is paramount.

## Language Overview

The Key/Value Pair feature is a fundamental aspect of the language, defining a unique identifier (key) associated with a corresponding value. Each key is followed by a space, and the data following the key is considered its value. This structure ensures a clear and unambiguous representation of information, where keys uniquely identify specific attributes or properties, and values hold the associated data.
The Key/Value Pair is an integral part of the entity structure.

The array is the **default structure** if another structure is not explicitly specified.

**Key**

A new key always starts on a new line. Keys, essential for identifying attributes or properties, must be unique values and cannot include spaces or dots, ensuring a straightforward and unambiguous structure.

**Value**

A value can take various forms, such as an entity, an array, a single-line value, a multi-line value, or an empty one. This versatility allows for the expression of diverse types of information within the markup language. It provides flexibility in data representation to accommodate various scenarios and enhances the language's adaptability.

## Entity

The "Entity" in Nano Markup signifies a structured collection of key/value pairs. Each key/value pair within the entity starts from a new line for clarity, enhancing readability and organization. The use of curly braces "{}" encapsulates the entity, offering a clear visual delineation and reinforcing the hierarchical structure of the data. This deliberate design ensures a well-defined and organized representation of related data within a distinct entity, promoting clarity and ease of interpretation.
```
{
    name James
    age 20
    // the inlined contacts entity
    contacts {
        email james@gmail.com
        mobile 123456789
    }
}
```
In this example, an anonymous entity encapsulates key/value pairs like "name" with the value "James" and "age" with the value "20". "contacts" is the inlined entity. The use of curly braces "{}" provides a clear and structured way to represent entities in the language.

## Array

Each value is presented on a new line, contributing to the overall clarity of the structure. Furthermore, the array can include inline arrays or inline entities, adding an extra layer of flexibility to accommodate various data structures. The use of square brackets "[]" encapsulates the array, offering a distinct visual representation. This intentional design ensures a clean and organized portrayal of ordered data associated with a specific key, promoting clarity and facilitating the effective representation of structured information.
```
bread
salt
// the inline array of vegetables
[
    potato
    cucumber
]
// the inline car entity
{
    name car
    year 2023
    color black
}
```
In this example, the associated array includes values like 'bread' and 'salt', showcasing both inlined array and inlined entity. The root square brackets are omitted, and it is considered an array by default. This syntax promotes readability and organization, while the option for inline arrays or entities adds versatility to the representation of structured data.

## Value

A **single-line value** is a data representation placed within the current line. It provides a streamlined way to express information without the need for additional formatting.

A **multi-line value** offers the flexibility to capture more extensive information by spanning across multiple lines. It is denoted by enclosing the content within the backtick at both the beginning and the end. This feature allows for the expression of detailed and multiline data, facilitating a more comprehensive representation within the markup language.
```
name Ariana
age 12
description `
This is a multi-line value.
You can more than one line for data representation.
`
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

## Use Cases

- Configuration Files: Ideal for configuration files in applications, Nano Markup simplifies the setup process with its intuitive structure.
- Data Exchange: Facilitate smooth data exchange between systems and applications with Nano Markup's straightforward syntax.
- RESTful APIs: Nano Markup can be used as a lightweight alternative to JSON for defining data payloads in RESTful API communication.
- IoT Device Communication: Simplify communication between Internet of Things (IoT) devices with Nano Markup, ensuring efficient and standardized data exchange in connected ecosystems.
- Configuration Management: Enhance configuration management systems with the simplicity and flexibility of Nano Markup, providing a standardized format for defining and managing settings across applications and environments.

## Example

```
universities [
    {
        name Harvard University
        country USA
        address `
Massachusetts Hall
Cambridge, MA 02138
`
        students [
            {
                name Mark
                age 20
                contacts {
                    email mark@gmail.com
                    mobile 123456789
                }
            }
            {
                name Mary
                age 20
                contacts {
                    email mary@gmail.com
                    mobile 678912345
                }
            }
        ]
    }
    {
        name University Of Oxford
        country United Kingdom
        address `
Wellington Square
Oxford
OX1 2JD
United Kingdom
`
        students [
            {
                name James
                age 20
                contacts {
                    email james@gmail.com
                    mobile 123456789
                }
            }
            {
                name John
                age 21
                contacts {
                    email john@gmail.com
                    mobile 345678912
                }
            }     
        ]
    }
]
```
