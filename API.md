### System Search

Search for a system by name.

**Endpoint:**

```http
GET https://ed-cct.duckdns.org/ED-TTC/bgs/api/system/{system_name}
```

> **Note:** The system name must be [URL-encoded](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/encodeURIComponent) using percent-encoding.

#### Example

| Parameter   | Value                         |
| ----------- | ----------------------------- |
| System name | `Yin Sector GW-W c1-26`       |
| URL-encoded | `Yin%20Sector%20GW-W%20c1-26` |

**Request:**

```http
GET https://ed-cct.duckdns.org/ED-TTC/bgs/api/system/Yin%20Sector%20GW-W%20c1-26
```

**API response format:**

```json
{
  "System": "string - Name of the star system",
  "Pos": "number[3] - System coordinates in [X, Y, Z] format",

  "Events": [
    {
      "Faction": "string - Name of the faction",
      "FactionState": "string - Current state of the faction",
      "Government": "string - Government type of the faction",
      "Allegiance": "string - Political allegiance of the faction",
      "States": {
        "PendingState": [
          {
            "State": "string - Pending faction state"
          }
        ],
        "ActiveState": [
          {
            "State": "string - Active faction state"
          }
        ],
        "RecoveringState": [
          {
            "State": "string - Recovering faction state"
          }
        ]
      },

      "Infs": [
        {
          "Inf": "string - Numeric influence value of the faction",
          "timestamp": "string - Timestamp of the influence record in ISO 8601 UTC format"
        }
      ]
    }
  ],

  "Wars": [
    {
      "Faction1": "string - Name of the first faction involved in the conflict",
      "Faction2": "string - Name of the second faction involved in the conflict",
      "Lost1": "string - Station or asset lost by the first faction",
      "Lost2": "string - Station or asset lost by the second faction",
      "Win1": "number - Number of wins achieved by the first faction",
      "Win2": "number - Number of wins achieved by the second faction",
      "Type": "string - Type of conflict, such as War, Civil War or Election",
      "Status": "string - Current status of the conflict, such as Active, Pending or End",
      "timestamp": "string - Timestamp of the conflict record in ISO 8601 UTC format"
    }
  ]
}
```

#### Example

