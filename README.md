# Robot-Arm-Control-Pane

🤖 Robot Arm Control Panel
📌 Overview
This project is a web-based control panel for a 6-motor robotic arm. It allows users to:
•	Adjust motor angles using sliders
•	Save and manage multiple poses
•	Load and run saved poses
•	Store pose data in a MySQL database
Built using PHP, MySQL, HTML, CSS, JavaScript and designed for use with XAMPP.

Features
•	🎛️ Sliders: Control 6 motors (0–180°)
•	💾 Save Poses: Store motor positions
•	📋 Pose Table: View all saved poses
•	🔄 Load Pose: Activate a saved pose
•	🗑️ Remove Pose: Delete a saved pose
•	▶️ Run Pose: Send pose data to Arduino (future integration)
•	🎨 Modern UI: Clean design with hover animations

 Installation
1️⃣ Setup XAMPP
•	Install XAMPP
•	Start Apache and MySQL
2️⃣ Create Database
1.	Open phpMyAdmin
2.	Run the following SQL:
CREATE DATABASE robot_arm;
USE robot_arm;

CREATE TABLE poses (
    id INT AUTO_INCREMENT PRIMARY KEY,
    motor1 INT NOT NULL,
    motor2 INT NOT NULL,
    motor3 INT NOT NULL,
    motor4 INT NOT NULL,
    motor5 INT NOT NULL,
    motor6 INT NOT NULL,
    status TINYINT DEFAULT 1
);
Project Files
Place all files inside:
C:\xampp\htdocs\robot_arm\
Files included:
•	index.php → Main control panel
•	save_pose.php → Saves new poses
•	remove_pose.php → Deletes poses
•	load_pose.php → Loads and activates a pose
•	get_run_pose.php → Retrieves active pose
•	update_status.php → Updates pose status

4️⃣ Run the Project
Open browser and go to:
http://localhost/robot_arm/

🚀 Usage
1.	Move sliders to adjust motor angles
2.	Click Save Pose → Pose added to database
3.	Use Load and Run to activate saved poses
4.	Remove unwanted poses using Remove button

🔧 Future Enhancements
•	Connect to Arduino via USB or Serial for real motor movement
•	Add WebSocket for real-time control
•	Include authentication for multiple users

📜 License
This project is open-source and free to use.

Diagram 




