# Express Backend Template

This is a template for building an Express backend with user routes and authentication integrated.

## Prerequisites

Before getting started, make sure you have the following installed on your machine:

- Node.js
- npm (Node Package Manager)

## Installation

1. Clone this repository to your local machine.
2. Navigate to the project directory in your terminal.
3. Run the following command to install the required dependencies:

    ```shell
    npm install
    ```

## Configuration

1. Create a `config.env` file in the config directory of the project.
2. Add the following environment variables to the `config.env` file:

    ```plaintext
    PORT=3000
    DB_URI=<your_database_connection_string>
    JWT_SECRET=<jwt_secret>
    JWT_EXPIRE=5d
    COOKIE_EXPIRE=5d
    SMPT_SERVICE =
    SMPT_MAIL=Enter_Email_address
    SMPT_PASSWORD=Enter_email_password
    SMPT_HOST=Enter_host_name
    SMPT_PORT=465
    ```

## Usage

1. Start the server by running the following command:

    ```shell
    npm start
    ```

2. The server will start running on `http://localhost:3000` (or the port specified in the `.env` file).

## API Endpoints

### User Routes

- `POST /api/user/register`: Register a new user.
- `POST /api/user/login`: Log in an existing user.
- `GET /api/user/profile`: Get the profile of the currently logged-in user.
- `PUT /api/user/profile`: Update the profile of the currently logged-in user.
- `DELETE /api/user/profile`: Delete the profile of the currently logged-in user.

### Authentication

- Authentication is handled using JSON Web Tokens (JWT).
- Include the JWT token in the `Authorization` header of each request as follows:

  ```plaintext
  Authorization: Bearer <your_jwt_token>
  ```

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please open an issue or submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).