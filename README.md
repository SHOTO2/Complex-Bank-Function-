# Banking System Management Code Overview

## Key Components

### Structs and Enums
- **stUser**: Represents a user with attributes like username, password, permissions, and a flag for deletion.
- **sClient**: Represents a client with attributes like account number, pin code, name, phone, account balance, and a flag for deletion.
- **enTransactionsMenueOptions**, **enManageUsersMenueOptions**, **enMainMenueOptions**, **enMainMenuePermissions**: Enumerations for various menu options and permissions.

### Global Variables
- **ClientsFileName** and **UsersFileName**: Constants for the filenames where client and user data are stored.
- **CurrentUser**: A global variable representing the currently logged-in user.

### Utility Functions
- **SplitString**: Splits a string based on a delimiter.
- **ConvertUserLinetoRecord**, **ConvertLinetoRecord**: Convert a line from the file into a `stUser` or `sClient` struct.
- **ConvertRecordToLine**, **ConvertUserRecordToLine**: Convert a `sClient` or `stUser` struct into a line for the file.

### File Operations
- **LoadUsersDataFromFile**, **LoadCleintsDataFromFile**: Load user and client data from files into vectors.
- **SaveCleintsDataToFile**, **SaveUsersDataToFile**: Save client and user data from vectors to files.
- **AddDataLineToFile**: Append a line to a file.

## Client and User Management
- Functions to read new client/user data, check if a client/user exists, add new clients/users, delete clients/users, update clients/users, and find clients/users by their identifiers.

## Transaction Handling
- Functions to handle deposits and withdrawals, and to show total balances.

## Menu Display and Navigation
- Functions to display various menus (main menu, transactions menu, manage users menu) and handle user input to navigate through these menus.

## Access Control
- **CheckAccessPermission**: Checks if the current user has the required permissions to perform an action.

## Main Functions
### LoadUserInfo
- This function checks if the provided username and password match any user in the system. If a match is found, it loads the user information into `CurrentUser` and returns true; otherwise, it returns false.

### Login
- This function handles the login process. It repeatedly prompts the user for a username and password until valid credentials are provided. If the login fails, it displays an error message. Once logged in, it shows the main menu.

### main
- The entry point of the program. It calls the `Login` function to authenticate the user and then pauses the system.

## Conclusion
- The code is a comprehensive implementation of a banking system's backend, handling user and client management, transactions, and access control. It uses file I/O for persistent storage and provides a console-based interface for interaction.
