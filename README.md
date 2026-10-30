# Address Book

An address book built with JavaScript constructors and prototypes. Contacts are stored in an `AddressBook` object (a mock database) and each one gets a unique, never-reused ID.

**Live site:** https://njenga77.github.io/Code-Along/

## Setup
1. Clone this repository.
2. Open `index.html` in your browser.
3. To run the tests below, open DevTools, paste the contents of `script.js` into the console, then run each **Code** line.

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

---

**Describe:** AddressBook.prototype.findContact()

**Test:** It should return the contact that matches the id.
**Code:** `addressBook.findContact(1);`
**Expected Output:** `Contact { firstName: "Titus", lastName: "Njenga", phoneNumber: "070-555-0100", id: 1 }`


**Test:** It should return false if no contact has that id.
**Code:** `addressBook.findContact(99);`
**Expected Output:** `false`

---

**Describe:** AddressBook.prototype.deleteContact()

**Test:** It should remove the contact with the matching id and return true.
**Code:** `addressBook.deleteContact(1);`
**Expected Output:** `true` (and `addressBook.contacts` is now `{}`)


**Test:** It should return false if no contact has that id.
**Code:** `addressBook.deleteContact(99);`
**Expected Output:** `false`


**Test:** It should never reuse a deleted contact's id.
**Code:** `addressBook.currentId;` (after deleting contact 1 when 2 contacts were added)
**Expected Output:** `2`