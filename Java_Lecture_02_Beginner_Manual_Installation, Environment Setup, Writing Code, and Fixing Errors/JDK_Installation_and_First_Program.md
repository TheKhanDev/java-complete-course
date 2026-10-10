# Java Beginner's Manual: Installation, Environment Setup, Writing Code, and Fixing Errors

**Complete Beginner Lecture**

## Table of Contents

1. What Is JDK?
2. Download and Install JDK
3. Set Environment Variables in Windows
4. Verify Installation
5. Write Your First Java Program
6. Compile and Run the Program
7. Common Errors and Fixes
8. Quick Revision
9. Practice Task
10. Conclusion

---

## 1. What Is JDK?

- **JDK (Java Development Kit):** Used to develop and run Java programs.
- **JVM (Java Virtual Machine):** Executes Java bytecode.
- **JRE (Java Runtime Environment):** Provides components needed to run Java applications.

**Recommendation:** Install a stable JDK LTS release compatible with your system.

## 2. Download and Install JDK

1. Visit the official website: https://www.oracle.com/java/technologies/downloads/
2. Download a JDK compatible with your operating system and architecture.
3. Run the installer or extract the downloaded archive.
4. Note the installation directory.

Example Windows path:

```text
C:\Program Files\Java\jdk-25
```

**Note:** Your installation folder may have a different name.

## 3. Set Environment Variables in Windows

Environment variables help Windows locate Java commands.

### Step 1: Open Environment Variables

1. Press `Win + S`.
2. Search for **Edit the system environment variables**.
3. Open it and click **Environment Variables**.

### Step 2: Create JAVA_HOME

Under **System variables**:

1. Click **New**.
2. Variable name: `JAVA_HOME`
3. Variable value: Your JDK installation directory.

Example:

```text
C:\Program Files\Java\jdk-25
```

**Important:** Do not include the `bin` folder in `JAVA_HOME`.

### Step 3: Add Java to PATH

1. Under **System variables**, select `Path`.
2. Click **Edit**, then **New**.
3. Add:

```text
%JAVA_HOME%\bin
```

4. Click **OK** to save all changes.

**Important:** Do not delete existing PATH entries.

## 4. Verify Installation

Open a new Command Prompt and run:

```bash
java -version
javac -version
```

- `java`: Runs Java applications.
- `javac`: Compiles Java source code.

If both commands display version information, the installation is working.

If either command fails, check `JAVA_HOME`, `Path`, and the JDK installation directory. Open a new terminal after making changes.

## 5. Write Your First Java Program

### Step 1: Create a Folder

Create a folder named:

```text
JavaPractice
```

### Step 2: Create a Java File

Inside the folder, create:

```text
HelloWorld.java
```

### Step 3: Write the Code

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

### Step 4: Understand the Code

| Code | Purpose |
|---|---|
| `class HelloWorld` | Defines a class. |
| `main()` | Entry point of the program. |
| `System.out.println()` | Prints text followed by a new line. |
| `;` | Terminates a statement. |
| `{ }` | Enclose a block of code. |

**Rule:** The public class name must match the filename, including capitalization.

## 6. Compile and Run the Program

Open Command Prompt inside the folder containing `HelloWorld.java`.

### Step 1: Compile

```bash
javac HelloWorld.java
```

This creates:

```text
HelloWorld.class
```

### Step 2: Run

```bash
java HelloWorld
```

Expected output:

```text
Hello, World!
```

**Remember:** Use the class name without `.java` or `.class` when running the program.

### Java Execution Workflow

```text
HelloWorld.java
      |
      | javac HelloWorld.java
      v
HelloWorld.class
      |
      | java HelloWorld
      v
Hello, World!
```

## 7. Common Errors and Fixes

| Error | Solution |
|---|---|
| `java is not recognized` | Check PATH and reopen the terminal. |
| `javac is not recognized` | Check that the JDK bin folder is in PATH. |
| `Could not find or load main class` | Check the current directory and class name. |
| Public class filename error | Match the filename to the public class name. |
| `';' expected` | Check for a missing semicolon. |

## 8. Quick Revision

| Command or Variable | Purpose |
|---|---|
| `JAVA_HOME` | Stores the JDK installation directory. |
| `%JAVA_HOME%\bin` | Helps Windows locate Java commands. |
| `java -version` | Checks the Java runtime version. |
| `javac -version` | Checks the compiler version. |
| `javac HelloWorld.java` | Compiles the source file. |
| `java HelloWorld` | Runs the compiled class. |

## 9. Practice Task

Modify the program to display:

```text
My name is Student.
I am learning Java.
This is my first program.
```

Use three `System.out.println()` statements.

### Example Solution

```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("My name is Student.");
        System.out.println("I am learning Java.");
        System.out.println("This is my first program.");
    }
}
```

Compile and run the program again.

## 10. Conclusion

In this lecture, we covered:

- JDK, JVM, and JRE.
- Downloading and installing the JDK.
- Configuring `JAVA_HOME` and `Path`.
- Verifying the installation.
- Creating a Java source file.
- Understanding basic Java syntax.
- Compiling with `javac`.
- Running with `java`.
- Troubleshooting common errors.

### Final Steps

1. Install the JDK.
2. Set `JAVA_HOME`.
3. Add `%JAVA_HOME%\bin` to PATH.
4. Verify the installation.
5. Create a `.java` file.
6. Compile using `javac`.
7. Run using `java`.

**Congratulations! You have completed your first Java program.**
