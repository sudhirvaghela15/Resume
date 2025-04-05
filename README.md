<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sudhir Vaghela - iOS Developer Resume</title>
    <style>
        /* Google Fonts */
        @import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@400;600;700&family=Roboto+Condensed:wght@700&display=swap');
        
        :root {
            --primary: #2C3E50;
            --secondary: #3498db;
            --light-bg: #f8f9fa;
            --dark-text: #333;
            --light-text: #777;
        }
        
        body {
            font-family: 'Open Sans', sans-serif;
            line-height: 1.6;
            color: var(--dark-text);
            margin: 0;
            padding: 0;
            background-color: #f5f5f5;
        }
        
        .resume-container {
            max-width: 1000px;
            margin: 30px auto;
            display: flex;
            box-shadow: 0 0 25px rgba(0,0,0,0.1);
            background: white;
        }
        
        /* Left Column */
        .left-column {
            flex: 30%;
            background: var(--primary);
            color: white;
            padding: 40px 30px;
        }
        
        .profile-header h1 {
            font-family: 'Roboto Condensed', sans-serif;
            font-size: 28px;
            margin-bottom: 5px;
            color: white;
        }
        
        .profile-header h2 {
            font-size: 16px;
            font-weight: 400;
            margin-top: 0;
            color: #ecf0f1;
        }
        
        .contact-info {
            margin: 30px 0;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            margin-bottom: 15px;
        }
        
        .contact-icon {
            margin-right: 12px;
            color: var(--secondary);
            width: 20px;
            text-align: center;
        }
        
        .section-title {
            font-family: 'Roboto Condensed', sans-serif;
            font-size: 20px;
            color: var(--secondary);
            border-bottom: 2px solid rgba(52, 152, 219, 0.3);
            padding-bottom: 8px;
            margin: 30px 0 20px 0;
        }
        
        .skills-list {
            margin-bottom: 30px;
        }
        
        .skill-item {
            margin-bottom: 15px;
        }
        
        .skill-name {
            display: flex;
            justify-content: space-between;
            margin-bottom: 5px;
            font-size: 14px;
        }
        
        .skill-bar {
            height: 8px;
            background: rgba(255,255,255,0.2);
            border-radius: 4px;
            overflow: hidden;
        }
        
        .skill-level {
            height: 100%;
            background: var(--secondary);
            border-radius: 4px;
        }
        
        .education-item {
            margin-bottom: 20px;
        }
        
        .education-item h3 {
            font-size: 16px;
            margin-bottom: 5px;
        }
        
        .education-item p {
            font-size: 14px;
            margin: 5px 0;
            color: #ecf0f1;
        }
        
        .strengths-list {
            list-style-type: none;
            padding-left: 0;
        }
        
        .strengths-list li {
            position: relative;
            padding-left: 25px;
            margin-bottom: 10px;
            font-size: 14px;
        }
        
        .strengths-list li:before {
            content: "✓";
            color: var(--secondary);
            position: absolute;
            left: 0;
        }
        
        /* Right Column */
        .right-column {
            flex: 70%;
            padding: 40px 30px;
        }
        
        .summary {
            margin-bottom: 30px;
            font-size: 15px;
            line-height: 1.7;
        }
        
        .experience-item {
            margin-bottom: 30px;
        }
        
        .experience-header {
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
        }
        
        .experience-header h3 {
            font-size: 18px;
            margin: 0;
            color: var(--primary);
        }
        
        .experience-header .date {
            color: var(--light-text);
            font-weight: 600;
        }
        
        .company {
            font-weight: 600;
            color: var(--primary);
            margin-bottom: 10px;
        }

        .company:hover {
            background-color: #b0aeae53;
            transform: translateY(-2px);
        }
        
        .company:active {
            transform: translateY(0);
        }
        
        .experience-details {
            list-style-type: none;
            padding-left: 0;
        }
        
        .experience-details li {
            position: relative;
            padding-left: 25px;
            margin-bottom: 8px;
            font-size: 14px;
        }
        
        .experience-details li:before {
            content: "•";
            color: var(--secondary);
            position: absolute;
            left: 10px;
            font-size: 20px;
            line-height: 0;
        }
        
        .project-item {
            margin-bottom: 20px;
        }
        
        .project-header {
            display: flex;
            justify-content: space-between;
            margin-bottom: 5px;
        }
        
        .project-header h3 {
            font-size: 16px;
            margin: 0;
            color: var(--primary);
        }
        
        .project-description {
            font-size: 14px;
            margin: 0;
        }
        
        .testing-experience {
            margin-top: 30px;
        }
        
        .testing-list {
            list-style-type: none;
            padding-left: 0;
        }
        
        .testing-list li {
            position: relative;
            padding-left: 25px;
            margin-bottom: 8px;
            font-size: 14px;
        }
        
        .testing-list li:before {
            content: "▹";
            color: var(--secondary);
            position: absolute;
            left: 0;
        }
        
        .references {
            font-style: italic;
            color: var(--light-text);
            font-size: 14px;
            margin-top: 30px;
        }
