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

---

**Describe:** Contact()

**Test:** It should create a Contact object with firstName, lastName and phoneNumber properties.
**Code:** `let contact = new Contact("Titus", "Njenga", "070-555-0100");`
**Expected Output:** `Contact { firstName: "Titus", lastName: "Njenga", phoneNumber: "070-555-0100" }`

---

**Describe:** Contact.prototype.fullName()

**Test:** It should return a contact's first and last name joined by a space.
**Code:** `contact.fullName();`
**Expected Output:** `"Titus Njenga"`

---

**Describe:** AddressBook.prototype.assignId()

**Test:** It should increase currentId by 1 and return it each time it is called.
**Code:** `addressBook.assignId();`
**Expected Output:** `1` (then `2` on the next call)

---

**Describe:** AddressBook.prototype.addContact()

**Test:** It should give a contact an id and store it in contacts under that id.
**Code:** `addressBook.addContact(contact); addressBook.contacts[contact.id];`
**Expected Output:** `Contact { firstName: "Titus", lastName: "Njenga", phoneNumber: "070-555-0100", id: 1 }`