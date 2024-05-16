# SQLite Database structure
The latest version (The Yard #148) of the SQLite database file can be downloaded [here](https://drive.google.com/file/d/1Uu2ya1sI1U1IBI0UWmIxWnxcYJuzC5O_/view?usp=sharing).

All of these data were gathered using [yt-dlp](https://github.com/yt-dlp/yt-dlp), and computed using python with the help of [scikit-learn](https://scikit-learn.org)

Using yt-dlp auto generated English substitle files were downloaded.

## Tables 📊

 * **inverted_index**: Stores the mapping between words and the documents they appear in.
 * **word_time**: Stores words and the time stamp they appear in.
 * **time_dialogue**: Links timestamps to specific dialogue snippets within videos.
 * **all_dialogues**: Stores all dialogue text extracted from the videos.
 * **video_titles**: Stores the titles of the videos.
 * **term_positions**: Indicates the specific positions of words within documents.
 * **all_episodes_tfidf_count**: Stores tfidf, count and magnitude for each term in a document.

### inverted_index
| Column |  Data type|Example
|--|--|--|
| index| INTEGER |775
| term| TEXT |yard
| video_id| TEXT |psC5ugFPlF4,OVPsV-O5eh4,y8K6QazBqrY,x7UDHcATxn4,No0-vEYExZQ,kxnZuddEYCg,ajjnZ3Vrq50,bzEINLNJI4w ...


### word_time
| Column |  Data type|Example
|--|--|--|
| index| INTEGER |267987
| video_id| TEXT |-4iG7Lloy1U
| term| TEXT |yard
| times| TEXT |"1291s","3038s","3042s","3054s"...

### time_dialogue
| Column |  Data type|Example
|--|--|--|
| index| INTEGER |1719
| video_id| TEXT |bTHkgMOuzcc
| time| TEXT |4058s
| dialogue| TEXT |yo you actually i prefer you bald and i

### all_dialogues
| Column |  Data type|Example
|--|--|--|
| index| INTEGER |0
| video_id| TEXT |bTHkgMOuzcc
| words| TEXT |oh you do your accent oh you make fun of her so much and it's like you just named do you actually use a delay no no he doesn't he's lying he's trying to think welcome back to the yard podcast ...

### video_titles
| Column |  Data type|Example
|--|--|--|
| index| INTEGER |147
| title| TEXT |Linus INSTANTLY Regrets Doing Our Podcast | The Yard
| video_id| TEXT |vvtaDS0B334


### term_positions
| Column |  Data type|Example
|--|--|--|
| index| INTEGER |28
| video_id| TEXT |bTHkgMOuzcc
| terms| TEXT |yard
| positions| TEXT |46,5558,5571,7447,9753,10554,11044,16447 ...

### all_episodes_tfidf_count
| Column |  Data type|Example
|--|--|--|
| index| INTEGER |1061865
| video_id| TEXT |nFcH9BaFgAo
| term| TEXT |tax
| tfidf| REAL |0.030633051231763332
| count| INTEGER |22
| magnitude| REAL |0.000938383827767837




