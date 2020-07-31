---
title: date.week() function
description: >
  The `date.week()` function returns the ISO week of the year for a specified time.
  Results range from `[1-53]`.
aliases:
  - /v2.0/reference/flux/functions/date/week/
menu:
  v2_0_ref:
    name: date.week
    parent: Date
weight: 301
---

The `date.week()` function returns the ISO week of the year for a specified time.
Results range from `[1-53]`.

_**Function type:** Transformation_  

```js
import "date"

date.week(t: 2019-07-17T12:05:21.012Z)

// Returns 29
```

## Parameters

### t
The time to operate on.
Use an absolute time, relative duration, or integer.
Durations are relative to `now()`.
Integers are **nanosecond** [Unix timestamps](/v2.0/reference/glossary/#unix-timestamp).

_**Data type:** Time | Duration | Integer_

## Examples

##### Return the week of the year
```js
import "date"

date.week(t: 2020-02-11T12:21:03.293534940Z)

// Returns 7
```

##### Return the week of the year using a relative duration
```js
import "date"

option now = () => 2020-02-11T12:21:03.293534940Z

date.week(t: -12d)

// Returns 5
```

##### Return the week of the year using a nanosecond Unix timestamp
```js
import "date"

date.week(t: 1581423663293534940)

// Returns 7
```