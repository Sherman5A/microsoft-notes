
# File Storage

Data storage types:

## Delimited Text Files

Data is stored in plain text format with specific delimiters and row terminators.

Most common format is CSV (comma-separated values) where the delimiters are commas, and rows are
terminated by new lines.

Other formats are:
- Tab-seperated values
- Space-delimited
- Fixed-width data

**Example:** Typical CSV Entry

```csv
FirstName,LastName,Email
Joe,Jones,joe@litware.com
Samir,Nadoy,samir@northwind.com
```

## JavaScript Object Notation: (JSON)

Hierarchial format that defines data entities with multiple data entities (objects) that have
attributes value pairs, these attributes can be other objects or collections of objects.

**Example:** JSON File

```json
{
  "customers":
  [
    {
      "firstName": "Joe",
      "lastName": "Jones",
      "contact":
      [
        {
          "type": "home",
          "number": "555 123-1234"
        },
        {
          "type": "email",
          "address": "joe@litware.com"
        }
      ]
    },
    {
      "firstName": "Samir",
      "lastName": "Nadoy",
      "contact":
      [
        {
          "type": "email",
          "address": "samir@northwind.com"
        }
      ]
    }
  ]
}
```

The JSON file stores a collection of customers.

Each customer has 3 attributes (`firstName`, `lastName`, `contact`).

- `firstName` stores a single String object
- `lastName` stores a single String object
- `contact` stores a collection of objects, `type` and `number`
    - `type` stores a String object
    - `address` stores a String object

## Extensible Markup Language (XML)

HUman readable format. XML uses tags define elements and attributes.

```xml
<Customers>
  <Customer name="Joe" lastName="Jones">
    <ContactDetails>
      <Contact type="home" number="555 123-1234"/>
      <Contact type="email" address="joe@litware.com"/>
    </ContactDetails>
  </Customer>
  <Customer name="Samir" lastName="Nadoy">
    <ContactDetails>
      <Contact type="email" address="samir@northwind.com"/>
    </ContactDetails>
  </Customer>
</Customers>
```

## Binary Large Object (BLOB)

All files are stored as primary data. However, the human-readable formats are mapped to printable
characters. Non-human-readable data consists of raw binary.

Common BLOB types are:
- Images
- Video
- Audio
- Application-specific documents

## Optimised File Formats

Readable formats are not designed to make good use of storage space and processing.

Specialised readable file formats:

![[parquet.webp]]

- Avro
    - Row based format
    - Each record contaiins a header that describes structure of record's data
    - Header is stored as a JSON
    - Data stored as binary information
    - Allows for compression of data, minimising storage and bandwidth requirements
- OCR (Optimised Row Columnar)
    - Orangises data in columns rather than rows
    - OCR contains stripes of data
    - Each stripe holds data for a column
    - A stripe contains an index for the stripe rorws, data for each row, and a footer that contains
      statistical information (count, sum max, min, etc.)
- Parquet
    - Column file format
    - Row group contains a chunk of data, from both row and columns.
    - Metadata describes the set of rows in each chunk
    - Quick location fo chunks by row, and easy retrieval of columns.

