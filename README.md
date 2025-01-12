<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Examination Management System</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <!-- Navigation Bar -->
    <header>
        <nav>
            <h1>Examination Management System</h1>
            <ul>
                <li><a href="#login">Login</a></li>
                <li><a href="#admin-dashboard">Admin</a></li>
                <li><a href="#student-dashboard">Student</a></li>
            </ul>
        </nav>
    </header>

    <!-- Login Section -->
    <section id="login">
        <h2>Login</h2>
        <form action="/login" method="POST">
            <label for="username">Username:</label>
            <input type="text" id="username" name="username" required>

            <label for="password">Password:</label>
            <input type="password" id="password" name="password" required>

            <button type="submit">Login</button>
        </form>
    </section>

    <!-- Admin Dashboard -->
    <section id="admin-dashboard">
        <h2>Admin Dashboard</h2>
        <div>
            <button onclick="addExamination()">Add Examination</button>
            <button onclick="viewForms()">View Submitted Forms</button>
        </div>

        <!-- Add Examination Form -->
        <div id="add-exam" style="display: none;">
            <h3>Add New Examination</h3>
            <form action="/admin/add-exam" method="POST">
                <label for="exam-name">Examination Name:</label>
                <input type="text" id="exam-name" name="examName" required>

                <label for="exam-date">Date:</label>
                <input type="date" id="exam-date" name="examDate" required>

                <label for="exam-time">Time:</label>
                <input type="time" id="exam-time" name="examTime" required>

                <button type="submit">Create Examination</button>
            </form>
        </div>
    </section>

    <!-- Student Dashboard -->
    <section id="student-dashboard">
        <h2>Student Dashboard</h2>
        <div>
            <button onclick="viewExams()">View Exams</button>
            <button onclick="downloadHallTicket()">Download Hall Ticket</button>
        </div>

        <!-- Examination Form -->
        <div id="exam-form" style="display: none;">
            <h3>Fill Examination Form</h3>
            <form action="/student/submit-form" method="POST">
                <label for="student-name">Name:</label>
                <input type="text" id="student-name" name="studentName" required>

                <label for="student-id">Student ID:</label>
                <input type="text" id="student-id" name="studentID" required>

                <label for="exam-select">Select Examination:</label>
                <select id="exam-select" name="examID">
                    <option value="1">Mathematics</option>
                    <option value="2">Science</option>
                    <option value="3">History</option>
                </select>

                <button type="submit">Submit Form</button>
            </form>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <p>&copy; 2025 Examination Management System</p>
    </footer>

    <script>
        function addExamination() {
            document.getElementById("add-exam").style.display = "block";
        }

        function viewForms() {
            alert("Viewing all submitted forms (Demo Placeholder)");
        }

        function viewExams() {
            alert("Listing available exams (Demo Placeholder)");
        }

        function downloadHallTicket() {
            alert("Downloading hall ticket (Demo Placeholder)");
        }
    </script>
</body>
</html>
