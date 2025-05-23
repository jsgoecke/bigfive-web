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

The website lives in the `web` folder. To run it locally or deploy it,
follow these steps:

1. Install [Node.js](https://nodejs.org/) and [yarn](https://yarnpkg.com/).
2. `cd web` and run `yarn` to install dependencies.
3. Create a `.env.local` file (see `web/README.md` for the variables).
4. If you want to store results locally, start MongoDB with `docker-compose up -d`.
5. For development run `yarn dev`. For production build and start with:
   ```
   yarn build
   yarn start
   ```

## Help wanted

If you want to help by translating the items to other languages look
[here](https://b5.translations.alheimsins.net/).

## License

[MIT](LICENSE)
