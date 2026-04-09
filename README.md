Comic-Con Parking System

📦 Entities Breakdown
1. Vehicle
vehicle_id (PK)
license_plate
vehicle_category_id (FK)

3. VehicleCategory
vehicle_category_id (PK)
name (Bike, Car, SUV, EV, etc.)

5. ParkingSpot
spot_id (PK)
zone_id (FK)
level_id (FK)
vehicle_category_id (FK)
reserved_category_id (FK, nullable)
is_available (boolean)

7. Zone
zone_id (PK)
name (A, B, VIP Zone, etc.)
8. Level
level_id (PK)
level_number

10. ReservedCategory
reserved_category_id (PK)
name (Cosplayer, VIP, Staff, Exhibitor, EV Charging)

12. ParkingSession
session_id (PK)
vehicle_id (FK)
spot_id (FK)
entry_time
exit_time

14. Ticket
ticket_id (PK)
session_id (FK)
issued_time

16. Payment
payment_id (PK)
ticket_id (FK)
amount
status (Paid, Pending)

payment_time<img width="5028" height="2247" alt="diagram-export-09-04-2026-22_20_58" src="https://github.com/user-attachments/assets/01bdca9d-3448-4c4f-81e6-49ff723ed8b2" />
