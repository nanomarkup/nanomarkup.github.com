# Nano Markup
Nano Markup is a minimalist markup language designed to prioritize simplicity, clarity, and efficiency. With a focus on core elements like key/value pairs and indentation, Nano Markup offers a straightforward syntax that makes document creation fast and intuitive. Ideal for scenarios where lightweight and human-readable formats are crucial, it provides an elegant way to structure data and information without unnecessary complexity. 

## Language Overview
In Nano Markup, the Key/Value pair forms the foundation of the language, serving as the primary building block for representing data. Documents are inherently structured as **List** by default, where all top-level elements are treated as entries in an implicit list.

Each document consists of one or more sections composed of keys, which act as unique identifiers, paired with their corresponding values. This design ensures clarity by defining relationships and properties in an unambiguous and consistent manner.

#### Key Characteristics
- Keys
    - Unique within their scope
    - Always appear on a new line
    - Cannot include spaces or special characters
- Values
    - Single-line values: For concise data
    - Multi-line values: For extended or descriptive content
    - Empty values: For placeholders or default entries
    - Lists: For collections of related items
    - Sections: For grouping related key/value pairs under a common entity
- Indentation
    - Defines hierarchical relationships
    - Organizes data into clear, logical structures
    - Ensures documents are both human-readable and machine-parsable

## Sections
Sections group related key/value pairs under a single entity. Each section is defined with the double dot "..", followed by an indented block containing its key/value pairs. Indentation is vital for establishing hierarchy and readability.
```
Ariana..
    birthday 7.8.2011
    contacts..
        email ariana@gmail.com
        mobile 123456789
```
In this example:
- **Ariana** is a section containing a birthday key/value pair and a nested **contacts** section.
- Indentation determines the scope of key/value pairs and sections.
#### Key Notes
- ".." signals the start of a Section
- All keys and values within a Section are indented with one tab

## Lists
A document in Nano Markup is treated as a **List by default**, meaning all top-level elements are considered entries within an implicit list structure.

Lists are explicitly defined using a colon ":" after the key. If the key is omitted, the list becomes **anonymous**. Items in the list appear on subsequent lines, each indented by one tab. Lists can also contain Sections, indicated by the ".." symbol.
```
students:
    ..
        name James
        age 20
    ..
        name John
        age 21

:
    Math
    English
    History
```
This design provides flexibility, allowing lists to contain both simple values and complex entities, all within a structured framework. The use of one-tab indentation for each list item, along with special handling for entities, ensures that data remains easy to read, organized, and adaptable to various needs.
#### Key Notes
- The entire document is implicitly a List at the top level
- A colon ":" after the key indicates the start of the list
- The key can be omitted for anonymous lists (lists without a key)
- Each list item is indented by one tab
- Sections within a List are preceded by a double dot ".." and indented with an additional tab

## Values
Values define the data associated with a key and come in two forms:
- A **single-line value** is data representation placed within the current line
- A **multi-line value** is extended data spans multiple lines, with additional lines indented by one tab
```
name Ariana
age 12
description This is a multi-line value.
    You can add more than one line for data representation.
```
This method provides a clear, intuitive way to express complex or multi-line data, without requiring additional syntax. It maintains the hierarchical structure of the document, promoting readability and simplicity.
#### Key Notes
- A single-line value is written directly on the same line as the key
- A multi-line value starts on the same line as the key and is continued on subsequent lines, each indented with an additional tab
- Extra indentation for multi-line values ensures readability and consistency

## Comments
A comment is used to add notes, explanations, or annotations to the document. The comment must always begin on a new line. It cannot be placed alongside a value, key, or section. This ensures that comments remain separate from the actual data and do not interfere with the structure.

A **single-line comment** starts with the "#" symbol and occupy a single line.
A **multi-line comment** starts with the "#" and subsequent lines are indented with one extra tab to continue the comment.
```
# This is a single-line comment. It should start from a new line.

# This is a multiline comment.
    You can describe something here.
    It spans multiple lines and provides detailed information.
```
#### Key Notes
- Comments must begin on a new line
- Comments cannot be placed alongside keys or values
- Multi-line comments require additional indentation for continuation

## Use Cases
- Documentation and Notes: Nano Markup is perfect for creating structured, simple documents and notes. Its clear, minimal syntax makes it easy to write and update textual content without unnecessary complexity.
- Log Files: Nano Markup is ideal for capturing structured log entries. The simplicity of its format makes it easy to parse log data, providing a human-readable way to store and retrieve log information.
- Metadata Storage: For basic metadata management, Nano Markup offers an efficient way to define and store metadata (e.g., tags, descriptions, attributes) using key/value pairs and lists, without adding unnecessary overhead.
- Configuration Files: With its straightforward syntax, Nano Markup is excellent for configuration files in applications, simplifying the process of defining and managing application settings in a readable format.
- Data Exchange: Nano Markup provides an easy-to-understand format for data exchange between systems, offering a lightweight alternative to more complex data formats. 
- Template Systems: Using Nano Markup for templates (e.g., emails, configuration files, or reports) is easy due to its simple, flexible structure, making it easy to define placeholders and reusable components.
- RESTful APIs: For lightweight data payloads in RESTful APIs, Nano Markup serves as a simple alternative to JSON. Its compact and clear syntax makes it ideal for API communication.
- Scripting and Automation: Nano Markup is useful for defining parameters and configurations in scripts and automation workflows. It offers a concise way to store task lists, state definitions, or automation configurations.
- Knowledge Base: Organizing and structuring knowledge base content with Nano Markup is easy, as its simple format allows for fast updates and clear content management that is accessible to both technical and non-technical users.
- Data Serialization: When serializing data in a human-readable format, Nano Markup provides a simple way to structure and transfer data between systems or applications. Its text-based format makes it easy to serialize and deserialize data without complex parsing.
- Configuration Management: Nano Markup enhances configuration management systems by providing a simple and flexible format for defining and managing settings across environments and applications, reducing the overhead of complex configuration formats.
- IoT Device Communication: In IoT applications, Nano Markup ensures efficient data exchange between devices with varying capabilities. Its simplicity is crucial for managing communication in connected ecosystems where devices may have limited resources.

## Example
```
universities:
    ..
        name Harvard University
        country USA
        address Massachusetts Hall
            Cambridge, MA 02138
        students:
            ..
                name Mark
                age 20
                contacts
                    email mark@gmail.com
                    mobile 12345678
            ..
                name Mary
                age 20
                contacts 
                    email mary@gmail.com
                    mobile 678912345
    ..
        name University Of Oxford
        country United Kingdom
        address Wellington Square
            Oxford
            OX1 2JD
            United Kingdom
        students:
            ..
                name James
                age 20
                contacts
                    email james@gmail.com
                    mobile 123456789
            ..
                name John
                age 21
                contacts 
                    email john@gmail.com
                    mobile 345678912
```
