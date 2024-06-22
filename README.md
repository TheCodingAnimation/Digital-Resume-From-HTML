<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Digital Resume</title>
    <style>
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
            color: #333;
        }
        .container {
            width: 80%;
            margin: auto;
            overflow: hidden;
        }
        header {
            background: #4CAF50;
            color: #fff;
            padding-top: 30px;
            min-height: 70px;
            border-bottom: #388E3C 3px solid;
        }
        header a {
            color: #fff;
            text-decoration: none;
            text-transform: uppercase;
            font-size: 16px;
            display: inline-block;
            padding: 10px 20px;
            background-color: #388E3C;
            border-radius: 5px;
            margin: 0 10px;
            transition: background-color 0.3s;
        }
        header a:hover {
            background-color: #2E7D32;
        }
        header ul {
            padding: 0;
            list-style: none;
            text-align: center;
        }
        header li {
            display: inline;
        }
        .showcase {
            min-height: 400px;
            text-align: center;
            color: #fff;
        }
        .showcase h1 {
            margin-top: 100px;
            font-size: 55px;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px #000;
        }
        .showcase p {
            font-size: 20px;
            text-shadow: 1px 1px 2px #000;
        }
        .profile-image {
            text-align: center;
            margin-top: -100px;
        }
        .profile-image img {
            border-radius: 50%;
            border: 5px solid #fff;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            width: 150px;
            height: 150px;
            cursor: pointer;
        }
        .profile-image input {
            display: none;
        }
        .main-section {
            padding: 20px;
            background: #fff;
            margin-top: -50px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        .main-section h2 {
            text-align: center;
            margin-bottom: 20px;
            color: #4CAF50;
        }
        .main-section .section {
            margin-bottom: 20px;
        }
        .main-section .section h3 {
            border-bottom: 2px solid #4CAF50;
            padding-bottom: 10px;
            color: #388E3C;
        }
        .main-section .section p {
            margin: 10px 0;
            line-height: 1.6;
        }
        footer {
            background: #4CAF50;
            color: #fff;
            text-align: center;
            padding: 10px;
            margin-top: 20px;
            position: relative;
            bottom: 0;
            width: 100%;
        }
        .skills ul {
            list-style: none;
            padding: 0;
        }
        .skills ul li {
            background: #e4e4e4;
            margin: 5px 0;
            padding: 10px;
            border-radius: 5px;
        }
        .contact p {
            margin: 5px 0;
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <h1>Mr. Prince</h1>
            <ul>
                <li><a href="#contact">Contact</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#experience">Experience</a></li>
                <li><a href="#education">Education</a></li>
            </ul>
        </div>
    </header>
    
    <div class="showcase">
        <div class="container">
            <h1>Mr. Prince</h1>
            <p>Web Developer | Programmer | Designer</p>
        </div>
    </div>
    
    <div class="profile-image">
        <img id="profile-pic" src="https://via.placeholder.com/150" alt="Profile Image" onclick="document.getElementById('file-input').click();">
        <input type="file" id="file-input" accept="image/*" onchange="loadFile(event)">
    </div>

    <div class="container main-section">
        <section id="education" class="section">
            <h2>Education</h2>
            <h3>ABC University</h3>
            <p>Bachelor of Science in Computer Science, 2018 - 2022</p>
        </section>

        <section id="experience" class="section">
            <h2>Experience</h2>
            <h3>XYZ Company</h3>
            <p>Junior Web Developer, June 2022 - Present</p>
            <p>Responsibilities:</p>
            <ul>
                <li>Developed responsive web applications using HTML, CSS, and JavaScript.</li>
                <li>Collaborated with designers and backend developers to improve usability.</li>
                <li>Performed code reviews and provided constructive feedback.</li>
            </ul>
        </section>

        <section id="skills" class="section skills">
            <h2>Skills</h2>
            <ul>
                <li>HTML</li>
                <li>CSS</li>
                <li>JavaScript</li>
                <li>React</li>
                <li>Node.js</li>
            </ul>
        </section>

        <section id="contact" class="section contact">
            <h2>Contact</h2>
            <p>Email: john.doe@example.com</p>
            <p>Phone: (123) 456-7890</p>
            <p>LinkedIn: <a href="https://www.linkedin.com/in/the-coding-animation-868937271" target="_blank">linkedin.com/in/The coding Animation</a></p>
            <p>Instagram: <a href="https://www.instagram.com/the_coding_animation?utm_source=ig_web_button_share_sheet&igsh=ZDNlZDc0MzIxNw==" target="_blank">instagram.com/in/The Coding Animation</a></p>
            <p>YouTube: <a href="https://youtube.com/@thecodinganimation?si=w7EeF8lIheuGgEv4" target="_blank">youtube.com/in/The Coding Animation</a></p>
        </section>
    </div>
    
    <footer>
        <p>&copy; 2024 Mr. Prince. All rights reserved.</p>
    </footer>

    <script>
        function loadFile(event) {
            var image = document.getElementById('profile-pic');
            image.src = URL.createObjectURL(event.target.files[0]);
            image.onload = function() {
                URL.revokeObjectURL(image.src);
            }
        }
    </script>
</body>
</html>