```json
{
  "System": "Yin Sector GW-W c1-26",
  "Pos": [19.125, 15.4375, -12.28125],
  "Events": [
    {
      "Faction": "Abrogo Partnership",
      "FactionState": "None",
      "Government": "Confederacy",
      "Allegiance": "Federation",
      "States": {
        "PendingState": [],
        "ActiveState": [],
        "RecoveringState": []
      },
      "Infs": [
        {
          "Inf": "0.048241",
          "timestamp": "2026-08-30T16:47:42.000Z"
        },
        {
          "Inf": "0.065261",
          "timestamp": "2026-09-01T08:06:03.000Z"
        },
        {
          "Inf": "0.061245",
          "timestamp": "2026-09-01T12:22:41.000Z"
        },
        {
          "Inf": "0.069347",
          "timestamp": "2026-09-03T04:58:54.000Z"
        },
        {
          "Inf": "0.072289",
          "timestamp": "2026-09-04T17:58:53.000Z"
        },
        {
          "Inf": "0.077387",
          "timestamp": "2026-09-04T18:41:56.000Z"
        }
      ]
    },
    {
      "Faction": "Aetas Eternum",
      "FactionState": "None",
      "Government": "Corporate",
      "Allegiance": "Federation",
      "States": {
        "PendingState": [],
        "ActiveState": [],
        "RecoveringState": []
      },
      "Infs": [
        {
          "Inf": "0.138693",
          "timestamp": "2026-08-30T16:47:42.000Z"
        },
        {
          "Inf": "0.140562",
          "timestamp": "2026-09-01T08:06:03.000Z"
        },
        {
          "Inf": "0.141566",
          "timestamp": "2026-09-01T12:22:41.000Z"
        },
        {
          "Inf": "0.122613",
          "timestamp": "2026-09-03T04:58:54.000Z"
        },
        {
          "Inf": "0.116466",
          "timestamp": "2026-09-04T17:58:53.000Z"
        },
        {
          "Inf": "0.121608",
          "timestamp": "2026-09-04T18:41:56.000Z"
        }
      ]
    },
    {
      "Faction": "Earth Defense Fleet",
      "FactionState": "Boom",
      "Government": "Corporate",
      "Allegiance": "Federation",
      "States": {
        "PendingState": [
          {
            "State": "Expansion"
          }
        ],
        "ActiveState": [],
        "RecoveringState": [
          {
            "State": "Election"
          }
        ]
      },
      "Infs": [
        {
          "Inf": "0.238191",
          "timestamp": "2026-08-30T16:47:42.000Z"
        },
        {
          "Inf": "0.237952",
          "timestamp": "2026-09-01T08:06:03.000Z"
        },
        {
          "Inf": "0.237952",
          "timestamp": "2026-09-01T12:22:41.000Z"
        },
        {
          "Inf": "0.238191",
          "timestamp": "2026-09-03T04:58:54.000Z"
        },
        {
          "Inf": "0.182731",
          "timestamp": "2026-09-04T17:58:53.000Z"
        },
        {
          "Inf": "0.195980",
          "timestamp": "2026-09-04T18:41:56.000Z"
        }
      ]
    },
    {
      "Faction": "Minutemen",
      "FactionState": "Boom",
      "Government": "Corporate",
      "Allegiance": "Federation",
      "States": {
        "PendingState": [],
        "ActiveState": [
          {
            "State": "Boom"
          }
        ],
        "RecoveringState": []
      },
      "Infs": [
        {
          "Inf": "0.336683",
          "timestamp": "2026-08-30T16:47:42.000Z"
        },
        {
          "Inf": "0.318273",
          "timestamp": "2026-09-01T08:06:03.000Z"
        },
        {
          "Inf": "0.321285",
          "timestamp": "2026-09-01T12:22:41.000Z"
        },
        {
          "Inf": "0.331658",
          "timestamp": "2026-09-03T04:58:54.000Z"
        },
        {
          "Inf": "0.344378",
          "timestamp": "2026-09-04T17:58:53.000Z"
        },
        {
          "Inf": "0.328643",
          "timestamp": "2026-09-04T18:41:56.000Z"
        }
      ]
    },
    {
      "Faction": "Sirius Corporation",
      "FactionState": "Expansion",
      "Government": "Corporate",
      "Allegiance": "Independent",
      "States": {
        "PendingState": [],
        "ActiveState": [
          {
            "State": "Expansion"
          }
        ],
        "RecoveringState": [
          {
            "State": "Election"
          }
        ]
      },
      "Infs": [
        {
          "Inf": "0.238191",
          "timestamp": "2026-08-30T16:47:42.000Z"
        },
        {
          "Inf": "0.237952",
          "timestamp": "2026-09-01T08:06:03.000Z"
        },
        {
          "Inf": "0.237952",
          "timestamp": "2026-09-01T12:22:41.000Z"
        },
        {
          "Inf": "0.238191",
          "timestamp": "2026-09-03T04:58:54.000Z"
        },
        {
          "Inf": "0.284137",
          "timestamp": "2026-09-04T17:58:53.000Z"
        },
        {
          "Inf": "0.276382",
          "timestamp": "2026-09-04T18:41:56.000Z"
        }
      ]
    }
  ],
  "Wars": [
    {
      "Faction1": "Sirius Corporation",
      "Faction2": "Earth Defense Fleet",
      "Lost1": "Alcock Relay",
      "Lost2": "",
      "Win1": 4,
      "Win2": 1,
      "Type": "Election",
      "Status": "End",
      "timestamp": "2026-09-04T18:41:56.000Z"
    }
  ]
}
```

### Faction Search

Search for a faction by name.

**Endpoint:**

```http
GET https://ed-cct.duckdns.org/ED-TTC/bgs/api/faction/{faction_name}
```

> **Note:** The faction name must be [URL-encoded](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/encodeURIComponent) using percent-encoding.

#### Example

| Parameter   | Value                         |
| ----------- | ----------------------------- |
| Faction name | `Aurora Venatores`       |
| URL-encoded | `Aurora%20Venatores` |

**Request:**

```http
GET https://ed-cct.duckdns.org/ED-TTC/bgs/api/faction/Aurora%20Venatores
```

**API response format:**

