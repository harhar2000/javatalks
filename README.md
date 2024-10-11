# JavaTalks

#### [Click here to see app deployed ](https://jacebook-app-latest-erwi.onrender.com/)


### Demo Video

<video width="640" height="360" controls>
  <source src="https://drive.google.com/uc?export=download&id=1iViuvRe4tUNPnAN24T9s4NG0zUlwCdzN" type="video/mp4">
</video>




This project is a social networking web application built with **Java** and **Spring Boot**, allowing users to interact through posts, comments, and likes. It is designed to manage user sessions and provide a user-friendly interface for engaging with content.

## Features

- **User Registration**: New users can register and be saved into the database.
- **User Login & Sessions**: Session management ensures that user sessions are handled securely.
- **Posts Management**: Users can create and view posts.
- **Commenting System**: Users can add comments to posts and delete their comments.
- **Likes**: Users can like posts.
- **Navigation**: Simple navigation for users to browse different sections of the app.

## Project Structure

The project follows a typical Java Spring Boot structure. Below is an overview of the main directories and files:

### `src/main/java/com/makersacademy/acebook`

- **config**:
    - `SecurityConfiguration.java`: Handles security and authentication configurations.
- **controller**:
    - `CommentController.java`: Manages creating and deleting comments.
    - `HomeController.java`: Handles requests for the home page.
    - `LikesController.java`: Manages like actions on posts.
    - `NavbarController.java`: Manages the navigation bar and its interactions.
    - `PostLoginController.java`: Handles actions post-login.
    - `PostsController.java`: Manages creating, displaying, and interacting with posts.
    - `SessionController.java`: Manages session checks to ensure user authentication.
    - `UsersController.java`: Handles user registration and user-related operations.
- **model**:
    - `Comment.java`: Represents the comment entity.
    - `Like.java`: Represents the like entity.
    - `Post.java`: Represents the post entity.
    - `User.java`: Represents the user entity.
- **repository**:
    - `CommentRepository.java`: Data access for `Comment` entities.
    - `LikeRepository.java`: Data access for `Like` entities.
    - `PostRepository.java`: Data access for `Post` entities.
    - `UserRepository.java`: Data access for `User` entities.

### `src/main/resources`

- **db/migration**:
    - Contains SQL scripts for database migrations:
        - `V1_init.sql`: Initial database setup.
        - `V2_create_users_table.sql`: Creates the users table.
        - `V3_add_timestamp_column.sql`: Adds a timestamp column to tables.
        - `V4_no_nulls.sql`: Ensures no null values for critical fields.
        - `V5_add_user_id_to_posts.sql`: Adds user IDs to the posts.
        - `V6_likes_table.sql`: Creates the likes table.
        - `V7_create_comments_table.sql`: Creates the comments table.
- **static**:
    - **images**: Contains images for the application.
    - `main.css`: Stylesheet for the application.
- **templates**:
    - **fragments**:
        - `confirmation.html`, `confirmation_comment.html`: Confirmation messages.
        - `edit.html`, `edit_comment.html`: Templates for editing posts and comments.
        - `footer.html`, `new_comment.html`, `postcards.html`: UI elements.
    - **posts**:
        - `index.html`: Home page for posts with a list of posts and forms for creating and commenting on posts&#8203;:contentReference[oaicite:0]{index=0}.
        - `feed.html`: Displays a central feed of posts with functionality for adding and editing posts and comments&#8203;:contentReference[oaicite:1]{index=1}.
        - `friends.html`: Manages friend interactions, displaying a list of friends&#8203;:contentReference[oaicite:2]{index=2}.
        - `my-posts.html`: Shows posts made by the logged-in user, providing a personalised view&#8203;:contentReference[oaicite:3]{index=3}.
        - `navbar.html`: Contains the navigation bar with links to the feed, friends, my posts, and profile pages&#8203;:contentReference[oaicite:4]{index=4}.
        - `profile.html`: Displays user profile information and related actions&#8203;:contentReference[oaicite:5]{index=5}.

### `src/test/java/com/makersacademy/acebook`

- Contains test cases for the application, ensuring each feature works as expected.

### `pom.xml`

- Project Object Model file for managing dependencies using Maven.

### `Dockerfile`

- Configuration for containerising the application using Docker.

### `.gitignore`

- Specifies files and directories that should be ignored by Git.

## Getting Started

### Prerequisites

- **Java 17** or higher
- **Spring Boot 3.x**
- **Maven** for dependency management

### Setup & Run

1. **Clone the repository**:
    ```bash
    git clone https://github.com/harhar2000/acebook.git
    cd acebook
    ```

2. **Build the project**:
    ```bash
    mvn clean install
    ```

3. **Run the application**:
    ```bash
    mvn spring-boot:run
    ```

4. Access the application at `http://localhost:8080`.

### API Endpoints

- **User Registration**: `POST /users`
- **Check Session**: `GET /check-session`
- **Create Post**: `POST /posts`
- **Create Comment**: `POST /comments`
- **Delete Comment**: `DELETE /comments/{comment_id}`
- **Like Post**: `POST /likes`

## Technologies Used

- **Java** & **Spring Boot**: Backend framework for building RESTful services.
- **Spring Security**: For handling user authentication and authorisation.
- **H2 Database**: In-memory database for quick setup and testing.
- **Thymeleaf**: Template engine for rendering HTML pages.
- **Maven**: Dependency management.

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a feature branch (`git checkout -b feature/YourFeature`).
3. Commit your changes (`git commit -m 'Add your feature'`).
4. Push to the branch (`git push origin feature/YourFeature`).
5. Open a pull request.

---

Feel free to reach out if you have any questions or suggestions!
