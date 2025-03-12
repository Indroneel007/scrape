# Web Scraping Application

A Next.js application that allows users to scrape content from multiple websites simultaneously using Puppeteer.

## Features

- Scrape multiple URLs in parallel using Promise.all()
- Dynamic URL input fields - add or remove as many URLs as needed
- Clean and modern UI built with Tailwind CSS
- Real-time feedback on scraping progress
- Display of scraped content including page titles and text content
- Support for Browserless.io cloud browser service

## Technologies Used

- Next.js 14 with App Router
- TypeScript
- Puppeteer for web scraping
- Tailwind CSS for styling
- Browserless.io integration (optional)

## Getting Started

### Prerequisites

- Node.js 18.17 or later
- npm or yarn

### Installation

1. Clone the repository:

```bash
git clone <repository-url>
cd scraping-app
```

2. Install dependencies:

```bash
npm install
# or
yarn install
```

3. Run the development server:

```bash
npm run dev
# or
yarn dev
```

4. Open [http://localhost:3000](http://localhost:3000) in your browser to see the application.

## Usage

1. Enter one or more URLs in the input fields
2. Click "Add Another URL" to add more URL input fields
3. Click "Start Scraping" to begin the scraping process
4. View the results displayed below the form

## Deployment

This application can be deployed to Vercel or any other hosting platform that supports Next.js applications.

```bash
npm run build
# or
yarn build
```

## Notes

- The application uses Puppeteer in a serverless environment, which may have limitations depending on the hosting provider.
- For production use, consider using a dedicated browser service like Browserless.io or similar.

### Environment Variables

Create a `.env.local` file in the root of your project with the following variables:

```
# Browserless API key
# Get your API key from https://browserless.io
BROWSERLESS_API_KEY=your-browserless-api-key
```

Replace `your-browserless-api-key` with your actual API key from Browserless.io.

### Using Browserless

The application is configured to use Browserless.io if an API key is provided in the environment variables. If no API key is provided, it will fall back to using a local Puppeteer browser instance.

To get a Browserless API key:

1. Sign up at [Browserless.io](https://browserless.io)
2. Navigate to your dashboard and copy your API key
3. Add it to your `.env.local` file as shown above

For production deployments, add the environment variable to your hosting platform (Vercel, Netlify, etc.).

## License

MIT
