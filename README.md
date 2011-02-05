Actions
=======

* A character buys a glass yogurt pot

POST /

    {
      "character": "Galaad_II",
      "verb": "buyGlassYogurtPot",
      "timestamp": "2011-02-04 18:02:45",
      "place": "parisDairy",
      "effects": {
        "economy": -5,
        "environment": 5
      }
    }

* Effects on the character (aka points)

GET /effects_by_character/Galaad_II


* Effects on the place


GET /effects_by_place/parisDairy


* Effects on the whole world

GET /effects/


Position
========

* Ongoing moves in a place

GET /_changes

GET /_changes?feed=continuous&since=LAST_SEQ&filter=sos21/place&place=parisDairy


* A character moves

GET /playable_character/Galaad_II

PUT /playable_character/Galaad_II
    {
      "_rev": "...",
      "loggedOn": true,
      "place": "parisDairy",
      "x": 26,
      "y": 18
    }


Away from keyboard
==================

* Online characters sorted by the last time they moved

GET /away_from_keyboard?descending=true