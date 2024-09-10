# ACME System3 Desktop Application Automation Library

This UiPath library automates operations within the ACME System3 desktop application. It can launch the desktop application, log in to an ACME account, search by client ID, extract client details and account movements, and navigate through the application’s windows. This library is a reusable solution for automating tasks related to the ACME System3 desktop environment.

## Features
- Launches the ACME System3 desktop application
- Logs in to an ACME account
- Navigates to the "Search by ID" feature
- Searches for a client by ID
- Opens the client details window
- Opens the client accounts window
- Navigates to and displays all account movements
- Extracts all account movements for a given client
- Closes all open windows and returns to the "Search by ID" screen

## Prerequisites
- UiPath Studio (latest version)
- Download ACME System3 desktop application
- UiPath Desktop Automation packages
- Valid ACME System account credentials

## Installation

1. Download or clone this Library.
   - [ACME System3 Desktop Application Automation Library](https://github.com/mnsy1/UiPath_ACMESystem3Application/blob/main/ACME.System3.Application.1.0.8.nupkg)
3. Open UiPath Studio and load the library into your project.

## Usage

1. **Import the Library**: After downloading, import the library into your UiPath project.

2. **Setup Credentials**: Ensure that your ACME System3 login credentials are stored securely, either using UiPath Orchestrator Assets or Windows Credential Manager.

3. **Use Activities**: Below is the sequence of activities for automating the ACME System3 desktop application:
   - **Launch Application**: Opens the ACME System desktop application.
   - **Login**: Automates the login process using stored credentials.
   - **Search by ID**: Navigates to the "Search by ID" screen and inputs the client ID.
   - **Open Client Details**: Opens the client details window for the specified ID.
   - **Open Client Accounts**: Navigates to the client accounts window.
   - **Show All Account Movements**: Displays all account movements for the selected account.
   - **Extract Account Movements**: Extracts all visible account movements.
   - **Close Windows**: Closes all open windows and navigates back to the "Search by ID" screen.

### Example Workflow

1. **Launch and Login**: The automation starts by launching the ACME System3 application and logging in using stored credentials.
2. **Search and Navigate**: After login, the automation navigates to the "Search by ID" screen and enters a client ID to search for.
3. **Client Details and Accounts**: It opens the client details and client accounts windows to gather the relevant data.
4. **Extract Account Movements**: The automation opens the account movements window, displays all movements, and extracts them for further processing.
5. **Cleanup**: After extraction, it closes all open windows, returning to the "Search by ID" window, and the session is completed.

## Customization

- **Client ID Input**: The client ID to be searched can be dynamically passed as an argument in the workflow.
- **Error Handling**: The library includes error handling mechanisms to retry in case of application crashes or unexpected UI changes.
- **Window Handling**: Custom logic for handling specific windows can be added based on UI changes in the ACME System3 application.

## Error Handling

- If the ACME System3 application fails to launch, the process will retry a set number of times before exiting.
- Proper exception handling is built into the workflow to ensure smooth navigation and data extraction.

## Contributions

Feel free to submit issues or pull requests to enhance the library.
