# Trello API Automation Tests

This project contains automated tests for the Trello API using Postman. The goal is to validate the functionality of various endpoints and ensure the proper behavior of the system under different scenarios.

## Features

- **Boards**:
  - Create a new board.
  - Retrieve all boards for the authenticated user.
  - Retrieve a specific board by ID.
  - Delete a board.
  - Validate that deleted boards are inaccessible.

- **Lists**:
  - Create lists (e.g., "To Do", "Done") on a board.
  - Retrieve all lists on a board.
  - Retrieve a specific list by ID.

- **Cards**:
  - Create cards in a specific list.
  - Move cards between lists (e.g., "To Do" to "Done").
  - Validate card details such as name, list, and board association.

## Technologies

- **Postman**:
  - Used for creating, executing, and automating API tests.
  - Scripts written in JavaScript to validate responses and set dynamic variables.

## Setup

1. Clone this repository to your local machine.
2. Install Postman if not already installed: [Download Postman](https://www.postman.com/downloads/).
3. Import the Postman collection file (`Trello.postman_collection.json`) into Postman.
4. Set the following environment variables in Postman:
   - `key`: Your Trello API key.
   - `token`: Your Trello API token.
   - `baseUrl`: `https://api.trello.com/1`.

## How to Run the Tests

1. Open Postman and select the imported "Trello" collection.
2. Set up the environment with the required variables.
3. Run individual requests or use the Postman Collection Runner to execute all tests in the collection.

## Scripts Used

- **Pre-request Scripts**:
  - Incremental board numbering for unique board names.
  - Dynamic variable assignment (e.g., board IDs, list IDs, card IDs).

- **Tests**:
  - Validation of response status codes (e.g., 200, 404).
  - Assertions for expected values in the API response.

## Example Scenarios

- Creating a board and validating its default settings (e.g., private permission level).
- Adding "To Do" and "Done" lists to a board and verifying their properties.
- Creating a card in the "To Do" list, moving it to the "Done" list, and confirming the changes.
- Deleting a board and ensuring it becomes inaccessible.

## Improvements

- Add negative test cases for invalid API requests.
- Enhance automation by integrating with CI/CD tools (e.g., GitHub Actions).
- Expand test coverage to include additional Trello API endpoints.

## License

This project is licensed under the MIT License. Feel free to use, modify, and distribute it.

---

**Author:** André F. Hauszler

For more details, check out the [Trello API documentation](https://developer.atlassian.com/cloud/trello/).

