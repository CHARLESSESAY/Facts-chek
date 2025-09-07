<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sierra Leone Truth Platform - Proposal Mockup</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Comic+Neue:wght@400;700&family=Bangers&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Comic Neue', sans-serif;
            background: linear-gradient(135deg, #e6f3fa 0%, #d4edda 100%);
            color: #1a202c;
            overflow-x: hidden;
        }
        h1, h2, h3 {
            font-family: 'Bangers', cursive;
        }
        /* Animations */
        @keyframes slideUp {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }
        @keyframes pulse {
            0% { transform: scale(1); }
            50% { transform: scale(1.05); }
            100% { transform: scale(1); }
        }
        @keyframes bounce {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-10px); }
        }
        @keyframes colorChange {
            0% { color: #0047ab; }
            50% { color: #008000; }
            100% { color: #0047ab; }
        }
        @keyframes rotateCard {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(2deg); }
        }
        .slide-up {
            animation: slideUp 0.8s ease-out forwards;
        }
        .pulse:hover {
            animation: pulse 0.3s ease-in-out;
        }
        .bounce-text {
            animation: bounce 1s infinite;
        }
        .color-change {
            animation: colorChange 3s infinite;
        }
        .card:hover {
            transform: translateY(-5px) rotate(2deg);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
            animation: rotateCard 0.3s ease-in-out;
        }
        /* Hero Section */
        .hero-bg {
            background: linear-gradient(to bottom, rgba(0, 71, 171, 0.7), rgba(0, 128, 0, 0.7)), url('https://images.unsplash.com/photo-1600585154340-be6161a56a0c?ixlib=rb-4.0.3&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
        }
        /* Marquee for logos */
        .marquee {
            overflow: hidden;
            white-space: nowrap;
            box-sizing: border-box;
        }
        .marquee-content {
            display: inline-block;
            animation: marquee 15s linear infinite;
        }
        @keyframes marquee {
            from { transform: translateX(0); }
            to { transform: translateX(-50%); }
        }
        .marquee img {
            width: 150px;
            height: auto;
            margin: 0 20px;
        }
        /* Custom Components */
        .nav-link {
            position: relative;
            transition: color 0.3s ease;
        }
        .nav-link::after {
            content: '';
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -2px;
            left: 0;
            background-color: #00ff00;
            transition: width 0.3s ease;
        }
        .nav-link:hover::after {
            width: 100%;
        }
        .card {
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            background: linear-gradient(135deg, #ffffff, #f0f0ff);
        }
        .verdict, .chat-response {
            transition: opacity 0.5s ease, transform 0.5s ease;
        }
        .verdict.show, .chat-response.show {
            opacity: 1;
            transform: translateY(0);
        }
        .btn-primary {
            background: linear-gradient(to right, #0047ab, #008000);
            transition: background 0.3s ease, transform 0.2s ease;
        }
        .btn-primary:hover {
            background: linear-gradient(to right, #003087, #006400);
            transform: scale(1.05);
        }
        /* Accessibility */
        button:focus, input:focus, select:focus, textarea:focus {
            outline: 3px solid #00ff00;
            outline-offset: 2px;
        }
        /* Mobile Optimizations */
        @media (max-width: 768px) {
            .hero-bg {
                background-attachment: scroll;
            }
            .nav-links {
                flex-direction: column;
                gap: 1rem;
            }
            .marquee img {
                width: 100px;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header class="hero-bg text-white py-20 text-center">
        <h1 class="text-5xl md:text-6xl font-bold mb-6 slide-up bounce-text color-change">Sierra Leone Truth Platform</h1>
        <p class="text-xl md:text-2xl max-w-3xl mx-auto mb-8 slide-up">Your fun, trusty hub for verifying info across all industries—health, tech, finance, and more—using texts, URLs, images, or audio!</p>
        <a href="#join" class="btn-primary text-white px-8 py-4 rounded-full font-semibold text-lg pulse slide-up">Join the Truth Party!</a>
    </header>

    <!-- Navigation -->
    <nav class="bg-gray-900 text-white py-5 sticky top-0 z-20 shadow-lg">
        <div class="max-w-7xl mx-auto flex justify-center nav-links">
            <a href="#mission" class="nav-link px-4 py-2 text-lg font-medium">Mission</a>
            <a href="#ask" class="nav-link px-4 py-2 text-lg font-medium">Ask TruthBot</a>
            <a href="#verify" class="nav-link px-4 py-2 text-lg font-medium">Verify Info</a>
            <a href="#news" class="nav-link px-4 py-2 text-lg font-medium">Verified News</a>
            <a href="#report" class="nav-link px-4 py-2 text-lg font-medium">Report Misinfo</a>
            <a href="#impact" class="nav-link px-4 py-2 text-lg font-medium">Impact</a>
        </div>
    </nav>

    <!-- Main Content -->
    <main class="max-w-7xl mx-auto py-16 px-4 sm:px-6 lg:px-8">
        <!-- Media Houses Logos Loop -->
        <section class="mb-20 slide-up">
            <h2 class="text-4xl font-bold text-gray-900 mb-6 bounce-text color-change">Our Media Partners</h2>
            <div class="marquee bg-white p-4 rounded-xl shadow-lg">
                <div class="marquee-content">
                    <img src="https://static.wikia.nocookie.net/logopedia/images/6/6b/Slbclogo.png/revision/latest?cb=20191003140436" alt="SLBC Logo">
                    <img src="https://via.placeholder.com/150x100?text=AYV+News" alt="AYV News Logo">
                    <img src="https://via.placeholder.com/150x100?text=Awoko" alt="Awoko Logo">
                    <img src="https://via.placeholder.com/150x100?text=Concord+Times" alt="Concord Times Logo">
                    <img src="https://via.placeholder.com/150x100?text=SL+Telegraph" alt="Sierra Leone Telegraph Logo">
                    <img src="https://static.wikia.nocookie.net/logopedia/images/6/6b/Slbclogo.png/revision/latest?cb=20191003140436" alt="SLBC Logo">
                    <img src="https://via.placeholder.com/150x100?text=AYV+News" alt="AYV News Logo">
                    <img src="https://via.placeholder.com/150x100?text=Awoko" alt="Awoko Logo">
                    <img src="https://via.placeholder.com/150x100?text=Concord+Times" alt="Concord Times Logo">
                    <img src="https://via.placeholder.com/150x100?text=SL+Telegraph" alt="Sierra Leone Telegraph Logo">
                </div>
            </div>
        </section>

        <!-- Mission Section -->
        <section id="mission" class="mb-20 slide-up">
            <h2 class="text-4xl font-bold text-gray-900 mb-6 bounce-text color-change">Our Mission</h2>
            <p class="text-lg text-gray-700 max-w-3xl mx-auto mb-8">To bring joy and truth to Sierra Leone with a super-cool tool for verifying info from all industries, using AI and blockchain for crystal-clear transparency!</p>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <div class="card bg-white p-8 rounded-xl shadow-lg">
                    <h3 class="text-2xl font-semibold text-blue-700 mb-4 color-change">For Citizens</h3>
                    <p class="text-gray-600">Check out any info—health, tech, or more—in English or Krio, with texts, URLs, images, or audio!</p>
                </div>
                <div class="card bg-white p-8 rounded-xl shadow-lg">
                    <h3 class="text-2xl font-semibold text-green-700 mb-4 color-change">For Government</h3>
                    <p class="text-gray-600">Share true updates, zap false info, and build trust with blockchain records.</p>
                </div>
                <div class="card bg-white p-8 rounded-xl shadow-lg">
                    <h3 class="text-2xl font-semibold text-blue-700 mb-4 color-change">For Media & Industries</h3>
                    <p class="text-gray-600">Spread legit content, team up on truth-checking, and shine as verified!</p>
                </div>
            </div>
        </section>

        <!-- Ask TruthBot Section -->
        <section id="ask" class="mb-20 slide-up">
            <h2 class="text-4xl font-bold text-gray-900 mb-6 bounce-text color-change">Ask TruthBot!</h2>
            <p class="text-lg text-gray-700 mb-8">Got a question about anything? Ask TruthBot, our AI buddy, and get instant, verified answers with a sprinkle of fun!</p>
            <div class="bg-white p-8 rounded-xl shadow-lg">
                <div class="form-group mb-6">
                    <label for="question" class="block text-gray-800 font-semibold mb-3 text-lg">Your Question</label>
                    <textarea id="question" rows="4" class="w-full p-4 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-green-500 transition" placeholder="e.g., 'Is the new malaria vaccine safe?' or 'What’s the latest on tech startups in Sierra Leone?'"></textarea>
                </div>
                <button onclick="showChatResponse()" class="btn-primary text-white px-8 py-4 rounded-full font-semibold text-lg pulse">Ask Now!</button>
                <div id="chat-response" class="chat-response mt-8 p-6 rounded-lg opacity-0 translate-y-4 hidden" style="background-color: #fefcbf; border: 1px solid #fef08a; color: #713f12;">
                    <h3 class="text-xl font-semibold mb-2">TruthBot Says:</h3>
                    <p>Answer: The malaria vaccine is safe, backed by WHO trials showing 75% efficacy in kids under 5. No major side effects reported! Confidence: 95%.</p>
                    <p class="mt-2">Sources: <a href="#" class="underline hover:text-green-600">WHO Malaria Report</a>, <a href="#" class="underline hover:text-green-600">SL Ministry of Health</a></p>
                    <p class="text-sm mt-3 font-mono">Blockchain Hash: 0xyz789... (Verified on Polygon - Sept 6, 2025)</p>
                </div>
            </div>
        </section>

        <!-- Verify Info Section -->
        <section id="verify" class="mb-20 slide-up">
            <h2 class="text-4xl font-bold text-gray-900 mb-6 bounce-text color-change">Verify Information</h2>
            <p class="text-lg text-gray-700 mb-8">Got a claim? Upload texts, URLs, images, or audio from any industry. Our AI checks it against trusted sources like SLBC and WHO!</p>
            <div class="bg-white p-8 rounded-xl shadow-lg">
                <div class="form-group mb-6">
                    <label for="input-type" class="block text-gray-800 font-semibold mb-3 text-lg">Input Type</label>
                    <select id="input-type" class="w-full p-4 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-green-500 transition">
                        <option>Text</option>
                        <option>URL</option>
                        <option>Image Upload</option>
                        <option>Audio Upload</option>
                    </select>
                </div>
                <div class="form-group mb-6">
                    <label for="content" class="block text-gray-800 font-semibold mb-3 text-lg">Enter Content</label>
                    <textarea id="content" rows="5" class="w-full p-4 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-green-500 transition" placeholder="Paste text/URL, or upload image/audio file..."></textarea>
                </div>
                <div class="form-group mb-6">
                    <label for="category" class="block text-gray-800 font-semibold mb-3 text-lg">Industry/Category</label>
                    <select id="category" class="w-full p-4 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-green-500 transition">
                        <option>Health</option>
                        <option>Technology</option>
                        <option>Finance</option>
                        <option>Environment</option>
                        <option>Education</option>
                        <option>Economy</option>
                        <option>Social Issues</option>
                        <option>Other</option>
                    </select>
                </div>
                <div class="form-group mb-6">
                    <label for="language" class="block text-gray-800 font-semibold mb-3 text-lg">Language</label>
                    <select id="language" class="w-full p-4 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-green-500 transition">
                        <option>English</option>
                        <option>Krio</option>
                    </select>
                </div>
                <button onclick="showVerdict()" class="btn-primary text-white px-8 py-4 rounded-full font-semibold text-lg pulse">Verify Now!</button>
                <div id="verdict" class="verdict mt-8 p-6 rounded-lg opacity-0 translate-y-4 hidden" style="background-color: #d1fae5; border: 1px solid #a7f3d0; color: #065f46;">
                    <h3 class="text-xl font-semibold mb-2">Verdict: True</h3>
                    <p>Explanation: The image shows accurate data on Sierra Leone's GDP growth. Confidence: 92%.</p>
                    <p class="mt-2">Sources: <a href="#" class="underline hover:text-green-600">World Bank Report</a>, <a href="#" class="underline hover:text-green-600">Sierra Leone Stats</a></p>
                    <p class="text-sm mt-3 font-mono">Blockchain Hash: 0xabc123... (Verified on Polygon - Sept 6, 2025)</p>
                </div>
            </div>
        </section>

        <!-- Verified News Section -->
        <section id="news" class="mb-20 slide-up">
            <h2 class="text-4xl font-bold text-gray-900 mb-6 bounce-text color-change">Blockchain-Verified News</h2>
            <p class="text-lg text-gray-700 mb-8">Catch the latest trusted updates from government, media, and industry pros, stamped on Polygon blockchain!</p>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <div class="card bg-white p-8 rounded-xl shadow-lg">
                    <p class="font-semibold text-blue-700 text-lg">Ministry of Health</p>
                    <p class="text-gray-600">New malaria prevention strategies launched!</p>
                    <p class="text-sm text-gray-500 mt-4 font-mono">Sept 5, 2025 - Blockchain Verified</p>
                </div>
                <div class="card bg-white p-8 rounded-xl shadow-lg">
                    <p class="font-semibold text-green-700 text-lg">Tech Hub SL</p>
                    <p class="text-gray-600">AI boosts farming tech in rural areas.</p>
                    <p class="text-sm text-gray-500 mt-4 font-mono">Sept 4, 2025 - Blockchain Verified</p>
                </div>
                <div class="card bg-white p-8 rounded-xl shadow-lg">
                    <p class="font-semibold text-blue-700 text-lg">Bank of Sierra Leone</p>
                    <p class="text-gray-600">Digital currency trials underway!</p>
                    <p class="text-sm text-gray-500 mt-4 font-mono">Sept 3, 2025 - Blockchain Verified</p>
                </div>
            </div>
        </section>

        <!-- Report Misinformation Section -->
        <section id="report" class="mb-20 slide-up">
            <h2 class="text-4xl font-bold text-gray-900 mb-6 bounce-text color-change">Report Information</h2>
            <p class="text-lg text-gray-700 mb-8">Spot something fishy? Report it anonymously and help us keep Sierra Leone’s info legit!</p>
            <div class="bg-white p-8 rounded-xl shadow-lg">
                <div class="form-group mb-6">
                    <label for="report" class="block text-gray-800 font-semibold mb-3 text-lg">Report Content</label>
                    <textarea id="report" rows="5" class="w-full p-4 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-green-500 transition" placeholder="e.g., 'Saw fake news about a finance scam on social media' or upload image/audio"></textarea>
                </div>
                <button onclick="showReportConfirmation()" class="btn-primary text-white px-8 py-4 rounded-full font-semibold text-lg pulse">Submit Report!</button>
                <div id="report-confirmation" class="mt-8 p-6 rounded-lg opacity-0 translate-y-4 hidden" style="background-color: #d4edda; border: 1px solid #c3e6cb; color: #155724;">
                    <p class="text-lg">Yay! Your report’s in! We’ll verify it soon. Check back for updates.</p>
                    <p class="text-sm mt-3 font-mono">Blockchain Hash: 0xghi789... (Logged on Polygon - Sept 6, 2025)</p>
                </div>
            </div>
        </section>

        <!-- Impact Section -->
        <section id="impact" class="mb-20 slide-up">
            <h2 class="text-4xl font-bold text-gray-900 mb-6 bounce-text color-change">Our Impact</h2>
            <p class="text-lg text-gray-700 mb-8">A super-fun platform for all Sierra Leoneans, covering every industry with awesome tech and local vibes!</p>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                <div class="card bg-white p-8 rounded-xl shadow-lg">
                    <h3 class="text-xl font-semibold text-blue-700 mb-4 color-change">Multi-Input Fun</h3>
                    <p class="text-gray-600">Toss in texts, URLs, images, or audio for epic verification!</p>
                </div>
                <div class="card bg-white p-8 rounded-xl shadow-lg">
                    <h3 class="text-xl font-semibold text-green-700 mb-4 color-change">Super Transparent</h3>
                    <p class="text-gray-600">Blockchain keeps records squeaky clean and auditable!</p>
                </div>
                <div class="card bg-white p-8 rounded-xl shadow-lg">
                    <h3 class="text-xl font-semibold text-blue-700 mb-4 color-change">All Industries</h3>
                    <p class="text-gray-600">Health, tech, finance, environment—we’ve got it all!</p>
                </div>
                <div class="card bg-white p-8 rounded-xl shadow-lg">
                    <h3 class="text-xl font-semibold text-green-700 mb-4 color-change">Cool Partnerships</h3>
                    <p class="text-gray-600">Teaming up with SLBC, government, and industry crews!</p>
                </div>
            </div>
        </section>

        <!-- Call to Action -->
        <section id="join" class="text-center bg-gradient-to-r from-blue-700 to-green-700 text-white py-16 rounded-xl slide-up">
            <h2 class="text-4xl font-bold mb-6 bounce-text">Join the Truth Party!</h2>
            <p class="text-lg max-w-3xl mx-auto mb-8">Team up with us to make Sierra Leone’s info scene awesome. We need developers and partners to rock this!</p>
            <a href="mailto:info@sltruthplatform.sl" class="btn-primary text-white px-8 py-4 rounded-full font-semibold text-lg pulse">Get Involved Now!</a>
        </section>
    </main>

    <!-- Footer -->
    <footer class="bg-gray-900 text-white text-center py-8">
        <p class="text-lg">&copy; 2025 Sierra Leone Truth Platform. Powered by xAI and Polygon.</p>
        <p class="text-sm mt-2">Contact: <a href="mailto:info@sltruthplatform.sl" class="underline hover:text-green-400">info@sltruthplatform.sl</a> | Partners: SLBC, Ministry of Health, Fourah Bay College</p>
    </footer>

    <!-- JavaScript for Interactivity -->
    <script>
        // Smooth scrolling for navigation
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });

        // Show verdict with animation
        function showVerdict() {
            const verdict = document.getElementById('verdict');
            verdict.classList.remove('hidden');
            verdict.classList.add('show');
            verdict.scrollIntoView({ behavior: 'smooth' });
        }

        // Show report confirmation with animation
        function showReportConfirmation() {
            const confirmation = document.getElementById('report-confirmation');
            confirmation.classList.remove('hidden');
            confirmation.classList.add('show');
            confirmation.scrollIntoView({ behavior: 'smooth' });
        }

        // Show chat response with animation
        function showChatResponse() {
            const response = document.getElementById('chat-response');
            response.classList.remove('hidden');
            response.classList.add('show');
            response.scrollIntoView({ behavior: 'smooth' });
        }

        // Trigger slide-up animations on scroll
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('slide-up');
                }
            });
        }, { threshold: 0.2 });

        document.querySelectorAll('.slide-up').forEach(element => {
            observer.observe(element);
        });
    </script>
</body>
</html>
