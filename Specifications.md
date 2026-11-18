# Initial Problem statement

"We want to create a software to manage an aquarium, with multiple exhibits.
Each exhibit has a number of animals, and a number of sensors.

An Admin has to create a schedule of urgent, recurrent and batch Tasks to administer to the Caretakers.
The creation of said Tasks is managed by the Admin themselves or when a new Exhibit is open or when an Animal is added.

A Caretaker has three lists of Tasks they need to complete (either urgent, recurrent or batch), after selecting one of them they're instructed on what to do (with a Strategy pattern).

An Admin also receives updates from Sensors (using an Observer pattern) and can create Tickets, that specify a problem that a Maintainer will need to solve.

Tickets have a short description, time of creation, the id of the sensor that originated it, the associated Exhibit and the reading that originated it.

A Maintainer can pick up a Ticket to resolve (uses a Strategy pattern too?).

An Exhibit has a number of Animals, and a list of values that will be read by the Sensors.
> **Question** should the Exhibit themselves originate the values? Or should the Sensors create them and, later on, pass them onto the Exhibit.
"

# Specifications for classes

## Workers

### Admin

### Caretaker

### Maintainer

## Exhibits

### Sensors

### Animals

## Extra

### Tickets

### Tasks/Schedules
