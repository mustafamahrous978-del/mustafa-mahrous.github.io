<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Contact Page</title>

    <!-- =====================
         GLOBAL STYLES (DARK THEME)
    ====================== -->
    <style>
        :root {
            /* Accent color – change this to customize the highlight color */
            --accent: #4da3ff;
            --bg-dark: #0f172a;
            --card-bg: #111827;
            --text-main: #e5e7eb;
            --text-muted: #9ca3af;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: "Segoe UI", Tahoma, sans-serif;
        }

        body {
            background: radial-gradient(circle at top, #111827, var(--bg-dark));
            color: var(--text-main);
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
        }

        /* =====================
           MAIN CONTAINER
        ====================== */
        .container {
            width: 100%;
            max-width: 900px;
            padding: 40px 20px;
            text-align: center;
        }

        /* =====================
           LANDING SECTION
        ====================== */
        .landing {
            margin-bottom: 50px;
            animation: fadeUp 1s ease forwards;
        }

            .landing h1 {
                font-size: 2.5rem;
                font-weight: 700;
                margin-bottom: 10px;
            }

            .landing span {
                color: var(--accent);
            }

            .landing p {
                font-size: 1.1rem;
                color: var(--text-muted);
            }

        /* =====================
           CONTACT CARDS GRID
        ====================== */
        .cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
            gap: 20px;
        }

        .card {
            background: linear-gradient(145deg, #111827, #0b1220);
            border-radius: 16px;
            padding: 25px 15px;
            text-decoration: none;
            color: var(--text-main);
            position: relative;
            overflow: hidden;
            transform: translateY(20px);
            opacity: 0;
            transition: transform 0.4s ease, box-shadow 0.4s ease, background 0.4s ease;
        }

            .card:hover {
                transform: translateY(-8px) scale(1.02);
                box-shadow: 0 15px 40px rgba(77, 163, 255, 0.25);
            }

            .card::before {
                content: "";
                position: absolute;
                inset: 0;
                background: linear-gradient(120deg, transparent, rgba(77,163,255,0.15), transparent);
                opacity: 0;
                transition: opacity 0.4s ease;
            }

            .card:hover::before {
                opacity: 1;
            }

        /* =====================
           ICONS
        ====================== */
        .icon {
            width: 40px;
            height: 40px;
            margin: 0 auto 12px;
            fill: var(--accent);
        }

        .card h3 {
            font-size: 1rem;
            font-weight: 600;
        }

        /* =====================
           ANIMATIONS
        ====================== */
        @keyframes fadeUp {
            from {
                opacity: 0;
                transform: translateY(25px);
            }

            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* =====================
           RESPONSIVE TWEAKS
        ====================== */
        @media (max-width: 480px) {
            .landing h1 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>

    <div class="container">

        <!-- =====================
             LANDING PAGE
             Edit your name & tagline here
        ====================== -->
        <section class="landing">
            <h1>Mustafa <span>Mahrous</span></h1>
            <p>كله بالحب ❤️</p>
        </section>

        <!-- =====================
             CONTACT ME SECTION
             Edit links only (easy to update later)
        ====================== -->
        <section class="cards">

            <!-- PHONE -->
            <a href="tel:+201031687080" class="card">
                <svg class="icon" viewBox="0 0 24 24">
                    <path d="M6.62 10.79a15.05 15.05 0 006.59 6.59l2.2-2.2a1 1 0 011.01-.24c1.12.37 2.33.57 3.58.57a1 1 0 011 1V21a1 1 0 01-1 1C10.85 22 2 13.15 2 2a1 1 0 011-1h3.5a1 1 0 011 1c0 1.25.2 2.46.57 3.59a1 1 0 01-.25 1.01l-2.2 2.19z" />
                </svg>
                <h3>Phone</h3>
            </a>

            <!-- EMAIL -->
            <a href="mustafamahrous978@gmail.com" class="card">
                <svg class="icon" viewBox="0 0 24 24">
                    <path d="M20 4H4a2 2 0 00-2 2v12a2 2 0 002 2h16a2 2 0 002-2V6a2 2 0 00-2-2zm0 4l-8 5-8-5V6l8 5 8-5v2z" />
                </svg>
                <h3>Email</h3>
            </a>

            <!-- WHATSAPP -->
            <a href="https://wa.me/201031687080" target="_blank" class="card">
                <svg class="icon" viewBox="0 0 24 24">
                    <path d="M20.52 3.48A11.82 11.82 0 0012 0 12 12 0 000 12a11.9 11.9 0 001.69 6.13L0 24l6.05-1.59A12 12 0 1012 0zm0 17.24a9.93 9.93 0 01-11.25 1.52l-.8-.47-3.59.94.96-3.49-.52-.84A10 10 0 1120.52 20.72z" />
                </svg>
                <h3>WhatsApp</h3>
          
            </a>

            <!-- FACEBOOK -->
            <a href="https://www.facebook.com/share/1GQwshSgem/" target="_blank" class="card">
                <svg class="icon" viewBox="0 0 24 24">
                    <path d="M22 12a10 10 0 10-11.5 9.9v-7h-2v-3h2v-2.3c0-2 1.2-3.1 3-3.1.9 0 1.8.16 1.8.16v2h-1c-1 0-1.3.62-1.3 1.25V12h2.3l-.37 3h-1.93v7A10 10 0 0022 12z" />
                </svg>
                <h3>Facebook</h3>
            </a>

            <!-- INSTAGRAM -->
            <a href="https://www.instagram.com/most.desha1?igsh=MWhtMHAzeDF1bWhvYQ==" target="_blank" class="card">
                <svg class="icon" viewBox="0 0 24 24">
                    <path d="M7 2h10a5 5 0 015 5v10a5 5 0 01-5 5H7a5 5 0 01-5-5V7a5 5 0 015-5zm5 5a5 5 0 100 10 5 5 0 000-10zm6-1a1 1 0 11-2 0 1 1 0 012 0z" />
                </svg>
                <h3>Instagram</h3>
            </a>

            <!-- TELEGRAM -->
            <a href="https://t.me/Desha978" target="_blank" class="card">
                <svg class="icon" viewBox="0 0 24 24">
                    <path d="M21.5 2.5L2.7 10.3c-1.2.5-1.2 1.2-.2 1.5l4.8 1.5 1.8 5.5c.2.5.4.7.8.7.4 0 .6-.2.9-.5l2.6-2.5 5.4 4c1 .6 1.7.3 2-.9l3.4-15.8c.4-1.5-.6-2.2-1.7-1.8z" />
                </svg>
                <h3>Telegram</h3>
            </a>

            <!-- LINKEDIN -->
            <a href="https://www.linkedin.com/in/mustafa-mahrous-46567b35a?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app" target="_blank" class="card">
                <svg class="icon" viewBox="0 0 24 24">
                    <path d="M4.98 3.5a2.5 2.5 0 110 5 2.5 2.5 0 010-5zM3 9h4v12H3zM9 9h4v1.7c.6-1 1.7-2 3.6-2 3.8 0 4.4 2.5 4.4 5.8V21h-4v-5.5c0-1.3 0-3-1.8-3s-2.1 1.4-2.1 2.9V21H9z" />
                </svg>
                <h3>LinkedIn</h3>
            </a>

        </section>
    </div>

    <!-- =====================
         SIMPLE SCROLL ANIMATION (PURE JS)
    ====================== -->
    <script>
        const cards = document.querySelectorAll('.card');

        const observer = new IntersectionObserver(entries => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.animation = "fadeUp 0.8s ease forwards";
                    observer.unobserve(entry.target);
                }
            });
        }, { threshold: 0.2 });

        cards.forEach(card => observer.observe(card));
    </script>

</body>
</html>
