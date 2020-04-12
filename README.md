# Interval Format String

Make it easier to work with Interval timing. I hope....

Useful for working with dynamic Cron tasks like Quantum job scheduler.

## Structure of the String

Each type has different initial parameters. For example: Daily type has only one initial parameter and that's the Time (each day).

# IDK

  - Is there a standard for Day first letter usage? I've seen charts of MTWHF, using H as Thursday to not confuse from Tuesday?
    - So? M T W H F S A? if not?

### Types

- D : daily interval
- W : weekly interval
- CD : certain days interval
- M : monthly interval
- Y : yearly interval (idk if this is even needed?)

#### Daily Interval

Example: `D.1300.CST`
Basically the simplest interval.

- D specifies that this will happen daily.
- 1300 is the 24hr time.
- CST is the timezone, thought idk if that's necessary since timestamps will likely convert to UTC before hitting the server.

#### Weekly Interval

Example: `W.H.1300.CST`

  - W says this is a Weekly interval
  - H is Thursday (each week)
  - 1300 is the time of day (1:00PM) in 24 hr format.
  - CST is timezone. ^ note above.

#### Certain Day Interval

Example: `CD.MHFSA.1300.CST`
- CD says this is happening only certain days of the week.
  - Note: I don't know if there is a standard for these types of formats, so I'm substituting: 
    - H : Thursday
    - A : Sunday

- MHFSA ()
- 1300 is the time of day (1:00PM) in 24 hr format.
- CST is timezone. ^ note above.

#### Monthly Interval

D1 day one,
W1 first week
of the month

Example: `M.D1W1.1300.CST`

- M says this is a Monthly interval
- H is Thursday (each week)
- 1300 is the time of day (1:00PM) in 24 hr format.
- CST is timezone. ^ note above.

Daily @ 1:00PM TZ(CST)
  D.1300.CST

Monday, Wednesday, Friday @ 1:00PM TZ(CST)

Every Monday @ 1:00PM TZ(CST)
W.M.1300.CST

# Pay no attention to below here... Just notes for myself.

#### Monthly Interval

idk wtf to do with this format.

Example: `M.`

## 
first entry would be :: 4/12/2020 1:00PM
  // when is the first check happening?
  // easier to figure future ocurring times

interval P1D
  // time between checks


