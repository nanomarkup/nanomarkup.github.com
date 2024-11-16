# Nano Markup

Nano Markup is a minimalist markup language designed to prioritize simplicity, clarity, and efficiency. With a focus on core elements like key/value pairs and indentation, Nano Markup offers a straightforward syntax that makes document creation fast and intuitive. Ideal for scenarios where lightweight and human-readable formats are crucial, it provides an elegant way to structure data and information without unnecessary complexity. 

## Language Overview

The Key/Value Pair feature is a fundamental aspect of Nano Markup, defining a unique identifier (key) associated with a corresponding value. Each key is followed by a space, and the data following the key is considered its value. This structure ensures a clear and unambiguous representation of information, where keys uniquely identify specific attributes or properties, and values hold the associated data.

In addition to the Key/Value Pair, indentation plays a crucial role in Nano Markup's syntax. The language uses a special indentation format to structure data hierarchies. This indentation is not just for readability—it's a core feature of the language that defines relationships between elements and organizes data logically. Proper indentation is essential for the accurate parsing and interpretation of the document, ensuring that nested elements and their properties are clearly defined.

The combination of Key/Value pairs and structured indentation makes Nano Markup both efficient and intuitive, offering a clean way to represent information with minimal complexity.

**Key**

A new key always starts on a new line. Keys, essential for identifying attributes or properties, must be unique values and cannot include spaces, ensuring a straightforward and unambiguous structure.

**Value**

A value can take various forms, such as an entity, a list, a single-line value, a multi-line value, or an empty one. This versatility allows for the expression of diverse types of information within the markup language. It provides flexibility in data representation to accommodate various scenarios and enhances the language's adaptability.

## Entity

The Entity represents a structured collection of key/value pairs. Each key/value pair within the entity is placed on a new line, and the entire collection is defined by a consistent one-tab indentation. This indentation creates a clear visual hierarchy, making the data easy to read and interpret.

The one-tab indentation serves as the primary way to define the boundaries of the entity, ensuring that the relationship between the key/value pairs is clear and unambiguous. This approach enhances readability while maintaining a simple, efficient structure for representing related data within a distinct entity.
```
name James
age 20
contacts
    email james@gmail.com
    mobile 123456789
```
In this example, an anonymous entity encapsulates key/value pairs like "name" with the value "James" and "age" with the value "20". "contacts" is the inlined entity. By relying on indentation to structure data, Nano Markup maintains its focus on minimalism and efficiency, making it easy to represent complex information without unnecessary syntax.

## List

The List is an ordered collection of items, where each item is presented on a new line, starting with a one-tab indentation. This structure ensures clarity and organization of the list’s contents.

The list is defined by placing a colon ":" after the key. The key can be empty for an anonymous list. The items begin directly on the next line, indented by a tab. Inline lists or inlined entities also follow this pattern. If an item in the list is an Entity, it is preceded by a dash "-", and the entity starts on the next line with an additional tab of indentation to maintain hierarchical clarity.
```
:
    bread
    salt
:
    onion
    cucumber
```
```
students:
    -
        name James
        age 20
    -
        name John
        age 21
```
This design provides flexibility, allowing lists to contain both simple values and complex entities, all within a structured framework. The use of one-tab indentation for each list item, along with special handling for entities, ensures that data remains easy to read, organized, and adaptable to various needs.

## Value

A **single-line value** is a data representation placed within the current line. It provides a streamlined way to express information without the need for additional formatting.

A **multi-line value** value allows for more extensive information to be captured across several lines. To define a multi-line value, the content is placed on subsequent lines, each starting with an extra tab of indentation. This approach allows the value to span multiple lines, making it ideal for representing more detailed or structured data.

When defining a multi-line value for a key/value pair, any additional lines of the value are indented with an extra tab, preserving the logical flow of the data.
```
name Ariana
age 12
description This is a multi-line value.
    You can add more than one line for data representation.
```
This method provides a clear, intuitive way to express complex or multiline data without the need for additional syntax, promoting readability and simplicity while maintaining the hierarchical structure of the document.

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

- Documentation and Notes: Nano Markup is perfect for creating structured, simple documents and notes. Its clear, minimal syntax makes it easy to write and update textual content without unnecessary complexity.
- Log Files: Nano Markup is ideal for capturing structured log entries. The simplicity of its format makes it easy to parse log data, providing a human-readable way to store and retrieve log information.
- Metadata Storage: For basic metadata management, Nano Markup offers an efficient way to define and store metadata (e.g., tags, descriptions, attributes) using key/value pairs and lists, without adding unnecessary overhead.
- Configuration Files: With its straightforward syntax, Nano Markup is excellent for configuration files in applications, simplifying the process of defining and managing application settings in a readable format.
- Data Exchange: Nano Markup provides an easy-to-understand format for data exchange between systems, offering a lightweight alternative to more complex data formats. It ensures smooth communication while keeping data compact.
- Template Systems: Using Nano Markup for templates (e.g., emails, configuration files, or reports) is easy due to its simple, flexible structure, making it easy to define placeholders and reusable components.
- RESTful APIs: For lightweight data payloads in RESTful APIs, Nano Markup serves as a simple alternative to JSON. Its compact and clear syntax makes it ideal for API communication where reduced payload size is important.
- Scripting and Automation: Nano Markup is useful for defining parameters and configurations in scripts and automation workflows. It offers a concise way to store task lists, state definitions, or automation configurations.
- Knowledge Base: Organizing and structuring knowledge base content with Nano Markup is easy, as its simple format allows for fast updates and clear content management that is accessible to both technical and non-technical users.
- Data Serialization: When serializing data in a human-readable format, Nano Markup provides a simple way to structure and transfer data between systems or applications. Its text-based format makes it easy to serialize and deserialize data without complex parsing.
- Configuration Management: Nano Markup enhances configuration management systems by providing a simple and flexible format for defining and managing settings across environments and applications, reducing the overhead of complex configuration formats.
- IoT Device Communication: In IoT applications, Nano Markup ensures efficient data exchange between devices with varying capabilities. Its simplicity is crucial for managing communication in connected ecosystems where devices may have limited resources.
- Configuration for Embedded Systems: For embedded systems with memory or processing constraints, Nano Markup’s small footprint makes it an excellent choice for configuration management, offering a lightweight format to define system settings in resource-limited environments.

## Example

```
universities:
    -
        name Harvard University
        country USA
        address Massachusetts Hall
            Cambridge, MA 02138
        students:
            -
                name Mark
                age 20
                contacts
                    email mark@gmail.com
                    mobile 12345678
            -
                name Mary
                age 20
                contacts 
                    email mary@gmail.com
                    mobile 678912345
    -
        name University Of Oxford
        country United Kingdom
        address Wellington Square
            Oxford
            OX1 2JD
            United Kingdom
        students:
            -
                name James
                age 20
                contacts
                    email james@gmail.com
                    mobile 123456789
            -
                name John
                age 21
                contacts 
                    email john@gmail.com
                    mobile 345678912
```
