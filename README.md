# Internationalization in this Project

This project uses the `next-intl` package for internationalization (i18n).

## How it works

The `next-intl` package provides React hooks and components to format dates, numbers, and strings. It also supports message translation and pluralization.

## Configuration

The configuration for `next-intl` is in the [`i18n.ts`](i18n.ts) and [`middleware.ts`](middleware.ts) files.

In [`i18n.ts`](i18n.ts), we define the supported locales and import the corresponding message files from the `messages` directory.

In [`middleware.ts`](middleware.ts), we create a middleware using `next-intl` that sets the locale for each request.

## Usage

In the pages of the application (for example, [`app/[locale]/page.tsx`](app/[locale]/page.tsx)), we use the `useTranslations` hook from `next-intl` to get the translated messages.

## Adding a new locale

To add a new locale:

1. Add the locale to the `locales` array in [`i18n.ts`](i18n.ts) and [`middleware.ts`](middleware.ts).
2. Create a new JSON file in the `messages` directory with the translations for the new locale.

## Running the project

To run the project with internationalization, use the same commands as usual (`npm run dev`, `npm run build`, `npm run start`).

The locale is determined by the URL of the page. For example, to view the page in English, you would go to `http://localhost:3000/en/page`.
