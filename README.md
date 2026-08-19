<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">

    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <meta name="description"
        content="Lysam Hub Training & Tech Services offers professional training and technical services including web design, virtual assistance, networking, computer repair and more.">

    <title>Lysam Hub | Training & Tech Services</title>

    <style>
        /* =========================
           GENERAL STYLES
        ========================== */

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: "Segoe UI", Arial, sans-serif;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            background: #f8f9fa;
            color: #333;
            line-height: 1.6;
        }

        a {
            text-decoration: none;
        }


        /* =========================
           NAVBAR
        ========================== */

        header {
            background: linear-gradient(135deg, #004aad, #007bff);
            color: white;
            padding: 15px 0;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }

        nav {
            width: 90%;
            max-width: 1200px;
            margin: auto;

            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        nav h1 {
            font-size: 1.5rem;
        }

        nav ul {
            list-style: none;
            display: flex;
            gap: 20px;
        }

        nav a {
            color: white;
            font-weight: 500;
            transition: 0.3s;
        }

        nav a:hover {
            color: #ffd700;
        }

        /* Mobile menu button */

        .menu-btn {
            display: none;
            background: transparent;
            border: none;
            color: white;
            font-size: 28px;
            cursor: pointer;
        }


        /* =========================
           HERO SECTION
        ========================== */

        .hero {
            background:
                linear-gradient(
                    rgba(0, 74, 173, 0.8),
                    rgba(0, 123, 255, 0.8)
                ),
                url("https://picsum.photos/1200/600?random=1")
                center/cover;

            color: white;
            text-align: center;
            padding: 100px 20px;
        }

        .hero h2 {
            font-size: 2.5rem;
            margin-bottom: 15px;
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 25px;
        }


        /* =========================
           BUTTON
        ========================== */

        .btn {
            display: inline-block;

            background: #ffd700;
            color: #004aad;

            padding: 12px 25px;

            border: none;
            border-radius: 8px;

            font-weight: bold;
            cursor: pointer;

            transition: 0.3s;
        }

        .btn:hover {
            background: #ffc107;
            transform: scale(1.05);
        }


        /* =========================
           SERVICES
        ========================== */

        .services {
            width: 90%;
            max-width: 1200px;

            margin: 60px auto;

            text-align: center;
        }

        .services h2 {
            color: #004aad;
            margin-bottom: 40px;
            font-size: 2rem;
        }

        .service-grid {
            display: grid;

            grid-template-columns:
                repeat(auto-fit, minmax(250px, 1fr));

            gap: 25px;
        }

        .card {
            background: white;

            padding: 25px;

            border-radius: 12px;

            box-shadow:
                0 4px 15px rgba(0, 0, 0, 0.1);

            transition: 0.3s;

            cursor: pointer;
        }

        .card:hover {
            transform: translateY(-8px);

            box-shadow:
                0 8px 20px rgba(0, 0, 0, 0.15);
        }

        .card .icon {
            font-size: 2.5rem;
            margin-bottom: 15px;
        }

        .card h3 {
            color: #007bff;
            margin-bottom: 10px;
        }


        /* =========================
           CONTACT
        ========================== */

        .contact {
            background: #004aad;

            color: white;

            padding: 60px 20px;

            text-align: center;
        }

        .contact h2 {
            margin-bottom: 20px;
        }

        #contactForm {
            max-width: 500px;

            margin: auto;

            display: flex;

            flex-direction: column;

            gap: 15px;
        }

        #contactForm input,
        #contactForm textarea {
            width: 100%;

            padding: 12px;

            border: none;

            border-radius: 8px;

            font-size: 1rem;
        }

        #contactForm input:focus,
        #contactForm textarea:focus {
            outline: 3px solid #ffd700;
        }

        #contactForm textarea {
            resize: vertical;
        }

        #formStatus {
            margin-top: 15px;

            font-weight: bold;
        }


        /* =========================
           FOOTER
        ========================== */

        footer {
            background: #002a63;

            color: white;

            text-align: center;

            padding: 20px;
        }


        /* =========================
           MOBILE RESPONSIVE DESIGN
        ========================== */

        @media (max-width: 768px) {

            nav {
                position: relative;
            }

            .menu-btn {
                display: block;
            }

            nav ul {
                display: none;

                position: absolute;

                top: 60px;
                left: 0;

                width: 100%;

                background: #004aad;

                flex-direction: column;

                gap: 0;

                padding: 10px 0;
            }

            nav ul.active {
                display: flex;
            }

            nav ul li {
                text-align: center;

                padding: 12px;
            }

            nav ul li:hover {
                background: #007bff;
            }

            .hero {
                padding: 80px 20px;
            }

            .hero h2 {
                font-size: 2rem;
            }

            .hero p {
                font-size: 1rem;
            }
        }


        @media (max-width: 480px) {

            nav h1 {
                font-size: 1.2rem;
            }

            .hero h2 {
                font-size: 1.7rem;
            }

            .services h2 {
                font-size: 1.7rem;
            }
        }
    </style>
</head>


