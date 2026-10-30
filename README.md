# Address Book

An address book built with JavaScript constructors and prototypes. Contacts are stored in an `AddressBook` object (a mock database) and each one gets a unique, never-reused ID.

## Setup
1. Clone this repository.
2. Open `index.html` in your browser.
3. To run the tests below, open DevTools, paste the contents of `js/scripts.js` into the console, then run each **Code** line.

## Technologies
HTML, CSS, Bootstrap 5, JavaScript (constructors, prototypes, DOM, event delegation)

## Tests

**Describe:** AddressBook()

**Test:** It should create an AddressBook object with an empty contacts object and a currentId of 0.
**Code:** `let addressBook = new AddressBook();`
**Expected Output:** `AddressBook { contacts: {}, currentId: 0 }`