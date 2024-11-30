# TSMS


Here is the link to get the demo 

https://kollege.onrender.com/

**Contact**: sahuashish940@gmail.com  
**Readme Created By**: Ashish sahu  


A College-Based Data Management System.

- There are two types of roles: Staff [Teacher, HOD] and Student.

## Login Details

PS: BE KIND :)

### Teacher [Staff]

**Username:** Delphine  
**Password:** Delphine123

Teacher can add or edit:

- Notes
- Attendance
- Internal Marks
- Time Schedule

### HOD (Head of Department) [Staff]

**Username:** Moriah  
**Password:** Moriah123

HOD can do everything a Teacher can do.  
Additionally, HOD can:

- Approve new Teachers
- Add New Paper

### Student

**Username:** Bret  
**Password:** Bret

Or register a new Student and log in.  
You can also log in with the first name of any student in the class.

Student can view:

- Notes
- Attendance
- Internal Marks

> Attendance and marks need to be added by the teacher first.  
> Students can also join or leave a paper (subject).

## Tech Stack

**Client:** React, TailwindCSS

**Server:** NodeJS, ExpressJS

**Database:** MongoDB, Mongoose

## Other Features

- Profile
- Dark Theme
- Mobile Responsive

## Setting Up

Change Directory:

```bash
  cd tsms
```

Install dependencies:

```bash
  npm install
```

Finally, start the server:

```bash
  npm start
```

To use your own server and database, modify the backend configuration in the frontend to match your setup.

## Roadmap

- Add admin functionality 😴
- Cache Queries
- Paginate Queries

## Contact

Errors are bound to happen, and the documentation is incomplete.  
We’d love to hear your feedback and suggestions.  

Developed by: Ashish, Aruna, Ayush.


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




