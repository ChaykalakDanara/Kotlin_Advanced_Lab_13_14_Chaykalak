# Лабораторная работа №13-14
Коллекции, обобщения и функциональный стиль в Kotlin
## Описание
Данная лабораторная работа посвящена изучению продвинутых возможностей языка Kotlin,
которые активно используются при разработке Android-приложений.
В рамках работы рассматриваются:- обобщённые типы (Generics);- коллекции Kotlin;- функции высшего порядка;- extension-функции;
Все примеры ориентированы на практическое применение и подготовку к разработке
мобильных приложений.

В рамках работы рассматриваются:
- обобщённые типы (Generics);
- коллекции Kotlin;
- функции высшего порядка;
- extension-функции и свойства;
- scope-функции;
- enum class и data class;
- singleton-объекты.
## Как запустить проект
1. Клонируйте репозиторий:
```bash
git clone <URL_репозитория>
```

## Изученные темы

### 1. Generics (обобщённые типы)
Создание универсальных классов, работающих с разными типами данных:
```kotlin
class Question<T>(val questionText: String, val answer: T, val difficulty: Difficulty)
```
### 2. Enum class
```kotlin
enum class Difficulty { EASY, MEDIUM, HARD }
```
### 3. Data class
```kotlin
data class Question<T>(val questionText: String, val answer: T, val difficulty: Difficulty)
```
### 4. Singleton и companion object
Объекты, существующие в единственном экземпляре:
```kotlin
object StudentProgress {
var total: Int = 10
var answered: Int = 3
}
```
### 5. Extension-функции и свойства
Расширение возможностей существующих классов без наследования:
```kotlin
val Quiz.StudentProgress.progressText: String
get() = "${answered} of ${total} answered"
```
### 6. Scope-функции (let, apply, run, with, also)
Удобные функции для работы с объектами и их контекстом:
```kotlin
quiz.apply {
printQuiz()
}
```
### 7. Коллекции в Kotlin
- Arrays — фиксированный размер, быстрый доступ по индексу
- Lists — упорядоченные коллекции с изменяемым размером
- Sets — неупорядоченные коллекции без дубликатов
- Maps — коллекции ключ-значение
## Автор
Чайкалак.Д.Р
## Лицензия
Проект создан в учебных целях.
### 8. Функции высшего порядка для коллекций
- forEach() — перебор элементов
- map() — преобразование элементов
- filter() — фильтрация по условию
- groupBy() — группировка по ключу
- fold() — аккумулирование значений
- sortedBy() — сортировка по свойству