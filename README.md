
# 🍽️ Recipe Ingredient Web Application
A comprehensive web application for managing and sharing recipes. Built using PHP, HTML, CSS, JavaScript, Bootstrap, Ajax, and MySQL, this application allows users to register, log in, add, edit, delete, and view recipes, with features such as ingredient lists, reviews, and ratings.

## 🌟 Features
- User registration and login 🔐
- Add new recipes 🆕
- Edit existing recipes ✏️
- Delete recipes ❌
- View recipes with detailed ingredients 👩‍🍳
- Search and filter recipes by category or name 🔍
- Review and rate recipes ⭐
- Responsive design using Bootstrap 📱💻
- AJAX for dynamic content updates ⚡

## 🛠️ Technologies Used
- **Frontend**: HTML, CSS, Bootstrap, JavaScript, jQuery
- **Backend**: PHP, MySQL
- **AJAX**: For seamless updates

## 📝 Setup Instructions
Follow these steps to set up the project locally:

### 1. Clone the Repository
```bash
git clone https://github.com/obadaKraishan/RecipeIngredientApp.git
cd RecipeIngredientApp
```

### 2. Set Up the Database
1. Start your local server using XAMPP, WAMP, or MAMP.
2. Open phpMyAdmin and create a new database named `recipe_ingredient`.
3. Import the SQL file to set up the tables:
   ```sql
   CREATE DATABASE recipe_ingredient;
   USE recipe_ingredient;

   CREATE TABLE users (
       id int(11) NOT NULL,
       name varchar(100) NOT NULL,
       email varchar(255) NOT NULL,
       password varchar(255) NOT NULL,
       city varchar(100) DEFAULT NULL,
       gender enum('Male','Female','Other') DEFAULT NULL,
       bio text DEFAULT NULL,
       profile_image varchar(255) DEFAULT NULL,
       created_at timestamp NOT NULL DEFAULT current_timestamp()

   );

   CREATE TABLE recipes (
       id INT AUTO_INCREMENT PRIMARY KEY,
       title VARCHAR(255) NOT NULL,
       description TEXT NOT NULL,
       instructions TEXT NOT NULL,
       image VARCHAR(255) NOT NULL,
       category VARCHAR(255) NOT NULL,
       created_by INT NOT NULL,
       video_url varchar(255) DEFAULT NULL,
       category varchar(255) NOT NULL
   );

   CREATE TABLE ingredients (
       id INT AUTO_INCREMENT PRIMARY KEY,
       recipe_id INT NOT NULL,
       name VARCHAR(255) NOT NULL,
       quantity VARCHAR(255) NOT NULL,
       FOREIGN KEY (recipe_id) REFERENCES recipes(id)
   );

   CREATE TABLE reviews (
       id INT AUTO_INCREMENT PRIMARY KEY,
       recipe_id INT NOT NULL,
       user_id INT NOT NULL,
       rating INT NOT NULL,
       comment TEXT,
       created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
       FOREIGN KEY (recipe_id) REFERENCES recipes(id),
       FOREIGN KEY (user_id) REFERENCES users(id)
   );
   ```

### 3. Run the Application
Open a web browser and navigate to `http://localhost/RecipeIngredient`.

## 🎨 Customization

### 1. Update Styles
Modify the styles in `/css/style.css` to match your design preferences.

### 2. Update JavaScript
Enhance the JavaScript functionality in `/js/script.js` to customize the interactivity.

### 3. Update Content
Modify the HTML content in `index.php` to personalize the text and recipes.

## 📄 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👥 Contributors

- [Obada Kraishan](https://github.com/obadaKraishan)
![IMG-20250429-WA0018](https://github.com/user-attachments/assets/be3dfc26-e2d2-4382-bed3-958edd889e4b)
![IMG-20250429-WA0017](https://github.com/user-attachments/assets/9331d647-b261-4c12-ac3f-e34f00e1d4e5)
![IMG-20250429-WA0016](https://github.com/user-attachments/assets/d491396c-1443-4265-896b-75bab32b7d87)
![IMG-20250429-WA0015](https://github.com/user-attachments/assets/f84c3e3e-628d-4e38-bea2-63609120b35d)
![IMG-20250429-WA0014](https://github.com/user-attachments/assets/771e2437-f929-4f70-b341-a37ef9b38286)
![IMG-20250429-WA0013](https://github.com/user-attachments/assets/dc298de6-b24e-48bf-a8ea-489d0a0b14ea)
![IMG-20250429-WA0012](https://github.com/user-attachments/assets/482243d9-83d1-454c-bf88-cea83a4f3597)
![IMG-20250429-WA0011](https://github.com/user-attachments/assets/dedf9cfd-7c9c-4365-8b14-f9c0dde62401)
![IMG-20250429-WA0010](https://github.com/user-attachments/assets/6b2b0881-62ab-44e9-a8f1-8543636f59a8)


