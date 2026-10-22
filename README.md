# Masakan Kekinian (msknkkn)

A recipe discovery website powered by the Spoonacular API: search recipes by keyword, browse by type of meal, and open full recipe details with ingredients and cooking steps.

**Live:** https://msknkkn.xsrazy.web.id

> This is a documentation (showcase) repository. The application source code is private and lives in a separate repository.

## About

Masakan Kekinian ("Trending Recipes") is a recipe discovery website aimed primarily at Indonesian users looking for everyday cooking ideas as well as dishes for special occasions. There is no account and no cost: open the site, search or pick a type of meal, and the recipe appears. All recipe data, images, and scores come live from the Spoonacular API, fetched fresh when a page opens. The interface is in English, and recipe content is displayed exactly as provided by the Spoonacular catalog.

## Features

- Recipe search by keyword from the homepage hero and from the search box on the Recipes page, with results fetched live from the Spoonacular API
- Browse by type of meal with 15 filters: Main Course, Side Dish, Dessert, Appetizer, Salad, Bread, Breakfast, Soup, Beverage, Sauce, Marinade, Fingerfood, Snack, Drink, and All
- A "Find Your Type of Meal" picker on the homepage for the most common meal types
- A "Popular Food Recipe" section on the homepage with paginated recipe cards (8 per page, with Prev and Next)
- Recipe detail pages with a large photo, a summary with nutrition highlights and the Spoonacular score, a full ingredients list, cooking time, servings, and step-by-step cooking instructions

## Architecture

- **Frontend:** a single-page application built with React 18 and Create React App, styled with Tailwind CSS. React Router 6 handles the routes: Home (`/`), Recipes and search (`/search/...`), recipe detail (`/recipe/:id`), and About (`/about`).
- **Data fetching:** React Query 3 hooks call the Spoonacular API directly from the visitor's browser: `/recipes/search` for popular recipes, `/recipes/complexSearch` for search and meal-type browsing, and `/recipes/{id}/information` for recipe details.
- **Backend:** none. There is no server, database, or user account system; the visitor's browser talks to the Spoonacular API directly.
- **Hosting and deploy:** Vercel, deployed from the private source repository to the domain msknkkn.xsrazy.web.id.

## Notes

- Recipes are never stored on this site; every page load, search, and detail view is served live from the Spoonacular catalog
- The name "msknkkn" is a casual abbreviation of "Masakan Kekinian"
- Known issues on the live site (verified 23 October 2026): the About page (`/about`) currently renders as a blank page, and the sidebar on the Recipes page still shows the site's earlier name, "Recipefy"

## Credits

- Recipe data, images, and scores: [Spoonacular API](https://spoonacular.com/food-api)

## License

MIT License. See [LICENSE](LICENSE) for details.