/* linkedin and git hub stypes */
        .profile-links a {
           color: #0077b5; /* LinkedIn blue - change as needed */
           text-decoration: none;
           font-weight: 500;
           padding: 0 2px;
           transition: all 0.2s ease;
        }

        .profile-links a:first-child {
           color: #0077b5; /* LinkedIn blue */
        }
  
        .profile-links a:last-child {
            color: #fff; /* GitHub black */
        }
  
        .profile-links a:hover {
            opacity: 0.8;
            text-decoration: underline;
            text-underline-offset: 3px;
        }
        
        .profile-links a:active {
            transform: scale(0.98);
        }

/* App store badge */

        .app-store-badge {
            display: inline-block;
            background-color: #000;
            color: #fff;
            text-decoration: none;
            padding: 4px 8px;
            border-radius: 8px;
            font-weight: 500;
            font-size: 14px;
            font-weight: bold;
            transition: all 0.3s ease;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        .nike-app-link {
            font-family: 'Helvetica Neue', Arial, sans-serif;
            display: inline-block;
        }
    
        .nike-app-link h3 {
            color: #111;
            margin-bottom: 12px;
            font-size: 18px;
            font-weight: 600;
        }
        
        .app-store-badge span {
            position: relative;
            display: inline-block;
        }
        
        .app-store-badge:hover {
            background-color: #333;
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(0,0,0,0.15);
        }
        
        .app-store-badge:active {
            transform: translateY(0);
            box-shadow: 0 2px 3px rgba(0,0,0,0.1);
        }
        
    </style>
</head>
<body>
    <div class="resume-container">
        <!-- Left Column -->
        <div class="left-column">
            <div class="profile-header">
                <h1>Sudhir Vaghela</h1>
                <h2>iOS Developer</h2>
            </div>
            
            <div class="contact-info">
                <div class="contact-item">
                    <span class="contact-icon">📍</span>
                    <span>Ahmedabad, India</span>
                </div>
                <div class="contact-item">
                    <span class="contact-icon">📞</span>
                    <span>+91 70165 77536</span>
                </div>
                <div class="contact-item">
                    <span class="contact-icon">📧</span>
                    <span>sudhirvaghela15@hotmail.com</span>
                </div>
                <div class="contact-item">
                    <span class="contact-icon">🔗</span>
                    <!-- <span>LinkedIn | GitHub</span> -->
                    <span class="profile-links">
                        <a href="https://www.linkedin.com/in/your-profile" target="_blank">LinkedIn</a> | 
                        <a href="https://github.com/your-username" target="_blank">GitHub</a>
                      </span>
                </div>
            </div>
            
            <h3 class="section-title">Technical Skills</h3>
            <div class="skills-list">
                <div class="skill-item">
                    <div class="skill-name">
                        <span>Swift</span>
                        <span>90%</span>
                    </div>
                    <div class="skill-bar">
                        <div class="skill-level" style="width: 90%;"></div>
                    </div>
                </div>
                <div class="skill-item">
                    <div class="skill-name">
                        <span>UIKit</span>
                        <span>85%</span>
                    </div>
                    <div class="skill-bar">
                        <div class="skill-level" style="width: 85%;"></div>
                    </div>
                </div>
                <div class="skill-item">
                    <div class="skill-name">
                        <span>SwiftUI</span>
                        <span>55%</span>
                    </div>
                    <div class="skill-bar">
                        <div class="skill-level" style="width: 75%;"></div>
                    </div>
                </div>
                <div class="skill-item">
                    <div class="skill-name">
                        <span>XCTest</span>
                        <span>80%</span>
                    </div>
                    <div class="skill-bar">
                        <div class="skill-level" style="width: 80%;"></div>
                    </div>
                </div>
           
            </div>
            
            <h3 class="section-title">Languages</h3>
            <div class="skills-list">
                <div class="skill-item">
                    <div class="skill-name">
                        <span>Swift</span>
                    </div>
                </div>
                <div class="skill-item">
                    <div class="skill-name">
                        <span>Java</span>
                    </div>
                </div>
                <div class="skill-item">
                    <div class="skill-name">
                        <span>Kotlin</span>
                    </div>
                </div>
                <div class="skill-item">
                    <div class="skill-name">
                        <span>Dart</span>
                    </div>
                </div>
                <div class="skill-item">
                    <div class="skill-name">
                        <span>C/C++</span>
                    </div>
                </div>
            </div>
            
            <h3 class="section-title">Education</h3>
            <div class="education-item">
                <h3>M.Sc. IT</h3>
                <p>Mobile Apps & UI Development</p>
                <p>Gujarat University, 2022</p>
            </div>
            <div class="education-item">
                <h3>B.C.A.</h3>
                <p>Computer Applications</p>
                <p>L.J.C.C.A, Gujarat University, 2018</p>
            </div>
            
            <h3 class="section-title">Core Strengths</h3>
            <ul class="strengths-list">
                <li>Strong debugging & analytical skills</li>
                <li>Clean, modular, and testable code</li>
                <li>Excellent communicator & collaborator</li>
                <li>Fast learner with proactive mindset</li>
                <li>Focused on performance and UX</li>
            </ul>
        </div>
        
        <!-- Right Column -->
        <div class="right-column">
            <h3 class="section-title">Professional Summary</h3>
            <div class="summary">
                <p>Detail-oriented and passionate iOS Developer with 3 years of experience building high-quality mobile apps using Swift and UIKit. Adept in MVC, MVVM, and Clean Swift architectures with a strong grasp of REST APIs, Firebase, and third-party SDKs. Skilled in writing unit and UI tests using XCTest & XCUITest to ensure code reliability. Proven record of delivering apps featured on the App Store. Seeking to contribute to a forward-thinking product team.</p>
            </div>
            
            <h3 class="section-title">Work Experience</h3>
            <div class="experience-item">
                <div class="experience-header">
                    <h3>iOS Developer</h3>
                    <span class="date">Feb 2022 – Present</span>
                </div>
                <span class="company">
                    <a href="https://www.linkedin.com/in/your-profile" target="_blank">Brainvire Infotech Inc.</a> 
                </span>
                <!-- <a href="https://www.brainvire.com"  target="_blank">
                    <div class="company">Brainvire Infotech Inc.</div>
                </a> -->

                <ul class="experience-details">
                    <li>Developed and maintained iOS apps using Swift, UIKit, and SwiftUI</li>
                    <li>Integrated Firebase, MoEngage, Snowplow, and payment gateways</li>
                    <li>Wrote modular code with MVVM and Clean Swift patterns</li>
                    <li>Implemented unit & UI tests with XCTest/XCUITest for all major releases</li>
                </ul>
            </div>
            
            <h3 class="section-title">Key Projects</h3>
            <div class="project-item">
                <div class="project-header">
                    <h3>📚 Bunny Books – Instant Photobook Creation App</h3>
                    <a href="https://apps.apple.com/in/app/bunny-books/id6450604232"  target="_blank">
                        <span class="app-store-badge">App Store</span>
                    </a>
                </div>
                <p class="project-description">Custom photobook creator with PDF layering.</p>
            </div>
            
            <div class="project-item">
                <div class="project-header">
                    <h3>🛍️ Nike ME</h3>
                    <a href="https://apps.apple.com/app/nike-sports-wear-sneakers/id6444790147"  target="_blank">
                        <span class="app-store-badge">App Store</span>
                    </a>
                </div>
                <p class="project-description">Developed a high-performance Nike e-commerce app with personalized alerts, seamless multi-payment checkout, and optimized launch-time scalability.</p>
            </div>

            <div class="project-item">
                <div class="project-header">
                    <h3>🏃‍♂️ Sun & Sand Sports – Shop Online</h3>
                    <a href="https://apps.apple.com/us/app/sun-sand-sports-shop-online/id1163601891"  target="_blank">
                        <span class="app-store-badge">App Store</span>
                    </a>
                </div>
                <p class="project-description">Developed a high-performance sports e-commerce app with dynamic product feeds, enhanced navigation, personalized recommendations, and secure checkout.</p>
            </div>

            <div class="project-item">
                <div class="project-header">
                    <h3>🛒 Under Armour ME – Shop Online</h3>
                    <a href=" https://apps.apple.com/app/under-armour-me-shop-online/id1591394964"  target="_blank">
                        <span class="app-store-badge">App Store</span>
                    </a>
                </div>
                <p class="project-description">Developed a high-performance shopping app for Under Armour ME with personalized recommendations, Apple Pay integration, and seamless order tracking.</p>
            </div>

            <div class="project-item">
                <div class="project-header">
                    <h3>👟 Dropkick – Online Shopping</h3>
                    <a href=" https://apps.apple.com/us/app/dropkick-online-shopping/id1591789765"  target="_blank">
                        <span class="app-store-badge">App Store</span>
                    </a>
                </div>
                <p class="project-description">Built a dynamic e-commerce app with exclusive sneaker drops, real-time order tracking, and optimized performance for peak traffic.</p>
            </div>
            <div class="project-item">
                <div class="project-header">
                    <h3>🎁 Soughah Loyalty – Exclusive Loyalty Program</h3>
                    <a href="https://apps.apple.com/in/app/sougha-rewards/id6447970385"  target="_blank">
                        <span class="app-store-badge">App Store</span>
                    </a>
                </div>
                <p class="project-description">Built a luxury loyalty app with real-time rewards, premium brand integration, and seamless user experience across online and in-store platforms.</p>
            </div>
            
            <div class="testing-experience">
                <h3 class="section-title">Unit/UI Testing Experience</h3>
                <ul class="testing-list">
                    <li>Wrote unit tests for business logic using XCTest, achieving 80%+ code coverage in recent projects</li>
                    <li>Built UI tests with XCUITest to automate key user flows and detect regressions early</li>
                    <li>Integrated testing into CI/CD pipelines for continuous quality assurance</li>
                </ul>
            </div>
            
            <!-- <div class="references">
                <p>References available upon request</p>
            </div> -->
        </div>
    </div>
</body>
</html>
