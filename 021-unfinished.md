# 2026-07-01

## Task 1: Euler’s number

Write a script to calculate the value of e, also known as Euler’s number and Napier’s constant. Please checkout wiki page for more information.

### Uiua

```
˜ⁿ +1⊸(˜÷1) pow 52 2
```

## Task 2: URL normalization (RFC 3986)

Write a script for URL normalization based on rfc3986. This task was shared by Anonymous Contributor.
According to Wikipedia, URL normalization is the process by which URLs are modified and standardized in a consistent manner. The goal of the normalization process is to transform a URL into a normalized URL so it is possible to determine if two syntactically different URLs may be equivalent.

### Uiua

```
A ← "HTTP://User@Example.COM/Foo%2a"
B ← "HTTP://Example.COM/Foo%2a"

R ← $$ (\w[\w\d\.\-\+]+):\/\/([\w\d\+\-\!\$\:]+@)?([\w\d\%\.\~]+)(\:\d+)?(\/[\w\d\%\/\.\-\=\_]+)?(\?[\w\d\.\~\=\&]+)?(#[\w\d\%\.\~\=\&]+)?
Capitalize ← ≡(⨬(∘|+-@a@A) ×>0⟜<26⊸˜-@z)

♭⬚"" regex R A
```
