# MenuFi Server
## Entry Point
com.menufi.backend.springboot.MenuFiSpringBootApplication

## Configuration
Edit `spring.profiles.active` property in _src/main/resources/application.properties_ to either:
* `default` (uses `CloudSqlQuerier`)
* `test` (uses `MockQuerier`)

## Gradle Wrapper
Change gradle properties in `gradle/wrapper`

To run locally: `./gradlew appengineRun`

More tasks: `./gradlew tasks`

## Public API Routes
`GET` [/items?restaurantId=](http://128.61.105.97:8080/items?restaurantId=0)

`GET` [/restaurants/nearby?location=](http://128.61.105.97:8080/restaurants/nearby?location=somewhere)

`POST` /items
> { restaurantId: number, name: string, description: string, price: number }