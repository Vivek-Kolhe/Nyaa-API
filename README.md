# Nyaa-API
Nyaa API is an **Unofficial Nyaa.si API**. It just scrapes the website to satisfy the need for an API.\
And I'm sorry I've decided to keep the API closed source. I might make it open source in the near future. \
***Note:*** This API doesn't make authenticated requests to Nyaa, so you cannot make changes to your account or upload anything.

## Update
 - Added Sukebei search ***(NSFW content!)***.

## Usage
***Note:*** The API is hosted at **heroku** so it might be slow to respond. The API will fetch only recently uploaded 750 torrents, if the number of torrents are larger.

**The API is available at:** ```https://nyaaapi.herokuapp.com/```

- ### Anime Torrent Search
  **Endpoint Path:** ```/anime/search```\
  The endpoint takes **three arguments**.
  
  | **Request** | **Arguments** | **Description** |
  | ------| ------| ------ |
  | <p>Anime torrent search using query and category.</p> | <p> ```query``` **(Required)**</p><p>```category```**(Required)**</p> | <p>**Query:** Anime to be searched.</p><p>**Category:** Can be any of the category. Check below for the complete list of <a href="https://github.com/Vivek-Kolhe/Nyaa-API/blob/main/README.md#anime-torrent-search-1">categories</a>. </p> |
  | <p>Anime torrent search using torrent ID.</p> | <p> ```id``` </p> **(Required)**</p> | <p>**ID:** ID is generally the numerical part located at the end of the particular torrent's url.</p><p>**Eg:** ```https://nyaa.si/view/1234567 ```, here ID is ***1234567***</p> |
  
  ***Note:*** When using ```id``` as argument, then the other two arguments are not required.\
  **Example:**
  - ```https://nyaaapi.herokuapp.com/anime/search?category=eng&query=clannad```
  - ```https://nyaaapi.herokuapp.com/anime/search?id=1270739```
  
- ### Manga Torrent Search
  **Endpoint Path:** ```/manga/search```\
  This endpoint also takes **three arguments**.
  
  | **Request** | **Arguments** | **Description** |
  | ------| ------| ------ |
  | <p>Manga torrent search using query and category.</p> | <p> ```query``` **(Required)**</p><p>```category```**(Required)**</p> | <p>**Query:** Query to be searched.</p><p>**Category:** Can be any of the category. Check below for the complete list of <a href="https://github.com/Vivek-Kolhe/Nyaa-API/blob/main/README.md#manga-torrent-search-1">categories</a>. </p> |
  | <p>Manga torrent search using torrent ID.</p> | <p> ```id``` </p> **(Required)**</p> | <p>**ID:** ID is generally the numerical part located at the end of the particular torrent's url.</p><p>**Eg:** ```https://nyaa.si/view/1234567 ```, here ID is ***1234567***</p> |
  
  ***Note:*** When using ```id``` as argument, then the other two arguments are not required.\
  *For examples, refer to the above section.*
 
 - ### Sukebei Search
   **Endpoint Path:** ```/sukebei/search```\
   This endpoint also takes **three arguments**.
  
   | **Request** | **Arguments** | **Description** |
   | ------| ------| ------ |
   | <p>Torrent search using query and category.</p> | <p> ```query``` **(Required)**</p><p>```category```**(Required)**</p> | <p>**Query:** Query to be searched.</p><p>**Category:** Can be any of the category. Check below for the complete list of <a href="https://github.com/Vivek-Kolhe/Nyaa-API/blob/main/README.md#sukebei-search-1">categories</a>. </p> |
   | <p>Torrent search using torrent ID.</p> | <p> ```id``` </p> **(Required)**</p> | <p>**ID:** ID is generally the numerical part located at the end of the particular torrent's url.</p><p>**Eg:** ```https://sukebei.nyaa.si/view/1234567 ```, here ID is ***1234567***</p> |
  
   ***Note:*** When using ```id``` as argument, then the other two arguments are not required.\
   **Example:**
   - ```https://nyaaapi.herokuapp.com/sukebei/search?query=euphoria&category=anime```
   - ```https://nyaaapi.herokuapp.com/sukebei/search?id=2847009```
 
 - ### Uploaded by a particular user
   **Endpoint Path:** ```/user```\
   The endpoint takes only one argument.
   
   | **Request** | **Argument** | **Description** |
   | ------| ------| ------ |
   | <p>Torrents uploaded by an user.</p> | <p>```user```**(Required)**</p> | <p>**User:** Username of the uploader.</p> |
   
   ***Note:*** The user shouldn't be anonymous and user's exact username must be passed.\
   **Example:**
   - ```https://nyaaapi.herokuapp.com/user?user=judas```

## Available Categories
- ### Anime Torrent Search
  | **Abbreviation** | **Definition** |
  |---------|---------|
  | ```all``` | Can be used to fetch results from all categories. |
  | ```amv``` | Anime Music Video. |
  | ```eng``` | English translated anime torrents. |
  | ```non-eng``` | Non - English anime torrents. |
  | ```raw``` | Raw anime torrents. |

- ### Manga Torrent Search
  | **Abbreviation** | **Definition** |
  |---------|---------|
  | ```all``` | Can be used to fetch results from all categories. |
  | ```eng``` | English translated manga torrents. |
  | ```non-eng``` | Non - English manga torrents. |
  | ```raw``` | Raw manga torrents. |

- ### Sukebei Search
  | **Abbreviation** | **Definition** |
  |---------|---------|
  | ```all``` | Can be used to fetch results from all categories. |
  | ```art``` | Art. |
  | ```anime``` | Anime torrents. |
  | ```dou``` | Doujin torrents. |
  | ```games``` | Games torrents. |
  | ```manga``` | Manga torrents. |
  | ```pics``` | Pictures torrents. |
  | ```real``` | Might be JAV torrents (I never tried. T-T). |
  | ```picbook``` | Picturebook torrents. |
  | ```vid``` | Video torrents. |

## Disclaimer
**I do not host any of the torrents fetched by the API. The API is just meant to scrape the website and return the results. I do not promote piracy, if you guys can afford legal methods, then use them and support the industry :).\
Use it at your own risk, LOL!**
