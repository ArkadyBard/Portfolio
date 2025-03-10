# Kotlin

Пример кода
Поиск полиндромов

 - Функция поиска полиндрома слова
```kotlin
fun isPalindrome(word: String): Boolean = word == word.reversed()
```

 - А эта функция, с игнорированием регистра
```kotlin
fun isPalIgnoreCase(word: String): Boolean = isPalindrome(word.lowercase())
```
 
 - А это для поиска полиндрома/предложения
```
fun isPalindromeSentence(sentence: String): Boolean {
    var str = ""
    for (ch in sentence) {
        if (isLetter(ch)) {
            str += ch
        }
    }

    return isPalIgnoreCase(str)
}
```


 - Вспомогательная функция для поиска символов
 ```kotlin
 fun isLetter(char: Char): Boolean =
    char in 'a'..'z' ||
    char in 'A'..'Z'
```