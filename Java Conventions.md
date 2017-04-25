# Java Conventions

References

* [Google Java Style Guide](https://google.github.io/styleguide/javaguide.html)
* [CERT Java Coding Guidelines](https://www.securecoding.cert.org/confluence/display/java/Java+Coding+Guidelines)

## Source file

##### ●　File name

The source file name consists of the case-sensitive name of the top-level class it contains, plus the .java extension.

##### ●　File encoding

Source files are encoded in UTF-8.

##### ●　Special escape sequences

For any character that has a special escape sequence (\b, \t, \n, \f, \r, \", \' and \\), that sequence is used rather than the corresponding octal (e.g. \012) or Unicode (e.g. \u000a) escape.

## Source file structure

##### ●　Structure

A source file consists of, in order:

1. License or copyright information, if present
1. Package statement
1. Import statements
1. Exactly one top-level class

Exactly one blank line separates each section that is present.

##### ●　Package statement

The package statement is not line-wrapped. The column limit does not apply to package statements.

##### ●　Import statements

1. Wildcard imports, static or otherwise, are not used.

1. Import statements are not line-wrapped. The column limit does not apply to import statements.

    ```
    // bad
    import java.awt.*;

    // good
    import java.awt.Panel;
    import java.awt.Graphics;
    ```
