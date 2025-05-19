#  alu_regex-data-extraction-Julia04-rub

This repository contains a Python-based tool that uses regular expressions (regex)to extract specific types of data from a given input string. The tool is designed to identify and extract:

- Email Addresses
- Phone Numbers
- Credit Card Numbers
- HTML Tags
- Hashtags

##  What This Tool Does

Using Python's built-in `re` module, this script scans a multiline input string and extracts all matching patterns for the selected data types. The code is modular, reusable, and easy to extend with additional regex validations if needed.


##  Extracted Data Types

1. Email Addresses
 Formats: `user@example.com`, `firstname.lastname@domain.co.uk`

2. Phone Numbers
 Formats: `(123) 456-7890`, `123-456-7890`, `123.456.7890`

3. Credit Card Numbers
 Formats: `1234 5678 9012 3456`, `1234-5678-9012-3456`

4. HTML Tags
 Examples: `<p>`, `<div class="example">`, `<img src="image.jpg" alt="description">`

5. Hashtags
 Examples: `#example`, `#ThisIsAHashtag`


##  Sample Input

```text
user@example.com firstname.lastname@company.co.uk invalid-email
https://www.example.com http://subdomain.example.org/page ftp://not-a-valid-url
(123) 456-7890 123-456-7890 123.456.7890 not-a-phone-number
1234 5678 9012 3456 1234-5678-9012-3456 invalid-card
14:30 2:30 PM invalid-time
<p> <div class="example"> <img src="image.jpg" alt="description">
#example #ThisIsAHashtag invalid-hashtag
$19.99 $1,234.56 invalid-currency
