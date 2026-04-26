# Metro Booking System

## Description
The Metro Booking System is a simple application that allows users to book metro tickets by selecting source and destination stations. The system calculates the fare based on distance and generates a ticket.

This project demonstrates basic concepts of programming such as user input, conditional logic, and data handling.

## Features
- Select source and destination stations
- Automatic fare calculation
- Ticket generation
- Simple and user-friendly interface

## Technologies Used
- Programming Language: Python / C / Java (choose what you used)
- Platform: Console-based application

## How It Works
1. User enters source station
2. User enters destination station
3. System calculates the distance
4. Fare is calculated based on distance
5. Ticket is displayed with details

## Sample Output
Enter Source: A  
Enter Destination: D  
Distance: 3 stations  
Fare: ₹30  
Ticket Booked Successfully!

## Future Improvements
- Add GUI interface
- Online payment integration
- QR code ticket generation
- Database for storing bookings

## Conclusion
This project helps in understanding the basic working of a ticket booking system and improves programming skills.
#include <stdio.h>

int main() {
    int source, destination, distance, fare;

    printf("=== Metro Booking System ===\n");

    // Display stations
    printf("\nStations:\n");
    printf("1. A\n2. B\n3. C\n4. D\n5. E\n");

    // User input
    printf("\nEnter Source Station Number: ");
    scanf("%d", &source);

    printf("Enter Destination Station Number: ");
    scanf("%d", &destination);

    // Validation
    if (source < 1 || source > 5 || destination < 1 || destination > 5) {
        printf("\nInvalid station selection!\n");
        return 0;
    }

    if (source == destination) {
        printf("\nSource and Destination cannot be same!\n");
        return 0;
    }

    // Calculate distance
    if (source > destination)
        distance = source - destination;
    else
        distance = destination - source;

    // Fare calculation (₹10 per station)
    fare = distance * 10;

    // Output ticket
    printf("\n--- Ticket Details ---\n");
    printf("Distance: %d stations\n", distance);
    printf("Fare: ₹%d\n", fare);
    printf("Status: Ticket Booked Successfully!\n");

    return 0;
}
