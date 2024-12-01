# Intro

Base react native app

# Prerequisites

- npm, nodejs, yarn
- Ref here to install eas-cli `https://docs.expo.dev/build/setup`:
  - `npm install -g eas-cli`
  - Run login
  - Copy file `.env.example` to `.env` file for local development

# How to start

- `yarn start`

# Environment variables management

- Follow docs `https://docs.expo.dev/build/setup`
- Naming should be started with prefix `EXPO_PUBLIC_`
- Accessing env var: `process.env.EXPO_PUBLIC_XXX`

# Run build application with expo cli environment variables

- Use expo for development environment
- Ref `https://docs.expo.dev/guides/environment-variables/#how-variables-are-loaded`
- Build environment file templates: `.env.*`
  - Example start with `.env` file as environment file: `yarn start`
  - Example start with `.env.example` file as environment file: `NODE_ENV=example yarn start`

# Run build application with EAS cli environment variables

- Use eas when need verify app builds
- Ref `https://docs.expo.dev/build/setup/#run-a-build`
- Build environment file: `.env`
- Build app for specific environment for ios: `https://docs.expo.dev/build-reference/simulators/`
  - Example build: `eas build -p ios --profile preview`
  - Install to simulator: `eas build:run -p ios`
  - Wait for build to finish (take around 15 minutes)
  - For CI environment vars, need to use `--environment` option with `eas update` command
