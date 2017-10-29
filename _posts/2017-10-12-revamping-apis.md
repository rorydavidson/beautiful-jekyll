---
layout: post
title: Bring on the v2
subtitle: Revamping APIs
date: '2017-10-12 12:01:47 +0100'
tags: [snomed, api]
gh-repo: IHTSDO/sct-snapshot-rest-api
gh-badge: [star, fork, follow]
show-avatar: false
---

Over the last few years, the team at SNOMED International have implemented a number of open REST APIs as part of the rapid development of tools to manage and interact with SNOMED CT.


Any software development project involves looking for the best balance between elegance and clarity in designs and developments, against the business need for speed of deployment. Our approach has leaned more to necessity and speed. Now that we have moved to a more stable development phase, we have the time to review and refactor our APIs to present a more standard view.


At the moment, our most commonly used APIs are those used in the SNOMED CT Browser, amongst the first ones that we developed (SNOMED CT Snapshot REST API). This has been the ideal place to start, looking to see how we can provide more standardized APIs so that any consumers can expect the same standard.


And like magic this has been done and v2 of the API has now been deployed. More details can be found here - [http://ihtsdo.github.io/sct-snapshot-rest-api/api.html](http://ihtsdo.github.io/sct-snapshot-rest-api/api.html).


The main highlight is the JSON representation of a concept, which uses standard terms for the labels, instead of shortcuts like the current version, and provides most things that would be needed to represent a SNOMED CT concept in one call

```
{
  "_id": "59d8cf1ee63829a42851a1ca",
  "memberships": [
    {
      "type": "SIMPLEMAP",
      "referencedComponentId": "79859009",
      "refset": {
        "conceptId": "900000000000497000",
        "preferredTerm": "CTV3 simple map"
      },
      "otherValue": "02B3.",
      "uuid": "92ca1e61-fff8-51d2-a11c-545d83797bbc",
      "active": true,
      "effectiveTime": "20020131",
      "module": {
        "conceptId": "900000000000207008",
        "preferredTerm": "SNOMED CT core"
      }
    }
  ],
  "descriptions": [
    {
      "descriptionId": "132493010",
      "conceptId": "79859009",
      "type": {
        "conceptId": "900000000000013009",
        "preferredTerm": "Synonym"
      },
      "languageCode": "en",
      "term": "Computer programmer",
      "length": 19,
      "caseSignificance": {
        "conceptId": "900000000000448009",
        "preferredTerm": "Case insensitive"
      },
      "acceptability": [
        {
          "descriptionId": "132493010",
          "languageReferenceSet": {
            "conceptId": "900000000000508004",
            "preferredTerm": "GB English"
          },
          "acceptability": {
            "conceptId": "900000000000548007",
            "preferredTerm": "Preferred"
          },
          "uuid": "599edffd-9492-57c2-a615-212f9916e23d",
          "active": true,
          "effectiveTime": "20020131",
          "module": {
            "conceptId": "900000000000207008",
            "preferredTerm": "SNOMED CT core"
          }
        },
        {
          "descriptionId": "132493010",
          "languageReferenceSet": {
            "conceptId": "900000000000509007",
            "preferredTerm": "US English"
          },
          "acceptability": {
            "conceptId": "900000000000548007",
            "preferredTerm": "Preferred"
          },
          "uuid": "63ea720a-e2c4-5e85-9758-4536606ad0b3",
          "active": true,
          "effectiveTime": "20080131",
          "module": {
            "conceptId": "900000000000207008",
            "preferredTerm": "SNOMED CT core"
          }
        }
      ],
      "active": true,
      "effectiveTime": "20170731",
      "module": {
        "conceptId": "900000000000207008",
        "preferredTerm": "SNOMED CT core"
      }
    },
    {
      "descriptionId": "504232014",
      "conceptId": "79859009",
      "type": {
        "conceptId": "900000000000013009",
        "preferredTerm": "Synonym"
      },
      "languageCode": "en",
      "term": "Computer programr",
      "length": 17,
      "caseSignificance": {
        "conceptId": "900000000000020002",
        "preferredTerm": "Initial character case insensitive"
      },
      "active": false,
      "effectiveTime": "20080131",
      "module": {
        "conceptId": "900000000000207008",
        "preferredTerm": "SNOMED CT core"
      }
    },
    {
      "descriptionId": "820955016",
      "conceptId": "79859009",
      "type": {
        "conceptId": "900000000000003001",
        "preferredTerm": "Fully specified name"
      },
      "languageCode": "en",
      "term": "Computer programmer (occupation)",
      "length": 32,
      "caseSignificance": {
        "conceptId": "900000000000448009",
        "preferredTerm": "Case insensitive"
      },
      "acceptability": [
        {
          "descriptionId": "820955016",
          "languageReferenceSet": {
            "conceptId": "900000000000508004",
            "preferredTerm": "GB English"
          },
          "acceptability": {
            "conceptId": "900000000000548007",
            "preferredTerm": "Preferred"
          },
          "uuid": "26b45dfb-3d13-52c4-b6c5-f3cab43b5ad6",
          "active": true,
          "effectiveTime": "20020131",
          "module": {
            "conceptId": "900000000000207008",
            "preferredTerm": "SNOMED CT core"
          }
        },
        {
          "descriptionId": "820955016",
          "languageReferenceSet": {
            "conceptId": "900000000000509007",
            "preferredTerm": "US English"
          },
          "acceptability": {
            "conceptId": "900000000000548007",
            "preferredTerm": "Preferred"
          },
          "uuid": "772accf1-7627-5366-b1b8-1f246416521e",
          "active": true,
          "effectiveTime": "20020131",
          "module": {
            "conceptId": "900000000000207008",
            "preferredTerm": "SNOMED CT core"
          }
        }
      ],
      "active": true,
      "effectiveTime": "20170731",
      "module": {
        "conceptId": "900000000000207008",
        "preferredTerm": "SNOMED CT core"
      }
    }
  ],
  "relationships": [
    {
      "relationshipId": "4076360022",
      "type": {
        "conceptId": "116680003",
        "preferredTerm": "Is a"
      },
      "destination": {
        "conceptId": "106297009",
        "preferredTerm": "Statistician, mathematician, systems analyst AND/OR related technician",
        "fullySpecifiedName": "Statistician, mathematician, systems analyst/related technician (occupation)",
        "definitionStatus": {
          "conceptId": "900000000000074008",
          "preferredTerm": "Primitive"
        },
        "statedDescendants": 13,
        "inferredDescendants": 13,
        "active": true,
        "effectiveTime": "20020131",
        "module": {
          "conceptId": "900000000000207008",
          "preferredTerm": "SNOMED CT core"
        }
      },
      "sourceId": "79859009",
      "relationshipGroup": 0,
      "characteristicType": {
        "conceptId": "900000000000010007",
        "preferredTerm": "Stated relationship"
      },
      "modifier": {
        "conceptId": "900000000000451002",
        "preferredTerm": "Some"
      },
      "active": true,
      "effectiveTime": "20080731",
      "module": {
        "conceptId": "900000000000207008",
        "preferredTerm": "SNOMED CT core"
      }
    },
    {
      "relationshipId": "4076361021",
      "type": {
        "conceptId": "116680003",
        "preferredTerm": "Is a"
      },
      "destination": {
        "conceptId": "158832009",
        "preferredTerm": "Systems analyst/computer programmer",
        "fullySpecifiedName": "Systems analyst/computer programmer (occupation)",
        "definitionStatus": {
          "conceptId": "900000000000074008",
          "preferredTerm": "Primitive"
        },
        "statedDescendants": 4,
        "inferredDescendants": 4,
        "active": true,
        "effectiveTime": "20020131",
        "module": {
          "conceptId": "900000000000207008",
          "preferredTerm": "SNOMED CT core"
        }
      },
      "sourceId": "79859009",
      "relationshipGroup": 0,
      "characteristicType": {
        "conceptId": "900000000000010007",
        "preferredTerm": "Stated relationship"
      },
      "modifier": {
        "conceptId": "900000000000451002",
        "preferredTerm": "Some"
      },
      "active": true,
      "effectiveTime": "20080731",
      "module": {
        "conceptId": "900000000000207008",
        "preferredTerm": "SNOMED CT core"
      }
    },
    {
      "relationshipId": "277869024",
      "type": {
        "conceptId": "116680003",
        "preferredTerm": "Is a"
      },
      "destination": {
        "conceptId": "158832009",
        "preferredTerm": "Systems analyst/computer programmer",
        "fullySpecifiedName": "Systems analyst/computer programmer (occupation)",
        "definitionStatus": {
          "conceptId": "900000000000074008",
          "preferredTerm": "Primitive"
        },
        "statedDescendants": 4,
        "inferredDescendants": 4,
        "active": true,
        "effectiveTime": "20020131",
        "module": {
          "conceptId": "900000000000207008",
          "preferredTerm": "SNOMED CT core"
        }
      },
      "sourceId": "79859009",
      "relationshipGroup": 0,
      "characteristicType": {
        "conceptId": "900000000000011006",
        "preferredTerm": "Inferred relationship"
      },
      "modifier": {
        "conceptId": "900000000000451002",
        "preferredTerm": "Some"
      },
      "active": true,
      "effectiveTime": "20020131",
      "module": {
        "conceptId": "900000000000207008",
        "preferredTerm": "SNOMED CT core"
      }
    },
    {
      "relationshipId": "277870020",
      "type": {
        "conceptId": "116680003",
        "preferredTerm": "Is a"
      },
      "destination": {
        "conceptId": "106297009",
        "preferredTerm": "Statistician, mathematician, systems analyst AND/OR related technician",
        "fullySpecifiedName": "Statistician, mathematician, systems analyst/related technician (occupation)",
        "definitionStatus": {
          "conceptId": "900000000000074008",
          "preferredTerm": "Primitive"
        },
        "statedDescendants": 13,
        "inferredDescendants": 13,
        "active": true,
        "effectiveTime": "20020131",
        "module": {
          "conceptId": "900000000000207008",
          "preferredTerm": "SNOMED CT core"
        }
      },
      "sourceId": "79859009",
      "relationshipGroup": 0,
      "characteristicType": {
        "conceptId": "900000000000011006",
        "preferredTerm": "Inferred relationship"
      },
      "modifier": {
        "conceptId": "900000000000451002",
        "preferredTerm": "Some"
      },
      "active": true,
      "effectiveTime": "20020131",
      "module": {
        "conceptId": "900000000000207008",
        "preferredTerm": "SNOMED CT core"
      }
    }
  ],
  "isLeafInferred": true,
  "isLeafStated": true,
  "v": "2",
  "conceptId": "79859009",
  "preferredTerm": "Computer programmer",
  "fullySpecifiedName": "Computer programmer (occupation)",
  "definitionStatus": {
    "conceptId": "900000000000074008",
    "preferredTerm": "Primitive"
  },
  "statedDescendants": 0,
  "inferredDescendants": 0,
  "active": true,
  "effectiveTime": "20020131",
  "module": {
    "conceptId": "900000000000207008",
    "preferredTerm": "SNOMED CT core"
  }
}
```

Feedback is always welcome.
