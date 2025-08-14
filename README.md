# Movie Library Application

A modern movie search application built with React and Vite that allows users to discover and search for movies using The Movie Database (TMDB) API. The application tracks trending searches using Appwrite backend services.

## Features

- Search movies by title
- View trending movies based on search frequency
- Display movie details including ratings, release year, and language
- Responsive design using Tailwind CSS
- Real-time search with debouncing
- Loading indicators for API requests
- Error handling for failed requests

## Technology Stack

- **Frontend**: React 19, Vite
- **Styling**: Tailwind CSS
- **Backend**: Appwrite (for tracking trending searches)
- **API**: TMDB (The Movie Database) API
- **Utilities**: react-use (for debouncing)

## Prerequisites

Before you begin, ensure you have the following installed:
- Node.js (version 16 or higher)
- npm or yarn

## Setup Instructions

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd movie_libary
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env.local` file in the root directory with the following variables:
   ```env
   VITE_TMDB_API_KEY=your_tmdb_api_key_here
   VITE_APPWRITE_PROJECT_ID=your_appwrite_project_id
   VITE_APPWRITE_DATABASE_ID=your_appwrite_database_id
   VITE_APPWRITE_COLLECTION_ID=your_appwrite_collection_id
   ```

4. Start the development server:
   ```bash
   npm run dev
   ```

## Environment Variables

The application requires the following environment variables:

| Variable | Description |
|---------|-------------|
| `VITE_TMDB_API_KEY` | Your TMDB API key for accessing movie data |
| `VITE_APPWRITE_PROJECT_ID` | Your Appwrite project ID |
| `VITE_APPWRITE_DATABASE_ID` | Your Appwrite database ID |
| `VITE_APPWRITE_COLLECTION_ID` | Your Appwrite collection ID for tracking searches |

## API Integration

This application uses two main APIs:

1. **TMDB API**: Fetches movie data including titles, ratings, posters, and release dates
2. **Appwrite API**: Tracks search terms and displays trending movies based on search frequency

## Project Structure

```
src/
├── App.jsx              # Main application component
├── appwrite.js          # Appwrite service integration
├── components/
│   ├── MovieCard.jsx    # Component for displaying movie information
│   ├── Search.jsx       # Search input component
│   └── Spinner.jsx     # Loading spinner component
├── assets/             # Static assets
└── ...
```

## Available Scripts

- `npm run dev` - Starts the development server
- `npm run build` - Builds the application for production
- `npm run lint` - Runs ESLint on the project
- `npm run preview` - Previews the production build locally

## How It Works

1. Users can search for movies using the search bar
2. The application fetches movie data from TMDB API
3. Search terms are tracked in Appwrite database
4. Trending movies section displays the most searched movies
5. Each search increments a counter for that search term in Appwrite

## Contributing

1. Fork the repository
2. Create a new branch for your feature
3. Make your changes
4. Submit a pull request

## Learn More

- [React Documentation](https://reactjs.org/)
- [Vite Documentation](https://vitejs.dev/)
- [TMDB API Documentation](https://developers.themoviedb.org/)
- [Appwrite Documentation](https://appwrite.io/docs)
