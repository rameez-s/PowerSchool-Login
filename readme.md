# PowerSchool Login

This class will allow you to quickly and easily connect to a Pearson Powered PowerSchool site for you to parse the pages concealed by the Username and Password credentials using Java.

Brief Description:
  - Create an object of the class, passing it the Username and Password parameters
  - Use JSoup or another Java library for web parsing to parse the pages
  - Profit?

### Setup
* Download [HTMLUnit]: GUI-less web browser! Make sure you've imported this library.
* Download [JSoup] or other Web Parse Java Library 
* Initialize String variable *loginURL* in *login()* method to link of your PowerSchool Login Page.

### Printing the Title of the Gradebook Page

* Download and add the PSLogin.java class to your project
* Import HTMLUnit
* Import JSoup
* In your Main class:

```java
String user = "17jsmith";
String pass = "123456";
String link = "link"; //paste link to landing page after login
PSLogin client = new PSLogin(user, pass);
client.login();
String page = client.get(link);
Document doc = Jsoup.parse(page);
System.out.println(doc.title());
```

### Methods


* Constructor: Passes inititalizes username and password variables
* void login(): Passes site username and password credentials, and presses submit
* String get(String url): Returns html of page of url

### Development
I'm working on a PowerSchool universal GPA Calculator, I'll make the repo soon for collaboration!

License
----

MIT

   [HTMLUnit]: <http://htmlunit.sourceforge.net/>
   [JSoup]: <https://jsoup.org/download>

