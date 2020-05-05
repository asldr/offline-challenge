# Offline Challenge API

The following requests are currently available (WIP). <br />
There are request for **challenges** and **participants** so far.

## Create challenge

Creates a new challenge

### Request

`POST http://localhost:1337/challenges`

### Example Payload

```
{
  "name": "erster Test",
  "description": "Dies ist die Beschreibung für die erste Challenge",
  "type": "distance",
  "goal": "30"
}
```

|   Property    |          Description          |
| :-----------: | :---------------------------: |
|    name\*     |     name of the challenge     |
| description\* | description of the challenge  |
|  start_date   |  start date of the challenge  |
|   end_date    |   end date of the challenge   |
|    type\*     |     type of the challenge     |
| participants  | participants of the challenge |
|    goal\*     |     goal of the challenge     |

`* required`

## Update a challenge

Updates a challenge by ID, using the same payload properties as POST

### Request

`PUT http://localhost:1337/challenges/:id`

### Example Payload

```
{
  "participants": {
    "id": 1
  }
}
```

## Get all challenges

Gets all challenges in database

### Request

`GET http://localhost:1337/challenges`

### Example response

```
[
  {
    "id": 1,
    "name": "erster Test",
    "description": "Dies ist die erste Beschreibung für die erste Challenge",
    "start_date": null,
    "end_date": null,
    "type": "steps",
    "goal": "5000",
    "created_at": "2020-04-20T19:54:36.668Z",
    "updated_at": "2020-04-21T20:32:39.279Z",
    "participants": [
      {
        "id": 1,
        "name": "Wolf Niklas",
        "email": null,
        "password": null,
        "created_at": "2020-04-21T20:14:09.616Z",
        "updated_at": "2020-04-21T20:14:09.616Z"
      }
    ]
  },
  {
    "id": 2,
    "name": "erster Test",
    "description": "Dies ist die erste Beschreibung für die erste Challenge",
    "start_date": null,
    "end_date": null,
    "type": "distance",
    "goal": "30",
    "created_at": "2020-04-21T20:40:20.353Z",
    "updated_at": "2020-04-21T20:40:20.353Z",
    "participants": []
  }
]
```

## Get a single challenge

Gets a single challenge by ID from database

### Request

`GET http://localhost:1337/challenges/:id`

### Example response

```
{
  "id": 2,
  "name": "erster Test",
  "description": "Dies ist die erste Beschreibung für die erste Challenge",
  "start_date": null,
  "end_date": null,
  "type": "distance",
  "goal": "30",
  "created_at": "2020-04-21T20:40:20.353Z",
  "updated_at": "2020-04-21T20:40:20.353Z",
  "participants": []
}
```

## Remove challange

Removes a challenge, identified by ID

### Request

`DELETE http://localhost:1337/challenges/:id`

### Example response

```
{
  "id": 4,
  "name": "erster Tesat",
  "description": "Dies ist die erste Beschreibung für die erste Challenge",
  "start_date": null,
  "end_date": null,
  "type": "distance",
  "goal": "30",
  "created_at": "2020-04-21T20:46:38.587Z",
  "updated_at": "2020-04-21T20:46:38.587Z",
  "participants": []
}
```

---

## Create participant

Creates a participant

### Request

`POST http://localhost:1337/participants/`

|  Property  |             Description              |
| :--------: | :----------------------------------: |
|    name    |       name of the participant        |
|    uui     | unique identifier of the participant |
| challenges |    challenges of the participant     |

## Get all participants

Gets all participants in database

### Request

`GET http://localhost:1337/participants`

### Example response

```
[
  {
    "id": 1,
    "name": "Wolf Niklas",
    "email": null,
    "password": null,
    "created_at": "2020-04-21T20:14:09.616Z",
    "updated_at": "2020-04-21T20:14:09.616Z",
    "challenges": [
      {
        "id": 1,
        "name": "erster Test",
        "start_date": null,
        "end_date": null,
        "type": "steps",
        "goal": "5000",
        "description": "Dies ist die erste Beschreibung für die erste Challenge",
        "created_at": "2020-04-20T19:54:36.668Z",
        "updated_at": "2020-04-21T20:32:39.279Z"
      }
    ]
  },
  {
    "id": 2,
    "name": "Axel Salder",
    "email": null,
    "password": null,
    "created_at": "2020-04-28T16:18:28.035Z",
    "updated_at": "2020-04-28T16:18:28.035Z",
    "challenges": [
      {
        "id": 1,
        "name": "erster Test",
        "start_date": null,
        "end_date": null,
        "type": "steps",
        "goal": "5000",
        "description": "Dies ist die erste Beschreibung für die erste Challenge",
        "created_at": "2020-04-20T19:54:36.668Z",
        "updated_at": "2020-04-21T20:32:39.279Z"
      }
    ]
  },
  {
    "id": 3,
    "name": "Max Mustermann",
    "email": null,
    "password": null,
    "created_at": "2020-04-28T16:19:42.597Z",
    "updated_at": "2020-04-28T16:19:42.597Z",
    "challenges": []
  }
]
```

## Get a single participant

Gets a single participant by ID from database

### Request

`GET http://localhost:1337/participants/:id`

### Example response

```
{
  "id": 2,
  "name": "Axel Salder",
  "email": null,
  "password": null,
  "created_at": "2020-04-28T16:18:28.035Z",
  "updated_at": "2020-04-28T16:18:28.035Z",
  "challenges": [
    {
      "id": 1,
      "name": "erster Test",
      "start_date": null,
      "end_date": null,
      "type": "steps",
      "goal": "5000",
      "description": "Dies ist die erste Beschreibung für die erste Challenge",
      "created_at": "2020-04-20T19:54:36.668Z",
      "updated_at": "2020-04-21T20:32:39.279Z"
    }
  ]
}
```
