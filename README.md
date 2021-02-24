# PPSL-TEST

## License for data
**GNU Free Documentation License 1.3 or later.**

For the main use in [Rossmann Repair Group](https://wiki2.rossmanngroup.com/index.php?title=Main_Page)'s Wiki.

A thanks to all of the people who contributed to the Google Docs that this data is scraped from.

## Relation
Product has problems.
Problems may have solutions.
Solutions may have links.

Legends: `?` = May be left optional

- Product `"Name is the label."`
  - description `string` `?`
  - number `string` `?`
  - year `string` `?`
  - problems `array of strings that have the name of the problem` `?`
- Problem `"Name is the number of entry"`
  - label `string` `?`
  - description `string` `?`
  - solutions `array of strings that have the name of the solution` `?`
- Solution `"Name is the number of entry"`
  - label `string` `?`
  - description `string` `?`
  - links `optional array of strings that have the name of the link` `?`
- Link `"Name is the number of entry"`
  - label `string` `?`
  - description `string` `?`
  - url `string` `?`
