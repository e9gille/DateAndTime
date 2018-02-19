# DateAndTime

Functions for manipulating Date and Time related stuff in Dyalog APL.


## Overview

This namespace contains functions that deal with date and time.

Note that most of the functions have been implemented by Phil Last (http://aplwiki.com/PhilLast) - unless stated otherwise - and generously granted to the APLTree project.

This class does not need .NET.


## Examples

The following table gives examples for all functions. The table is ordered by categories.

Note that not all syntactically possible features are demonstrated by these examples. For details execute:

```
      ]ADOC #.DateAndTime
```

| **Result**       | **`⍺`**                    | **Function**             | **`⍵`**      | |
|------------------------|----------------------------------|--------------------------------|--------------------|-|
| **Cast**                                                                                                          |
| 735965.058159722       |                                  | `DateTime2DayDecimal`          | 20160102.012345    | |
| 20160102.012345        |                                  | `DayDecimal2DateTime`          | 735965.058159722   | |
| 24193                  |                                  | `DateTime2Month`               | 20160102.058159722 | |
| 20160101               |                                  | `Month2DateTime`               | 24193              | |
| 2016 1 1 1 23 45 0     |                                  | `DateTime2Timestamp`           | 20160101.012345    | |
| 20160101.012345        |                                  | `Timestamp2DateTime`           | 2016 1 1 1 23 45   | |
| 2016 1 2 1 23 44 999   |                                  | `DayDecimal2Timestamp`         | 735965.058159722   | |
| 735965.058148148       |                                  | `Timestamp2DayDecimal`         | 2016 1 2 1 23 44   | |
| 736329                 |                                  | `Date2GregorianSerialDate`     | 2016 12 31         | |
| 2016 12 31             |                                  | `GregorianSerialDate2Date`     | 736329             | |
| **Week numbers**                                                                                                  |
| 52                     |                                  | `WeekNo_ISO`                   | 2016 12 31         | |
| 2016 12 26             |                                  | `DateFrom_Year_WeekNumberISO`  | 2016 52            | |
| 2016 12 29             | 'Thursday'                       | `DateFrom_Year_WeekNumberISO`  | 2016 52            | |
| 53                     |                                  | `WeekNo_US`                    | 016 12 31          | |
| 2016 12 25             |                                  | `DateFrom_Year_WeekNumberUS`   | 2016 53            | |
| 2016 12 29             | 'Thursday'                       | `DateFrom_Year_WeekNumberUS`   | 2016 53            | |
| 2017 10 30 16 20 35 8  |                                  | `FileDate2Timestap`            | `2⊃⎕FRDCI ftn compNo`| |
| **Misc**                                                                                                          |
| 5                      |                                  | `DayOfWeekAsNumber`            | 2016 1 1           | |
| 'Friday'               |                                  | `DayOfWeek`                    | 2016 1 1           | |
| 20000423 20010415      |                                  | `Easter`                       | 2000 2001          | |
| '2016-12-31 01:23:45'  |                                  | `FormatDateTime`               | 20161231.012345    | |
| 1 1 0                  |                                  | `LeapYear`                     | 2000 2016 2100     | |
| 60                     |                                  | `OrdinalNumber`                | 2016 2 29          | |
| **Math**                                                                                                          |
| 20161231               | 0                                | `AddPeriod2DateTime`           | 20161231           |Add nothing |
| 20181229               | 2                                | `AddPeriod2DateTime`           | 20161229           |Add a year |
| 20160229               | 0 2                              | `AddPeriod2DateTime`           | 20151229           |Add a month |
| 20161231               | 0 0 2                            | `AddPeriod2DateTime`           | 20161229           |Add a day |
| 20161229.032345        | 0 0 0 2                          | `AddPeriod2DateTime`           | 20161229.012345    |Add an hour |
| 20161230.022345        | 0 0 0 25                         | `AddPeriod2DateTime`           | 20161229.012345    |Add a minute |
| 20161229.014845        | 0 0 0 0 25                       | `AddPeriod2DateTime`           | 20161229.012345    |Add a second |
| 20161229.012348        | 0 0 0 0 0 3                      | `AddPeriod2DateTime`           | 20161229.012345    |Add a millisecond |
| 20000101               | 0                                | `AddPeriod2DateTime`           | 20000101           | |
| 20030101               | 3                                | `AddPeriod2DateTime`           | 20000101           | |
| 20030201               | 3 1                              | `AddPeriod2DateTime`           | 20000101           | |
| 20030203               | 3 1 2                            | `AddPeriod2DateTime`           | 20000101           | |
| 20030203.04            | 3 1 2 4                          | `AddPeriod2DateTime`           | 20000101           | |
| 20030203.23            | 3 1 2 23                         | `AddPeriod2DateTime`           | 20000101           | |
| 20030204               | 3 1 2 24                         | `AddPeriod2DateTime`           | 20000101           | |
| 20030203.0405          | 3 1 2 4 5                        | `AddPeriod2DateTime`           | 20000101           | |
| 20030203.0459          | 3 1 2 4 59                       | `AddPeriod2DateTime`           | 20000101           | |
| 20030203.05            | 3 1 2 4 60                       | `AddPeriod2DateTime`           | 20000101           | |
| 20030203.040507        | 3 1 2 4 5 7                      | `AddPeriod2DateTime`           | 20000101           | |
| 20030203.040607        | 3 1 2 4 5 67                     | `AddPeriod2DateTime`           | 20000101           | |
| 20141229               | ¯2                               | `AddPeriod2DateTime`           | 20161229           |Subtract two years |


## Requirements

`DateAndTime` needs at least version 14.1.