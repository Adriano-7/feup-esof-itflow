# ITFlow 

> **Project**
> <br />
> Course Unit: (Software Engineering (Engenharia de Software), 2022/2023
> <br />
> Faculty: **FEUP** (Faculty of Engineering of the University of Porto)
> <br />
> Project evaluation: **18**/20

## Documentation

* Business modeling 
  * [Product Vision](docs/ProductVision.md)
  * [Elevator Pitch](docs/ElevatorPitch.md)
* [Requirements](docs/requirements.md)
  * [Domain model](docs/requirements.md)
* [Architecture and Design](docs/ArchitectureAndDesign.md)
  * [Logical architecture](docs/ArchitectureAndDesign.md#logical-architecture)
  * [Physical architecture](docs/ArchitectureAndDesign.md#physical-architecture)
  * [Vertical prototype](docs/ArchitectureAndDesign.md#vertical-prototype)
* [Test](docs/Test.md)
* [Project management](docs/ProjectManagement.md)

---

## Project Goals

Finding a role in the IT industry can be daunting, but **ITFlow** simplifies the process by connecting you directly with job opportunities. 

![ITFlow Preview](docs/images/Gif.gif) *(Preview of the application)*

## Technical Architecture

The software is structured into distinct layers following a structured MVC-like pattern adapted for Flutter:

### 1. Logical Architecture
*   **Widgets**: Reusable UI building blocks (buttons, custom forms, navbars, job offer cards).
*   **Screens**: The main application views (Home, Login, Search, Profile, Settings) composed of various widgets.
*   **Controllers**: Responsible for data gathering, manipulation, and business logic. This includes form validation, Firebase Authentication, Firestore read/writes, and fetching/parsing data from the ITJobs API.
*   **Models**: Abstractions of the problem domain (e.g., `User`, `Company`, `Job`). 

### 2. Key Features Developed
*   **Authentication & Profiles**: Registration flow for two distinct user types (Standard and Enterprise). Includes profile picture and PDF CV uploads.
*   **External API Integration**: Real-time fetching of job offers and companies using the `itjobs.pt` API.
*   **Advanced Filtering**: Users can filter job searches by location, job type (Full-time, Part-time), contract type, and required programming languages.
*   **Bookmarking System**: Job seekers can save (bookmark) their favorite job listings, which are stored persistently in Firestore and accessible via their profile.
*   **Theming**: Custom UI with consistent light and dark mode support.

## Running the code

**Prerequisites:**
*   [Flutter SDK](https://docs.flutter.dev/get-started/install) (version >=3.3.0)
*   Dart (version >=2.19.2)

**Setup:**
```bash
# Clone the repository
git clone https://github.com/your-username/itflow.git
cd itflow/app

# Install dependencies
flutter pub get

# Run the app (ensure an emulator is running or a device is connected)
flutter run
```

## Tech stack

*   **Frontend**: Flutter, Dart
*   **Backend & Database**: Firebase (Authentication, Cloud Firestore, Cloud Storage)
*   **External Services**: ITJobs REST API
*   **Key Packages**: `http` (API requests), `cloud_firestore` / `firebase_auth` (Backend), `file_picker` (CV uploads), `flutter_html` (Rendering job descriptions).

## Team

- Adriano Machado
- Igor Cherstnev
- José Pedro Evans
- Luís Jesus
- Henrique Caridade
