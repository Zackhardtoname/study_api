# Study Api

This is the graphql api for study together.

It has a query for getting a user's study statistics. Soon to add a query for getting leaderboard information.

## Usage

Run `npm install && npm run dev` to start the api.

### Queries:

#### `getUserStats`

Example request:
```graphql
query {
  getUserStats(userId:"5"){
    studyTime{ 
      pastDay
      pastWeek
      pastMonth
      allTime
    }
    leaderboardPlacement{
      pastDay
      pastWeek
      pastMonth
      allTime
    }
    studyRole{
      currentStudyRole
      nextStudyRole
      studyTimeToPromotion
      roleRank
    }
    pastDayTimeSeries {
      datetime
      y
    }
    
    pastWeekTimeSeries {
      datetime
      y
    }
    
    pastMonthTimeSeries {
      datetime
      y
    }
    allTimeTimeSeries {
      datetime
      y
    }
  }
}
```

Example response:
```json
{
  "data": {
    "getUserStats": {
      "studyTime": {
        "pastDay": 2.0796604618808487,
        "pastWeek": 40.248521272367725,
        "pastMonth": 180.65533224706758,
        "allTime": null
      },
      "leaderboardPlacement": {
        "pastDay": 254,
        "pastWeek": 260,
        "pastMonth": 175,
        "allTime": null
      },
      "studyRole": {
        "currentStudyRole": "@master (80-120h)",
        "nextStudyRole": "@grandmaster (120-160h)",
        "studyTimeToPromotion": 0.5,
        "roleRank": 9
      },
      "pastDayTimeSeries": [
        {
          "datetime": "2021-01-28T17:24:31.288Z",
          "y": 7.651936994279822
        },
        {
          "datetime": "2021-01-28T18:24:31.288Z",
          "y": 46.32579777141018
        },
        {
          "datetime": "2021-01-28T19:24:31.288Z",
          "y": 27.150436576630455
        },
        {
          "datetime": "2021-01-28T20:24:31.288Z",
          "y": 33.3831216335966
        },
        {
          "datetime": "2021-01-28T21:24:31.288Z",
          "y": 29.214425757674576
        },
        {
          "datetime": "2021-01-28T22:24:31.288Z",
          "y": 47.75749489766895
        },
        {
          "datetime": "2021-01-28T23:24:31.288Z",
          "y": 12.982796025680727
        },
        {
          "datetime": "2021-01-29T00:24:31.288Z",
          "y": 28.94994133617729
        },
        {
          "datetime": "2021-01-29T01:24:31.288Z",
          "y": 35.070287761700456
        },
        {
          "datetime": "2021-01-29T02:24:31.288Z",
          "y": 45.55704270183924
        },
        {
          "datetime": "2021-01-29T03:24:31.288Z",
          "y": 3.472984721420289
        },
        {
          "datetime": "2021-01-29T04:24:31.288Z",
          "y": 39.669472219502495
        },
        {
          "datetime": "2021-01-29T05:24:31.288Z",
          "y": 50.70108064449414
        },
        {
          "datetime": "2021-01-29T06:24:31.288Z",
          "y": 51.959231273449404
        },
        {
          "datetime": "2021-01-29T07:24:31.288Z",
          "y": 34.94797402909171
        },
        {
          "datetime": "2021-01-29T08:24:31.288Z",
          "y": 11.091145053942455
        },
        {
          "datetime": "2021-01-29T09:24:31.288Z",
          "y": 47.33346637811337
        },
        {
          "datetime": "2021-01-29T10:24:31.288Z",
          "y": 5.876069577934686
        },
        {
          "datetime": "2021-01-29T11:24:31.288Z",
          "y": 16.24919973903161
        },
        {
          "datetime": "2021-01-29T12:24:31.288Z",
          "y": 40.22209598455447
        },
        {
          "datetime": "2021-01-29T13:24:31.288Z",
          "y": 4.413416922252509
        },
        {
          "datetime": "2021-01-29T14:24:31.288Z",
          "y": 52.70409427008417
        },
        {
          "datetime": "2021-01-29T15:24:31.288Z",
          "y": 58.01000096081225
        },
        {
          "datetime": "2021-01-29T16:24:31.288Z",
          "y": 1.5048722659412306
        },
        {
          "datetime": "2021-01-29T17:24:31.288Z",
          "y": 7.651936994279822
        }
      ],
      "pastWeekTimeSeries": [
        {
          "datetime": "2021-01-23T05:00:00.000Z",
          "y": 7.933894443900499
        },
        {
          "datetime": "2021-01-24T05:00:00.000Z",
          "y": 8.205108856585866
        },
        {
          "datetime": "2021-01-25T05:00:00.000Z",
          "y": 7.482561232200169
        },
        {
          "datetime": "2021-01-26T05:00:00.000Z",
          "y": 3.2017490028702014
        },
        {
          "datetime": "2021-01-27T05:00:00.000Z",
          "y": 1.4232128720686887
        },
        {
          "datetime": "2021-01-28T05:00:00.000Z",
          "y": 9.922334402861452
        },
        {
          "datetime": "2021-01-29T05:00:00.000Z",
          "y": 2.0796604618808487
        }
      ],
      "pastMonthTimeSeries": [
        {
          "datetime": "2020-12-29T05:00:00.000Z",
          "y": 2.0796604618808487
        },
        {
          "datetime": "2020-12-30T05:00:00.000Z",
          "y": 2.5375868261035066
        },
        {
          "datetime": "2020-12-31T05:00:00.000Z",
          "y": 7.423997160058207
        },
        {
          "datetime": "2021-01-01T05:00:00.000Z",
          "y": 10.39184625468988
        },
        {
          "datetime": "2021-01-02T05:00:00.000Z",
          "y": 6.989594805818342
        },
        {
          "datetime": "2021-01-03T05:00:00.000Z",
          "y": 2.218229010788491
        },
        {
          "datetime": "2021-01-04T05:00:00.000Z",
          "y": 9.466693275622674
        },
        {
          "datetime": "2021-01-05T05:00:00.000Z",
          "y": 1.1752139155869372
        },
        {
          "datetime": "2021-01-06T05:00:00.000Z",
          "y": 3.249839947806322
        },
        {
          "datetime": "2021-01-07T05:00:00.000Z",
          "y": 8.044419196910894
        },
        {
          "datetime": "2021-01-08T05:00:00.000Z",
          "y": 0.8826833844505018
        },
        {
          "datetime": "2021-01-09T05:00:00.000Z",
          "y": 10.540818854016834
        },
        {
          "datetime": "2021-01-10T05:00:00.000Z",
          "y": 11.60200019216245
        },
        {
          "datetime": "2021-01-11T05:00:00.000Z",
          "y": 0.3009744531882461
        },
        {
          "datetime": "2021-01-12T05:00:00.000Z",
          "y": 1.5303873988559644
        },
        {
          "datetime": "2021-01-13T05:00:00.000Z",
          "y": 9.265159554282036
        },
        {
          "datetime": "2021-01-14T05:00:00.000Z",
          "y": 5.430087315326091
        },
        {
          "datetime": "2021-01-15T05:00:00.000Z",
          "y": 6.67662432671932
        },
        {
          "datetime": "2021-01-16T05:00:00.000Z",
          "y": 5.842885151534915
        },
        {
          "datetime": "2021-01-17T05:00:00.000Z",
          "y": 9.55149897953379
        },
        {
          "datetime": "2021-01-18T05:00:00.000Z",
          "y": 2.5965592051361455
        },
        {
          "datetime": "2021-01-19T05:00:00.000Z",
          "y": 5.789988267235458
        },
        {
          "datetime": "2021-01-20T05:00:00.000Z",
          "y": 7.014057552340091
        },
        {
          "datetime": "2021-01-21T05:00:00.000Z",
          "y": 9.111408540367847
        },
        {
          "datetime": "2021-01-22T05:00:00.000Z",
          "y": 0.6945969442840578
        },
        {
          "datetime": "2021-01-23T05:00:00.000Z",
          "y": 7.933894443900499
        },
        {
          "datetime": "2021-01-24T05:00:00.000Z",
          "y": 8.205108856585866
        },
        {
          "datetime": "2021-01-25T05:00:00.000Z",
          "y": 7.482561232200169
        },
        {
          "datetime": "2021-01-26T05:00:00.000Z",
          "y": 3.2017490028702014
        },
        {
          "datetime": "2021-01-27T05:00:00.000Z",
          "y": 1.4232128720686887
        },
        {
          "datetime": "2021-01-28T05:00:00.000Z",
          "y": 9.922334402861452
        },
        {
          "datetime": "2021-01-29T05:00:00.000Z",
          "y": 2.0796604618808487
        }
      ],
      "allTimeTimeSeries": null
    }
  }
}
```

