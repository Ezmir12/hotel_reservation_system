# Hotel Reservation System

A C++ console application for managing hotel room reservations. Data is
persisted to a plain text file (`reservations.txt`) in the working
directory, loaded automatically on startup and saved on exit (if chosen).

## Features

- Add a reservation with room number, guest name, phone number,
  check-in date, number of days, and daily rate
- View all current reservations, with total cost computed per stay
- Search for a reservation by room number
- Delete a reservation by room number
- Input validation throughout: room numbers, phone numbers (10 digits),
  and check-in dates (including real days-per-month and leap-year checks)
- Save on exit, or exit without saving

## Build & Run

```bash
g++ -o hotel_reservation_system hotel_reservation_system.cpp
./hotel_reservation_system
```

## Known limitations

- Reservations are capped at 100 (fixed-size array, no dynamic growth)
- No check for overlapping stays on the same room across different dates
  — a room is simply "booked" or not, with no date-range awareness

## Future Improvements
- Move storage to a real database (e.g. MySQL) instead of a flat file
- Support overlapping-stay / date-range checks per room
- Replace the fixed-size array with a dynamic container

## Author
Yonatan Azmir
