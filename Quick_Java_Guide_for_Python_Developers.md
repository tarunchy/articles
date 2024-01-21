
# Quick Java Guide for Python Developers

## Introduction
This guide is for Python developers who need to quickly adapt to Java. We cover setting up Java, running applications, unit testing, and basic coding, along with comparing key programming concepts between Python and Java.

## Environment Setup

### Install Java
1. **Download JDK**: Visit the [Oracle website](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) and download the Java Development Kit (JDK) for your OS.
2. **Install JDK**: Follow the installation instructions for your OS.

### Set up an IDE
1. **Download IntelliJ IDEA**: [JetBrains](https://www.jetbrains.com/idea/download/).
2. **Install IntelliJ IDEA**: Follow the setup wizard.

## Running a Java Application

1. **Create a New Project**:
   - Open IntelliJ IDEA.
   - Select `Create New Project` > `Java` > ensure JDK is selected > `Next` > `Finish`.

2. **Write a Simple Java Program**:
   ```java
   public class HelloWorld {
       public static void main(String[] args) {
           System.out.println("Hello, world!");
       }
   }
   ```

3. **Run the Program**:
   - Right-click on the file > `Run 'HelloWorld.main()'`.

## Basic Java Syntax vs Python

- **Variables**:
  Java: `int number = 10;`
  Python: `number = 10`

- **Loops**:
  Java: 
  ```java
  for (int i = 0; i < 5; i++) {
      System.out.println("Loop " + i);
  }
  ```
  Python:
  ```python
  for i in range(5):
      print("Loop", i)
  ```

- **Functions**:
  Java: 
  ```java
  public static int addNumbers(int a, int b) {
      return a + b;
  }
  ```
  Python:
  ```python
  def add_numbers(a, b):
      return a + b
  ```

## Unit Testing in Java

1. **Add JUnit**:
   - `File > Project Structure > Libraries` > `+` > Add JUnit.

2. **Write a Test**:
   ```java
   import org.junit.jupiter.api.Test;
   import static org.junit.jupiter.api.Assertions.assertEquals;

   public class CalculatorTest {

       @Test
       public void testAddition() {
           assertEquals(4, Calculator.addNumbers(2, 2));
       }
   }
   ```

3. **Run the Test**:
   - Right-click on the test file > `Run 'CalculatorTest'`.

## Conclusion

This guide provides a quick start into Java for Python developers. Explore further to master Java.

## Resources

- [Oracle Java Documentation](https://docs.oracle.com/javase/8/docs/)
- [IntelliJ IDEA Documentation](https://www.jetbrains.com/idea/documentation/)
- [JUnit User Guide](https://junit.org/junit5/docs/current/user-guide/)
