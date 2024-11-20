# Nano Markup
Nano Markup is a minimalist markup language designed to prioritize simplicity, clarity, and efficiency. With a focus on core elements like key/value pairs and indentation, Nano Markup offers a straightforward syntax that makes document creation fast and intuitive. Ideal for scenarios where lightweight and human-readable formats are crucial, it provides an elegant way to structure data and information without unnecessary complexity. 

## Language Overview
In Nano Markup, the **Key/Value** pair is a fundamental building block of the language, forming the core of how data is represented within a document. Each section consists of one or more keys, which act as unique identifiers, and their associated values. This structure ensures clarity and precision by defining relationships and properties in an unambiguous manner.

Keys always appear on a new line and must be unique within the same scope. They cannot include spaces or special characters, ensuring simplicity and consistency. Values, assigned to these keys, are versatile and can take various forms:
- Single-line values for concise data.
- Multi-line values for descriptive or extended content.
- Lists for collections of related items.
- Empty values for placeholder-like entries.

Additionally, indentation is a crucial element of Nano Markup. It is not merely a formatting choice but an integral part of the syntax. Indentation defines the hierarchical relationships between records and organizes data into clear, logical structures. Proper use of indentation ensures the document is both human-readable and machine-parsable.

## Section
A **Section** represents a structured collection of key/value pairs. Each key/value pair within the section appears on its own line, and the entire collection is defined by consistent one-tab indentation. This indentation not only visually organizes the data but also defines the hierarchical structure of the section, making the content both easy to read and interpret.

The use of one-tab indentation is essential, as it clearly demarcates the boundaries of the section and ensures an unambiguous relationship between the key/value pairs. This approach enhances the overall readability of the document, while keeping the structure simple and efficient for representing related data within a distinct unit.
```
Ariana..
    birthday 7.8.2011
    contacts..
        email ariana@gmail.com
        mobile 123456789
```
In this example, the **Ariana** section encapsulates key/value pair such as "birthday" with the value "7.8.2011" and a **contacts** section. The **contacts** section, which is indented under **Ariana**, is an inlined section, containing its own key/value pairs. By relying on indentation to structure the data, Nano Markup maintains its focus on minimalism and efficiency, enabling the representation of complex information without unnecessary syntax.
#### Key Notes
- ".. " defines the beginning of a Section, signaling the start of a structured collection of key/value pairs.
- Each **key** and its **value** are placed on their own line, and the entire Section is indented with one tab.

## List
A List is an ordered collection of items, where each item appears on a new line and is indented with a single tab. This structure ensures that the list’s contents are clear and organized.

A list is defined by placing a colon (":") after the key. The key can be omitted for an **anonymous list**. The list items follow immediately on the next line, each indented by one tab. Inline lists or inlined sections follow this same pattern.

If an item in the list is a **Section**, it is preceded by a double dot (".."). The section itself starts on the next line with an additional tab of indentation, ensuring that the hierarchy remains clear and properly structured.
```
:
    Math
    English
    History

students:
    ..
        name James
        age 20
    ..
        name John
        age 21
```
This design provides flexibility, allowing lists to contain both simple values and complex entities, all within a structured framework. The use of one-tab indentation for each list item, along with special handling for entities, ensures that data remains easy to read, organized, and adaptable to various needs.
#### Key Notes
- A colon (":") after the key indicates the start of the list.
- The key can be omitted for anonymous lists (lists without a key).
- Each item in the list is indented with one tab.
- Sections within a list are preceded by a double dot ("..") and indented with an additional tab.

## Value
A **single-line value** is a data representation placed within the current line. This provides a streamlined way to express information without requiring extra formatting.

A **multi-line value** allows for more extensive information to be captured across several lines. To define a multi-line value, the content is placed on subsequent lines, each starting with an additional tab of indentation. This approach is ideal for representing more detailed or structured data that spans multiple lines.

When defining a multi-line value for a key/value pair, any additional lines of the value are indented with one extra tab, preserving the logical structure and readability of the document.
```
name Ariana
age 12
description This is a multi-line value.
    You can add more than one line for data representation.
```
This method provides a clear, intuitive way to express complex or multi-line data, without requiring additional syntax. It maintains the hierarchical structure of the document, promoting readability and simplicity.
#### Key Notes
- A **single-line value** is written directly on the same line as the key.
- A **multi-line value** starts on the same line as the key and is continued on subsequent lines, each indented with an additional tab.
- The extra tab of indentation for multi-line values maintains the structure of the document and ensures clarity.
- **Multi-line values** are ideal for representing complex or structured data that spans more than one line.

## Comment 
A **comment** is used to add notes, explanations, or annotations to the document. Comments are ignored during parsing and are purely for human readability and documentation.

A **comment** must always begin on a new line. It cannot be placed alongside a value, key, or section. This ensures that comments remain separate from the actual data and do not interfere with the structure.

A **single-line comment** begins with the # symbol, followed by the comment text. The entire comment is confined to that line.

A **multi-line comment** starts with # on the first line, and subsequent lines are indented with one extra tab to continue the comment.
```
# This is a single-line comment. It should start from a new line.

# This is a multiline comment.
    You can describe something here.
    It spans multiple lines and provides detailed information.
```
#### Key Notes
- A **comment** must always start on a new line and cannot be added to a value, key, or section.
- A **single-line comment** begins with # and continues to the end of the line.
- A **multi-line comment** starts with # and continues on subsequent lines, each indented with one extra tab.
- Comments are ignored during parsing and are intended for human readability and documentation.
- **Multi-line comments** allow for longer explanations or detailed notes.

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
