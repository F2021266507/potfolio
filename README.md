<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Personal Portfolio</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Your Name</h1>
        <h2>Your Designation</h2>
        <p>Your Title Line</p>
    </header>
    
    <section id="education">
        <h2>Education</h2>
        <ul>
            <li>Matriculation: School Name</li>
            <li>BS in Your Major: University Name</li>
        </ul>
    </section>

    <section id="skills">
        <h2>Skills</h2>
        <ul>
            <li>Skill 1</li>
            <li>Skill 2</li>
            <li>Skill 3</li>
        </ul>
    </section>

    <section id="experience">
        <h2>Experience</h2>
        <ul>
            <li>Job Title at Company - Dates</li>
            <li>Job Title at Company - Dates</li>
        </ul>
    </section>

    <section id="projects">
        <h2>Projects</h2>
        <ul>
            <li>Project 1 - <a href="link_to_project1">View Project</a></li>
            <li>Project 2 - <a href="link_to_project2">View Project</a></li>
        </ul>
    </section>

    <section id="contact">
        <h2>Contact Me</h2>
        <form id="contactForm">
            <label for="name">Name:</label>
            <input type="text" id="name" name="name" required>
            
            <label for="email">Email:</label>
            <input type="email" id="email" name="email" required>
            
            <label for="message">Message:</label>
            <textarea id="message" name="message" required></textarea>
            
            <button type="submit">Submit</button>
        </form>
    </section>

    <script src="scripts.js"></script>
</body>
</html>
body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
    margin: 0;
    padding: 0;
    background: #f4f4f4;
    color: #333;
}

header {
    background: #333;
    color: #fff;
    padding: 1rem 0;
    text-align: center;
}

header h1 {
    margin: 0;
}

header h2 {
    margin: 0.5rem 0;
}

header p {
    font-style: italic;
}

section {
    padding: 2rem;
    background: #fff;
    margin: 1rem 0;
}

section h2 {
    margin-bottom: 1rem;
}

ul {
    list-style-type: none;
    padding: 0;
}

ul li {
    background: #f4f4f4;
    margin: 0.5rem 0;
    padding: 0.5rem;
    border-left: 5px solid #333;
}

form {
    display: flex;
    flex-direction: column;
}

form label {
    margin-top: 1rem;
}

form input, form textarea, form button {
    margin-top: 0.5rem;
    padding: 0.5rem;
    border: 1px solid #ccc;
    border-radius: 4px;
}

form button {
    background: #333;
    color: #fff;
    border: none;
    cursor: pointer;
}

form button:hover {
    background: #555;
}
document.getElementById('contactForm').addEventListener('submit', function(event) {
    event.preventDefault();

    const name = document.getElementById('name').value;
    const email = document.getElementById('email').value;
    const message = document.getElementById('message').value;

    console.log('Form submitted:', { name, email, message });
    alert('Thank you for contacting me, ' + name + '!');

    // Optionally, you can add code here to send form data to your email or server
    this.reset();
});

