# Aquarium manager

## Statement

## Ideas

An application aimed to help managing and monitor an aquarium.
Making sure that the flora and fauna inside have the proper level of cleanliness, nutrients and temperature.

> **Warning** decide if you want to manage a single house aquarium or a whole aquarium (like Monterey Bay Aquarium)

There can be human operators which can be either care taker, vets, guides or entertainers.
Each exhibit has their own animals, each of which has their own needs, can be part of a guided tour or can be closed for maintenance.

Care takers follow a strategy design pattern to implement a FSM where they can either clean the enclosure/vat, feed animals, play with them or check the animal''re also an observer for care takers, being notified when an health problem for an animal appears.
> **Think hard** about what type of design patter best suits a vet.

There are clients who can simply buy a ticket or request a guided tour or attend a performance (which involves a specific enclosure/animals and an entertainer).

Each exhibit has their own sensors to monitor water temperature, cleanliness, sounds and some videocameras. There is an admin which is an observer of those, and can decide to dispatch caretakers (and how many), close an exhibit or call a vet immediately.
> **Decision** decide whether or not the caretakers should be subscribed to the readings, or if there should be an admin class that is the observer which can dispatch caretakers as needed.

## Actors

- Worker:
  - Admin, observer for sensors.
  - Caretaker, has a strategy pattern to decide what to do.
  - Entertainer, changes how it behaves based on which animal they're performing with.
  - Guide, gives tours, avoids exhibits that are under maintenance.
  - Vet, decides how to treat an animal based on their species and symptoms. Maybe there are multiple type of vets???

- Customer: changes the fee paid based on their age or other special discounts (like disability or being a student).

- Exhibit. Each exhibit has their group of animal, and a certain temperature, humidity and cleanliness of water. An exhibit can be under maintenance if there's a major issue.
  - Enclosure: for amphibious animals.
  - Vat: mainly for aquatic animals.

- Sensor:
  - Video cameras
  - Thermometer
  - Humidity sensor
  - Water pressure sensor

- Animal. Each animal has an overall health value (which depends on the condition of the exhibit), hunger and extra notes for caretakers (like if they are extra playful, need certain food and so on).
  - Fish
  - Mollusk
  - Crustacean
  - Mammal:
    - Cetacean

> **Decision** decide if you also want to have mollusks and crustaceans.

### Design Pattern Used

- DAOS, for database interactions.
- Strategy, for the caretakers.
- Observer, for Admin and Sensors.

## Use Cases

## UML

## Used technologies and tools