```json
{{
  "Faction": "string - Name of the faction",
  "Government": "string - Government type of the faction",
  "Allegiance": "string - Political allegiance of the faction",

  "Events": [
    {
      "Pos": "number[3] - System coordinates in [X, Y, Z] format",
      "System": "string - Name of the star system",
      "FactionState": "string - Current state of the faction",

      "States": {
        "PendingState": [
          {
            "State": "string - Pending state"
          }
        ],
        "ActiveState": [
          {
            "State": "string - Active state"
          }
        ],
        "RecoveringState": [
          {
            "State": "string - Recovering state"
          }
        ]
      },

      "Infs": [
        {
          "Inf": "string (numeric) - Influence value",
          "timestamp": "string (ISO 8601 UTC) - Timestamp of the influence record"
        }
      ]
    }
  ],

  "Wars": [
    {
      "Pos": "number[3] - System coordinates in [X, Y, Z] format",
      "System": "string - Name of the system",
      "Enemy": "string - Name of the opposing faction",
      "EnemyWin": "number - Number of wins by the opposing faction",
      "FactionWin": "number - Number of wins by this faction",
      "EnemyLost": "string - Asset lost by the opposing faction",
      "FactionLost": "string - Asset lost by this faction",
      "Type": "string - Conflict type, such as War, Civil War or Election",
      "Status": "string - Conflict status, such as Active, Pending or End",
      "timestamp": "string (ISO 8601 UTC) - Timestamp of the record"
    }
  ]
}
```

#### Example

