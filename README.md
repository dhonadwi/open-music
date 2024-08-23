# Open Music API

This repository provides the backend for the Open Music API hosted at [https://open-music-zeta.vercel.app](https://open-music-zeta.vercel.app). This API offers functionality to manage songs, albums, and playlists.

## Base URL

All API requests are made to the following base URL:

https://open-music-zeta.vercel.app

## API Routes and Usage

### 1. Get All Songs
Retrieve all the songs in the database.

- **Method**: `GET`
- **Endpoint**: `/songs`
  
### 2. Get Song by ID
Retrieve a song by its unique ID.

- **Method**: `GET`
- **Endpoint**: `/songs/{id}`

### 3. Add new Song 
Add a new song to the collection.

- **Method**: `POST`
- **Endpoint**: `/songs`
- **Content-Type**: `application/json`

  Example Request Body:
  ```json
  {
  "title": "New Song Title",
  "year": 2023,
  "performer": "New Performer",
  "genre": "Rock",
  "duration": 210
  }

### 4. Update Song by ID 
Update the details of an existing song by its ID.

- **Method**: `PUT`
- **Endpoint**: `/songs`
- **Content-Type**: `application/json`

Example Request Body:
  ```json
  {
  "title": "Updated Song Title",
  "year": 2023,
  "performer": "Updated Performer",
  "genre": "Jazz",
  "duration": 180,
  "albumId": "albumId-123456789"
  }
```
### 5. Get All Albums 
Retrieve all the albums available.

- **Method**: `GET`
- **Endpoint**: `/albums`

### 6. Get Album by ID
Retrieve an album by its unique ID.

- **Method**: `GET`
- **Endpoint**: `/albums/{id}`

### 7. Add a New Album
Add a new album to the database.

- **Method**: `POST`
- **Endpoint**: `/albums`
- **Content-Type**: `application/json`

Example Request Body:
  ```json
{
  "name": "New Album Title",
  "year": 2023
}
```

### 8. Update Album by ID
Update an album's details using its ID.

- **Method**: `PUT`
- **Endpoint**: `/albums/{id}`
- **Content-Type**: `application/json`

Example Request Body:
  ```json
{
  "name": "Updated Album Title",
  "year": 2023
}
```

### 9. Add a Song to Album
Associate a song with a specific album.

- **Method**: `POST`
- **Endpoint**: `/albums/{albumId}/songs`
- **Content-Type**: `application/json`

Example Request Body:
  ```json
{
  "songId": "songId1"
}
```

## Technologies Used
- **Backend**: Node.js, Hapi.js
- **Database**: PostgreSQL

## License
This project is licensed under the MIT License.
