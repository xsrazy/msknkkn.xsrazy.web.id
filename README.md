# Masakan Kekinian (msknkkn)

**Live: https://msknkkn.xsrazy.web.id**

Masakan Kekinian ("Trending Recipes") is a recipe discovery website. Visitors can search for recipes by keyword, browse recipes by type of meal, see a list of popular dishes, and open full recipe details with ingredients and cooking steps. All recipe data comes from the Spoonacular API and is displayed in English as provided by the source, while the site itself is aimed primarily at Indonesian users looking for cooking ideas.

> This is a documentation (showcase) repository. The application's source code is private and is not included here.

## Why This Website Was Made

Finding cooking ideas is a common everyday problem: the ingredients are in the kitchen, but the ideas run out. Existing recipe websites are often heavy, full of ads, or require signing up before a recipe can be read in full. Masakan Kekinian was made as a lightweight alternative that works right away: open the site, search or pick a type of meal, and the recipe appears, with no account and no cost.

The website is also a practice project for building a modern React web app that pulls data directly from a public API, all the way through deployment on its own domain.

## Purpose

- Help Indonesian users quickly find ideas for everyday meals as well as dishes for special occasions.
- Provide simple recipe search: just a keyword or a type of meal, no registration needed.
- Show popular recipes as instant inspiration for visitors who do not yet know what to cook.
- Be part of a personal web portfolio that is managed and deployed independently.

## Features

- **Homepage** with a hero reading "Your Best Cooking Companion", a meal type picker "Find Your Type of Meal", and a "Popular Food Recipe" list.
- **Recipe search** by keyword, with results fetched live from the Spoonacular API.
- **Browsing by type of meal**, such as appetizer, beverage, bread, breakfast, brunch, dessert, dinner, drink, salad, sauce, snack, and soup, each with its own category icon.
- **Popular dishes**: a list of trending recipes shown automatically on the homepage as inspiration.
- **Recipe details**: ingredients and cooking steps for every selected recipe.
- **Recipe cards (FoodCard)** used consistently across all lists, showing the dish image and name.
- **Navbar and sidebar** for navigating between pages, plus a footer closing the page.
- **Loading indicators** while recipe data is fetched from the API, so visitors know the page is working.

## Frontend

- Built as a single-page application (SPA) with **React 18** and **Create React App** (react-scripts 5).
- Page routing uses **React Router DOM 6**; API data fetching and caching is handled by **React Query 3**.
- Styling uses **Tailwind CSS** plus per-component CSS.
- The main components live in `src/components/`: NavBar, HeroSection, MealType, PopularFoods, FoodCard, SideBar, and Footer.
- Data fetching logic is separated into `src/hooks/`: `useFetchPopularFood` for popular dishes, `useFetchRecipe` for recipe details, and `useSearch` for search.

## Backend / How It Works

- The application has no backend of its own: no server, no serverless functions, no database, and no user account system.
- The visitor's browser calls the **Spoonacular API** directly from the client side whenever a page is opened, a search is run, or a recipe detail is requested. Recipe data, food images, and search results are all provided by that external API at that moment.
- Because the data is live from the API, the recipe collection shown always follows the Spoonacular catalog and is not stored locally on this site.
- The site is deployed on **Vercel**; every change to the source code that lands on the main branch is deployed straight to production and is accessible through the domain msknkkn.xsrazy.web.id.

## Notes

- This repository contains documentation only. The Masakan Kekinian source code is kept in a separate private repository.
- The name "msknkkn" is a casual abbreviation of "Masakan Kekinian".

## 🌐 Socials
[![Behance](https://img.shields.io/badge/Behance-1769ff?logo=behance&logoColor=white)](https://behance.net/xsrazy) [![Discord](https://img.shields.io/badge/Discord-%237289DA.svg?logo=discord&logoColor=white)](https://discord.gg/xsrazy) [![Facebook](https://img.shields.io/badge/Facebook-%231877F2.svg?logo=Facebook&logoColor=white)](https://facebook.com/xsrazy) [![Instagram](https://img.shields.io/badge/Instagram-%23E4405F.svg?logo=Instagram&logoColor=white)](https://instagram.com/xsrazy) [![LinkedIn](https://img.shields.io/badge/LinkedIn-%230077B5.svg?logo=linkedin&logoColor=white)](https://linkedin.com/in/xsrazy) [![Medium](https://img.shields.io/badge/Medium-12100E?logo=medium&logoColor=white)](https://medium.com/@xsrazy) [![Pinterest](https://img.shields.io/badge/Pinterest-%23E60023.svg?logo=Pinterest&logoColor=white)](https://pinterest.com/xsrazy) [![Quora](https://img.shields.io/badge/Quora-%23B92B27.svg?logo=Quora&logoColor=white)](https://quora.com/profile/xsrazy) [![Reddit](https://img.shields.io/badge/Reddit-%23FF4500.svg?logo=Reddit&logoColor=white)](https://reddit.com/user/xsrazy) [![Stack Overflow](https://img.shields.io/badge/-Stackoverflow-FE7A16?logo=stack-overflow&logoColor=white)](https://stackoverflow.com/users/31065073) [![Twitch](https://img.shields.io/badge/Twitch-%239146FF.svg?logo=Twitch&logoColor=white)](https://twitch.tv/xsrazy) [![Twitter](https://img.shields.io/badge/Twitter-%231DA1F2.svg?logo=Twitter&logoColor=white)](https://twitter.com/xsrazy) [![YouTube](https://img.shields.io/badge/YouTube-%23FF0000.svg?logo=YouTube&logoColor=white)](https://youtube.com/c/xsrazy)

## 💰 You can help me by Donating
[![BuyMeACoffee](https://img.shields.io/badge/Buy%20Me%20a%20Coffee-ffdd00?style=plastic&logo=buy-me-a-coffee&logoColor=black)](https://buymeacoffee.com/xsrazy) [![PayPal](https://img.shields.io/badge/PayPal-00457C?style=plastic&logo=paypal&logoColor=white)](https://paypal.me/xsrazy) [![Patreon](https://img.shields.io/badge/Patreon-F96854?style=plastic&logo=patreon&logoColor=white)](https://patreon.com/Xsrazy) [![Ko-Fi](https://img.shields.io/badge/Ko--fi-F16061?style=plastic&logo=ko-fi&logoColor=white)](https://ko-fi.com/xsrazy)
