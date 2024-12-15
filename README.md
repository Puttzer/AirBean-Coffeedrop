
# AirBean

AirBean is a Vue.js application designed to deliver a coffee experience out of this world!

## Features
- **Order System:** Add products to your cart and view your orders.
- **Responsive Design:** Optimized for different screen sizes.
- **Modern UI:** Built with Vue.js and SCSS for a smooth user experience.

---

## Project Setup

Follow these steps to get the project up and running locally:

1. Clone the repository:
   ```bash
   git clone https://github.com/<username>/AirBean.git
   ```
   Replace `<username>` with the owner of this repository.

2. Navigate to the project directory:
   ```bash
   cd AirBean
   ```

3. Install dependencies:
   ```bash
   npm install
   ```

---

## Development

### Compiles and Hot-Reloads for Development
To start a development server with hot-reloading enabled, run:
```bash
npm run serve
```

By default, the development server will be accessible at:
```
http://localhost:8080/
```

---

## API Setup

This project includes an API for managing data. Follow these steps to set up and run the API locally:

NOTE: BEFORE DOING THIS OPEN A DIFFERENT WINDOW SO THAT YOU DONT KILL THE VUE PROJECT :)

1. Navigate to the `api/` directory within the project:
   ```bash
   cd api
   ```

2. Install the required dependencies for the API:
   ```bash
   npm install
   ```

3. Start the API server:
   ```bash
   npm start
   ```

The API server will run on `http://localhost:3000/` by default.

Ensure the Vue.js app is configured to communicate with this API. Update API base URLs in the Vue app as needed.

---

## Production

### Compiles and Minifies for Production
To build the project for production, use:
```bash
npm run build
```

The compiled files will be placed in the `dist/` directory. You can deploy this directory to a static hosting service (e.g., GitHub Pages, Netlify, or Vercel).

---

## Linting

### Lints and Fixes Files
To check and fix code linting issues, run:
```bash
npm run lint
```

---

## Deployment

To deploy the app to GitHub Pages:
1. Generate a production build:
   ```bash
   npm run build
   ```
2. Deploy the contents of the `dist/` folder to the `gh-pages` branch using a deployment tool like `gh-pages`.

---

## Customize Configuration

To customize the Vue CLI configuration, see the official [Vue CLI Configuration Reference](https://cli.vuejs.org/config/).

---

## Contributing
Contributions are welcome! Please fork the repository and submit a pull request.

---

## License
This project is licensed under the [MIT License](LICENSE).
