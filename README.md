# Hypermedia document format comparison

This repository contains a little comparison I wanted to make between the numerous Hypermedia document formats that can be found, used to represent the same document.

## Original document

The original document (as it could be served by any non-hypermedia "so-called-REST-API"), as represented in jdo.json, is the following :

```javascript
{
  "trigram": "JDO",
  "first_name": "John",
  "last_name": "Doe",
  "phone_numbers": [
    "0102030405"
  ],
  "email": "jdoe@acme.com",
  "manager": "TED",
  "team": "SOFT",
  "entry_date": "2017-05-02",
  "leaving_date": null,
  "description": "I am a very nice person",
  "skills": [
        {
          "category": "dev",
          "name": "Python",
          "level": 1.0,
          "motivation": 2.0
        },
        {
          "category": "dev",
          "name": "REST API",
          "level": 1.0,
          "motivation": 2.0
        }
  ]
}
```

As you can see it represents a document that could be served by any company employee directory. The "trigram" is a 3-letter, unique identificator for every employee.
The employee here is John Doe, whose trigram is JDO, who works for Acme with his manager Tom Edwards (TED) in the "SOFT" team.

## Compared formats

I compared here Collection+JSON, HAL, JSON-API, JSON-LD, Hydra, Mason, Siren and Uber. I may add other formats but only JSON-based.
You can find some comments on every format in the "Comments.md" document : those are mainly comments that came to my mind while I was writing JDO's representation in each particular format and are not meant to be a "ground truth".
