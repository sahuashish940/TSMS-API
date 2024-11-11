
--

# TSMS API
# Developed by: Ashish, Aruna, Ayush
# Contect : Ashish sahu


REST API for the TSMS (College-Based Data Management System)

## Setting Up

Clone the project:

```bash
  git clone https://github.com/yourusername/tsms_api.git
```

Change Directory:

```bash
  cd tsms_api
```

Install dependencies:

```bash
  npm install
```

Create a `.env` file and paste your MongoDB Database URI:

```javascript
  DATABASE_URI = mongodb+srv://username:password@.....mongodb.net/tsms
  // you can give a name of your preference to the database instead of "tsms"
```

Start the server (Node.js version 19+):

```bash
  npm run dev
```

### Allowing Requests without Headers During Development

Inside `config/corsOptions.js`, uncomment `|| !origin` during development to allow requests without specific origins.

```javascript
 if (
      allowedOrigins.indexOf(origin) !== -1
      //! comment out/remove in production
       || !origin
    )
```

### Adding HOD

Since an admin role hasn’t been added yet, the HOD manages most things.  
To add an HOD manually, use a REST API client like Postman or Thunder Client.

- **Request Method:** `POST`  
- **Request URL:** `http://localhost:3500/staff` (use the server port, default is `3500`)

Request Body:

```json
{
  "name": "...",
  "email": "...",
  "department": "Computer",
  "username": "...",
  "password": "...",
  "role": "HOD"
}
```

- **Note:** Replace **"..."** with the necessary details.

#### Important

After development, remember to comment out `|| !origin` in `config/corsOptions.js`:

```javascript
 if (
      allowedOrigins.indexOf(origin) !== -1
      //! comment out/remove in production
      // || !origin
    )
```

### Troubleshooting CORS Errors

If you’re getting CORS errors, ensure your front-end address is included in `allowedOrigins` within `config/corsOptions.js`:

```javascript
const allowedOrigins = [
  "http://localhost:3000",
  // Add the address if you host your front-end somewhere
  "https://example.address.com",
];
```

## Contact

Errors are bound to happen, and the documentation is incomplete.  
We’d love to hear your feedback and suggestions.

Developed by: Ashish, Aruna, Ayush

## Acknowledgements

- Node.js Tutorial by Dave Gray

## License
