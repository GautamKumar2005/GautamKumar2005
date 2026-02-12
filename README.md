<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gautam - Competitive Programmer</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #0f0c29, #302b63, #24243e);
            color: #fff;
            min-height: 100vh;
            padding: 20px;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
        }

        /* Hero Section */
        .hero {
            text-align: center;
            padding: 60px 20px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 20px;
            backdrop-filter: blur(10px);
            margin-bottom: 40px;
            animation: fadeInDown 0.8s ease;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(30, 144, 255, 0.1) 0%, transparent 70%);
            animation: rotate 20s linear infinite;
        }

        @keyframes rotate {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        .hero-content {
            position: relative;
            z-index: 1;
        }

        .wave {
            font-size: 3rem;
            display: inline-block;
            animation: wave 2s ease-in-out infinite;
        }

        @keyframes wave {
            0%, 100% { transform: rotate(0deg); }
            25% { transform: rotate(20deg); }
            75% { transform: rotate(-20deg); }
        }

        h1 {
            font-size: 3.5rem;
            margin: 20px 0;
            background: linear-gradient(45deg, #1E90FF, #00D4FF);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: fadeInUp 1s ease;
        }

        .subtitle {
            font-size: 1.3rem;
            color: #aaa;
            margin-bottom: 20px;
        }

        .location {
            font-size: 1rem;
            color: #888;
            margin-bottom: 30px;
        }

        /* Stats Grid */
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-bottom: 40px;
        }

        .stat-card {
            background: rgba(255, 255, 255, 0.08);
            padding: 30px;
            border-radius: 15px;
            text-align: center;
            transition: all 0.3s ease;
            cursor: pointer;
            border: 2px solid transparent;
            animation: fadeInUp 0.8s ease;
        }

        .stat-card:hover {
            transform: translateY(-10px);
            background: rgba(255, 255, 255, 0.12);
            border-color: #1E90FF;
            box-shadow: 0 10px 30px rgba(30, 144, 255, 0.3);
        }

        .stat-number {
            font-size: 3rem;
            font-weight: bold;
            background: linear-gradient(45deg, #1E90FF, #00D4FF);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 10px;
        }

        .stat-label {
            color: #aaa;
            font-size: 1rem;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        /* Platform Cards */
        .platform-section {
            margin-bottom: 50px;
        }

        .section-title {
            font-size: 2.5rem;
            margin-bottom: 30px;
            text-align: center;
            position: relative;
            padding-bottom: 15px;
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 4px;
            background: linear-gradient(90deg, #1E90FF, #00D4FF);
            border-radius: 2px;
        }

        .platform-card {
            background: rgba(255, 255, 255, 0.08);
            border-radius: 20px;
            padding: 40px;
            margin-bottom: 30px;
            transition: all 0.3s ease;
            border: 2px solid rgba(255, 255, 255, 0.1);
            animation: fadeInUp 1s ease;
        }

        .platform-card:hover {
            transform: translateY(-5px);
            border-color: #1E90FF;
            box-shadow: 0 15px 40px rgba(30, 144, 255, 0.2);
        }

        .platform-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 30px;
            flex-wrap: wrap;
            gap: 20px;
        }

        .platform-logo {
            font-size: 2rem;
            font-weight: bold;
        }

        .leetcode-logo {
            color: #FFA116;
        }

        .codeforces-logo {
            color: #1F8ACB;
        }

        .codechef-logo {
            color: #5B4638;
        }

        .codolio-logo {
            color: #1E90FF;
        }

        .badge {
            display: inline-block;
            padding: 8px 16px;
            border-radius: 20px;
            font-size: 0.9rem;
            font-weight: bold;
            animation: pulse 2s ease-in-out infinite;
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.05); }
        }

        .badge-knight {
            background: linear-gradient(135deg, #FFA116, #FFB84D);
            color: #000;
        }

        .badge-specialist {
            background: linear-gradient(135deg, #03A89E, #4FC3F7);
            color: #fff;
        }

        .badge-3star {
            background: linear-gradient(135deg, #684A23, #5B4638);
            color: #fff;
        }

        /* Progress Bar */
        .progress-container {
            margin: 20px 0;
        }

        .progress-label {
            display: flex;
            justify-content: space-between;
            margin-bottom: 10px;
            color: #aaa;
        }

        .progress-bar {
            width: 100%;
            height: 12px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            overflow: hidden;
            position: relative;
        }

        .progress-fill {
            height: 100%;
            background: linear-gradient(90deg, #1E90FF, #00D4FF);
            border-radius: 10px;
            transition: width 1.5s ease;
            position: relative;
            overflow: hidden;
        }

        .progress-fill::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.3), transparent);
            animation: shimmer 2s infinite;
        }

        @keyframes shimmer {
            0% { transform: translateX(-100%); }
            100% { transform: translateX(100%); }
        }

        /* Image Grid */
        .image-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }

        .image-wrapper {
            position: relative;
            overflow: hidden;
            border-radius: 15px;
            transition: transform 0.3s ease;
            cursor: pointer;
        }

        .image-wrapper:hover {
            transform: scale(1.05);
        }

        .image-wrapper img {
            width: 100%;
            height: auto;
            display: block;
            border-radius: 15px;
            transition: all 0.3s ease;
        }

        .image-wrapper:hover img {
            filter: brightness(1.2);
        }

        /* CTA Button */
        .cta-button {
            display: inline-block;
            padding: 15px 40px;
            background: linear-gradient(135deg, #1E90FF, #00D4FF);
            color: #fff;
            text-decoration: none;
            border-radius: 30px;
            font-weight: bold;
            font-size: 1.1rem;
            transition: all 0.3s ease;
            margin: 10px;
            border: none;
            cursor: pointer;
            box-shadow: 0 5px 15px rgba(30, 144, 255, 0.3);
        }

        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 25px rgba(30, 144, 255, 0.5);
        }

        /* Footer */
        .footer {
            text-align: center;
            padding: 40px 20px;
            margin-top: 60px;
            border-top: 2px solid rgba(255, 255, 255, 0.1);
        }

        .footer-text {
            color: #888;
            font-size: 1.1rem;
            margin-bottom: 20px;
        }

        .rocket {
            display: inline-block;
            animation: rocket 1.5s ease-in-out infinite;
        }

        @keyframes rocket {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }

        /* Animations */
        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        /* Responsive */
        @media (max-width: 768px) {
            h1 {
                font-size: 2.5rem;
            }

            .section-title {
                font-size: 2rem;
            }

            .stat-number {
                font-size: 2.5rem;
            }

            .platform-header {
                flex-direction: column;
                align-items: flex-start;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Hero Section -->
        <div class="hero">
            <div class="hero-content">
                <span class="wave">👋</span>
                <h1>Hey, I'm Gautam!</h1>
                <p class="subtitle">Competitive Programmer | Problem Solver</p>
                <p class="location">📍 Delhi, India</p>
                <p style="color: #aaa; max-width: 600px; margin: 20px auto;">
                    Daily grinding across platforms — watch my progress update live!
                </p>
            </div>
        </div>

        <!-- Quick Stats -->
        <div class="stats-grid">
            <div class="stat-card" style="animation-delay: 0.1s">
                <div class="stat-number" id="totalSolved">1500+</div>
                <div class="stat-label">Problems Solved</div>
            </div>
            <div class="stat-card" style="animation-delay: 0.2s">
                <div class="stat-number" id="platforms">4+</div>
                <div class="stat-label">Active Platforms</div>
            </div>
            <div class="stat-card" style="animation-delay: 0.3s">
                <div class="stat-number" id="streak">🔥</div>
                <div class="stat-label">Daily Grind</div>
            </div>
        </div>

        <!-- LeetCode Section -->
        <div class="platform-section">
            <h2 class="section-title">💡 LeetCode Performance</h2>
            
            <div class="platform-card">
                <div class="platform-header">
                    <div class="platform-logo leetcode-logo">LeetCode</div>
                    <span class="badge badge-knight">Knight 🏆</span>
                </div>

                <div class="progress-container">
                    <div class="progress-label">
                        <span>Problem Solving Progress</span>
                        <span id="leetcode-percent">65%</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress-fill" style="width: 65%"></div>
                    </div>
                </div>

                <div class="image-grid">
                    <div class="image-wrapper">
                        <a href="https://leetcode.com/u/Gautam_coder2005/" target="_blank">
                            <img src="https://leetcard.jacoblin.cool/Gautam_coder2005?theme=dark&font=Ubuntu&ext=heatmap" alt="LeetCode Stats">
                        </a>
                    </div>
                </div>

                <div style="text-align: center; margin-top: 20px;">
                    <a href="https://leetcode.com/u/Gautam_coder2005/" target="_blank" class="cta-button">
                        View Full LeetCode Profile →
                    </a>
                </div>
            </div>
        </div>

        <!-- Portfolio Section -->
        <div class="platform-section">
            <h2 class="section-title">📊 Aggregated Portfolio</h2>
            
            <div class="platform-card">
                <div class="platform-header">
                    <div class="platform-logo codolio-logo">Codolio Dashboard</div>
                    <span class="badge" style="background: linear-gradient(135deg, #1E90FF, #00D4FF);">Live Stats</span>
                </div>

                <p style="color: #aaa; margin-bottom: 30px; text-align: center; font-size: 1.1rem;">
                    📈 All my competitive programming stats in one place — ratings, solved counts, and global ranks auto-updated!
                </p>

                <div class="image-grid">
                    <div class="image-wrapper">
                        <a href="https://codolio.com/profile/Gautam_coder2005" target="_blank">
                            <img src="https://codolio-readme-stats.vercel.app/api?username=Gautam_coder2005&theme=dark" alt="Codolio Stats">
                        </a>
                    </div>
                </div>

                <div style="text-align: center; margin-top: 20px;">
                    <a href="https://codolio.com/profile/Gautam_coder2005" target="_blank" class="cta-button">
                        View Complete Dashboard →
                    </a>
                </div>
            </div>
        </div>

        <!-- Codeforces & CodeChef Section -->
        <div class="platform-section">
            <h2 class="section-title">⚔️ Contest Platforms</h2>
            
            <!-- Codeforces -->
            <div class="platform-card">
                <div class="platform-header">
                    <div class="platform-logo codeforces-logo">Codeforces</div>
                    <span class="badge badge-specialist">Specialist</span>
                </div>

                <div class="progress-container">
                    <div class="progress-label">
                        <span>Rating Progress</span>
                        <span>1400+</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress-fill" style="width: 58%; background: linear-gradient(90deg, #1F8ACB, #4FC3F7)"></div>
                    </div>
                </div>

                <div class="image-grid">
                    <div class="image-wrapper">
                        <a href="https://codeforces.com/profile/Gautam_coder2005" target="_blank">
                            <img src="https://codeforces-readme-stats.vercel.app/api/card?username=Gautam_coder2005&theme=github_dark" alt="Codeforces Stats">
                        </a>
                    </div>
                </div>

                <div style="text-align: center; margin-top: 20px;">
                    <a href="https://codeforces.com/profile/Gautam_coder2005" target="_blank" class="cta-button">
                        View Codeforces Profile →
                    </a>
                </div>
            </div>

            <!-- CodeChef -->
            <div class="platform-card">
                <div class="platform-header">
                    <div class="platform-logo codechef-logo">CodeChef</div>
                    <span class="badge badge-3star">3 Star ⭐⭐⭐</span>
                </div>

                <div class="progress-container">
                    <div class="progress-label">
                        <span>Contest Performance</span>
                        <span>1600+</span>
                    </div>
                    <div class="progress-bar">
                        <div class="progress-fill" style="width: 53%; background: linear-gradient(90deg, #5B4638, #8B6F47)"></div>
                    </div>
                </div>

                <div style="text-align: center; margin-top: 30px;">
                    <a href="https://www.codechef.com/users/gautam_2005" target="_blank">
                        <img src="https://img.shields.io/badge/CodeChef-Profile-5B4638?style=for-the-badge&logo=codechef&logoColor=white" alt="CodeChef Profile">
                    </a>
                </div>

                <div style="text-align: center; margin-top: 20px;">
                    <a href="https://www.codechef.com/users/gautam_2005" target="_blank" class="cta-button">
                        View CodeChef Profile →
                    </a>
                </div>
            </div>
        </div>

        <!-- Footer -->
        <div class="footer">
            <p class="footer-text">
                💪 Keep solving, keep growing! <span class="rocket">🚀</span>
            </p>
            <p style="color: #666; font-size: 0.9rem;">
                Everything updates live from the platforms — no manual updates needed!
            </p>
        </div>
    </div>

    <script>
        // Animate numbers on scroll
        function animateValue(id, start, end, duration) {
            const obj = document.getElementById(id);
            const range = end - start;
            const increment = end > start ? 1 : -1;
            const stepTime = Math.abs(Math.floor(duration / range));
            let current = start;
            
            const timer = setInterval(() => {
                current += increment;
                obj.textContent = current + (id === 'totalSolved' ? '+' : id === 'platforms' ? '+' : '');
                if (current == end) {
                    clearInterval(timer);
                }
            }, stepTime);
        }

        // Trigger animations when page loads
        window.addEventListener('load', () => {
            animateValue('totalSolved', 1000, 1500, 1500);
            animateValue('platforms', 1, 4, 1000);
        });

        // Add click effect to cards
        document.querySelectorAll('.stat-card, .platform-card').forEach(card => {
            card.addEventListener('click', function() {
                this.style.animation = 'none';
                setTimeout(() => {
                    this.style.animation = '';
                }, 10);
            });
        });

        // Smooth scroll for better UX
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });
    </script>
</body>
</html>
