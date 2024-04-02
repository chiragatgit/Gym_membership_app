
# Gym Membership Application
## Project Goal
This user-friendly application that allows users to find and join gyms, manage their memberships, and access workout plans. The application should support various user roles, including Customers, Trainers, and Administrators, each with specific permissions and responsibilities

![Gym App](https://github.com/chiragatgit/expense_manager_app/assets/119803371/8ae978ff-8e10-47ce-b38a-cf79fdd335cb)

## Gym Management System APIs

## ADMIN Role API:

- **GET** `/user/all`: This API allows the admin to fetch all the users from the database and returns an OK HTTP status.

- **DELETE** `/user/{id}` (`@PathVariable Long id`): This API lets the admin delete a User record by its ID and returns an OK HTTP status.

## TRAINER Role API:

- **POST** `/user/workout/{userId}` (`@RequestBody WorkoutDto workoutDto`, `@PathVariable Long userId`): This API allows the trainer to assign a workout to a customer by its ID and returns a CREATED HTTP status.

## CUSTOMER Role API:

- **GET** `/user/{id}`: This API allows the customer to fetch the user record by its ID and returns an OK HTTP status.

- **PUT** `/user/{id}`: This API allows customers to update a user record by its ID and returns an OK HTTP status.

## PUBLIC API:

- **POST** `/user/register` (`@RequestBody UserRequest userRequest`): This API registers a new user record into the database and can be accessed by anyone. It returns a CREATED HTTP status.

## GymController Class

Complete the GymController class by auto-wiring the necessary dependencies and creating the following APIs by completing the relevant controller methods.

### ADMIN Role API:

- **GET** `/gym/{id}` (`@PathVariable Long id`): This API allows the user to fetch the tax record by its ID and returns an OK HTTP status.

- **GET** `/gym/all`: This API allows the admin to fetch all the gym records and returns an OK HTTP status.

- **PUT** `/gym/{id}` (`@RequestBody GymDto gymDto`, `@PathVariable Long id`): This API allows admins to update a gym record by its ID and returns an OK HTTP status.

- **DELETE** `/gym/{id}` (`@PathVariable Long id`): This API lets admins delete a gym record by its ID and returns an OK HTTP status.

- **POST** `/gym/addMember` (`@RequestParam Long userId`, `@RequestParam Long gymId`): This API allows the admin to add users to a particular gym by passing userId and gymId as requestParam. It returns a CREATED HTTP status.

- **DELETE** `/user/deleteMember` (`@PathParam("userId") Long userId`, `@PathParam("gymId") Long gymId`): This API allows the admin to delete users to a particular gym by passing userId and gymId as path params. It returns an OK HTTP status.

- **POST** `/gym/create`: This API allows the admin to create a gym record and returns a CREATED HTTP status.
