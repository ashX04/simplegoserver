# Go Web Server with Form Handling

This is a simple Go-based web server that serves static files and handles form submissions. It allows users to submit their name and address via an HTML form and responds with a personalized greeting.

## Features

- Serves static files (HTML, CSS, JS) from the `static/` directory.
- Provides a simple form for users to submit data.
- Handles form submissions and displays the input back to the user.
- Implements basic routing for different endpoints.

## Project Structure

```
project-folder/
│── main.go
│── static/
│   │── index.html
│   │── form.html
```

## Getting Started

### Prerequisites

- Install [Go](https://go.dev/dl/)

### Running the Server

1. Clone this repository:
   ```sh
   git clone https://github.com/ashX04/simplegoserver.git
   cd simplegoserver
   ```
2. Run the Go server:
   ```sh
   go run main.go
   ```
3. Open your browser and visit:
   ```
   http://localhost:8080/
   ```

## Endpoints

| Endpoint | Method | Description                                           |
| -------- | ------ | ----------------------------------------------------- |
| `/`      | GET    | Serves static files from `static/` folder.            |
| `/form`  | POST   | Handles form submission and responds with user input. |
| `/hello` | GET    | Responds with a simple "Hello World!" message.        |

## Example Form Submission

```sh
curl -X POST http://localhost:8080/form -d "name=John&address=New+York"
```

The server will respond with:

```
Hello [Your Name] from [Your Address]
```

## Troubleshooting

- Restart the server after making changes.

## License

This project is open-source and available under the [MIT License](LICENSE).
