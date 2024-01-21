
# Quick Java Web Development Guide for Python Developers

## Introduction
This guide is for Python developers who need to quickly adapt to Java for web development. We'll cover setting up Java in VSCode, basic web app development in Python and Java, and API development using Flask in Python and Spring in Java.

## Setting Up Java in VSCode

1. **Install VSCode**:
   - Download from [Visual Studio Code website](https://code.visualstudio.com/).

2. **Install Java Extensions**:
   - Open VSCode.
   - Go to Extensions (`Ctrl+Shift+X`).
   - Search and install `Java Extension Pack` by Microsoft.

3. **Configure Java Environment**:
   - VSCode will automatically detect JDK if installed. Otherwise, follow prompts to install JDK.

## Building a Web App in Python vs Java

### Python Web App with Flask

1. **Create a Flask App**:
   ```python
   from flask import Flask
   app = Flask(__name__)

   @app.route('/')
   def hello_world():
       return 'Hello, world!'
   ```

2. **Run Flask App**:
   - Set environment variable: `export FLASK_APP=hello.py`.
   - Run `flask run`.

### Java Web App with Jetty and Spring

1. **Create a Spring Boot Project**:
   - Use [Spring Initializr](https://start.spring.io/) to generate a project with `Spring Web` dependency.
   - Extract and open the project in VSCode.

2. **Create a Controller**:
   ```java
   import org.springframework.web.bind.annotation.GetMapping;
   import org.springframework.web.bind.annotation.RestController;

   @RestController
   public class HelloController {

       @GetMapping("/")
       public String helloWorld() {
           return "Hello, world!";
       }
   }
   ```

3. **Run Spring Application**:
   - Right-click on the main application file.
   - Select `Run`.

## Developing APIs: Python Flask vs Java Spring

### API Development in Flask

- **Define a Route**:
  ```python
  @app.route('/api/items')
  def get_items():
      return jsonify(items)
  ```

- **Run Flask App**:
  - `flask run`.

### API Development in Spring

- **Define a Controller**:
  ```java
  import org.springframework.web.bind.annotation.GetMapping;
  import org.springframework.web.bind.annotation.RequestMapping;
  import org.springframework.web.bind.annotation.RestController;
  import java.util.List;

  @RestController
  @RequestMapping("/api/items")
  public class ItemController {

      @GetMapping
      public List<Item> getItems() {
          return List.of(new Item("Item 1"), new Item("Item 2"));
      }
  }
  ```

- **Run Spring Application**:
  - Right-click on the main application file > `Run`.

## Conclusion

This guide provides an overview of setting up Java in VSCode and developing web applications in both Python and Java. Remember, practice and exploration are key to mastering these technologies.

## Resources

- [VSCode Java Documentation](https://code.visualstudio.com/docs/languages/java)
- [Spring Documentation](https://spring.io/projects/spring-boot)
- [Flask Documentation](https://flask.palletsprojects.com/en/1.1.x/)
