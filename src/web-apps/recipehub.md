# RecipeHub

**The gist**: GitHub for recipes! But for food, not software.

I love cooking and baking. It's seriously so fun and creative. I love taking recipes and adjusting and tweaking them to my liking. The neat thing about recipes is that they're not observed by copyright! The photos, the descriptions, etc. are, but the actual ingredients and steps aren't. That always gets me thinking about how awesome it would be if there was a web application for people to share their recipes on. It would be centered around loading quickly, browsing by tags, collecting your favorites, and copying and modifying others' recipes.

I'm hungry and excited just writing this!

## Mock-Ups

There are a lot of features that could exist for this app, and mocking them all up would be a lot, but here's a gist of what some of the key elements of the UI could be like (viewing your recipes, viewing a recipe, and the recipe form):

![RecipeHub mobile mock-ups. First view: site title/logo, "Your Recipe Box" heading with "Add Recipe" button horizontally aligned and a two-column grid of recipes with a placeholder image and title each. Second view: placeholder image, recipe title and author with horizontally-aligned like/save and fork buttons, followed by the body of the recipe (description, tags, ingredients and instructions). Third view: "Add Recipe" heading followed by inputs for name, description, tags, photo, ingredients and instructions](./img/recipehub.webp)


## Specs

- User accounts (authentication)
- Recipe management
    - Data model for a recipe:
        - Name
        - Description
        - Ingredients
        - Instructions
- Viewing another user's recipes
- Fork a recipe (make a copy to edit and adjust to your liking, but maintain an association to the original)

## Concepts

- Authentication
- Permissions
- Data management
- Network graph

## Extra Credit

- Add ability to favorite another user's recipes & view your favorites
- More metadata like prep time and cooking time (and thus total time)
- Image upload for a recipe
- Tags for things like vegan, breakfast, etc. where you can discover similar recipes
- If you build the back-end with an API, you could then build out a mobile app that consumes it! That would be pretty handy when cooking in the kitchen
    - Dream feature: when viewing a recipe on the mobile app, prevent the phone from sleeping
