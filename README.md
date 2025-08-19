# NottyBlock
Text-Based Content Moderation for Modern Applications

The NottyBlock API is a RESTful content moderation API that detects inappropriate and profane language using deep learning models and word lists. The API endpoints are highly customizable, ensuring that both requests and responses are suitable for most software designs. 

The functionality currently provided is listed below
  1. Checking if text contains common profanity encountered in American English which does include a few words originating outside of English using wordlist and deep learning models.
  2. Checking if text contains offensive language including but not limited to profanity, hate speech, sexual content, or otherwise offensive content encountered in American English using only deep learning models.
  3. Removing profanity from text using only wordlists which includes both block lists and allow lists.


The deep learning models provide confidence that new and cleverly crafted offensive language is more likely to be detected, unlike would be the case with word lists alone.

The word lists alongside common character replacements, such as '$' being used as an 's', allow for strict word checking suitable for sensitive situations. However, they come with a greater potential for false negatives. To mitigate that, which is known as the Scunthorpe problem, the flagging process works with a list of whitelisted words to ensure that words like "bass" and "class" are not incorrectly flagged. 

The blocked words are available in the bad_words.csv file in this repository.
The whitelisted words are available in the good_words.csv file in this repository.

The character replacements used to preprocess the text are listed below
*  "@" -> "a"
*  "4" -> "a"
*  "8" -> "b"
*  "(" -> "c"
*  "3" -> "e"
*  "#" -> "h"
*  "!" -> "i"
*  "1" -> "i"
*  "0" -> "o"
*  "5" -> "s"
*  "$" -> "s"
*  "+" -> "t"

The API is available here https://rapidapi.com/runcieneild/api/nottyblock
For any inquiries, reachout to support@ndrsoftware.com.
This includes and bugs, improvements to functionality, or other similar concerns.
