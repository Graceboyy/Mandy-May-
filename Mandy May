<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MANDY MAY Meet Up With Fan</title>
    <style>
        .page {
            display: none;
        }
        .active {
            display: block;
        }
    </style>
</head>
<body>
    <header>
        <h1>MANDY MAY Meet Up With Fan</h1>
    </header>

    <!-- Page 1: Sign Up -->
    <div id="page1" class="page active">
        <h2>Sign Up</h2>
        <form id="signupForm">
            <label>Full Name: <input type="text" id="fullname" required></label><br>
            <label>Username: <input type="text" id="signupUsername" required></label><br>
            <label>Email Address: <input type="email" id="email" required></label><br>
            <label>Password: <input type="password" id="signupPassword" required></label><br>
            <label>Confirm Password: <input type="password" id="confirmPassword" required></label><br>
            <button type="button" onclick="signup()">Sign Up</button>
        </form>
    </div>

    <!-- Page 2: Login -->
    <div id="page2" class="page">
        <h2>Login</h2>
        <form id="loginForm">
            <label>Username: <input type="text" id="loginUsername" required></label><br>
            <label>Password: <input type="password" id="loginPassword" required></label><br>
            <button type="button" onclick="login()">Login</button>
        </form>
    </div>

    <!-- Page 3: Select State and City -->
    <div id="page3" class="page">
        <h2>Select Your State and City</h2>
        <label for="state">State:</label>
        <select id="state" onchange="populateCities()">
            <option value="">Select State</option>
            <option value="AL">Alabama</option>
            <option value="AK">Alaska</option>
            <option value="AZ">Arizona</option>
            <option value="AR">Arkansas</option>
            <option value="CA">California</option>
            <option value="CO">Colorado</option>
            <option value="CT">Connecticut</option>
            <option value="DE">Delaware</option>
            <option value="FL">Florida</option>
            <option value="GA">Georgia</option>
            <option value="HI">Hawaii</option>
            <option value="ID">Idaho</option>
            <option value="IL">Illinois</option>
            <option value="IN">Indiana</option>
            <option value="IA">Iowa</option>
            <option value="KS">Kansas</option>
            <option value="KY">Kentucky</option>
            <option value="LA">Louisiana</option>
            <option value="ME">Maine</option>
            <option value="MD">Maryland</option>
            <option value="MA">Massachusetts</option>
            <option value="MI">Michigan</option>
            <option value="MN">Minnesota</option>
            <option value="MS">Mississippi</option>
            <option value="MO">Missouri</option>
            <option value="MT">Montana</option>
            <option value="NE">Nebraska</option>
            <option value="NV">Nevada</option>
            <option value="NH">New Hampshire</option>
            <option value="NJ">New Jersey</option>
            <option value="NM">New Mexico</option>
            <option value="NY">New York</option>
            <option value="NC">North Carolina</option>
            <option value="ND">North Dakota</option>
            <option value="OH">Ohio</option>
            <option value="OK">Oklahoma</option>
            <option value="OR">Oregon</option>
            <option value="PA">Pennsylvania</option>
            <option value="RI">Rhode Island</option>
            <option value="SC">South Carolina</option>
            <option value="SD">South Dakota</option>
            <option value="TN">Tennessee</option>
            <option value="TX">Texas</option>
            <option value="UT">Utah</option>
            <option value="VT">Vermont</option>
            <option value="VA">Virginia</option>
            <option value="WA">Washington</option>
            <option value="WV">West Virginia</option>
            <option value="WI">Wisconsin</option>
            <option value="WY">Wyoming</option>
            <option value="DC">District of Columbia</option>
            <option value="AS">American Samoa</option>
            <option value="GU">Guam</option>
            <option value="MP">Northern Mariana Islands</option>
            <option value="PR">Puerto Rico</option>
            <option value="UM">United States Minor Outlying Islands</option>
            <option value="VI">Virgin Islands, U.S.</option>
        </select><br>
        <label for="city">City:</label>
        <select id="city">
            <option value="">Select City</option>
        </select><br>
        <button type="button" onclick="goToPage(4)">Next</button>
    </div>

    <!-- Page 4: Fill Address -->
    <div id="page4" class="page">
        <h2>Enter Your Address</h2>
        <label>Address: <input type="text" id="address" required></label><br>
        <button type="button" onclick="goToPage(5)">Next</button>
    </div>

    <!-- Page 5: Application Notice -->
    <div id="page5" class="page">
        <h2>Apply for MANDY MAY Meet Up With Fans</h2>
        <p>You are about to apply for MANDY MAY Meet Up With Fans.</p>
        <button type="button" onclick="goToPage(6)">Continue</button>
    </div>

    <!-- Page 6: Information & Agreement -->
    <div id="page6" class="page">
        <h2>Application Information</h2>
        <p>Thank you for your enthusiasm and interest in meeting MANDY MAY. We are excited to announce an exclusive opportunity for fans like you to apply for a personal meet-and-greet.</p>
        <button type="button" onclick="goToPage(7)">Next</button>
    </div>

    <!-- Page 7: Application Fee Notice -->
    <div id="page7" class="page">
        <h2>Application Fee</h2>
        <p>Please note that there is a $100 application fee for this event. This fee helps us manage and organize the event to ensure an unforgettable experience for all participants.</p>
        <button type="button" onclick="agree()">I Agree</button>
    </div>

    <!-- Page 8: Final Confirmation -->
    <div id="page8" class="page">
        <h2>Final Confirmation</h2>
        <p>Your application has been submitted successfully!</p>
    </div>

    <script>
        let users = {};

        function goToPage(pageNumber) {
            document.querySelectorAll('.page').forEach(page => page.classList.remove('active'));
            document.getElementById(`page${pageNumber}`).classList.add('active');
        }

        function signup() {
            const fullname = document.getElementById('fullname').value;
            const username = document.getElementById('signupUsername').value;
            const email = document.getElementById('email').value;
            const password = document.getElementById('signupPassword').value;
            const confirmPassword = document.getElementById('confirmPassword').value;

            if (password !== confirmPassword) {
                alert('Passwords do not match.');
                return;
            }

            users[username] = { fullname, email, password };
            alert('Sign up successful!');
            goToPage(2);
        }

        function login() {
            const username = document.getElementById('loginUsername').value;
            const password = document.getElementById('loginPassword').value;

            if (users[username] && users[username].password === password) {
                goToPage(3);
            } else {
                alert('Invalid username or password.');
            }
        }

        function populateCities() {
            const state = document.getElementById('state').value;
            const citySelect = document.getElementById('city');
            citySelect.innerHTML = '<option value="">Select City</option>';

            const cities = {
                "AL": ["Birmingham", "Montgomery", "Mobile", "Huntsville", "Tuscaloosa"],
                "AK": ["Anchorage", "Juneau", "Fairbanks", "Sitka", "Ketchikan"],
                "AZ
