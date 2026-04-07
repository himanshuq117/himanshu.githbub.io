<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PAWS (Protecting Animals With Support)</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        : root {
            --primary-color: #940c00f1;
            --primary-dark: #e65c50;
            --secondary-color: #4a90e2;
            --light-gray: #f5f5f5;
            --medium-gray: #e0e0e0;
            --dark-gray: #333;
            --white: #ffffff;
            --success-color: #4caf50;
            --error-color: #f44336;
        }

        * {
            box-sizing: border-box;
            margin: 0.1;
            padding: 0.1;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: var(--dark-gray);
            background-color: var(--light-gray);
        }

        header {
            background-color: var(--primary-color);
            color: var(--white);
            padding: 1.5rem 0;
            text-align: center;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }

        header h1 {
            font-size: 2.2rem;
            margin-bottom: 1rem;
        }

        nav ul {
            list-style: none;
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 1.5rem;
            padding: 0 1rem;
        }

        nav ul li a {
            color: var(--white);
            text-decoration: none;
            font-weight: 600;
            font-size: 1.1rem;
            transition: all 0.3s ease;
            padding: 0.5rem 1rem;
            border-radius: 4px;
        }

        nav ul li a:hover {
            background-color: rgba(155, 66, 66, 0.2);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 1rem;
        }

        .section {
            background-color: var(--white);
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            margin: 2rem auto;
            padding: 2rem;
            max-width: 900px;
        }

        .section h2 {
            color: var(--primary-color);
            margin-bottom: 1.5rem;
            font-size: 1.8rem;
            text-align: center;
        }

        .btn {
            background-color: var(--primary-color);
            color: var(--white);
            border: none;
            padding: 0.8rem 1.5rem;
            font-size: 1rem;
            font-weight: 600;
            border-radius: 4px;
            cursor: pointer;
            transition: all 0.3s ease;
            display: inline-block;
            text-align: center;
            margin: 1rem auto;
        }

        .btn:hover {
            background-color: var(--primary-dark);
            transform: translateY(-2px);
        }

        .btn-secondary {
            background-color: var(--secondary-color);
        }

        .btn-secondary:hover {
            background-color: #3a7bc8;
        }

        .hidden {
            display: none;
        }

        form {
            display: flex;
            flex-direction: column;
            gap: 1.2rem;
            max-width: 600px;
            margin: 0 auto;
        }

        .form-group {
            display: flex;
            flex-direction: column;
            gap: 0.5rem;
        }

        label {
            font-weight: 600;
            color: var(--dark-gray);
        }

        input, textarea, select {
            padding: 0.8rem;
            border: 1px solid var(--medium-gray);
            border-radius: 4px;
            font-size: 1rem;
            transition: border 0.3s ease;
        }

        input:focus, textarea:focus, select:focus {
            outline: none;
            border-color: var(--primary-color);
            box-shadow: 0 0 0 2px rgba(255, 111, 97, 0.2);
        }

        textarea {
            min-height: 120px;
            resize: vertical;
        }

        .error-message {
            color: var(--error-color);
            font-size: 0.9rem;
            margin-top: 0.2rem;
            display: none;
        }

        .success-message {
            background-color: rgba(76, 175, 80, 0.1);
            color: var(--success-color);
            padding: 1rem;
            border-radius: 4px;
            margin: 1rem 0;
            text-align: center;
            display: none;
        }

        footer {
            background-color: var(--dark-gray);
            color: var(--white);
            text-align: center;
            padding: 1.5rem;
            margin-top: 2rem;
        }

        .admin-section {
            margin-top: 2rem;
            padding: 1rem;
            border-top: 1px solid var(--medium-gray);
        }

        .admin-btn {
            background-color: var(--dark-gray);
            margin-top: 1rem;
        }

        .data-display {
            margin-top: 1rem;
            max-height: 300px;
            overflow-y: auto;
            border: 1px solid var(--medium-gray);
            padding: 1rem;
            border-radius: 4px;
            background-color: var(--light-gray);
        }

        @media (max-width: 768px) {
            header h1 {
                font-size: 1.8rem;
            }
            
            nav ul {
                gap: 0.8rem;
            }
            
            .section {
                padding: 1.5rem;
            }
        }

        /* Animation for form display */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .form-container {
            animation: fadeIn 0.3s ease-out forwards;
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <h1><i class="fas fa-paw"></i> PAWS (Protecting Animals With Support)</h1>
            <nav>
                <ul>
                    <li><a href="#report"><i class="fas fa-exclamation-circle"></i> Report</a></li>
                    <li><a href="#adopt"><i class="fas fa-home"></i> Adopt</a></li>
                    <li><a href="#volunteer"><i class="fas fa-hands-helping"></i> Volunteer</a></li>
                    <li><a href="#donate"><i class="fas fa-donate"></i> Donate</a></li>
                    <li><a href="#contact"><i class="fas fa-envelope"></i> Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <main class="container">
        <!-- Report Section -->
        <section id="report" class="section">
            <h2><i class="fas fa-exclamation-triangle"></i> Report an Animal</h2>
            <p>Help us protect animals by reporting lost pets, animals in danger, or deceased animals in Our Campus.</p>
            <button class="btn" onclick="showForm('reportForm')">Report Now</button>
            
            <div id="reportForm" class="hidden form-container">
                <div id="reportSuccess" class="success-message"></div>
                <form id="reportAnimalForm">
                    <div class="form-group">
                        <label for="reporterName">Your Name:</label>
                        <input type="text" id="reporterName" name="reporterName" required>
                        <div class="error-message" id="reporterNameError">Please enter your name</div>
                    </div>
                    
                    <div class="form-group">
                        <label for="reporterContact">Your Contact Info (Email or Phone):</label>
                        <input type="text" id="reporterContact" name="reporterContact" required>
                        <div class="error-message" id="reporterContactError">Please enter your contact information</div>
                    </div>
                    
                    <div class="form-group">
                        <label for="reportType">Type of Report:</label>
                        <select id="reportType" name="reportType" required>
                            <option value="">Select a report type</option>
                            <option value="lost">Lost Pet</option>
                            <option value="dead">Dead Animal</option>
                            <option value="threat">Animal in Danger</option>
                        </select>
                        <div class="error-message" id="reportTypeError">Please select a report type</div>
                    </div>

                    <div class="form-group">
                        <label for="animalLocation">Location:</label>
                        <input type="text" id="animalLocation" name="animalLocation" placeholder="Where was the animal seen?" required>
                        <div class="error-message" id="animalLocationError">Please provide a location</div>
                    </div>

                    <div class="form-group">
                        <label for="reportDetails">Details:</label>
                        <textarea id="reportDetails" name="reportDetails" placeholder="Please describe the situation in detail..." required></textarea>
                        <div class="error-message" id="reportDetailsError">Please provide details</div>
                    </div>
                    
                    <div class="form-group">
                        <label for="reportPhoto">Upload Photo (optional):</label>
                        <input type="file" id="reportPhoto" name="reportPhoto" accept="image/*">
                    </div>
                    
                    <button type="submit" class="btn">Submit Report</button>
                </form>
            </div>
        </section>
        
        <!-- Adopt Section -->
        <section id="adopt" class="section">
            <h2><i class="fas fa-home"></i> Adopt a Pet</h2>
            <p>Give a loving home to animals in need. Browse our available pets or apply for adoption.</p>
            <button class="btn" onclick="showForm('adoptForm')">Apply for Adoption</button>
            <div id="adoptForm" class="hidden form-container">
                <div id="adoptSuccess" class="success-message"></div>
                <form id="adoptionForm">
                    <div class="form-group">
                        <label for="adopterName">Your Name:</label>
                        <input type="text" id="adopterName" name="adopterName" required>
                        <div class="error-message" id="adopterNameError">Please enter your name</div>
                    </div>
                    
                    <div class="form-group">
                        <label for="adopterContact">Your Contact Info (Email or Phone):</label>
                        <input type="text" id="adopterContact" name="adopterContact" required>
                        <div class="error-message" id="adopterContactError">Please enter your contact information</div>
                    </div>
                    
                    <div class="form-group">
                        <label for="petPreference">Preferred Pet (Species/Breed):</label>
                        <input type="text" id="petPreference" name="petPreference" placeholder="e.g., Labrador Retriever, Siamese Cat" required>
                        <div class="error-message" id="petPreferenceError">Please specify your pet preference</div>
                    </div>
                    
                    <div class="form-group">
                        <label for="adoptionReason">Why do you want to adopt?</label>
                        <textarea id="adoptionReason" name="adoptionReason" placeholder="Tell us about your home, experience with pets, and why you want to adopt..." required></textarea>
                        <div class="error-message" id="adoptionReasonError">Please explain why you want to adopt</div>
                    </div>
                    
                    <div class="form-group">
                        <label for="housingType">Housing Type:</label>
                        <select id="housingType" name="housingType" required>
                            <option value="">Select your housing type</option>
                            <option value="house">House</option>
                            <option value="apartment">Apartment</option>
                            <option value="condo">Condo</option>
                            <option value="other">Other</option>
                        </select>
                        <div class="error-message" id="housingTypeError">Please select your housing type</div>
                    </div>
                    
                    <button type="submit" class="btn">Submit Adoption Request</button>
                </form>
            </div>
        </section>
        
        <!-- Volunteer Section -->
        <section id="volunteer" class="section">
            <h2><i class="fas fa-hands-helping"></i> Volunteer With Us</h2>
            <p>Join our team of dedicated volunteers helping animals in need.</p>
            <button class="btn" onclick="showForm('volunteerForm')">Volunteer Application</button>
            <div id="volunteerForm" class="hidden form-container">
                <div id="volunteerSuccess" class="success-message"></div>
                <form id="volunteerApplicationForm">
                    <div class="form-group">
                        <label for="volunteerName">Your Name:</label>
                        <input type="text" id="volunteerName" name="volunteerName" required>
                        <div class="error-message" id="volunteerNameError">Please enter your name</div>
                    </div>
                    
                    <div class="form-group">
                        <label for="volunteerEmail">Your Email:</label>
                        <input type="email" id="volunteerEmail" name="volunteerEmail" required>
                        <div class="error-message" id="volunteerEmailError">Please enter a valid email</div>
                    </div>
                    
                    <div class="form-group">
                        <label for="volunteerPhone">Phone Number:</label>
                        <input type="tel" id="volunteerPhone" name="volunteerPhone" required>
                        <div class="error-message" id="volunteerPhoneError">Please enter your phone number</div>
                    </div>
                    
                    <div class="form-group">
                        <label for="volunteerSkills">Skills/Experience:</label>
                        <textarea id="volunteerSkills" name="volunteerSkills" placeholder="Any relevant skills or experience with animals..." required></textarea>
                        <div class="error-message" id="volunteerSkillsError">Please describe your skills</div>
                    </div>
                    
                    <div class="form-group">
                        <label for="volunteerAvailability">Availability:</label>
                        <textarea id="volunteerAvailability" name="volunteerAvailability" placeholder="When are you available to volunteer?" required></textarea>
                        <div class="error-message" id="volunteerAvailabilityError">Please provide your availability</div>
                    </div>
                    
                    <button type="submit" class="btn">Submit Application</button>
                </form>
            </div>
        </section>
        
        <!-- Donate Section -->
        <section id="donate" class="section">
            <h2><i class="fas fa-donate"></i> Make a Donation</h2>
            <p>Your generous donations help us care for animals in need.</p>
            <button class="btn" onclick="showForm('donationForm')">Donate Now</button>
            <div id="donationForm" class="hidden form-container">
                <div id="donationSuccess" class="success-message"></div>
                <form id="donationFormElement">
                    <div class="form-group">
                        <label for="donorName">Your Name:</label>
                        <input type="text" id="donorName" name="donorName" required>
                        <div class="error-message" id="donorNameError">Please enter your name</div>
                    </div>
                    
                    <div class="form-group">
                        <label for="donorEmail">Your Email:</label>
                        <input type="email" id="donorEmail" name="donorEmail" required>
                        <div class="error-message" id="donorEmailError">Please enter a valid email</div>
                    </div>
                    
                    <div class="form-group">
                        <label for="donationAmount">Donation Amount (₹):</label>
                        <input type="number" id="donationAmount" name="donationAmount" min="1" step="1" required>
                        <div class="error-message" id="donationAmountError">Please enter a valid amount</div>
                    </div>
                    
                    <div class="form-group">
                        <label for="donationFrequency">Donation Frequency:</label>
                        <select id="donationFrequency" name="donationFrequency" required>
                            <option value="">Select frequency</option>
                            <option value="one-time">One-time</option>
                            <option value="monthly">Monthly</option>
                            <option value="quarterly">Quarterly</option>
                            <option value="yearly">Yearly</option>
                        </select>
                        <div class="error-message" id="donationFrequencyError">Please select donation frequency</div>
                    </div>
                    
                    <div class="form-group">
                        <label for="donationMessage">Message (optional):</label>
                        <textarea id="donationMessage" name="donationMessage" placeholder="Any special instructions or dedication..."></textarea>
                    </div>
                    
                    <button type="submit" class="btn">Proceed to Payment</button>
                </form>
            </div>
        </section>
        
        <!-- Contact Section -->
        <section id="contact" class="section">
            <h2><i class="fas fa-envelope"></i> Contact Us</h2>
            <p>Have questions? Reach out to our team for more information.</p>
            <button class="btn" onclick="showForm('contactForm')">Send a Message</button>
            <div id="contactForm" class="hidden form-container">
                <div id="contactSuccess" class="success-message"></div>
                <form id="contactFormElement">
                    <div class="form-group">
                        <label for="contactName">Your Name:</label>
                        <input type="text" id="contactName" name="contactName" required>
                        <div class="error-message" id="contactNameError">Please enter your name</div>
                    </div>
                    
                    <div class="form-group">
                        <label for="contactEmail">Your Email:</label>
                        <input type="email" id="contactEmail" name="contactEmail" required>
                        <div class="error-message" id="contactEmailError">Please enter a valid email</div>
                    </div>
                    
                    <div class="form-group">
                        <label for="contactSubject">Subject:</label>
                        <input type="text" id="contactSubject" name="contactSubject" required>
                        <div class="error-message" id="contactSubjectError">Please enter a subject</div>
                    </div>
                    
                    <div class="form-group">
                        <label for="contactMessage">Message:</label>
                        <textarea id="contactMessage" name="contactMessage" required></textarea>
                        <div class="error-message" id="contactMessageError">Please enter your message</div>
                    </div>
                    
                    <button type="submit" class="btn">Send Message</button>
                </form>
            </div>
        </section>

        <!-- Admin Section (Hidden by default) -->
        <section id="admin" class="section hidden">
            <h2><i class="fas fa-lock"></i> Admin Panel</h2>
            <div class="admin-section">
                <h3>View Submitted Data</h3>
                <select id="dataTypeSelect">
                    <option value="">Select data type to view</option>
                    <option value="reports">Animal Reports</option>
                    <option value="adoptions">Adoption Applications</option>
                    <option value="volunteers">Volunteer Applications</option>
                    <option value="donations">Donations</option>
                    <option value="contacts">Contact Messages</option>
                </select>
                <button class="btn admin-btn" onclick="viewData()">View Data</button>
                <button class="btn admin-btn" onclick="clearAllData()">Clear All Data</button>
                <div id="dataDisplay" class="data-display"></div>
            </div>
        </section>

        <!-- Admin Access Button -->
        <button id="adminAccessBtn" class="btn admin-btn" onclick="toggleAdminPanel()">Admin Access</button>
    </main>

    <footer>
        <div class="container">
            <p>&copy; Project 2025 PAWS (Protecting Animals With Support). All rights reserved.</p>
            <p><i class="fas fa-phone"></i> (+91) 9355179735 | <i class="fas fa-envelope"></i> info@paws.org</p>
            <div class="social-icons" style="margin-top: 1rem;">
                <a href="#" style="color: white; margin: 0 10px;"><i class="fab fa-facebook-f"></i></a>
                <a href="#" style="color: white; margin: 0 10px;"><i class="fab fa-twitter"></i></a>
                <a href="#" style="color: white; margin: 0 10px;"><i class="fab fa-instagram"></i></a>
            </div>
        </div>
    </footer>

    <script>
        // Data storage using localStorage
        const storageKeys = {
            reports: 'paws_animal_reports',
            adoptions: 'paws_adoption_applications',
            volunteers: 'paws_volunteer_applications',
            donations: 'paws_donations',
            contacts: 'paws_contact_messages'
        };

        // Initialize data storage if not exists
        function initializeStorage() {
            for (const key in storageKeys) {
                if (!localStorage.getItem(storageKeys[key])) {
                    localStorage.setItem(storageKeys[key], JSON.stringify([]));
                }
            }
        }

        // Show/hide forms
        function showForm(formId) {
            document.querySelectorAll('.form-container').forEach(form => {
                form.classList.add('hidden');
            });
            document.getElementById(formId).classList.remove('hidden');
            // Scroll to the form
            document.getElementById(formId).scrollIntoView({ behavior: 'smooth' });
        }

        // Toggle admin panel
        function toggleAdminPanel() {
            const adminPanel = document.getElementById('admin');
            const adminBtn = document.getElementById('adminAccessBtn');
            
            if (adminPanel.classList.contains('hidden')) {
                const password = prompt('Enter admin password:');
                if (password === 'himanshu448') { // Simple password protection
                    adminPanel.classList.remove('hidden');
                    adminBtn.textContent = 'Hide Admin Panel';
                } else {
                    alert('Incorrect password');
                }
            } else {
                adminPanel.classList.add('hidden');
                adminBtn.textContent = 'Admin Access';
            }
        }

        // View stored data
        function viewData() {
            const dataType = document.getElementById('dataTypeSelect').value;
            if (!dataType) return;
            
            const data = JSON.parse(localStorage.getItem(storageKeys[dataType])) || [];
            const dataDisplay = document.getElementById('dataDisplay');
            
            if (data.length === 0) {
                dataDisplay.innerHTML = '<p>No data found for this category.</p>';
                return;
            }
            
            let html = '<ul>';
            data.forEach((item, index) => {
                html += '<li>';
                html += `<strong>Entry ${index + 1}:</strong><br>`;
                for (const key in item) {
                    html += `<strong>${key}:</strong> ${item[key]}<br>`;
                }
                html += '</li><hr>';
            });
            html += '</ul>';
            
            dataDisplay.innerHTML = html;
        }

        // Clear all data (for admin)
        function clearAllData() {
            if (confirm('Are you sure you want to clear all data? This cannot be undone.')) {
                for (const key in storageKeys) {
                    localStorage.setItem(storageKeys[key], JSON.stringify([]));
                }
                document.getElementById('dataDisplay').innerHTML = '<p>All data has been cleared.</p>';
            }
        }

        // Form validation
        function validateForm(formId) {
            const form = document.getElementById(formId);
            const inputs = form.querySelectorAll('input[required], textarea[required], select[required]');
            let isValid = true;
            
            inputs.forEach(input => {
                const errorId = `${input.id}Error`;
                const errorElement = document.getElementById(errorId);
                
                if (!input.value.trim()) {
                    errorElement.style.display = 'block';
                    input.style.borderColor = 'var(--error-color)';
                    isValid = false;
                } else {
                    errorElement.style.display = 'none';
                    input.style.borderColor = 'var(--medium-gray)';
                }
                
                // Special validation for email fields
                if (input.type === 'email' && input.value.trim()) {
                    const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
                    if (!emailRegex.test(input.value)) {
                        document.getElementById(errorId).style.display = 'block';
                        input.style.borderColor = 'var(--error-color)';
                        isValid = false;
                    }
                }
            });
            
            return isValid;
        }

        // Form submission handlers
        function setupFormSubmit(formId, storageKey, successMessageId) {
            const form = document.getElementById(formId);
            
            form.addEventListener('submit', function(e) {
                e.preventDefault();
                
                if (!validateForm(formId)) return;
                
                const formData = {};
                const inputs = form.querySelectorAll('input, textarea, select');
                
                inputs.forEach(input => {
                    if (input.type !== 'button' && input.type !== 'submit') {
                        formData[input.name] = input.value;
                    }
                });
                
                // Add timestamp
                formData.timestamp = new Date().toISOString();
                
                // Save to localStorage
                const existingData = JSON.parse(localStorage.getItem(storageKey)) || [];
                existingData.push(formData);
                localStorage.setItem(storageKey, JSON.stringify(existingData));
                
                // Show success message
                const successMessage = document.getElementById(successMessageId);
                successMessage.textContent = 'Thank you! Your submission has been received.';
                successMessage.style.display = 'block';
                
                // Reset form
                form.reset();
                
                // Hide success message after 5 seconds
                setTimeout(() => {
                    successMessage.style.display = 'none';
                }, 5000);
            });
        }

        // Initialize the page
        document.addEventListener('DOMContentLoaded', function() {
            initializeStorage();
            
            // Set up form submissions
            setupFormSubmit('reportAnimalForm', storageKeys.reports, 'reportSuccess');
            setupFormSubmit('adoptionForm', storageKeys.adoptions, 'adoptSuccess');
            setupFormSubmit('volunteerApplicationForm', storageKeys.volunteers, 'volunteerSuccess');
            setupFormSubmit('donationFormElement', storageKeys.donations, 'donationSuccess');
            setupFormSubmit('contactFormElement', storageKeys.contacts, 'contactSuccess');
            
            // Smooth scrolling for navigation
            document.querySelectorAll('nav a').forEach(anchor => {
                anchor.addEventListener('click', function(e) {
                    e.preventDefault();
                    const targetId = this.getAttribute('href');
                    document.querySelector(targetId).scrollIntoView({
                        behavior: 'smooth'
                    });
                });
            });
        });
    </script>
</body>
</html>
