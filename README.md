<h1 align="center"> Nyaa API </h1>

<p align="center">
<a href="https://nyaaapi.onrender.com/docs"><img src="https://img.shields.io/website?url=https%3A%2F%2Fnyaaapi.onrender.com%2Fdocs&style=for-the-badge&label=Status&labelColor=%23555555" title="status"></a>
<a href="https://github.com/Vivek-Kolhe"><img src="https://img.shields.io/github/followers/Vivek-Kolhe?style=for-the-badge&labelColor=%23555555&color=%23263759" title="gh followers"></a>
<a href="https://github.com/Vivek-Kolhe/Nyaa-API/stargazers"><img src="https://img.shields.io/github/stars/Vivek-Kolhe/Nyaa-API?style=for-the-badge&labelColor=%23555555&color=%23263759" title="repo stars"></a>
<a href="https://telegram.dog/ded_sadge"><img src="https://img.shields.io/badge/ded__sadge-smthing?style=for-the-badge&logo=telegram&labelColor=%23555555&color=%23263759" title="repo stars"></a>
</p>

<p align="center">
Nyaa API is an Unofficial Nyaa.si API. It just scrapes the website to satisfy the need for an API.
<br>
The API is closed source for now. I might make it open source in the near future. <a href="https://nyaaapi.onrender.com/docs"> Documentation. </a>
</p>

## Usage
**The API is available at:** `https://nyaaapi.onrender.com/`

<details open>
<summary><span style="font-size: 15px; font-weight:bold"> Search </span></summary>
<p>

- **Nyaa Endpoint:** `https://nyaaapi.onrender.com/nyaa`
- **Sukebei Endpoint:** `https://nyaaapi.onrender.com/sukebei`

</p>
<details closed>
<summary><span style="font-size: 12px; font-weight: bold"> Examples </span></summary>
<p>

- `https://nyaaapi.onrender.com/nyaa?q={query}&category={torrent_category}`
- `https://nyaaapi.onrender.com/sukebei?q={query}&category={torrent_category}`

</p>
</details>

**Note:** These endpoints also take optional query parameters. For more info, [visit here](https://nyaaapi.onrender.com/docs#/Search).

</details>

<details open>
<summary><span style="font-size: 15px; font-weight:bold"> User search </span></summary>
<p>

- **Nyaa Endpoint:** `https://nyaaapi.onrender.com/nyaa/user/{user_name}`
- **Sukebei Endpoint:** `https://nyaaapi.onrender.com/sukebei/user/{user_name}`

</p>
<details closed>
<summary><span style="font-size: 12px; font-weight: bold"> Examples </span></summary>
<p>

- `https://nyaaapi.onrender.com/nyaa/user/{user_name}?q={query}&category={torrent_category}`
- `https://nyaaapi.onrender.com/sukebei/user/{user_name}?q={query}&category={torrent_category}`

</p>
</details>

**Note:** These endpoints also take optional query parameters. For more info, [visit here](https://nyaaapi.onrender.com/docs#/User%20search).

</details>

<details open>
<summary><span style="font-size: 15px; font-weight:bold"> Search using torrent ID </span></summary>
<p>

- **Nyaa Endpoint:** `https://nyaaapi.onrender.com/nyaa/id/{torrent_id}`
- **Sukebei Endpoint:** `https://nyaaapi.onrender.com/sukebei/id/{torrent_id}`

</p>
<details closed>
<summary><span style="font-size: 12px; font-weight: bold"> Examples </span></summary>
<p>

- `https://nyaaapi.onrender.com/nyaa/id/{torrent_id}`
- `https://nyaaapi.onrender.com/sukebei/id/{torrent_id}`

</p>
</details>

**Note:** For more info, [visit here](https://nyaaapi.onrender.com/docs#/ID%20Search).

</details>

## Allowed Param Values
- **Nyaa**
  
  | **Category**     | **Sub-Category**                        |
  | :--------------: | :-------------------------------------: |
  | `anime`          | `amv`, `eng`, `non-eng`, `raw`          |
  | `manga`          | `eng`, `non-eng`, `raw`                 |
  | `audio`          | `lossy`, `lossless`                     |
  | `pictures`       | `photos`, `graphics`                    |
  | `live_action`    | `promo`, `eng`, `non-eng`, `raw`        |
  | `software`       | `application`, `games`                  |

- **Sukebei**

  | **Category** | **Sub-Category**                                   |
  |:------------:|:-------------------------------------------------: |
  | `art`        | `anime`, `doujinshi`, `games`, `manga`, `pictures` |
  | `real`       | `photos`, `videos`                                 |

- **Sorting**

  `sort`: `id`, `leechers`, `seeders`, `size`, `downloads`

- **Ordering**

  `order`: `asc`, `desc`

**Note:** `sort` and `order` params are common for both endpoints.

## Disclaimer
**I do not host any of the torrents fetched by the API. The API is just meant to scrape the website and return the results. I do not promote piracy, if you guys can afford legal methods, then use them and support the industry :).\
Use it at your own risk!**