<body>

    <!-- =========================
         HEADER / NAVIGATION
    ========================== -->

    <header>

        <nav>

            <h1>Lysam Hub</h1>

            <button
                class="menu-btn"
                id="menuBtn"
                type="button"
                aria-label="Open navigation menu"
                aria-expanded="false"
            >
                ☰
            </button>

            <ul id="navMenu">

                <li>
                    <a href="#home">Home</a>
                </li>

                <li>
                    <a href="#services">Services</a>
                </li>

                <li>
                    <a href="#contact">Contact</a>
                </li>

            </ul>

        </nav>

    </header>


    <!-- =========================
         HERO SECTION
    ========================== -->

    <section class="hero" id="home">

        <h2>
            Welcome to Lysam Hub
            Training & Tech Services
        </h2>

        <p>
            We offer professional training and
            technical services to empower you.
        </p>

        <button
            class="btn"
            id="servicesBtn"
            type="button"
        >
            View Our Services
        </button>

    </section>


    <!-- =========================
         SERVICES SECTION
    ========================== -->

    <section
        class="services"
        id="services"
    >

        <h2>Our Services</h2>

        <div
            class="service-grid"
            id="serviceGrid"
        >
            <!-- JavaScript will add services here -->
        </div>

    </section>


    <!-- =========================
         CONTACT SECTION
    ========================== -->

    <section
        class="contact"
        id="contact"
    >

        <h2>Get In Touch</h2>

        <p>
            Have a question? Send us a message.
        </p>


        <form id="contactForm">

            <input
                type="text"
                id="name"
                name="name"
                placeholder="Your Name"
                required
            >


            <input
                type="email"
                id="email"
                name="email"
                placeholder="Your Email"
                required
            >


            <textarea
                id="message"
                name="message"
                rows="4"
                placeholder="Your Message"
                required
            ></textarea>


            <button
                type="submit"
                class="btn"
            >
                Send Message
            </button>

        </form>


        <p id="formStatus"></p>

    </section>


    <!-- =========================
         FOOTER
    ========================== -->

    <footer>

        <p>
            © 2026 Lysam Hub Training & Tech Services.
            All Rights Reserved.
        </p>

    </footer>


    <!-- =========================
         JAVASCRIPT
    ========================== -->

    <script>

        // ==========================================
        // 1. SERVICES DATA
        // ==========================================

        const services = [

            {
                icon: "💱",
                title: "Forex Trading Course",
                desc: "Learn professional forex trading strategies and risk management."
            },

            {
                icon: "💻",
                title: "Web Design",
                desc: "Modern, responsive websites for businesses and personal brands."
            },

            {
                icon: "🎥",
                title: "Content Creation",
                desc: "Graphics, video editing, and social media content that converts."
            },

            {
                icon: "🧑‍💼",
                title: "Virtual Assistance",
                desc: "Professional VA services including administration, emails and research."
            },

            {
                icon: "⚙️",
                title: "Software Installation",
                desc: "Operating systems, drivers, Office, antivirus and software setup."
            },

            {
                icon: "🌐",
                title: "Networking Services",
                desc: "LAN setup, WiFi configuration and network troubleshooting."
            },

            {
                icon: "📱",
                title: "Mobile & Computer Repair",
                desc: "Software repair, maintenance and computer troubleshooting."
            },

            {
                icon: "📄",
                title: "Government Applications",
                desc: "Assistance with online government application services."
            }

        ];


        // ==========================================
        // 2. LOAD SERVICES
        // ==========================================

        function loadServices() {

            const grid =
                document.getElementById("serviceGrid");


            services.forEach(function(service) {

                const card =
                    document.createElement("div");


                card.classList.add("card");


                card.innerHTML = `

                    <div
                        class="icon"
                        aria-hidden="true"
                    >
                        ${service.icon}
                    </div>

                    <h3>
                        ${service.title}
                    </h3>

                    <p>
                        ${service.desc}
                    </p>

                `;


                // When a user clicks a service

                card.addEventListener(
                    "click",
                    function() {

                        alert(
                            "You selected: " +
                            service.title +
                            "\n\nContact Lysam Hub to learn more!"
                        );

                    }
                );


                grid.appendChild(card);

            });

        }


        // ==========================================
        // 3. VIEW SERVICES BUTTON
        // ==========================================

        const servicesBtn =
            document.getElementById("servicesBtn");


        servicesBtn.addEventListener(
            "click",
            function() {

                document
                    .getElementById("services")
                    .scrollIntoView({
                        behavior: "smooth"
                    });

            }
        );


        // ==========================================
        // 4. CONTACT FORM
        // ==========================================

        const form =
            document.getElementById("contactForm");


        const formStatus =
            document.getElementById("formStatus");


        form.addEventListener(
            "submit",
            function(event) {

                // Prevent page refresh

                event.preventDefault();


                // Get user's name

                const name =
                    document.getElementById("name")
                    .value
                    .trim();


                // Display success message

                formStatus.textContent =
                    "Thank you, " +
                    name +
                    "! Your message has been received.";


                // Clear the form

                form.reset();

            }
        );


        // ==========================================
        // 5. MOBILE MENU
        // ==========================================

        const menuBtn =
            document.getElementById("menuBtn");


        const navMenu =
            document.getElementById("navMenu");


        menuBtn.addEventListener(
            "click",
            function() {

                navMenu.classList.toggle("active");


                const isOpen =
                    navMenu.classList.contains("active");


                menuBtn.setAttribute(
                    "aria-expanded",
                    isOpen
                );

            }
        );


        // ==========================================
        // 6. CLOSE MOBILE MENU AFTER CLICKING LINK
        // ==========================================

        const navLinks =
            document.querySelectorAll(
                "#navMenu a"
            );


        navLinks.forEach(function(link) {

            link.addEventListener(
                "click",
                function() {

                    navMenu.classList.remove("active");

                    menuBtn.setAttribute(
                        "aria-expanded",
                        "false"
                    );

                }
            );

        });


        // ==========================================
        // 7. START WEBSITE
        // ==========================================

        loadServices();

    </script>

</body>

</html>
