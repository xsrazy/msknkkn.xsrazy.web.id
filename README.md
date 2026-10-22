# Masakan Kekinian (msknkkn)

A recipe discovery website: search recipes by keyword, browse by type of meal, and open full recipe details with ingredients and cooking steps. All recipe data comes live from the Spoonacular API.

Live: https://msknkkn.xsrazy.web.id

> This is a documentation (showcase) repository. The application source code is private and lives in a separate repository.

## About

Masakan Kekinian ("Trending Recipes") is a lightweight recipe finder aimed primarily at Indonesian users looking for everyday cooking ideas. There is no account and no cost: open the site, search or pick a type of meal, and the recipe appears. Recipe content is displayed in English, exactly as provided by the Spoonacular catalog.

## Features

- Recipe search by keyword, with results fetched live from the Spoonacular API
- Browse by type of meal: appetizer, beverage, bread, breakfast, brunch, dessert, dinner, drink, salad, sauce, snack, and soup, each with its own category icon
- Popular Food Recipe list on the homepage for instant inspiration
- Full recipe details with ingredients and cooking steps
- Consistent recipe cards showing the dish image and name across all lists
- Loading indicators while recipe data is fetched

## Architecture

- Frontend: single-page application built with React 18 and Create React App, routed with React Router DOM 6
- Data fetching and caching: React Query 3, with separate hooks for popular dishes, recipe details, and search
- Styling: Tailwind CSS plus per-component CSS
- Backend: none. The visitor's browser calls the Spoonacular API directly; there is no server, database, or user account system
- Hosting: Vercel, deployed from the private source repository to the domain msknkkn.xsrazy.web.id

## Notes

- Recipes are never stored on this site; every page load, search, and detail view is served live from the Spoonacular catalog
- The name "msknkkn" is a casual abbreviation of "Masakan Kekinian"

## License

MIT. See [LICENSE](LICENSE).
