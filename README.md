<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The visual Compass</title>
    <!-- Load Tailwind CSS via CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Load Font Awesome for Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <!-- Set Custom Tailwind Configuration -->
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        'primary-dark': '#1F2937', // Deep Charcoal
                        'secondary-dark': '#374151', // Slightly Lighter Gray
                        'accent-blue': '#3B82F6', // Vibrant Blue
                        'accent-cyan': '#06B6D4', // Bright Cyan
                        'text-light': '#F9FAFB',
                    },
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                    }
                }
            }
        }
    </script>
    
    <!-- Custom CSS for Attractive Background and Structure -->
    <style>
        /* 1. Attractive Background (Dark, fixed, subtle texture) */
        body {
            background-color: #0e0e27; /* Slate 900 */
           
            color: #ffffff;
            font-family: 'Inter', sans-serif;
            line-height: 1.6;
            
        }

        /* Subtle animated background texture */
        .page-background {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -10;
            opacity: 0.1;
            background-image: radial-gradient(#1E293B 1px, transparent 1px);
            background-size: 40px 40px;
            
        }

        /* Smooth scroll for navigation */
        html {
            scroll-behavior: smooth;
        }

        /* Specific section padding */
        section {
            padding: 4rem 1rem;
            min-height: 80vh;
        }

        /* Table specific styling for visibility */
        .styled-table th, .styled-table td {
            border: 1px solid #4B5563; /* Gray-600 border */
        }
    </style>
</head>
<body class="min-h-screen antialiased">

    <!-- Subtle Background Effect -->
    <div class="page-background"></div>

    <!-- 2. Navigation Bar (Sticky, responsive) -->
    <header class="sticky top-0 z-50 shadow-lg bg-primary-dark/95 backdrop-blur-sm">
        <div class="container mx-auto px-4 sm:px-6 lg:px-8 flex justify-between items-center py-4">
            
            <!-- 7. Logo (Text/SVG Combination) -->
            <a href="#home" class="flex items-center text-2xl font-bold text-accent-cyan">
                <svg class="w-6 h-6 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 19V6l12-3v13M10 4l6 2m-1 8l-6 2"></path></svg>
                 **GYM**
            </a>

            <!-- Desktop Navigation Links -->
            <nav class="hidden md:flex space-x-6">
                <a href="#home" class="text-text-light hover:text-accent-blue transition duration-300">Home</a>
                <a href="#images" class="text-text-light hover:text-accent-blue transition duration-300">Images</a>
                <a href="#videos" class="text-text-light hover:text-accent-blue transition duration-300">Videos</a>
                <a href="#audio" class="text-text-light hover:text-accent-blue transition duration-300">Audio</a>
                <a href="#tables" class="text-text-light hover:text-accent-blue transition duration-300">Tables</a>
                <a href="#lists" class="text-text-light hover:text-accent-blue transition duration-300">Lists</a>
            </nav>

            <!-- Mobile Menu Button -->
            <button id="menu-toggle" class="md:hidden text-text-light focus:outline-none p-2 rounded-md hover:bg-secondary-dark/50">
                <i class="fas fa-bars text-xl"></i>
            </button>
        </div>
        
        <!-- Mobile Navigation Drawer -->
        <nav id="mobile-menu" class="hidden md:hidden bg-secondary-dark/95 pb-4">
            <a href="#home" class="block py-2 px-4 text-text-light hover:bg-secondary-dark border-b border-primary-dark" onclick="toggleMenu()">Home</a>
            <a href="#images" class="block py-2 px-4 text-text-light hover:bg-secondary-dark border-b border-primary-dark" onclick="toggleMenu()">Images</a>
            <a href="#videos" class="block py-2 px-4 text-text-light hover:bg-secondary-dark border-b border-primary-dark" onclick="toggleMenu()">Videos</a>
            <a href="#audio" class="block py-2 px-4 text-text-light hover:bg-secondary-dark border-b border-primary-dark" onclick="toggleMenu()">Audio</a>
            <a href="#tables" class="block py-2 px-4 text-text-light hover:bg-secondary-dark border-b border-primary-dark" onclick="toggleMenu()">Tables</a>
            <a href="#lists" class="block py-2 px-4 text-text-light hover:bg-secondary-dark" onclick="toggleMenu()">Lists</a>
        </nav>
    </header>
    

    <main class="container mx-auto">
        
        <!-- HOME SECTION -->
        <section id="home" class="text-center flex flex-col items-center justify-center pt-24 pb-16">
            <h1 class="text-5xl sm:text-7xl font-extrabold tracking-tight mb-4 text-transparent bg-clip-text bg-gradient-to-r from-accent-cyan to-accent-blue">
                Kevin the trainer's Fitness GYM
            </h1>
            <p class="text-lg sm:text-xl max-w-3xl text-gray-300 mb-8">
                Welcome to our Gym.
Whether you’re a beginner or a pro, this is your space to grow, improve, and push your limits.
            </p>
             
            <div class="space-x-4">
                <a href="#images" class="inline-flex items-center px-6 py-3 border border-transparent text-base font-medium rounded-full shadow-sm text-primary-dark bg-accent-cyan hover:bg-cyan-400 transition duration-300">
                    <i class="fas fa-camera mr-2"></i> View Media
                </a>
                <a href="#tables" class="inline-flex items-center px-6 py-3 border border-accent-blue text-base font-medium rounded-full text-accent-blue hover:bg-accent-blue hover:text-text-light transition duration-300">
                    <i class="fas fa-database mr-2"></i> Check Data
                </a>
            </div>
            
        </section>

        <!-- IMAGES SECTION -->
        <section id="images" class="bg-secondary-dark/30 rounded-xl shadow-2xl">
            <h2 class="text-4xl font-bold mb-8 border-b-2 border-accent-cyan pb-2">GYM's Gallery</h2>
            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">
                <!-- 3. Images (Placeholders) -->
                <div class="bg-primary-dark rounded-lg overflow-hidden shadow-xl hover:shadow-accent-blue/50 transition duration-500 transform hover:scale-[1.02]">
                    <img src="download (1).jfif" alt="Liffting weights" class="w-full h-48 object-cover">
                    <div class="p-4">
                        <h3 class="font-semibold text-lg text-accent-blue">Lifting Section</h3>
                        <p class="text-gray-400 text-sm">For every persons.</p>
                    </div>
                </div>
                
                <div class="bg-primary-dark rounded-lg overflow-hidden shadow-xl hover:shadow-accent-blue/50 transition duration-500 transform hover:scale-[1.02]">
                    <img src="download (2).jfif" alt="Vector Design Placeholder 2" class="w-full h-48 object-cover">
                    <div class="p-4">
                        <h3 class="font-semibold text-lg text-accent-cyan">Running Section</h3>
                        <p class="text-gray-400 text-sm">If you need your body to stay feet.</p>
                    </div>
                </div>
                <div class="bg-primary-dark rounded-lg overflow-hidden shadow-xl hover:shadow-accent-blue/50 transition duration-500 transform hover:scale-[1.02]">
                    <img src="images (2).jfif" alt="Vector Design Placeholder 2" class="w-full h-48 object-cover">
                    <div class="p-4">
                        <h3 class="font-semibold text-lg text-accent-cyan">Strecing Section</h3>
                        <p class="text-gray-400 text-sm">To strengthen our body.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- VIDEOS SECTION -->
        <section id="videos">
            <h2 class="text-4xl font-bold mb-8 border-b-2 border-accent-blue pb-2">Video Demonstration</h2>
            <div class="max-w-4xl mx-auto bg-secondary-dark p-6 rounded-xl shadow-2xl">
                <h3 class="text-xl font-semibold mb-4 text-gray-200">Interactive Code Snippet Demo</h3>
                <!-- 3. Videos (Placeholder Embed - using responsive aspect ratio) -->
                <div class="aspect-video w-full rounded-lg overflow-hidden shadow-inner shadow-primary-dark">
                    <!-- Placeholder YouTube embed structure -->
                    <iframe 
                        width="100%" 
                        height="100%" 
                        src="https://www.pinterest.com/pin/19984792092215617/" 
                        title="Video Placeholder" 
                        frameborder="0" 
                        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
                        allowfullscreen
                        onerror="this.parentNode.innerHTML='<div class=\'flex items-center justify-center w-full h-full bg-red-800/50 text-white p-4\'>Video failed to load or is restricted. Placeholder shown.</div>'"
                    ></iframe>
                </div>
                <p class="text-sm text-gray-400 mt-3 italic">Note: This video is a general placeholder for demonstration purposes.</p>
            </div>
        </section>

        <!-- AUDIO SECTION -->
        <section id="audio" class="bg-secondary-dark/30 rounded-xl shadow-2xl">
            <h2 class="text-4xl font-bold mb-8 border-b-2 border-accent-cyan pb-2">Audio Log & Sample</h2>
            <div class="max-w-2xl mx-auto space-y-6">
                <!-- 3. Audio (Placeholder Player) -->
                <div class="bg-primary-dark p-6 rounded-lg shadow-xl flex flex-col sm:flex-row items-center justify-between">
                    <div class="flex items-center mb-4 sm:mb-0">
                        <i class="fas fa-music text-3xl text-accent-cyan mr-4"></i>
                        <div>
                            <p class="font-semibold text-gray-100">Ambient Background Track</p>
                            <p class="text-sm text-gray-400">Loop 01 - Exploration Theme</p>
                        </div>
                    </div>
                    <!-- HTML5 Audio Element -->
                    <audio controls class="w-full sm:w-auto mt-4 sm:mt-0">
                        <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mp3">
                        Your browser does not support the audio element.
                    </audio>
                </div>
                <p class="text-gray-400 text-center">Use the player above to listen to a sample. The controls are provided by the standard HTML5 audio element.</p>
            </div>
        </section>

        <!-- TABLES SECTION -->
        <section id="tables">
            <h2 class="text-4xl font-bold mb-8 border-b-2 border-accent-blue pb-2">Structured Data (Table)</h2>
            <div class="overflow-x-auto bg-secondary-dark rounded-xl shadow-2xl p-4">
                <!-- 5. Tables -->
                <table class="styled-table w-full text-left text-sm text-gray-400 border-collapse">
                    <caption class="p-5 text-lg font-semibold text-text-light bg-secondary-dark rounded-t-lg">
                        Project Completion Status by Module
                        <p class="mt-1 text-sm font-normal text-gray-400">Tracking progress across main development streams.</p>
                    </caption>
                    <thead class="text-xs text-text-light uppercase bg-primary-dark">
                        <tr>
                            <th scope="col" class="px-6 py-3 rounded-tl-lg">Module</th>
                            <th scope="col" class="px-6 py-3">Owner</th>
                            <th scope="col" class="px-6 py-3">Status</th>
                            <th scope="col" class="px-6 py-3 rounded-tr-lg">Progress</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr class="bg-secondary-dark hover:bg-gray-700 transition duration-150">
                            <th scope="row" class="px-6 py-4 font-medium text-text-light whitespace-nowrap">Frontend UI</th>
                            <td class="px-6 py-4">Alice P.</td>
                            <td class="px-6 py-4 text-accent-cyan">In Review</td>
                            <td class="px-6 py-4">90%</td>
                        </tr>
                        <tr class="bg-secondary-dark hover:bg-gray-700 transition duration-150">
                            <th scope="row" class="px-6 py-4 font-medium text-text-light whitespace-nowrap">API Integration</th>
                            <td class="px-6 py-4">Bob S.</td>
                            <td class="px-6 py-4 text-green-400">Completed</td>
                            <td class="px-6 py-4">100%</td>
                        </tr>
                        <tr class="bg-secondary-dark hover:bg-gray-700 transition duration-150">
                            <th scope="row" class="px-6 py-4 font-medium text-text-light whitespace-nowrap">Database Schema</th>
                            <td class="px-6 py-4">Charlie D.</td>
                            <td class="px-6 py-4 text-yellow-400">In Progress</td>
                            <td class="px-6 py-4">65%</td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </section>

        <!-- LISTS SECTION -->
        <section id="lists" class="bg-secondary-dark/30 rounded-xl shadow-2xl">
            <h2 class="text-4xl font-bold mb-8 border-b-2 border-accent-cyan pb-2">Structured Content (Lists)</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
                
                <!-- 6. Unordered List -->
                <div class="p-6 bg-primary-dark rounded-lg shadow-xl">
                    <h3 class="text-2xl font-semibold mb-4 text-accent-cyan">Key Features</h3>
                    <ul class="space-y-3 list-disc list-inside text-gray-300">
                        <li class="hover:text-text-light transition duration-150"><i class="fas fa-check-circle text-accent-blue mr-2"></i> Real-time data synchronization.</li>
                        <li class="hover:text-text-light transition duration-150"><i class="fas fa-check-circle text-accent-blue mr-2"></i> Multi-platform access.</li>
                        <li class="hover:text-text-light transition duration-150"><i class="fas fa-check-circle text-accent-blue mr-2"></i> Customizable user profiles.</li>
                        <li class="hover:text-text-light transition duration-150"><i class="fas fa-check-circle text-accent-blue mr-2"></i> High-resolution asset support.</li>
                    </ul>
                </div>

                <!-- 6. Ordered List -->
                <div class="p-6 bg-primary-dark rounded-lg shadow-xl">
                    <h3 class="text-2xl font-semibold mb-4 text-accent-blue">Deployment Steps</h3>
                    <ol class="space-y-3 list-decimal list-inside text-gray-300">
                        <li class="hover:text-text-light transition duration-150"><span class="font-bold text-accent-cyan">Initialize</span>: Configure environment variables.</li>
                        <li class="hover:text-text-light transition duration-150"><span class="font-bold text-accent-cyan">Compile</span>: Run build scripts and minimize assets.</li>
                        <li class="hover:text-text-light transition duration-150"><span class="font-bold text-accent-cyan">Validate</span>: Execute automated security checks.</li>
                        <li class="hover:text-text-light transition duration-150"><span class="font-bold text-accent-cyan">Deploy</span>: Push artifact to staging server.</li>
                    </ol>
                </div>
            </div>
        </section>
        
    </main>

    <!-- 4. Good Footer -->
    <footer class="bg-primary-dark border-t border-gray-700 mt-12">
        <div class="container mx-auto px-4 py-12">
            <div class="grid grid-cols-2 md:grid-cols-4 gap-8">
                
                <!-- Footer Column 1: Logo & Mission -->
                <div>
                    <a href="#home" class="flex items-center text-xl font-bold text-accent-cyan mb-4">
                        <svg class="w-5 h-5 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 19V6l12-3v13M10 4l6 2m-1 8l-6 2"></path></svg>
                        **GYM**
                    </a>
                    <p class="text-sm text-gray-400">Guiding you through the digital landscape with structured and accessible content.</p>
                </div>

                <!-- Footer Column 2: Quick Links -->
                <div>
                    <h5 class="text-lg font-semibold text-text-light mb-4">Site Map</h5>
                    <ul class="space-y-2 text-sm text-gray-400">
                        <li><a href="#home" class="hover:text-accent-blue transition duration-300">Home</a></li>
                        <li><a href="#tables" class="hover:text-accent-blue transition duration-300">Data Tables</a></li>
                        <li><a href="#lists" class="hover:text-accent-blue transition duration-300">Lists & Steps</a></li>
                        <li><a href="#videos" class="hover:text-accent-blue transition duration-300">Media Vault</a></li>
                    </ul>
                </div>

                <!-- Footer Column 3: Resources -->
                <div>
                    <h5 class="text-lg font-semibold text-text-light mb-4">Resources</h5>
                    <ul class="space-y-2 text-sm text-gray-400">
                        <li><a href="#" class="hover:text-accent-blue transition duration-300">Documentation</a></li>
                        <li><a href="#" class="hover:text-accent-blue transition duration-300">API Status</a></li>
                        <li><a href="#" class="hover:text-accent-blue transition duration-300">Help Center</a></li>
                        <li><a href="#" class="hover:text-accent-blue transition duration-300">Privacy Policy</a></li>
                    </ul>
                </div>

                <!-- Footer Column 4: Contact & Social -->
                <div>
                    <h5 class="text-lg font-semibold text-text-light mb-4">Connect</h5>
                    <p class="text-sm text-gray-400 mb-4">Email: contact@compass.dev</p>
                    <div class="flex space-x-4">
                        <a href="#" class="text-gray-400 hover:text-accent-cyan transition duration-300"><i class="fab fa-twitter text-xl"></i></a>
                        <a href="#" class="text-gray-400 hover:text-accent-blue transition duration-300"><i class="fab fa-github text-xl"></i></a>
                        <a href="#" class="text-gray-400 hover:text-accent-blue transition duration-300"><i class="fab fa-linkedin text-xl"></i></a>
                    </div>
                </div>
            </div>

            <div class="mt-12 pt-6 border-t border-gray-800 text-center text-sm text-gray-500">
                &copy; 2025 The Visual Compass. All rights reserved. Built with Tailwind CSS.
            </div>
        </div>
    </footer>

    <!-- JavaScript for Mobile Menu Toggle -->
    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const menuToggle = document.getElementById('menu-toggle');
            const mobileMenu = document.getElementById('mobile-menu');

            window.toggleMenu = function() {
                mobileMenu.classList.toggle('hidden');
                // Change icon from bars to X when open
                const icon = menuToggle.querySelector('i');
                if (mobileMenu.classList.contains('hidden')) {
                    icon.classList.remove('fa-times');
                    icon.classList.add('fa-bars');
                } else {
                    icon.classList.remove('fa-bars');
                    icon.classList.add('fa-times');
                }
            }

            menuToggle.addEventListener('click', window.toggleMenu);
        });
    </script>

</body>
</html>
