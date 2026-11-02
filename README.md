# Closet — Digital Wardrobe

Closet is a lightweight, installable web app. It stores clothing photos and wardrobe details in the browser on your device using IndexedDB. It does not need an account or send wardrobe data to a server.

## Run it

Serve this folder from `localhost` or an HTTPS host. For example, with Python installed, open a terminal in this folder and run:

```sh
python -m http.server 8000
```

Open `http://localhost:8000` in a supported browser. Use the browser's **Install app** action or **Add to Home Screen** on mobile. The app shell is cached for offline use after its first load. (Opening `index.html` directly as a file does not enable PWA installation.)

## Use it

- Add one or more clothing photos. Category is guessed from the filename, then the image's shape is used as a fallback. You can edit the category before saving.
- The color guess is based on average image color; choose a color manually if the photo background affects it.
- “Clean up the background” removes connected pixels close to the photo's corner colors. It works best with a plain, evenly lit background. This is a local, lightweight cleanup and may leave halos or remove clothing that has a similar color to the background; it is not a full AI segmentation service.
- Outfit suggestions combine available categories for the selected occasion. Add an occasion to a piece to prioritize it for that event.

Clearing this browser's site data will remove the saved wardrobe. Export/backup is not included yet.
