## Best practice to store DateTime based on TimeZone

*Welcome to one of the hardest problems in non-computational programming - properly representing dates and times to end users.*

Realistically, timestamps should be stored in a fixed single representation regardless of how they will be interpreted, because no matter how hard you try, you will always have ambiguous cases, and you can't resolve them without a fixed representation. And you've picked one of the worst of the use cases - scheduling an appointment. The only worse common use case is air travel, where a trip might start in one time zone and end in another, possible at an earlier local time.

Always, always, ALWAYS store in UTC and display in the user's preferred or explicitly specified timezone. If at all possible, make the user tell you what timezone they believe the timestamp to be in when they input it (e.g., have an explicit timezone field and pre-populate it with their preferred zone).

Ross Patterson 

* [Ross Patterson - Stack Exchange](https://softwareengineering.stackexchange.com/users/6390/ross-patterson)
* [Ross Patterson - Linkedin](https://www.linkedin.com/in/rosspatterson)
* [**Link Stack Exchange**](https://softwareengineering.stackexchange.com/questions/209421/best-practice-to-store-datetime-based-on-timezone)

