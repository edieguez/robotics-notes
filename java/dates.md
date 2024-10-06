# Dates in Java

## Releavant classes

- `LocalDate` Only date. No time zone
- `LocalTime` Only time. No time zone
- `LocalDateTime` Date and time using local timezone
- `ZonedDateTime` Date and time using specific timezone

> All these classes have the static methods `now()` and `of()`

## Smaller periods of time

- `Period` Represents periods of time like years, months and days
- `Duration` Used for smaller time units like hours, minutes and seconds
- `TemporalUnit` For now the only implementation is `ChronoUnit`. Can be used to specify
    - `ChronoUnit.DAYS`
    - `ChronoUnit.HOURS`
    - `ChronoUnit.MINUTES`
    - `ChronoUnit.SECONDS`
    - `ChronoUnit.MILLIS`
    - `ChronoUnit.NANOS`
    - `ChronoUnit.HALF_DAYS`

## Time between two dates

``` java
LocalDate start = LocalDate.now().minus(Period.ofYears(5));
LocalDate end = LocalDate.now();

Period between = Period.between(start, end);

log.info("Years: {}", between);
```

## Instant

The `Instant` class represents a date in the GMT/UTC timezone.
