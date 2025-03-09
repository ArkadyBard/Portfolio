# Kotlin

Пример кода

```kotlin
fun isValidString(str: String): Boolean {
    var state = false
    if (str.isEmpty()) state = false
    else {
       for (ch in str) {
            if (ch == str[0]) {
                if (isLetter(ch) || ch == '_') state = true
                else state = false
            }
            else {
                if (isLetter(ch) || isDigit(ch)) state = true
                else state = false
            }
       }
    }
    return state
}
```

Функция isLetter
```kotlin
fun isLetter(ch: Char): Boolean {
    var state = false
    if (ch in 'a'..'z') {
        state = true
    }
    else if (ch in 'A'..'Z') {
        state = true
    }
    return state
}
```

Функция isDigit
```kotlin
fun isDigit(char: Char) = char in '0'..'9'
```
