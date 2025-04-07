# UML Class Diagrams
Use the app at [draw.io](https://draw.io) / [diagrams.net](https://diagrams.net) to create UML Class Diagrams for each of the object-oriented programming systems here.

Follow the St. Augustine CHS [ICS4U house style](https://github.com/davecheng-tech/Random-Notes/blob/main/object-oriented-programming/uml-class-diagrams.md) for the diagrams.

### File Formats from Draw.io
In the web editor, diagrams saved in `.drawio` file format retain the ability to edit.

However, the simplest way to embed these diagrams is to use a PNG version. In the app, select `File` > `Export as` > `PNG...` and change the `Zoom` to `200%` for a higher quality output.

Put the PNG files in the `images/` folder to keep the root directory of this repo clean and uncluttered. Embed the images in this `README.md` file below using the proper [Markdown syntax](https://www.squash.io/how-to-display-local-image-in-markdown/).

Let's begin.

<br>

## System 1
Design a simple text messaging system. Each `Message` object includes who sent it, who it’s to, when it was sent, and the content. An `Inbox` holds multiple messages and allows the user to browse previews or search by sender.

#### `EMBED UML CLASS DIAGRAM HERE`

#### Message.java
- Fields: `sender`, `recipient`, `timestamp`, `body`
- Constructor to initialize all fields
- Methods:
  - `String getPreview()` – returns first 30 characters of the body
  - Getters for all fields (no setters)

#### Inbox.java
- Aggregates a `List<Message>`
- Methods:
  - `void addMessage(Message m)`
  - `List<String> getPreviews()`
  - `List<Message> getMessagesFrom(String sender)`

<br>

## System 2
Write a simple restaurant ordering system. Each `MenuItem` has a name and a base price. An `Order` contains multiple menu items and calculates the total with tax.

#### `EMBED UML CLASS DIAGRAM HERE`

#### MenuItem.java
- Fields: `name`, `basePrice`
- Methods:
  - `double getPriceWithTax()` – assume 13% HST
  - `String toString()` – returns formatted string like `"Pizza - $11.29"`

#### Order.java
- Aggregates a `List<MenuItem>`
- Methods:
  - `void addItem(MenuItem item)`
  - `double getTotalBeforeTax()`
  - `double getTotalAfterTax()`
  - `void printReceipt()`

<br>

## System 3
Create a contact manager. Each `Person` object contains name and phone number. A `ContactList` stores multiple people and allows lookup by last name.

### Requirements:

#### `EMBED UML CLASS DIAGRAM HERE`

#### Person.java
- Fields: `firstName`, `lastName`, `phoneNumber`
- Methods:
  - `String getDisplayName()` – returns `"Last, First"`
  - `String getPhoneNumber()`

#### ContactList.java
- Aggregates a `List<Person>`
- Methods:
  - `void addPerson(Person p)`
  - `List<Person> findByLastName(String lastName)`
  - `List<String> getAllDisplayNames()`

<br>

## System 4
You’re building a basic tracker for a friend’s Pokémon card collection. They want a simple way to organize their cards and view interesting information about them. Your program should represent **individual Pokémon cards** and a **collection** of those cards.

#### `EMBED UML CLASS DIAGRAM HERE`