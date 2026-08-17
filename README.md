# Pastel Smart Grocery

Mobile-first static web app prototype based on the pastel dashboard design.

## Included
- Home action dashboard
- Shared shopping list
- Persistent state with localStorage
- Budget tab with manually editable min/max range
- Budget suggestions that preserve selected nutrient goals
- Nutrition goals with dynamic food suggestions
- Removing a nutrient removes that nutrient tag from recommendations; foods disappear when no selected nutrient still matches
- Meal search and custom recipe creation
- Add missing recipe ingredients directly to the shared shopping list
- Receipt-scan simulation
- Responsive mobile UI
- Installable web-app manifest

## Run locally
Open `index.html`, or preferably run:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.

## Production API architecture
Use a backend between the browser and external APIs:

```text
Browser UI
   ↓
Your backend API
   ├── retailer price adapters
   ├── nutrition adapter
   ├── recipe adapter
   ├── Maps adapter
   └── database/cache
```

Do not put retailer or Google API secrets directly in browser JavaScript.