```json
{
  "Faction": "Aurora Venatores",
  "Government": "Feudal",
  "Allegiance": "Independent",
  "Events": [
    {
      "Pos": [64.125, 58.09375, -91.65625],
      "System": "Caucandaga",
      "FactionState": "None",
      "States": {
        "PendingState": [],
        "ActiveState": [],
        "RecoveringState": []
      },
      "Infs": [
        {
          "Inf": "0.169154",
          "timestamp": "2026-08-30T09:14:50.000Z"
        },
        {
          "Inf": "0.156064",
          "timestamp": "2026-09-05T03:03:39.000Z"
        },
        {
          "Inf": "0.156064",
          "timestamp": "2026-09-05T11:32:21.000Z"
        }
      ]
    },
    {
      "Pos": [37.75, 106.28125, -141.4375],
      "System": "Col 285 Sector BG-K b10-0",
      "FactionState": "None",
      "States": {
        "PendingState": [],
        "ActiveState": [],
        "RecoveringState": []
      },
      "Infs": [
        {
          "Inf": "0.647817",
          "timestamp": "2026-08-31T19:58:50.000Z"
        }
      ]
    },
    {
      "Pos": [38.21875, 84.40625, -136.15625],
      "System": "Col 285 Sector QD-R c5-9",
      "FactionState": "None",
      "States": {
        "PendingState": [],
        "ActiveState": [],
        "RecoveringState": []
      },
      "Infs": [
        {
          "Inf": "0.130000",
          "timestamp": "2026-09-02T03:38:48.000Z"
        }
      ]
    },
    {
      "Pos": [36.875, 120.9375, -138.84375],
      "System": "Col 285 Sector ZK-K b10-1",
      "FactionState": "None",
      "States": {
        "PendingState": [],
        "ActiveState": [],
        "RecoveringState": []
      },
      "Infs": [
        {
          "Inf": "0.104146",
          "timestamp": "2026-08-31T20:33:52.000Z"
        }
      ]
    },
    {
      "Pos": [40.59375, 71.875, -124.9375],
      "System": "Gyvata",
      "FactionState": "None",
      "States": {
        "PendingState": [],
        "ActiveState": [],
        "RecoveringState": []
      },
      "Infs": [
        {
          "Inf": "0.664363",
          "timestamp": "2026-08-30T10:09:38.000Z"
        }
      ]
    },
    {
      "Pos": [36.71875, 56.34375, -123.40625],
      "System": "HIP 38172",
      "FactionState": "None",
      "States": {
        "PendingState": [],
        "ActiveState": [],
        "RecoveringState": []
      },
      "Infs": [
        {
          "Inf": "0.056830",
          "timestamp": "2026-09-05T02:05:05.000Z"
        },
        {
          "Inf": "0.056830",
          "timestamp": "2026-09-05T03:10:21.000Z"
        }
      ]
    },
    {
      "Pos": [47.6875, 100.40625, -101.28125],
      "System": "HIP 45406",
      "FactionState": "None",
      "States": {
        "PendingState": [],
        "ActiveState": [],
        "RecoveringState": []
      },
      "Infs": [
        {
          "Inf": "0.394269",
          "timestamp": "2026-09-04T20:42:49.000Z"
        }
      ]
    },
    {
      "Pos": [104.28125, -8.125, -117.875],
      "System": "Hyades Sector AQ-N b7-3",
      "FactionState": "None",
      "States": {
        "PendingState": [],
        "ActiveState": [],
        "RecoveringState": []
      },
      "Infs": [
        {
          "Inf": "0.143856",
          "timestamp": "2026-08-29T23:05:07.000Z"
        },
        {
          "Inf": "0.143856",
          "timestamp": "2026-08-30T01:01:44.000Z"
        },
        {
          "Inf": "0.148851",
          "timestamp": "2026-09-05T03:11:29.000Z"
        }
      ]
    },
    {
      "Pos": [106.96875, -31.5625, -124.53125],
      "System": "Hyades Sector DB-B a15-3",
      "FactionState": "None",
      "States": {
        "PendingState": [],
        "ActiveState": [],
        "RecoveringState": []
      },
      "Infs": [
        {
          "Inf": "0.130000",
          "timestamp": "2026-09-04T12:24:38.000Z"
        }
      ]
    },
    {
      "Pos": [55.21875, 47.5625, -129.1875],
      "System": "Hyades Sector EB-X d1-51",
      "FactionState": "None",
      "States": {
        "PendingState": [],
        "ActiveState": [],
        "RecoveringState": []
      },
      "Infs": [
        {
          "Inf": "0.068410",
          "timestamp": "2026-08-30T15:49:38.000Z"
        },
        {
          "Inf": "0.068410",
          "timestamp": "2026-08-30T19:45:07.000Z"
        },
        {
          "Inf": "0.068410",
          "timestamp": "2026-08-30T21:20:58.000Z"
        },
        {
          "Inf": "0.070423",
          "timestamp": "2026-08-31T11:57:53.000Z"
        },
        {
          "Inf": "0.070423",
          "timestamp": "2026-08-31T19:59:33.000Z"
        },
        {
          "Inf": "0.076459",
          "timestamp": "2026-08-31T21:22:36.000Z"
        },
        {
          "Inf": "0.076459",
          "timestamp": "2026-08-31T22:29:35.000Z"
        },
        {
          "Inf": "0.076459",
          "timestamp": "2026-09-01T08:03:01.000Z"
        },
        {
          "Inf": "0.076459",
          "timestamp": "2026-09-01T11:25:31.000Z"
        },
        {
          "Inf": "0.083501",
          "timestamp": "2026-09-01T22:28:46.000Z"
        },
        {
          "Inf": "0.083501",
          "timestamp": "2026-09-02T11:46:48.000Z"
        },
        {
          "Inf": "0.088531",
          "timestamp": "2026-09-03T04:18:27.000Z"
        },
        {
          "Inf": "0.088531",
          "timestamp": "2026-09-03T22:51:06.000Z"
        },
        {
          "Inf": "0.080483",
          "timestamp": "2026-09-04T11:07:01.000Z"
        },
        {
          "Inf": "0.080483",
          "timestamp": "2026-09-04T21:51:46.000Z"
        },
        {
          "Inf": "0.080483",
          "timestamp": "2026-09-05T02:15:48.000Z"
        },
        {
          "Inf": "0.080483",
          "timestamp": "2026-09-05T03:22:51.000Z"
        },
        {
          "Inf": "0.080483",
          "timestamp": "2026-09-05T04:56:46.000Z"
        },
        {
          "Inf": "0.079477",
          "timestamp": "2026-09-05T11:29:56.000Z"
        },
        {
          "Inf": "0.079477",
          "timestamp": "2026-09-05T12:30:23.000Z"
        }
      ]
    },
    {
      "Pos": [38.4375, 48.09375, -129.03125],
      "System": "Hyades Sector IC-U c3-18",
      "FactionState": "None",
      "States": {
        "PendingState": [],
        "ActiveState": [],
        "RecoveringState": []
      },
      "Infs": [
        {
          "Inf": "0.137000",
          "timestamp": "2026-09-01T11:25:30.000Z"
        }
      ]
    },
    {
      "Pos": [26.15625, 80.25, -129.21875],
      "System": "Hyades Sector II-Q b6-0",
      "FactionState": "None",
      "States": {
        "PendingState": [],
        "ActiveState": [],
        "RecoveringState": []
      },
      "Infs": [
        {
          "Inf": "0.146045",
          "timestamp": "2026-09-04T06:06:19.000Z"
        }
      ]
    },
    {
      "Pos": [44.75, 73.03125, -138.53125],
      "System": "Hyades Sector LD-Q b6-3",
      "FactionState": "None",
      "States": {
        "PendingState": [],
        "ActiveState": [],
        "RecoveringState": []
      },
      "Infs": [
        {
          "Inf": "0.577114",
          "timestamp": "2026-08-31T22:56:08.000Z"
        }
      ]
    },
    {
      "Pos": [53.09375, 45.3125, -131.84375],
      "System": "Hyades Sector NY-P b6-2",
      "FactionState": "None",
      "States": {
        "PendingState": [],
        "ActiveState": [],
        "RecoveringState": []
      },
      "Infs": [
        {
          "Inf": "0.062249",
          "timestamp": "2026-09-03T23:22:32.000Z"
        },
        {
          "Inf": "0.062249",
          "timestamp": "2026-09-04T02:00:00.000Z"
        },
        {
          "Inf": "0.062249",
          "timestamp": "2026-09-04T10:22:12.000Z"
        },
        {
          "Inf": "0.062249",
          "timestamp": "2026-09-04T11:39:56.000Z"
        }
      ]
    },
    {
      "Pos": [81.8125, 36.28125, -90.875],
      "System": "Hyades Sector XK-M b8-4",
      "FactionState": "None",
      "States": {
        "PendingState": [],
        "ActiveState": [],
        "RecoveringState": []
      },
      "Infs": [
        {
          "Inf": "0.116700",
          "timestamp": "2026-08-31T20:37:58.000Z"
        },
        {
          "Inf": "0.106747",
          "timestamp": "2026-09-04T02:04:04.000Z"
        },
        {
          "Inf": "0.106747",
          "timestamp": "2026-09-05T02:28:33.000Z"
        },
        {
          "Inf": "0.106747",
          "timestamp": "2026-09-05T03:43:05.000Z"
        }
      ]
    },
    {
      "Pos": [40.375, 79.21875, -119.6875],
      "System": "Jardha",
      "FactionState": "None",
      "States": {
        "PendingState": [],
        "ActiveState": [],
        "RecoveringState": []
      },
      "Infs": [
        {
          "Inf": "0.425344",
          "timestamp": "2026-08-31T21:13:41.000Z"
        }
      ]
    },
    {
      "Pos": [14.40625, 73.875, -109.5625],
      "System": "Kaitsan",
      "FactionState": "None",
      "States": {
        "PendingState": [],
        "ActiveState": [],
        "RecoveringState": []
      },
      "Infs": [
        {
          "Inf": "0.578000",
          "timestamp": "2026-09-04T22:11:46.000Z"
        }
      ]
    },
    {
      "Pos": [45.09375, 59.78125, -102.75],
      "System": "Kaushi",
      "FactionState": "None",
      "States": {
        "PendingState": [],
        "ActiveState": [],
        "RecoveringState": []
      },
      "Infs": [
        {
          "Inf": "0.081613",
          "timestamp": "2026-08-31T21:35:18.000Z"
        }
      ]
    },
    {
      "Pos": [75.1875, 50.28125, -70.65625],
      "System": "Lokans",
      "FactionState": "None",
      "States": {
        "PendingState": [],
        "ActiveState": [],
        "RecoveringState": []
      },
      "Infs": [
        {
          "Inf": "0.478958",
          "timestamp": "2026-09-05T03:02:55.000Z"
        },
        {
          "Inf": "0.478958",
          "timestamp": "2026-09-05T11:44:12.000Z"
        }
      ]
    },
    {
      "Pos": [71.125, 54.75, -72.8125],
      "System": "LTT 12294",
      "FactionState": "None",
      "States": {
        "PendingState": [],
        "ActiveState": [],
        "RecoveringState": []
      },
      "Infs": [
        {
          "Inf": "0.661736",
          "timestamp": "2026-08-31T11:24:07.000Z"
        },
        {
          "Inf": "0.640118",
          "timestamp": "2026-09-05T11:35:18.000Z"
        }
      ]
    },
    {
      "Pos": [17.625, 75.09375, -109.40625],
      "System": "Ngandavaret",
      "FactionState": "None",
      "States": {
        "PendingState": [],
        "ActiveState": [],
        "RecoveringState": []
      },
      "Infs": [
        {
          "Inf": "0.411355",
          "timestamp": "2026-09-01T11:21:48.000Z"
        }
      ]
    },
    {
      "Pos": [47.1875, 85.6875, -136.4375],
      "System": "Othiti",
      "FactionState": "None",
      "States": {
        "PendingState": [],
        "ActiveState": [],
        "RecoveringState": []
      },
      "Infs": [
        {
          "Inf": "0.700199",
          "timestamp": "2026-08-31T08:32:11.000Z"
        }
      ]
    },
    {
      "Pos": [42.46875, 61.71875, -137.15625],
      "System": "Ravane",
      "FactionState": "None",
      "States": {
        "PendingState": [],
        "ActiveState": [],
        "RecoveringState": []
      },
      "Infs": [
        {
          "Inf": "0.432645",
          "timestamp": "2026-08-30T14:15:38.000Z"
        },
        {
          "Inf": "0.432645",
          "timestamp": "2026-08-30T20:42:49.000Z"
        },
        {
          "Inf": "0.432645",
          "timestamp": "2026-08-31T05:25:27.000Z"
        },
        {
          "Inf": "0.393314",
          "timestamp": "2026-08-31T21:38:59.000Z"
        },
        {
          "Inf": "0.393314",
          "timestamp": "2026-09-01T06:10:36.000Z"
        },
        {
          "Inf": "0.393314",
          "timestamp": "2026-09-01T23:56:21.000Z"
        },
        {
          "Inf": "0.393314",
          "timestamp": "2026-09-02T11:59:49.000Z"
        },
        {
          "Inf": "0.370583",
          "timestamp": "2026-09-04T19:59:18.000Z"
        },
        {
          "Inf": "0.357642",
          "timestamp": "2026-09-05T13:40:55.000Z"
        }
      ]
    },
    {
      "Pos": [60.46875, 56.40625, -119.875],
      "System": "Sisi",
      "FactionState": "None",
      "States": {
        "PendingState": [],
        "ActiveState": [],
        "RecoveringState": []
      },
      "Infs": [
        {
          "Inf": "0.062187",
          "timestamp": "2026-09-05T12:11:29.000Z"
        }
      ]
    },
    {
      "Pos": [36.53125, 100.0625, -135.71875],
      "System": "Volkhab",
      "FactionState": "None",
      "States": {
        "PendingState": [],
        "ActiveState": [],
        "RecoveringState": []
      },
      "Infs": [
        {
          "Inf": "0.530938",
          "timestamp": "2026-08-31T11:56:19.000Z"
        },
        {
          "Inf": "0.530938",
          "timestamp": "2026-08-31T14:36:34.000Z"
        },
        {
          "Inf": "0.534397",
          "timestamp": "2026-09-04T16:48:18.000Z"
        }
      ]
    },
    {
      "Pos": [58.1875, 77.75, -83.5625],
      "System": "Wosraesi",
      "FactionState": "None",
      "States": {
        "PendingState": [],
        "ActiveState": [],
        "RecoveringState": []
      },
      "Infs": [
        {
          "Inf": "0.608739",
          "timestamp": "2026-09-04T15:29:27.000Z"
        }
      ]
    }
  ],
  "Wars": [
    {
      "Pos": [42.46875, 61.71875, -137.15625],
      "System": "Ravane",
      "Enemy": "Flat Galaxy Society",
      "EnemyWin": 3,
      "FactionWin": 0,
      "EnemyLost": "Ahern Platform",
      "FactionLost": "Plexico Hub",
      "Type": "War",
      "Status": "End",
      "timestamp": "2026-09-01T06:10:36.000Z"
    }
  ]
}
```
