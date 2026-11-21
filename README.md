# Dagania food orders - Make blueprint

Make scenario that receives a meal order from a webhook, checks it, and stores it in a Data store.

## Flow
1. **Custom webhook** - receives an order: `date`, `person`, `meat`, `veg`, `side1`, `side2`, `salad1`, `salad2`.
2. **Router** - checks whether the order is valid (name, date, and at least one main dish).
3. Valid order: **Data store - Add/replace a record** (key `date_person`, so a repeated order replaces the old one), then **Webhook response** 200.
4. Invalid order: **Webhook response** 400 with an error message.

## Import
Make > Create a new scenario > ... > Import Blueprint > choose `הזמנות אוכל דגניה.blueprint.json` (exported from Make).
After import, create a new webhook and a Data store (with the fields above) and select them in the modules.

---

# הזמנות אוכל דגניה - Blueprint של Make

תהליך ב-Make שמקבל הזמנת ארוחה ב-Webhook, בודק אותה ושומר ב-Data store.
