# Zombie Battleground API

## API Doc Site

To try out all the apis, see our doc explorer

[Zombie Battleground Api Docs Site](https://api-docs.loom.games)

## Base URL

```
https://api.loom.games
```

## API Version

```
https://api.loom.games/zb/v1
```

## Pagination

```
https://api.loom.games/zb/v1/decks?page=1&limit=40
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
      "id": 1812,
      "created_at": "2019-02-08T13:40:46Z",
      "updated_at": "2019-02-08T13:40:46Z",
      "user_id": "ZombieSlayer_5699",
      "deck_id": 1,
      "name": "Deck 1",
      "hero_id": 4,
      "cards": [
        {
          "card_name": "Hazmaz",
          "amount": 1
        },
        {
          "card_name": "Stapler",
          "amount": 1
        },
        {
          "card_name": "Nail Bomb",
          "amount": 1
        },
        {
          "card_name": "Germ",
          "amount": 1
        },
        {
          "card_name": "Draft",
          "amount": 1
        },
        {
          "card_name": "Azuraz",
          "amount": 2
        },
        {
          "card_name": "Ztalagmite",
          "amount": 2
        },
        {
          "card_name": "Blocker",
          "amount": 1
        },
        {
          "card_name": "Rockky",
          "amount": 1
        },
        {
          "card_name": "Rubble",
          "amount": 1
        },
        {
          "card_name": "Banshee",
          "amount": 1
        }
      ],
      "primary_skill_id": 21,
      "secondary_skill_id": 22,
      "version": "v5",
      "sender_address": "0xEeBA34eb21Ce7985925680c2AAC3F13b612D61A1",
      "block_height": 876225,
      "is_deleted": false
    },
    {
      "id": 2876,
      "created_at": "2019-02-11T04:30:02Z",
      "updated_at": "2019-02-11T04:30:02Z",
      "user_id": "ZombieSlayer_12654857602681251555495157711430534949859049166637086992294106168800544489412",
      "deck_id": 2,
      "name": "000000",
      "hero_id": 0,
      "cards": [
        {
          "card_name": "Bane",
          "amount": 1
        },
        {
          "card_name": "Azzazzin",
          "amount": 1
        },
        {
          "card_name": "GooZilla",
          "amount": 1
        },
        {
          "card_name": "Gloop",
          "amount": 4
        },
        {
          "card_name": "Germ",
          "amount": 1
        },
        {
          "card_name": "Cherno-bill",
          "amount": 1
        },
        {
          "card_name": "Harpoon",
          "amount": 1
        },
        {
          "card_name": "Nail Bomb",
          "amount": 1
        },
        {
          "card_name": "Rubble",
          "amount": 2
        },
        {
          "card_name": "Zky",
          "amount": 1
        },
        {
          "card_name": "Zwoop",
          "amount": 1
        }
      ],
      "primary_skill_id": 0,
      "secondary_skill_id": 0,
      "version": "v5",
      "sender_address": "0x59550a684Aa87c3fd06fa2af00Fb3f6A63260983",
      "block_height": 929950,
      "is_deleted": false
    }
  ]
}
```

## GET /deck/{id}

**Response**

```

{
  "id": 1813,
  "created_at": "2019-02-08T13:40:46Z",
  "updated_at": "2019-02-08T13:40:46Z",
  "user_id": "ZombieSlayer_38235065610765369970666124450095977654251015341547488228846975051479849607480",
  "deck_id": 2,
  "name": "HORDE 1",
  "hero_id": 0,
  "cards": [
    {
      "card_name": "Bane",
      "amount": 1
    },
    {
      "card_name": "Zwoop",
      "amount": 2
    },
    {
      "card_name": "GooZilla",
      "amount": 1
    },
    {
      "card_name": "Azzazzin",
      "amount": 1
    },
    {
      "card_name": "Cherno-bill",
      "amount": 1
    },
    {
      "card_name": "Harpoon",
      "amount": 1
    },
    {
      "card_name": "Nail Bomb",
      "amount": 1
    },
    {
      "card_name": "Germ",
      "amount": 1
    },
    {
      "card_name": "Gloop",
      "amount": 4
    },
    {
      "card_name": "Zky",
      "amount": 1
    },
    {
      "card_name": "Rubble",
      "amount": 1
    }
  ],
  "primary_skill_id": 0,
  "secondary_skill_id": 0,
  "version": "v5",
  "sender_address": "0x90aF312B0ec4641CfE019Ac3577b45E694Cc40A6",
  "block_height": 876231,
  "is_deleted": false
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
  "total": 3,
  "page": 1,
  "limit": 100,
  "matches": [
    {
      "id": 1454,
      "created_at": "2019-01-23T11:21:36Z",
      "updated_at": "2019-01-23T11:22:58Z",
      "player1_id": "ZombieSlayer_1660102160939616713929530094917607621856109004923959540063468893331468840626",
      "player2_id": "ZombieSlayer_50758609486196673937978411021251546451840453241737090773240881165998917431239",
      "player1_accepted": true,
      "player2_accepted": true,
      "player1_deck_id": 1,
      "player2_deck_id": 4,
      "status": "Ended",
      "version": "v3",
      "random_seed": 1548242486,
      "winner_id": "ZombieSlayer_50758609486196673937978411021251546451840453241737090773240881165998917431239",
      "block_height": 497513
    },
    {
      "id": 1455,
      "created_at": "2019-01-23T11:23:32Z",
      "updated_at": "2019-01-23T11:31:23Z",
      "player1_id": "ZombieSlayer_50758609486196673937978411021251546451840453241737090773240881165998917431239",
      "player2_id": "ZombieSlayer_2251332460754899311791167076384054146005516202205833986423615541675962783501",
      "player1_accepted": true,
      "player2_accepted": true,
      "player1_deck_id": 4,
      "player2_deck_id": 3,
      "status": "Canceled",
      "version": "v3",
      "random_seed": 1548242601,
      "winner_id": "ZombieSlayer_2251332460754899311791167076384054146005516202205833986423615541675962783501",
      "block_height": 497805
    },
    {
      "id": 1514,
      "created_at": "2019-01-23T22:03:31Z",
      "updated_at": "2019-01-23T22:03:31Z",
      "player1_id": "ZombieSlayer_21381983288297542503548358289910229702769718750289425781498318432412410749076",
      "player2_id": "ZombieSlayer_7260941436698941368709492298747749802933234869379693277084216267573241490196",
      "player1_accepted": true,
      "player2_accepted": false,
      "player1_deck_id": 2,
      "player2_deck_id": 1,
      "status": "Timedout",
      "version": "v3",
      "random_seed": 1548280881,
      "winner_id": "",
      "block_height": 512549
    }
  ]
}
```

## GET /match/{id}

**Response**

```
{
  "id": 1454,
  "created_at": "2019-01-23T11:21:36Z",
  "updated_at": "2019-01-23T11:22:58Z",
  "player1_id": "ZombieSlayer_1660102160939616713929530094917607621856109004923959540063468893331468840626",
  "player2_id": "ZombieSlayer_50758609486196673937978411021251546451840453241737090773240881165998917431239",
  "player1_accepted": true,
  "player2_accepted": true,
  "player1_deck_id": 1,
  "player2_deck_id": 4,
  "status": "Ended",
  "version": "v3",
  "random_seed": 1548242486,
  "winner_id": "ZombieSlayer_50758609486196673937978411021251546451840453241737090773240881165998917431239",
  "block_height": 497513
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
  "total": 183,
  "page": 1,
  "limit": 100,
  "cards": [
    {
      "id": 1,
      "mould_id": "1",
      "version": "v3",
      "kind": "CREATURE",
      "set": "AIR",
      "name": "Whizpar",
      "description": "<b>Attack:</b> +1 damage to Water zombies",
      "flavor_text": "The unfriendly ghost...",
      "picture": "Whizpar",
      "rank": "MINION",
      "type": "WALKER",
      "rarity": "",
      "frame": "",
      "damage": 1,
      "health": 1,
      "cost": 1,
      "ability": "",
      "block_height": 0,
      "image_url": "https://loom.games/img/cards/001.png"
    },
    [...]
  ]
}
```

## GET /card?mould_id={mould_id}&version={version}

**Response**

```
{
  "id": 1,
  "mould_id": "1",
  "version": "v3",
  "kind": "CREATURE",
  "set": "AIR",
  "name": "Whizpar",
  "description": "<b>Attack:</b> +1 damage to Water zombies",
  "flavor_text": "The unfriendly ghost...",
  "picture": "Whizpar",
  "rank": "MINION",
  "type": "WALKER",
  "rarity": "",
  "frame": "",
  "damage": 1,
  "health": 1,
  "cost": 1,
  "ability": "",
  "block_height": 0,
  "image_url": "https://loom.games/img/cards/001.png"
}
```
