# U.S. Sports Industry — website

Live site: **https://ussportsindustry.com**

The whole website is one file, **`index.html`**, plus the images in the **`assets`** folder.
Every change saved here on GitHub goes live on the website automatically in about 30–60 seconds.

---

## How to make a change (no software needed)

1. Open the file you want to change here on GitHub (usually `index.html`).
2. Click the **✏️ pencil** icon (top right of the file).
3. Make your change. Tip: press **Ctrl + F** (or ⌘ + F on Mac) to find the text you're looking for.
4. Click the green **Commit changes…** button, then **Commit changes** again.
5. Wait about a minute and refresh **ussportsindustry.com**.

Made a mistake? Open the file's **History**, find the last good version, and copy it back — or just ask for help.

---

## Common changes in `index.html`

Search (Ctrl + F) for the words in **bold** to jump straight to the right place.

### Change the prices
Search for **`const CATEGORIES`**. Each line has a `price:` — just change the number (US dollars, per kit):

```js
{ id:"soccer",     name:"Soccer Kits",   cover:"k01", price:24 },
{ id:"jerseys",    name:"Jerseys",       cover:"k05", price:16 },
{ id:"basketball", name:"Basketball",    cover:"k18", price:23 },
{ id:"women",      name:"Women's Kits",  cover:"k08", price:23 },
```

The new prices update everywhere automatically (cards, pop-up, order list and the WhatsApp message).
The headline text near the top also mentions "from $24 / from $16" — search **`Soccer kits from`** to update it, and **`Soccer kits $24`** for the free-shipping panel.

### Add, remove or rename a design
Search for **`const TEMPLATES`**. Each design is one line:

```js
{ img:"k01", name:"Classic Stripes Kit", cat:"soccer", desc:"Red & white striped shirt with navy shorts." },
```

- `img` — the photo file name in `assets/kits` (without `.jpg`)
- `name` — the design name shown on the site
- `cat` — which category it belongs to: `soccer`, `jerseys`, `basketball` or `women`
- `desc` — a short description shown in the pop-up

To **add** a design: upload the photo (see below), then copy any line, paste it underneath and change the values.
To **remove** one: delete its whole line.

### Add a new photo
1. Go to the **`assets/kits`** folder here on GitHub.
2. Click **Add file → Upload files**, drag the photo in, and click **Commit changes**.
3. Use a simple name like `k22.jpg` and use that name (`k22`) in `const TEMPLATES`.

Photos look best as **.jpg**, roughly square, on a **white background**, around 1000–1100 px wide.

### Change the WhatsApp number
Search for **`const WHATSAPP`**. Use the full number with country code, **digits only** (no +, spaces or dashes):

```js
const WHATSAPP = "14069643039";
```

### Change the numbers in the stats strip (225+, 9,000+, 12+, 4.9★)
Search for **`data-count=`** and change the numbers inside the quotes.

### Change the email, Instagram or Facebook links
Search for **`mailto:`**, **`instagram.com`** or **`facebook.com`**.

### Other things you can edit the same way
- Sizes in the pop-up: search **`const SIZES`**
- Extra sports listed on the "Any sport" card: search **`const OTHER_SPORTS`**
- The production steps: search **`const PROCESS`**
- Any other text: search for a few words of it and edit them directly

---

## Good to know
- Keep the quotes `" "`, commas `,` and brackets exactly as they are — only change the words and numbers between them.
- If the site looks broken after a change, the last edit probably removed a quote or comma. Undo it from the file's **History**.
- The domain (ussportsindustry.com) is registered at Namecheap; hosting is on Vercel. You don't need to touch either to edit the site.
