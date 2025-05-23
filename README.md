# bigfive-web

This repository contains the source code for [bigfive-test.com](https://bigfive-test.com),
a web application for the Big Five personality test. The project is based on the
[IPIP-NEO-PI](https://github.com/kholia/IPIP-NEO-PI) question set and makes use of
several reusable packages located in the `packages` directory.

## Contents

- **packages/** – TypeScript packages shared across the project
  - `questions` – exposes test items and their translations
  - `score` – functions to calculate scores from answers
  - `results` – generates textual feedback based on scores
- **web/** – Next.js frontend used on bigfive-test.com
- **old-packages/** – previous package versions kept for reference

Each package has its own README with more detailed documentation.

## Deploying

The website lives in the `web` folder. If you are starting from a completely
clean system without Node.js or yarn installed, these are the basic steps to get
the project running locally:

1. Install [Node.js](https://nodejs.org/) (the LTS version is recommended).
   This will also install `npm`, which is used to install yarn.
2. Install yarn globally with `npm install --global yarn`.
3. Clone this repository and change into the project directory.
4. `cd web` and run `yarn install` to install all dependencies. This will
   download Next.js, React and all other packages needed by the frontend.
5. Create a `.env.local` file (see `web/README.md` for the variables).
6. If you want to store results locally, start MongoDB with `docker-compose up -d`.
7. For development run `yarn dev`. If you see a `next: command not found`
   error, run `yarn install` again in the `web` directory to ensure that all
   dependencies are installed. For production build and start with:
   ```
   yarn build
   yarn start
   ```

## Help wanted

If you want to help by translating the items to other languages look
[here](https://b5.translations.alheimsins.net/).

## License

[MIT](LICENSE)
