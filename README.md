# Airline-Passenger-Management-System

# Language Used C

# Project Documentation: Airline Passenger Management System - Free Fall

## Overview

This project implements a passenger management system for a fictional airline named "Free Fall." The system allows the registration, search, removal, and display of passenger information, along with support for a waiting list.

## Key Features

### 1. Flight Selection

Upon starting the program, the user is presented with a menu offering options for available flights:

- BH-RIO (Option 1)
- BH-SP (Option 2)
- BH-BRASILIA (Option 3)

The user selects the desired flight, and from that point onward, all operations are performed for the chosen flight.

### 2. Operation Menu

After selecting the flight, the system displays a menu with the following options:

1. **Show Passenger List:** Displays the list of registered passengers for the chosen flight.
2. **Search Passenger by CPF:** Allows searching for a passenger by CPF.
3. **Search Passenger by Name:** Allows searching for a passenger by name.
4. **Register Passenger:** Adds a new passenger to the flight.
5. **Remove Passenger from List:** Removes a passenger from the flight.
6. **Show Waiting List:** Displays the list of passengers on the waiting list for the flight.
9. **Exit:** Closes the program.

### 3. Passenger Operations

#### 3.1. Show Passenger List

- Displays information for all passengers registered for the selected flight.
- Includes details such as CPF, name, address, telephone, ticket number, and seat number.
- If the flight does not exist, an appropriate message is displayed.

#### 3.2. Search Passenger by CPF

- Allows searching for a passenger by CPF.
- Displays the passenger's information if found, indicating CPF, name, address, telephone, ticket number, and seat number.
- If the passenger is not found on the flight, the search is extended to the waiting list.

#### 3.3. Search Passenger by Name

- Allows searching for a passenger by name.
- Displays the passenger's information if found, indicating CPF, name, address, telephone, ticket number, and seat number.
- If the passenger is not found on the flight, the search is extended to the waiting list.

#### 3.4. Register Passenger

- Requests information for the new passenger, such as CPF, name, address, telephone, ticket number, and seat number.
- Checks if there is space on the flight to register the passenger. If not, the passenger is added to the waiting list.
- If the waiting list is also full, registration is not allowed.

#### 3.5. Remove Passenger from List

- Removes a passenger from the flight, freeing up space for other passengers.
- If the removed passenger is in the waiting list, the next passenger in the queue is automatically moved to the flight.

#### 3.6. Show Waiting List

- Displays the list of passengers on the waiting list for the selected flight.
- Presents information such as CPF, name, address, telephone, ticket number, and seat number.

### 4. Space Control

- The system checks the maximum passenger capacity for a flight (`MAX_PASSAGEIROS`) and prevents registration if the limit is reached.
- A waiting list is implemented to accommodate passengers when the flight is full.

### 5. Data Persistence

- Passenger and waiting list information is stored in specific text files for each flight.
- The files follow the format `<flightName>.txt` for passengers and `waiting_list_<flightName>.txt` for the waiting list.
