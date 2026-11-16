# Aquarium manager

## Statement

## Ideas

An application aimed to help managing and monitor an aquarium.
Making sure that the flora and fauna inside have the proper level of cleanliness, nutrients and temperature.

> **Warning** decide if you want to manage a single house aquarium or a whole aquarium (like Monterey Bay Aquarium)

There can be human operators which can be either care taker, or maintainers.
Each exhibit has their own animals, each of which has their own needs, can be part of a guided tour or can be closed for maintenance.

(???) Caretakers follow a strategy design pattern to implement a FSM where they can either clean the enclosure/vat, feed animals, play with them or check the animal''re also an observer for care takers, being notified when an health problem for an animal appears.

There are clients who can simply buy a ticket or request a guided tour or attend a performance (which involves a specific enclosure/animals and an entertainer).

- Factory: Admins (or someone else) can also decide to open up new exhibits given a certain number and type of animals.

Each exhibit has their own sensors to monitor water temperature, cleanliness, sounds and some videocameras. There is an admin which is an observer of those, and can decide to dispatch caretakers (and how many), close an exhibit or call a vet immediately.


## Actors

- Worker:
  - Admin, receives sensor reads from Sensors, from which they can create tickets for Maintainers. Can create scheduled tasks and batch tasks for caretakers.
  - Caretaker, has a set of scheduled tasks or batch tasks set by the Admin, involving animal care, inventory and such.
  - Maintainer, resolves tickets given by the Admin.

- Customer: changes the fee paid based on their age or other special discounts (like disability or being a student).

- Exhibit. Each exhibit has their group of animal, and a certain temperature, humidity and cleanliness of water. An exhibit can be under maintenance if there's a major issue. An exhibit has a certain size that is related to how many sensors they have.
  - Enclosure: for amphibious animals.
  - Vat: mainly for aquatic animals.

- Factory: Admins (or someone else) can also decide to open up new exhibits given a certain number and type of animals.

- Sensor:
  - Video cameras, can either be working or not, an admin can look at them to have a glance if there are problems with the animals.
  - Thermometer,
  - Humidity sensor (could be included in the thermometer?)
  - Water pressure sensor/water quality sensor.

- Animal. Each animal has an overall health value (which depends on the condition of the exhibit), hunger and extra notes for caretakers (like if they are extra playful, need certain food and so on).
  - Fish
  - Mollusk
  - Crustacean
  - Mammal:
    - Cetacean

> **Decision** decide if you also want to have mollusks and crustaceans.

### Design Pattern Used

- DAOS, for database interactions.
- Strategy, for the caretakers. (???)
- Observer, for Admin and Sensors.
- Factory for opening up new exhibits.

## Use Cases

## UML

## Used technologies and tools
