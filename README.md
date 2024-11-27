# College ERP System - Frontend (ReactJS)

This is the frontend for the College ERP System built with **ReactJS**. It serves as an interface for both **students** and **teachers** to access various features and functionalities related to college management. The system includes user authentication and authorization to ensure secure access to different areas of the platform based on the user role.

## Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
  - [For Students](#for-students)
  - [For Teachers](#for-teachers)
- [Installation](#installation)
- [Usage](#usage)
- [Authentication and Authorization](#authentication-and-authorization)
- [Technologies Used](#technologies-used)
- [Contributing](#contributing)
- [License](#license)

## Project Overview

The College ERP System allows both students and teachers to access various functionalities such as viewing course materials, checking grades, submitting assignments, and managing personal information. It also includes admin features like managing courses, assignments, and grades.

### Features Include:
- Login/Signup for both students and teachers.
- Role-based access control (RBAC) to differentiate between student and teacher functionalities.
- Dashboard for students and teachers with role-specific data.
- Integration with backend APIs for course management, grades, and assignments.

## Features

### For Students:
- **Dashboard**: View personal details, enrolled courses, and grades.
- **Assignments**: Submit assignments for courses.
- **Course Materials**: View course-related documents and resources.
- **Grades**: Check results and performance for each subject.
- **Profile Management**: Update personal information.

### For Teachers:
- **Dashboard**: View courses being taught, student submissions, and class schedules.
- **Assignments**: Create and grade assignments for students.
- **Grade Management**: Assign grades to students for completed assignments.
- **Course Materials**: Upload and manage course materials for students.
- **Student Management**: View student profiles and academic progress.

## Installation

Follow these steps to set up the project locally:

1. Clone the repository:
    ```bash
    git clone https://github.com/KoustubhK2193/VRVSecurities.git
    ```

2. Navigate to the project directory:
    ```bash
    cd VRVSecurities
    ```

3. Install the dependencies:
    ```bash
    npm install
    ```

4. Start the development server:
    ```bash
    npm start
    ```

    The app will be available at [http://localhost:3000](http://localhost:3000).

## Usage

1. **Login**: Both students and teachers can log in with their credentials (email and password).  
2. **Dashboard**: Once logged in, users are directed to their respective dashboards based on their roles.
3. **Role-Specific Features**: The frontend displays different views and functionalities for students and teachers. Students will only have access to their grades, assignments, and courses, while teachers will have access to grading features, course management, and student information.

## Authentication and Authorization

### Authentication:
- **Login/Signup**: The system supports user login and registration. Users (both students and teachers) can register with an email and password, and after authentication, they receive a **JWT Token** (JSON Web Token) for session management.
- **Protected Routes**: The app uses protected routes for various functionalities. Routes such as the **Dashboard**, **Assignments**, **Grades**, etc., are accessible only when the user is authenticated.

### Authorization:
- **Role-Based Access**: After authentication, the user's role (student or teacher) is determined, and based on that, the system restricts access to certain features.
  - **Student Role**: Has access to student-specific views such as assignments and grades.
  - **Teacher Role**: Has access to teacher-specific features such as course management and grading assignments.
- **Redirects**: Unauthorized users are redirected to the login page if they attempt to access routes that are not allowed for their role.
