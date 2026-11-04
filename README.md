# Composition

Игра на устный счёт для Android. Игроку показывается сумма и одно видимое слагаемое, нужно выбрать правильный ответ из шести вариантов. Есть таймер, прогресс, несколько уровней сложности и экран с результатом.

Приложение написано на Kotlin с использованием ViewModel, LiveData, Data Binding и Navigation Component.

## Возможности

- Выбор уровня сложности: Test, Easy, Normal, Hard.
- Генерация вопросов на сложение с вариантами ответов.
- Обратный отсчёт времени на каждый раунд.
- Прогресс по количеству правильных ответов и по проценту.
- Экран результата с итогами и возможностью сыграть заново.
- Поддержка тёмной темы (values-night).

## Стек

- Язык: Kotlin 1.8.22
- Сборка: Gradle 7.4, Android Gradle Plugin 7.4.0
- compileSdk: 31, minSdk: 24, targetSdk: 30
- Архитектура: MVVM (ViewModel + LiveData)
- UI: Data Binding, View Binding, Navigation Component, Safe Args
- Parcelize для передачи данных между экранами

## Структура проекта

Внутри пакета три верхнеуровневых пакета:

- data — реализация репозитория (GameRepositoryImpl).
- domain — сущности (GameResult, GameSettings, Level, Question), интерфейс GameRepository и use cases (GenerateQuestionUseCase, GetGameSettingsUseCase).
- presentation — Activity, фрагменты, ViewModel, BindingAdapters.

## Сборка и запуск

1. Откройте проект в Android Studio (актуальная версия).
2. Дождитесь окончания Gradle Sync.
3. Запустите приложение на эмуляторе или устройстве (Run).

### Примечание о версиях

Проект изначально написан в 2021 году на старом стеке (AGP 4.2.2, Gradle 6.7.1, Kotlin 1.5.21, compileSdk 30). Чтобы он собирался и запускался в текущей Android Studio, версии подняты до минимально совместимых:

- AGP: 4.2.2 -> 7.4.0
- Gradle: 6.7.1 -> 7.4
- Kotlin: 1.5.21 -> 1.8.22
- compileSdk: 30 -> 31
- Исправлена сигнатура create в GameViewModelFactory под новую версию androidx.lifecycle.

Это не модернизация проекта, а минимальные правки для сборки.

## Автор курса

Андрей Сумин.

## Лицензия

Игра основана на материалах курса; доработка и сборка — в этом репозитории.