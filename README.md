# PPSL-Data

This data is mainly used in [Rossmann Repair Group](https://wiki2.rossmanngroup.com/index.php?title=Main_Page)'s Wiki.

Thanks to all of the people who contributed to the Google Docs that this data is scraped from.

## License for data

**GNU Free Documentation License 1.3 or later.**

    Permission is granted to copy, distribute and/or modify this document
    under the terms of the GNU Free Documentation License, Version 1.3
    or any later version published by the Free Software Foundation;
    with no Invariant Sections, no Front-Cover Texts, and no Back-Cover Texts.
    A copy of the license is included in a file named LICENSE found in the root of the project directory.

## Relation

- Product has problems.

- Product may have tags.

- Problems may have solutions.

- Problems may have tags.

- Tags may have parent tags.

- Solutions may have links.

- Solutions may have tags.

- Links may have tags.

## The format

The data is stored in yaml files in the directories of this repository.

All the data structures use their filename as their unique identifier, which is the equivalent of an "unique id" tag in a database.
Fieldnames must start with a lowercase character.

Legends: `?` = May be left empty.

- Product
  - description `string` `?` A brief description about the product
  - number `string` `?` Logic board number for the product
  - year `string` `?` Model release year
  - tags `array[Tag]` `?` Array of tags relating to this product
  - problems `array[Problem]` `?` Array of the problems relating to this product
  - ... [customField] `any` `?` A product can have extra fields as any type.

- Problem
  - label `string` `?` The name of the problem
  - description `string` `?` Brief description about the problem
  - tags `array[Tag]` `?` Array of tags relating to this problem
  - solutions `array[Solution]` `?` Array of solutions relating to this problem

- Solution
  - label `string` `?` The name of the solution
  - description `string` `?` Brief description about the solutions
  - tags `array[Tag]` `?` Array of tags relating to this solution
  - links `array[Link]` `?` Array of links relating to this problem

- Link
  - label `string` `?` The name of the link
  - description `string` `?` Brief description about the link
  - tags `array[Tag]` `?` Array of tags relating to this link
  - url `string` `?` URL of the link

- Tag
  - parent `integer` `?` The identifier of the parent tag
  - label `string` `?` Name of the tag
  - description `string` `?` Brief description about the tag
