Tracksite is a web application that allows users to efficiently manage projects, courses, websites, and applications, providing easy access and organisation of resources

## Features: 
- This React-based Bookmark Manager application allows users to create, view, and manage folders and bookmarks. It uses axios to interact with a backend API, enabling CRUD operations for organizing bookmarks, with real-time updates to folder and bookmark lists upon creation or deletion.
- Utilizes react-router-dom to create a multi-page user interface with routes for Home, About, Folders, and Login. It includes dynamic navigation and a custom logo for a smooth user experience.
- The homepage features a simple and engaging interface where users can navigate to the main app page with a 'Begin' button. It integrates React Router’s useNavigate hook for seamless page transitions and custom CSS for a clean layout

## Tech Stack: 

Frontend: React, Javascript, CSS

Backend: Python, FastAPI

Database: MySQL

Version Control: Git



SQL:
CREATE DATABASE tracksite_db;
SHOW DATABASES;
CREATE USER 'tracksite_user'@'localhost' IDENTIFIED BY 123;
GRANT ALL PRIVILEGES ON tracksite_db.* TO 'tracksite_user'@'localhost';
FLUSH PRIVILEGES;

USE tracksite_db;

CREATE TABLE folders (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(255) NOT NULL UNIQUE
);

CREATE TABLE bookmarks (
    id INT AUTO_INCREMENT PRIMARY KEY,
    title VARCHAR(255) NOT NULL,
    url VARCHAR(2048) NOT NULL,
    type VARCHAR(50) DEFAULT 'url',
    folder_id INT,
    FOREIGN KEY (folder_id) REFERENCES folders(id) ON DELETE SET NULL
);


https://github.com/user-attachments/assets/5af327e4-a83f-40a0-82cd-69c29fb072ce

