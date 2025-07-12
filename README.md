# easy-places-sdk

**easy-places-sdk** is a lightweight Node.js SDK to query countries, states, and cities from a PostgreSQL database. Ideal for apps needing location-based data.

## ✨ Features
- 🗺 Get all countries
- 📍 Fetch states by country
- 🏙 Get cities by state
- 🔌 Powered by PostgreSQL
- 💡 Written in TypeScript

## 🚀 Installation
```bash
npm install easy-places-sdk
```

## 🔧 Usage
```ts
import { countries, states, cities } from 'easy-places-sdk';

const allCountries = await countries.getAllCountries();
const statesInIndia = await states.getStatesByCountry(101);
const citiesInMP = await cities.getCitiesByState(45);
```

## 📦 API
### `countries`
- `getAllCountries(): Promise<Country[]>`
- `getCountryByCode(code: string): Promise<Country | undefined>`

### `states`
- `getStatesByCountry(countryId: number): Promise<State[]>`

### `cities`
- `getCitiesByState(stateId: number): Promise<City[]>`

## 🛠 Environment
Create a `.env` file:
```env
DB_HOST=localhost
DB_USER=postgres
DB_NAME=easy_places
DB_PASS=password
DB_PORT=5432
```

## 📜 License
MIT © Ajay Kaithwas