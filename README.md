# Nyaa-API
Nyaa API is an **Unofficial Nyaa.si API**. It just scrapes the website to satisfy the need for an API.\
The API is closed source for now. I might make it open source in the near future. \
***Note:*** This API doesn't make authenticated requests to Nyaa, so you cannot make changes to your account or upload anything.

## Update
 - Added Sukebei search ***(NSFW content!)***.
 - Covers complete Nyaa and Sukebei.
 - Added Sorting.

## Usage
***Note:*** The API is hosted at **heroku** so it might be slow to respond. The API will fetch only recently uploaded 750 torrents, if the number of torrents are larger.

**The API is available at:** ```https://nyaaapi.herokuapp.com/```

 - ### Nyaa Search
   - #### Available Endpoints
       **Every endpoint takes two arguments.**
       | **Arguments** | **Description** |
       |------|------|
       | ```query``` **(Required)** | Search query. |
       | ```sub_category``` **(Optional)** | Sub category of the torrents. |
       | ```sort``` **(Optional)** | Sorting parameter |
       | ```order``` **(Optional)** | Order of sorting. Defaults to ***Descending order***. |
       
       - **Endpoints:**
           | **Category** | **Endpoint** |
           |---------|---------|
           | Anime | ```/nyaa/anime``` |
           | Manga | ```/nyaa/manga``` |
           | Audio | ```/nyaa/audio``` |
           | Pictures | ```/nyaa/pictures``` |
           | Live Action | ```/nyaa/live_action``` |
           | Software | ```/nyaa/software``` |
       
       - **Sub-Categories:**
           | **Category** | **Sub-Category** |
           |------|------|
           | Anime | ```amv```, ```eng```, ```non-eng```, ```raw``` |
           | Manga | ```eng```, ```non-eng```, ```raw``` |
           | Audio | ```lossy```, ```lossless``` |
           | Pictures | ```photos```, ```graphics``` |
           | Live Action | ```promo```, ```eng```, ```non-eng```, ```raw``` |
           | Software | ```application```, ```games``` |
     
       - **Sorting:**
           | **Arguments** | **Methods**  |
           | ---- | ---- |
           | Sort | ```size```, ```seeders```, ```leechers```, ```date```, ```downloads``` |
           | Order | ```asc```, ```desc``` |
   - #### Examples
       -  ```https://nyaaapi.herokuapp.com/nyaa/anime?query={search_query}```
       -  ```https://nyaaapi.herokuapp.com/nyaa/anime?query={search_query}&sub_category{sub_category}```
       -  ```https://nyaaapi.herokuapp.com/nyaa/manga?query={search_query}&sub_category{sub_category}```
       -  ```https://nyaaapi.herokuapp.com/nyaa/anime?sub_category={sub_category}&query={search_query}&sort={sorting_parameter}```
       -  ```https://nyaaapi.herokuapp.com/nyaa/anime?sub_category={sub_category}&query={search_query}&sort={sorting_parameter}&order={order}```

- ### Sukebei Search
   - #### Available Endpoints
       **Every endpoint takes two arguments.**
       | **Arguments** | **Description** |
       |------|------|
       | ```query``` **(Required)** | Search query. |
       | ```sub_category``` **(Optional)** | Sub category of the torrents. |
       | ```sort``` **(Optional)** | Sorting parameter |
       | ```order``` **(Optional)** | Order of sorting. Defaults to ***Descending order***. |
       
       - **Endpoints:**
           | **Category** | **Endpoint** |
           |---------|---------|
           | Art | ```/sukebei/art``` |
           | Real | ```/sukebei/real``` |
       
       - **Sub-Categories:**
           | **Category** | **Sub-Category** |
           |------|------|
           | Art | ```anime```, ```doujinshi```, ```games```, ```manga```, ```pictures``` |
           | Real | ```photos```, ```videos``` |
           
       - **Sorting:**
           | **Arguments** | **Methods**  |
           | ---- | ---- |
           | Sort | ```size```, ```seeders```, ```leechers```, ```date```, ```downloads``` |
           | Order | ```asc```, ```desc``` |
           
   - #### Examples
       -  ```https://nyaaapi.herokuapp.com/sukebei/art?query={search_query}```
       -  ```https://nyaaapi.herokuapp.com/sukebei/art?query={search_query}&sub_category{sub_category}```
       -  ```https://nyaaapi.herokuapp.com/sukebei/real?query={search_query}&sub_category{sub_category}```
       -  ```https://nyaaapi.herokuapp.com/sukebei/art?sub_category={sub_category}&query={search_query}&sort={sorting_parameter}&order={order}```
       -  ```https://nyaaapi.herokuapp.com/sukebei/art?sub_category={sub_category}&query={search_query}&sort={sorting_parameter}```

 - ### Search Using ID
    - #### Available Endpoints
      - #### Nyaa ID
        **Endpoint:** ```/nyaa/id/<id>```\
        **Example:** ```https://nyaaapi.herokuapp.com/nyaa/id/{id}```

      - #### Sukebei ID
        **Endpoint:** ```/sukebei/id/<id>```\
        **Example:** ```https://nyaaapi.herokuapp.com/sukebei/id/{id}```

 - ### Torrents Uploaded by an User
    - #### Available Endpoints
        **Endpoint takes one argument.**
        | **Arguments** | **Description** |
        |------|------|
        | ```user``` **(Required)** | Username. |
        | ```sort``` **(Optional)** | Sorting parameter |
        | ```order``` **(Optional)** | Order of sorting. Defaults to ***Descending order***. |
        
       - **Sorting:**
           | **Arguments** | **Methods**  |
           | ---- | ---- |
           | Sort | ```size```, ```seeders```, ```leechers```, ```date```, ```downloads``` |
           | Order | ```asc```, ```desc``` |
           
       - **Nyaa User:**
         **Endpoint:** ```/nyaa/user```\
         **Examples:** \
                       ```https://nyaaapi.herokuapp.com/nyaa/user?user={user_name}``` \
                       ```https://nyaaapi.herokuapp.com/nyaa/user?user={user_name}&sort={sorting_parameter}```\
                       ```https://nyaaapi.herokuapp.com/nyaa/user?user={user_name}&sort={sorting_parameter}&order={order}```
       
       - **Sukebei User:**
         **Endpoint:** ```/sukebei/user```\
         **Examples:** \
                       ```https://nyaaapi.herokuapp.com/sukebei/user?user={user_name}``` \
                       ```https://nyaaapi.herokuapp.com/sukebei/user?user={user_name}&sort={sorting_parameter}```\
                       ```https://nyaaapi.herokuapp.com/sukebei/user?user={user_name}&sort={sorting_parameter}&order={order}```

## Disclaimer
**I do not host any of the torrents fetched by the API. The API is just meant to scrape the website and return the results. I do not promote piracy, if you guys can afford legal methods, then use them and support the industry :).\
Use it at your own risk, LOL!**

## ⭐ Made using Nyaa-API
  - [Nyaa-Telegram-Bot](https://t.me/meow_in_japanese_bot): Browse Sukebei and Nyaa torrents right inside Telegram. [GitHub](https://github.com/Vivek-Kolhe/Nyaa-Telegram-Bot).
  - [nyaamal](https://github.com/laxyapahuja/nyaamal): Chrome extension to download torrents directly from MyAnimeList and Anilist.
