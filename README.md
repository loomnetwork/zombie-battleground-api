# Zombie Battleground API

## Base URL

```
https://loom.games/api
```

## API Version

```
https://loom.games/api/zb/v1
```

## Pagination

```
https://loom.games/api/zb/v1/decks?page=1&limit=40
```

## Endpoints

| Method        |  URL | Description |
| :-------------| :-----| :-------: |
| `GET` | ```decks``` | List decks |
| `GET` | ```deck/{id}``` | Get a single deck |
| `GET` | ```matches``` | List matches |
| `GET` | ```match/{id}``` | Get a single match |
| `GET` | ```cards``` | List cards |
| `GET` | ```card``` | Get a single card by `mould_id` and `version`: `?mould_id=1&version=v3` |

## GET /decks

**Optional filter parameters:**

| Name        |  Type |
| :-----------| :-----|
| id | number |
| user_id | string |
| deck_id | number |
| name | string |
| hero_id | number |
| primary_skill_id | number |
| secondary_skill_id | number |
| version | string |

**Response**

```
{
    "total": 2,
    "page": 1,
    "limit": 100,
    "decks": [
        {
            "ID": 1,
            "CreatedAt": "2018-12-20T09:10:18Z",
            "UpdatedAt": "2018-12-20T09:10:18Z",
            "UserID": "player1",
            "DeckID": 6,
            "Name": "NewDeck",
            "HeroID": 1,
            "DeckCards": null,
            "PrimarySkillID": 0,
            "SecondarySkillID": 0,
            "Version": "v3",
            "SenderAddress": "0x123456789012345678901234567890"
        },
        {
            "ID": 2,
            "CreatedAt": "2018-12-27T10:19:04Z",
            "UpdatedAt": "2018-12-27T10:19:04Z",
            "UserID": "player1",
            "DeckID": 7,
            "Name": "NewDeck2",
            "HeroID": 1,
            "DeckCards": null,
            "PrimarySkillID": 0,
            "SecondarySkillID": 0,
            "Version": "v3",
            "SenderAddress": "0x123456789012345678901234567890"
        }
    ]
}
```

## GET /deck/{id}

**Response**

```
{
    "ID": 1,
    "CreatedAt": "2018-12-20T09:10:18Z",
    "UpdatedAt": "2018-12-20T09:10:18Z",
    "UserID": "player1",
    "DeckID": 6,
    "Name": "NewDeck",
    "HeroID": 1,
    "DeckCards": [
        {
            "ID": 1,
            "CreatedAt": "2018-12-20T09:10:18Z",
            "UpdatedAt": "2018-12-20T09:10:18Z",
            "UserID": "player1",
            "DeckID": 1,
            "CardName": "Pyromaz",
            "Amount": 2
        },
        {
            "ID": 2,
            "CreatedAt": "2018-12-20T09:10:18Z",
            "UpdatedAt": "2018-12-20T09:10:18Z",
            "UserID": "player1",
            "DeckID": 1,
            "CardName": "Burrrnn",
            "Amount": 1
        }
    ],
    "PrimarySkillID": 0,
    "SecondarySkillID": 0,
    "Version": "v3",
    "SenderAddress": "0x12345678900x12345678900x1234567890"
}
```

## GET /matches

**Optional filter parameters:**

| Name        |  Type |
| :-----------| :-----|
| id | number |
| player1_id | string |
| player2_id | string |
| status | string |
| version | string |
| winner_id | string |

**Response**

```
{
    "total": 1,
    "page": 1,
    "limit": 100,
    "matches": [
        {
            "ID": 2,
            "Player1ID": "player6",
            "Player2ID": "player7",
            "Player1Accepted": true,
            "Player2Accepted": true,
            "Player1DeckID": 1,
            "Player2DeckID": 1,
            "Status": "Playing",
            "Version": "v3",
            "RandomSeed": 1545916413,
            "Replay": {
                "ID": 0,
                "MatchID": 0,
                "ReplayJSON": null,
                "CreatedAt": "0001-01-01T00:00:00Z",
                "UpdatedAt": "0001-01-01T00:00:00Z"
            },
            "Deck": {
                "ID": 0,
                "CreatedAt": "0001-01-01T00:00:00Z",
                "UpdatedAt": "0001-01-01T00:00:00Z",
                "UserID": "",
                "DeckID": 0,
                "Name": "",
                "HeroID": 0,
                "DeckCards": null,
                "PrimarySkillID": 0,
                "SecondarySkillID": 0,
                "Version": "",
                "SenderAddress": ""
            },
            "WinnerID": "",
            "CreatedAt": "0001-01-01T00:00:00Z",
            "UpdatedAt": "2018-12-27T13:14:06Z"
        }
    ]
}
```

## GET /match/{id}

**Response**

```
{
    "ID": 2,
    "Player1ID": "player6",
    "Player2ID": "player7",
    "Player1Accepted": true,
    "Player2Accepted": true,
    "Player1DeckID": 1,
    "Player2DeckID": 1,
    "Status": "Playing",
    "Version": "v3",
    "RandomSeed": 1545916413,
    "Replay": {
        "ID": 0,
        "MatchID": 0,
        "ReplayJSON": null,
        "CreatedAt": "0001-01-01T00:00:00Z",
        "UpdatedAt": "0001-01-01T00:00:00Z"
    },
    "Deck": {
        "ID": 0,
        "CreatedAt": "0001-01-01T00:00:00Z",
        "UpdatedAt": "0001-01-01T00:00:00Z",
        "UserID": "",
        "DeckID": 0,
        "Name": "",
        "HeroID": 0,
        "DeckCards": null,
        "PrimarySkillID": 0,
        "SecondarySkillID": 0,
        "Version": "",
        "SenderAddress": ""
    },
    "WinnerID": "",
    "CreatedAt": "0001-01-01T00:00:00Z",
    "UpdatedAt": "2018-12-27T13:14:06Z"
}
```

## GET /cards

**Optional filter parameters:**

| Name        |  Type |
| :-----------| :-----|
| id | number |
| mould_id | number |
| version | string |
| kind | string |
| set | string |
| name | string |
| rank | string |
| type | string |
| rarity | string |
| damage | number |
| health | number |
| cost | number |

**Response**

```
{
    "total": 161,
    "page": 1,
    "limit": 100,
    "cards": [
        {
            "ID": 1,
            "mouldId": "1",
            "Version": "v3",
            "Kind": "CREATURE",
            "Set": "AIR",
            "Name": "Whizpar",
            "Description": "<b>Attack:</b> +1 damage to Water zombies",
            "FlavorText": "",
            "Picture": "Whizpar",
            "Rank": "MINION",
            "Type": "WALKER",
            "Rarity": "",
            "Frame": "",
            "Damage": 0,
            "Health": 0,
            "Cost": 0,
            "Ability": "",
            "UniqueAnimation": ""
        },
        [...]
    ]
}
```

## GET /card?mould_id={mould_id}&version={version}

**Response**

```
{
  "ID": 1,
  "mouldId": "1",
  "Version": "v3",
  "Kind": "CREATURE",
  "Set": "AIR",
  "Name": "Whizpar",
  "Description": "<b>Attack:</b> +1 damage to Water zombies",
  "FlavorText": "",
  "Picture": "Whizpar",
  "Rank": "MINION",
  "Type": "WALKER",
  "Rarity": "",
  "Frame": "",
  "Damage": 0,
  "Health": 0,
  "Cost": 0,
  "Ability": "",
  "UniqueAnimation": ""
}
```
