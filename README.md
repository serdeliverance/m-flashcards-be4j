<<<<<<< HEAD
# m-flashcards-be-4j
# m-flashcards-be-4j
# m-flashcards-be-4j
=======
# m-flashcards

Flashcards for learning languages. This project born from a real need and also comes in handy to dive deeper into `Java`, `Spring Boot`, and related technologies.

## Stack

- `Java 17 +`Spring Boot``
- `Mongo`
- `Docker`

## Requirements

- `Java 17`
- `Docker`

## Data model

So far the model is very simple:

```kotlin
data class Deck(val name: String, val type: String, val tags: List<String>, val flashcards: List<Flashcard>)

data class Flashcard(val front: String, val back: String, val example: String?)
```

We have `decks` and `flashcards`. A `deck` is a `flashcard` set with some metadata, such as `name` and `type`.
`type` indicates with type of `flashcard` the `deck` stores. `type` could be `phrase` or `vocabulary`. `vocabulary` flashcards use to have `example` value set.
`flaschcard` domain class is self-explanatory.

## Run backend locally

```
./gradlew bootRun
```

## Start DB

run `docker-compose`:

```
docker-compose up
```

## More info

- [Useful scripts](./docs/scripts.md)
>>>>>>> bdb1e40 (initial backend)
