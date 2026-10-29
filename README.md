
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Online Voting System</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header class="header">
        <h1>Online Voting System</h1>
        <p>Your Vote, Your Voice, Your Future</p>
    </header>

    <main>
        <!-- Welcome Page -->
        <section id="welcomePage" class="panel">
            <h2>Welcome to Online Voting</h2>
            <p>Cast your vote and make your choice count.</p>
            <button onclick="goToLogin()">Start Voting</button>
        </section>

        <!-- Login Page -->
        <section id="loginForm" class="panel hidden">
            <h2>Voter Login</h2>

            <form id="loginFormElement">
                <label for="username">Username</label>
                <input type="text" id="username" required>

                <label for="password">Password</label>
                <input type="password" id="password" required>

                <button type="submit">Login</button>
            </form>
        </section>

        <!-- Voting Page -->
        <section id="votingForm" class="panel hidden">
            <h2>Cast Your Vote</h2>
            <p>Enter your details and select one candidate.</p>

            <form id="voteForm">
                <label for="age">Age</label>
                <input type="number" id="age" min="1" max="120" required>

                <label for="code">Unique Voter Code</label>
                <input type="text" id="code" required>

                <h3>Select Your Candidate</h3>

                <div class="candidate-list">
                    <label class="candidate-card">
                        <input type="radio" name="candidate" value="TDP" required>
                        <img
                            src="https://th.bing.com/th/id/OIP.5xHPfsMU5yzPV_6t1p7RpwHaHa?rs=1&pid=ImgDetMain"
                            alt="TDP logo">
                        <span>TDP</span>
                        <small>Candidate A</small>
                    </label>

                    <label class="candidate-card">
                        <input type="radio" name="candidate" value="YCP">
                        <img
                            src="https://www.ysrcongress.com/sites/default/files/article_images/2020/03/13/YSRCP%20Logo-1.jpg"
                            alt="YCP logo">
                        <span>YCP</span>
                        <small>Candidate B</small>
                    </label>
                </div>

                <button type="submit">Submit Vote</button>
            </form>

            <button class="secondary" onclick="logout()">Logout</button>

            <button class="secondary"
                    onclick="window.open('vote-count.html', '_blank')">
                Show Vote Count
            </button>
        </section>

        <!-- Voter List -->
        <section id="voterListSection" class="panel hidden">
            <h2>Voter List</h2>
            <div id="voterList"></div>
        </section>
    </main>

    <footer>
        <p>Online Voting System | Educational Project</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>

