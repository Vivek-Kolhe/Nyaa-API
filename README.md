# Nyaa-API
Nyaa API is an **Unofficial Nyaa.si API**. It just scrapes the website to satisfy the need for an API.\
And I'm sorry I've decided to keep the API closed source. I might make it open source in the near future. \
***Note:*** This API doesn't make authenticated requests to Nyaa, so you cannot make changes to your account or upload anything.

## Update
 - Added Sukebei search ***(NSFW content!)***.
 - Covers complete Nyaa and Sukebei.

## Usage
***Note:*** The API is hosted at **heroku** so it might be slow to respond. The API will fetch only recently uploaded 750 torrents, if the number of torrents are larger.

**The API is available at:** ```https://nyaaapi.herokuapp.com/```\

 - ### Nyaa Search
   - #### Available Endpoints
       **Every endpoint takes two arguments.**
       | **Arguments** | **Description** |
       |------|------|
       | ```query``` **(Required)** | Search query. |
       | ```sub_category``` **(Optional)** | Sub category of the torrents. |
       
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
     
   - #### Examples
       -  ```https://nyaaapi.herokuapp.com/nyaa/anime?query={search_query}```
       -  ```https://nyaaapi.herokuapp.com/nyaa/anime?query={search_query}&sub_category{sub_category}```
       -  ```https://nyaaapi.herokuapp.com/nyaa/manga?query={search_query}&sub_category{sub_category}```

- ### Sukebei Search
   - #### Available Endpoints
       **Every endpoint takes two arguments.**
       | **Arguments** | **Description** |
       |------|------|
       | ```query``` **(Required)** | Search query. |
       | ```sub_category``` **(Optional)** | Sub category of the torrents. |
       
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
     
   - #### Examples
       -  ```https://nyaaapi.herokuapp.com/sukebei/art?query={search_query}```
       -  ```https://nyaaapi.herokuapp.com/sukebei/art?query={search_query}&sub_category{sub_category}```
       -  ```https://nyaaapi.herokuapp.com/sukebei/real?query={search_query}&sub_category{sub_category}```

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
        
       - **Nyaa User:**
         **Endpoint:** ```/nyaa/user```\
         **Example:** ```https://nyaaapi.herokuapp.com/nyaa/user?user={user_name}```
       
       - **Sukebei User:**
         **Endpoint:** ```/sukebei/user```\
         **Example:** ```https://nyaaapi.herokuapp.com/sukebei/user?user={user_name}```

## Disclaimer
**I do not host any of the torrents fetched by the API. The API is just meant to scrape the website and return the results. I do not promote piracy, if you guys can afford legal methods, then use them and support the industry :).\
Use it at your own risk, LOL!**