#### `getLeaderboard`

Example request:

```graphql
query {
  getLeaderboard(timeInterval: pastDay)
  {
   username
    studyTimeInMinutes
  }
}
```

Example response:

```json
{
  "data": {
    "getLeaderboard": [
      {
        "username": "ic2gTUdC",
        "studyTimeInMinutes": 360
      },
      {
        "username": "3r3K68hl",
        "studyTimeInMinutes": 360
      },
      {
        "username": "8FHgiJsG",
        "studyTimeInMinutes": 360
      },
      {
        "username": "xPjYWxOg",
        "studyTimeInMinutes": 360
      },
      {
        "username": "ENZi1d66",
        "studyTimeInMinutes": 360
      },
      {
        "username": "JNrTnRiQ",
        "studyTimeInMinutes": 360
      },
      {
        "username": "l2MO9C0C",
        "studyTimeInMinutes": 360
      },
      {
        "username": "12E9sW0H",
        "studyTimeInMinutes": 360
      },
      {
        "username": "8jaBukCn",
        "studyTimeInMinutes": 360
      },
      {
        "username": "MTyMFol3",
        "studyTimeInMinutes": 360
      },
      {
        "username": "7lIwiU8Z",
        "studyTimeInMinutes": 360
      },
      {
        "username": "0BYVjBCl",
        "studyTimeInMinutes": 360
      },
      {
        "username": "lj7ucRMK",
        "studyTimeInMinutes": 360
      },
      {
        "username": "asO3XyQe",
        "studyTimeInMinutes": 360
      },
      {
        "username": "peU3tBgB",
        "studyTimeInMinutes": 360
      },
      {
        "username": "tEyvvR5g",
        "studyTimeInMinutes": 360
      },
      {
        "username": "LErz0jIF",
        "studyTimeInMinutes": 360
      },
      {
        "username": "ADZxu5P3",
        "studyTimeInMinutes": 360
      },
      ...
    ]
  }
}
```
