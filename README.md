# Search Yard 🔍

**A fan-made search engine for The Yard podcast.** 

##  Frontend
Written in [Svelte](https://svelte.dev/).
 

## Backend
Written in Golang using [Gin](https://gin-gonic.com/).


## Database

Using a SQLite database and the [driver by mattn](https://github.com/mattn/go-sqlite3).

[More info](https://github.com/Tharusha-dev/searchYard/blob/main/searchYardAPI/db/README.md).

## How it works

The algorithm currently uses these techniques to rank documents. (in this order)

- Inverted Index
- Cosine similarity
-  Word proximity
- Title weight (If the title includes a query term it is rated higher)

When retrieving relevent documents,

And uses a simple `LIKE` sql statement in [all_dialogues](https://github.com/Tharusha-dev/searchYard/blob/main/searchYardAPI/db/README.md#all_dialogues) table for quoted search. 


## Known issues

### Speed when searching by relevance

The bottleneck is the database, I tried indexing a bunch of stuff but this is as fast as i could make it. If anyone have any suggestions to make reads faster, I'm all ears.

