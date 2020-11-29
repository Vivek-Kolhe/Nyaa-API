# Nyaa-API
Nyaa API is an **Unofficial Nyaa.si API**. It just scrapes the website to satisfy the need for an API.\
And I'm sorry I've decided to keep the API closed source. I might make it open source in the near future. \
***Note:*** This API doesn't make authenticated requests to Nyaa, so you cannot make changes to your account or upload anything.

## Usage
***Note:*** The API is hosted at **heroku** so it might be slow to respond. The API will fetch only recently uploaded 750 torrents, if the number of torrents are larger.

**The API is available at:** ```https://nyaaapi.herokuapp.com/```

- ### Anime Torrent Search
  **Endpoint Path:** ```/anime/search```\
  The endpoint takes **three arguments**.
  
  | **Request** | **Arguments** | **Description** |
  | ------| ------| ------ |
  | <p>Anime torrent search using query and category.</p> | <p> ```query``` **(Required)**</p><p>```category```**(Required)**</p> | <p>**Query:** Anime to be searched.</p><p>**Category:** Can be any of the category listed: ***amv***, ***eng***, ***non-eng***, ***raw*** or ***all***. </p> |
  | <p>Anime torrent search using torrent ID.</p> | <p> ```id``` </p> **(Required)**</p> | <p>**ID:** ID is generally the numerical part located at the end of the particular torrent's link.</p><p>**Eg:** ```https://nyaa.si/view/1234567 ```, here ID is ***1234567***</p> |
  
  ***Note:*** When using ```id``` as argument, the other two arguments are not required.\
  **Example:**
  - ```https://nyaaapi.herokuapp.com/anime/search?category=eng&query=clannad```
  - ```https://nyaaapi.herokuapp.com/anime/search?id=1270739```
  
- ### Manga Torrent Search
  **Endpoint Path:** ```/manga/search```\
  This endpoint also takes **three arguments**.
  
  | **Request** | **Arguments** | **Description** |
  | ------| ------| ------ |
  | <p>Manga torrent search using query and category.</p> | <p> ```query``` **(Required)**</p><p>```category```**(Required)**</p> | <p>**Query:** Query to be searched.</p><p>**Category:** Can be any of the category listed: ***eng***, ***non-eng***, ***raw*** or ***all***. </p> |
  | <p>Manga torrent search using torrent ID.</p> | <p> ```id``` </p> **(Required)**</p> | <p>**ID:** ID is generally the numerical part located at the end of the particular torrent's link.</p><p>**Eg:** ```https://nyaa.si/view/1234567 ```, here ID is ***1234567***</p> |
  
  ***Note:*** When using ```id``` as argument, the other two arguments are not required.\
  *For examples, refer to the above section.*
  
 - ### Uploaded by a particular user
   **Endpoint Path:** ```/user```\
   The enddpoint takes only one parameter.
   
   | **Request** | **Argument** | **Description** |
   | ------| ------| ------ |
   | <p>Torrents uploaded by an user.</p> | <p>```user```**(Required)**</p> | <p>**User:** Username of the uploader.</p> |
   
   ***Note:*** The user shouldn't be anonymous and user's exact username must be passed.\
   **Example:**
   - ```https://nyaaapi.herokuapp.com/user?user=judas```

## Disclaimer
**I do not host any of the torrents fetched by the API. The API is just meant to scrape the website and return the results. Use it at your own risk, LOL!**
