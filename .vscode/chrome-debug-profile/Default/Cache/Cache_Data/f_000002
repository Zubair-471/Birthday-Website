// Main JavaScript for Birthday Website

// Global variables
let currentAudio = null;
let isPlaying = false;
let currentSongIndex = 0;

// Song playlist
const songs = [
    { title: "Birthday Song", artist: "Special", file: "home_song.mp3" },
    { title: "Love Letter", artist: "Romantic", file: "letter_song.mp3" },
    { title: "Memory Lane", artist: "Nostalgic", file: "memories_song.mp3" },
    { title: "Surprise", artist: "Exciting", file: "surprise_song.mp3" }
];

// Sample quiz questions
const quizQuestions = [
    {
        question: "What's the most beautiful thing about love?",
        options: ["The way it makes you feel", "The memories you create", "The person you share it with", "All of the above"],
        correct: 3
    },
    {
        question: "What's the best way to celebrate a birthday?",
        options: ["With cake and presents", "With loved ones", "With laughter and joy", "All of the above"],
        correct: 3
    },
    {
        question: "What makes a relationship special?",
        options: ["Trust and communication", "Shared experiences", "Unconditional love", "All of the above"],
        correct: 3
    },
    {
        question: "What's the most important thing in life?",
        options: ["Success and money", "Love and happiness", "Health and family", "All of the above"],
        correct: 2
    },
    {
        question: "What's the best gift you can give someone?",
        options: ["Expensive jewelry", "Your time and love", "A surprise party", "All of the above"],
        correct: 1
    }
];

// Sample love messages
const loveMessages = [
    "You are my everything, my heart, my soul, my love. Every day with you is a blessing I cherish deeply.",
    "Your smile brightens my darkest days, your laugh is the most beautiful music I've ever heard.",
    "You make every day feel like a celebration just by being you. You are truly amazing.",
    "Thank you for being the most wonderful person in my life. I love you endlessly.",
    "Every moment with you is precious, every touch is electric, every glance is magical.",
    "You are the love of my life, my best friend, my soulmate. I'm so grateful for you.",
    "Your love has changed my life in the most beautiful ways. You are my greatest blessing.",
    "I fall in love with you more and more each day. You are perfect in every way.",
    "You are the reason I believe in love, in magic, in happily ever after.",
    "My heart beats only for you, my thoughts are always of you, my love is forever yours."
];

// Sample timeline events
const timelineEvents = [
    { date: "First Meeting", event: "The day our eyes first met and our hearts knew they had found home." },
    { date: "First Date", event: "A magical evening that changed everything and made us believe in love at first sight." },
    { date: "First Kiss", event: "The moment that sealed our fate and made us realize we were meant to be together." },
    { date: "First Home", event: "Building our nest together, creating a space filled with love and laughter." },
    { date: "First Promise", event: "The day we promised to love each other forever, no matter what life brings." },
    { date: "Overcoming Challenges", event: "Facing life's challenges together and coming out stronger and more in love." },
    { date: "Every Birthday", event: "Celebrating each year of your beautiful life and the joy you bring to mine." }
];

// Initialize when DOM is loaded
document.addEventListener('DOMContentLoaded', function() {
    initializeFloatingElements();
    initializeMusicPlayer();
    initializeCountdown();
    initializeInteractiveElements();
    initializeLoadingScreen();
    initializeSmoothScroll();
    initializeScrollToTop();
});

// Floating Hearts Animation
function initializeFloatingElements() {
    const heartsContainer = document.querySelector('.floating-hearts');
    if (!heartsContainer) return;

    // Create 18 floating hearts
    for (let i = 0; i < 18; i++) {
        const heart = document.createElement('div');
        heart.className = 'heart';
        heart.innerHTML = '💖';
        heart.style.left = Math.random() * 100 + '%';
        heart.style.animationDelay = Math.random() * 6 + 's';
        heart.style.animationDuration = (Math.random() * 3 + 3) + 's';
        heartsContainer.appendChild(heart);
    }
}

// Confetti Animation
function createConfetti() {
    const confettiContainer = document.querySelector('.confetti');
    if (!confettiContainer) return;

    // Create 40 confetti pieces
    for (let i = 0; i < 40; i++) {
        const confetti = document.createElement('div');
        confetti.className = 'confetti-piece';
        confetti.style.left = Math.random() * 100 + '%';
        confetti.style.animationDelay = Math.random() * 3 + 's';
        confetti.style.animationDuration = (Math.random() * 2 + 2) + 's';
        confetti.style.backgroundColor = `hsl(${Math.random() * 360}, 100%, 70%)`;
        confettiContainer.appendChild(confetti);
    }
}

// Sparkle Effect
function createSparkles(x, y) {
    for (let i = 0; i < 10; i++) {
        const sparkle = document.createElement('div');
        sparkle.className = 'sparkle';
        sparkle.style.left = (x + Math.random() * 100 - 50) + 'px';
        sparkle.style.top = (y + Math.random() * 100 - 50) + 'px';
        sparkle.style.animationDelay = Math.random() * 0.5 + 's';
        document.body.appendChild(sparkle);
        
        setTimeout(() => {
            sparkle.remove();
        }, 1500);
    }
}

// Countdown Timer
function initializeCountdown() {
    const countdownElement = document.getElementById('countdown');
    if (!countdownElement) return;

    const birthdayDate = new Date('January 1, 2026 00:00:00').getTime();

    function updateCountdown() {
        const now = new Date().getTime();
        const distance = birthdayDate - now;

        const days = Math.floor(distance / (1000 * 60 * 60 * 24));
        const hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
        const minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
        const seconds = Math.floor((distance % (1000 * 60)) / 1000);

        const countdownHTML = `
            <div class="countdown-item">
                <span class="countdown-number">${days}</span>
                <span class="countdown-label">Days</span>
            </div>
            <div class="countdown-item">
                <span class="countdown-number">${hours}</span>
                <span class="countdown-label">Hours</span>
            </div>
            <div class="countdown-item">
                <span class="countdown-number">${minutes}</span>
                <span class="countdown-label">Minutes</span>
            </div>
            <div class="countdown-item">
                <span class="countdown-number">${seconds}</span>
                <span class="countdown-label">Seconds</span>
            </div>
        `;

        countdownElement.innerHTML = countdownHTML;

        // Update button text when countdown reaches zero
        if (distance < 0) {
            const celebrateBtn = document.querySelector('.btn');
            if (celebrateBtn) {
                celebrateBtn.textContent = 'Celebrate Now! 🎉';
            }
        }
    }

    updateCountdown();
    setInterval(updateCountdown, 1000);
}

// Music Player
function initializeMusicPlayer() {
    const musicPlayer = document.querySelector('.music-player');
    if (!musicPlayer) return;

    const audio = document.createElement('audio');
    audio.src = `assets/music/${songs[currentSongIndex].file}`;
    audio.volume = 0.5;
    musicPlayer.appendChild(audio);

    const playBtn = musicPlayer.querySelector('.play-btn');
    const pauseBtn = musicPlayer.querySelector('.pause-btn');
    const nextBtn = musicPlayer.querySelector('.next-btn');
    const prevBtn = musicPlayer.querySelector('.prev-btn');
    const volumeSlider = musicPlayer.querySelector('.volume-slider');
    const musicTitle = musicPlayer.querySelector('.music-title');
    const musicArtist = musicPlayer.querySelector('.music-artist');

    // Update music info
    function updateMusicInfo() {
        musicTitle.textContent = songs[currentSongIndex].title;
        musicArtist.textContent = songs[currentSongIndex].artist;
    }

    // Play music
    function playMusic() {
        audio.play();
        isPlaying = true;
        playBtn.style.display = 'none';
        pauseBtn.style.display = 'block';
        musicPlayer.classList.add('playing');
    }

    // Pause music
    function pauseMusic() {
        audio.pause();
        isPlaying = false;
        playBtn.style.display = 'block';
        pauseBtn.style.display = 'none';
        musicPlayer.classList.remove('playing');
    }

    // Next song
    function nextSong() {
        currentSongIndex = (currentSongIndex + 1) % songs.length;
        audio.src = `assets/music/${songs[currentSongIndex].file}`;
        updateMusicInfo();
        if (isPlaying) {
            audio.play();
        }
    }

    // Previous song
    function prevSong() {
        currentSongIndex = (currentSongIndex - 1 + songs.length) % songs.length;
        audio.src = `assets/music/${songs[currentSongIndex].file}`;
        updateMusicInfo();
        if (isPlaying) {
            audio.play();
        }
    }

    // Event listeners
    if (playBtn) playBtn.addEventListener('click', playMusic);
    if (pauseBtn) pauseBtn.addEventListener('click', pauseMusic);
    if (nextBtn) nextBtn.addEventListener('click', nextSong);
    if (prevBtn) prevBtn.addEventListener('click', prevSong);
    if (volumeSlider) {
        volumeSlider.addEventListener('input', (e) => {
            audio.volume = e.target.value / 100;
        });
    }

    // Audio ended event
    audio.addEventListener('ended', nextSong);

    updateMusicInfo();
}

// Interactive Elements
function initializeInteractiveElements() {
    // Envelope interaction
    const envelope = document.querySelector('.envelope');
    if (envelope) {
        envelope.addEventListener('click', function() {
            this.classList.add('open');
            createSparkles(event.clientX, event.clientY);
            
            setTimeout(() => {
                const letterContent = document.querySelector('.letter-content');
                if (letterContent) {
                    letterContent.style.display = 'block';
                    letterContent.classList.add('fade-in');
                }
            }, 500);
        });

        // Auto-open envelope after 3 seconds
        setTimeout(() => {
            envelope.click();
        }, 3000);
    }

    // Gift box interaction
    const giftBox = document.querySelector('.gift-box');
    if (giftBox) {
        giftBox.addEventListener('click', function() {
            this.classList.add('open');
            createSparkles(event.clientX, event.clientY);
            
            setTimeout(() => {
                const surpriseContent = document.querySelector('.surprise-content');
                if (surpriseContent) {
                    surpriseContent.style.display = 'block';
                    surpriseContent.classList.add('fade-in');
                }
            }, 1000);
        });
    }

    // Cake interaction
    const cake = document.querySelector('.cake');
    if (cake) {
        cake.addEventListener('click', function() {
            // Blow out candle effect
            const flame = this.querySelector('.flame') || this;
            flame.style.animation = 'none';
            flame.style.opacity = '0';
            
            // Create wish animation
            const wish = document.createElement('div');
            wish.textContent = '✨ Make a wish! ✨';
            wish.style.position = 'absolute';
            wish.style.top = '-50px';
            wish.style.left = '50%';
            wish.style.transform = 'translateX(-50%)';
            wish.style.color = '#ffd700';
            wish.style.fontSize = '1rem';
            wish.style.animation = 'float 2s ease-out forwards';
            this.appendChild(wish);
            
            createSparkles(event.clientX, event.clientY);
            
            setTimeout(() => {
                wish.remove();
            }, 2000);
        });
    }

    // Card click effects
    const cards = document.querySelectorAll('.nav-card');
    cards.forEach(card => {
        card.addEventListener('click', function(e) {
            // Create ripple effect
            const ripple = document.createElement('div');
            ripple.style.position = 'absolute';
            ripple.style.borderRadius = '50%';
            ripple.style.background = 'rgba(255, 255, 255, 0.3)';
            ripple.style.transform = 'scale(0)';
            ripple.style.animation = 'ripple 0.6s linear';
            ripple.style.left = (e.clientX - this.offsetLeft) + 'px';
            ripple.style.top = (e.clientY - this.offsetTop) + 'px';
            ripple.style.width = ripple.style.height = '20px';
            
            this.appendChild(ripple);
            
            setTimeout(() => {
                ripple.remove();
            }, 600);
        });
    });

    // Quiz functionality
    initializeQuiz();
}

// Quiz System
function initializeQuiz() {
    const quizContainer = document.querySelector('.quiz-container');
    if (!quizContainer) return;

    const questions = quizQuestions;

    let currentQuestion = 0;
    let score = 0;

    function displayQuestion() {
        const question = questions[currentQuestion];
        const quizHTML = `
            <div class="quiz-question">
                <h3>Question ${currentQuestion + 1}</h3>
                <p>${question.question}</p>
                <div class="quiz-options">
                    ${question.options.map((option, index) => `
                        <div class="quiz-option" data-index="${index}">
                            ${option}
                        </div>
                    `).join('')}
                </div>
            </div>
        `;
        quizContainer.innerHTML = quizHTML;

        // Add event listeners to options
        const options = quizContainer.querySelectorAll('.quiz-option');
        options.forEach(option => {
            option.addEventListener('click', handleAnswer);
        });
    }

    function handleAnswer(e) {
        const selectedIndex = parseInt(e.target.dataset.index);
        const question = questions[currentQuestion];
        
        // Disable all options
        const options = document.querySelectorAll('.quiz-option');
        options.forEach(option => {
            option.style.pointerEvents = 'none';
        });

        // Show correct/incorrect
        if (selectedIndex === question.correct) {
            e.target.classList.add('correct');
            score++;
            createSparkles(e.clientX, e.clientY);
        } else {
            e.target.classList.add('incorrect');
            options[question.correct].classList.add('correct');
        }

        // Next question after delay
        setTimeout(() => {
            currentQuestion++;
            if (currentQuestion < questions.length) {
                displayQuestion();
            } else {
                showQuizResults();
            }
        }, 2000);
    }

    function showQuizResults() {
        const percentage = Math.round((score / questions.length) * 100);
        const message = percentage === 100 ? 
            "Perfect! You know everything about love! 💖" :
            percentage >= 70 ? 
            "Great! You have a beautiful heart! 💕" :
            "You're learning about love, and that's beautiful! 🌸";

        quizContainer.innerHTML = `
            <div class="quiz-question">
                <h3>Quiz Complete!</h3>
                <p>Your score: ${score}/${questions.length} (${percentage}%)</p>
                <p>${message}</p>
                <button class="btn" onclick="location.reload()">Take Quiz Again</button>
            </div>
        `;
    }

    displayQuestion();
}

// Modal System
function showModal(content) {
    const modal = document.createElement('div');
    modal.className = 'modal';
    modal.innerHTML = `
        <div class="modal-content">
            <button class="modal-close">&times;</button>
            ${content}
        </div>
    `;

    document.body.appendChild(modal);
    
    // Show modal
    setTimeout(() => {
        modal.classList.add('show');
    }, 10);

    // Close modal
    const closeBtn = modal.querySelector('.modal-close');
    closeBtn.addEventListener('click', () => {
        modal.classList.remove('show');
        setTimeout(() => {
            modal.remove();
        }, 300);
    });

    modal.addEventListener('click', (e) => {
        if (e.target === modal) {
            closeBtn.click();
        }
    });
}

// Message Carousel
function initializeMessageCarousel() {
    const carousel = document.querySelector('.message-carousel');
    if (!carousel) return;

    const messages = [
        "Every moment with you is a gift I cherish deeply 💖",
        "Your smile lights up my world like nothing else ✨",
        "You make every day feel like a celebration 🎉",
        "My heart beats only for you, now and forever 💕",
        "You are the missing piece that makes my life complete 🧩"
    ];

    let currentMessage = 0;

    function showMessage(index) {
        const slides = carousel.querySelectorAll('.message-slide');
        slides.forEach((slide, i) => {
            slide.classList.remove('active');
            if (i === index) {
                slide.classList.add('active');
                slide.innerHTML = `<p>${messages[index]}</p>`;
            }
        });
    }

    function nextMessage() {
        currentMessage = (currentMessage + 1) % messages.length;
        showMessage(currentMessage);
    }

    function prevMessage() {
        currentMessage = (currentMessage - 1 + messages.length) % messages.length;
        showMessage(currentMessage);
    }

    // Initialize first message
    showMessage(0);

    // Add navigation buttons
    const nav = document.createElement('div');
    nav.className = 'carousel-nav';
    nav.innerHTML = `
        <button class="carousel-btn prev-btn">‹</button>
        <button class="carousel-btn next-btn">›</button>
    `;
    carousel.appendChild(nav);

    nav.querySelector('.prev-btn').addEventListener('click', prevMessage);
    nav.querySelector('.next-btn').addEventListener('click', nextMessage);

    // Auto-advance messages
    setInterval(nextMessage, 5000);
}

// Loading Screen
function initializeLoadingScreen() {
    const loading = document.querySelector('.loading');
    if (!loading) return;

    // Hide loading screen after 2 seconds
    setTimeout(() => {
        loading.classList.add('hidden');
        setTimeout(() => {
            loading.remove();
        }, 500);
    }, 2000);
}

// Memory System
function initializeMemories() {
    const memories = {
        'first-meeting': { icon: '💕', title: 'First Meeting', desc: 'The day we first met', date: 'Our Beginning', media: '/images/memory1.svg' },
        'first-chat': { icon: '📱', title: 'First Conversation', desc: 'Our first meaningful conversation', date: 'Getting to Know Each Other', media: '/images/memory2.svg' },
        'first-date': { icon: '🍽️', title: 'First Date', desc: 'Our magical first date together', date: 'Romance Begins', media: '/images/memory3.svg' },
        'first-kiss': { icon: '💋', title: 'First Kiss', desc: 'That unforgettable moment', date: 'Love Blooms', media: '/images/memory4.svg' },
        'first-travel': { icon: '✈️', title: 'First Trip', desc: 'Our first adventure together', date: 'Exploring Together', media: '/images/memory5.svg' },
        'first-celebration': { icon: '🎉', title: 'First Celebration', desc: 'Our first special celebration', date: 'Joy Shared', media: '/images/memory6.svg' },
        'first-cook': { icon: '👨‍🍳', title: 'First Cook Together', desc: 'Cooking our first meal', date: 'Domestic Bliss', media: '/images/memory7.svg' },
        'first-movie': { icon: '🎬', title: 'First Movie', desc: 'Watching our first movie together', date: 'Entertainment', media: '/images/memory8.svg' },
        'first-dance': { icon: '💃', title: 'First Dance', desc: 'Dancing together for the first time', date: 'Rhythm of Love', media: '/images/memory9.svg' },
        'first-gift': { icon: '🎁', title: 'First Gift', desc: 'Exchanging our first gifts', date: 'Gift of Love', media: '/images/memory10.svg' },
        'first-stargaze': { icon: '⭐', title: 'First Stargazing', desc: 'Looking at stars together', date: 'Cosmic Love', media: '/images/memory11.svg' },
        'first-sunrise': { icon: '🌅', title: 'First Sunrise', desc: 'Watching sunrise together', date: 'New Beginnings', media: '/images/memory12.svg' }
    };

    function showMemoryModal(memoryId) {
        const memory = memories[memoryId];
        if (!memory) return;

        const modalContent = `
            <h3>${memory.icon} ${memory.title}</h3>
            <p><strong>${memory.date}</strong></p>
            <p>${memory.desc}</p>
            <div class="memory-image">
                <img src="${memory.media}" alt="${memory.title}" style="max-width: 200px; border-radius: 10px;">
            </div>
        `;

        showModal(modalContent);
    }

    // Add click events to memory cards
    const memoryCards = document.querySelectorAll('.memory-card');
    memoryCards.forEach(card => {
        card.addEventListener('click', function() {
            const memoryId = this.dataset.memory;
            showMemoryModal(memoryId);
        });
    });
}

// Initialize all systems
document.addEventListener('DOMContentLoaded', function() {
    initializeMemories();
    initializeMessageCarousel();
    createConfetti();
});

// Additional functions that were in HTML files
function sendKiss() {
    createSparkles(event.clientX, event.clientY);
    
    const kiss = document.createElement('div');
    kiss.innerHTML = '💋';
    kiss.style.position = 'fixed';
    kiss.style.left = (event.clientX - 20) + 'px';
    kiss.style.top = (event.clientY - 20) + 'px';
    kiss.style.fontSize = '2rem';
    kiss.style.pointerEvents = 'none';
    kiss.style.zIndex = '1000';
    kiss.style.animation = 'float 2s ease-out forwards';
    document.body.appendChild(kiss);
    
    setTimeout(() => {
        kiss.remove();
    }, 2000);
}

function giveRose() {
    createSparkles(event.clientX, event.clientY);
    
    const rose = document.createElement('div');
    rose.innerHTML = '🌹';
    rose.style.position = 'fixed';
    rose.style.left = (event.clientX - 20) + 'px';
    rose.style.top = (event.clientY - 20) + 'px';
    rose.style.fontSize = '2rem';
    rose.style.pointerEvents = 'none';
    rose.style.zIndex = '1000';
    rose.style.animation = 'float 3s ease-out forwards';
    document.body.appendChild(rose);
    
    setTimeout(() => {
        rose.remove();
    }, 3000);
}

function celebrate() {
    // Create multiple sparkle bursts
    for (let i = 0; i < 5; i++) {
        setTimeout(() => {
            createSparkles(
                Math.random() * window.innerWidth,
                Math.random() * window.innerHeight
            );
        }, i * 200);
    }
    
    // Add confetti effect
    const confettiContainer = document.querySelector('.confetti');
    for (let i = 0; i < 20; i++) {
        const confetti = document.createElement('div');
        confetti.className = 'confetti-piece';
        confetti.style.left = Math.random() * 100 + '%';
        confetti.style.animationDelay = '0s';
        confetti.style.animationDuration = (Math.random() * 2 + 2) + 's';
        confetti.style.backgroundColor = `hsl(${Math.random() * 360}, 100%, 70%)`;
        confettiContainer.appendChild(confetti);
        
        setTimeout(() => {
            confetti.remove();
        }, 4000);
    }
}

function showPhotoModal(title, description, emoji) {
    const modal = document.createElement('div');
    modal.className = 'modal';
    modal.innerHTML = `
        <div class="modal-content">
            <button class="modal-close">&times;</button>
            <div style="text-align: center;">
                <div style="font-size: 5rem; margin-bottom: 1rem;">${emoji}</div>
                <h3>${title}</h3>
                <p style="font-size: 1.1rem; line-height: 1.6; margin: 1rem 0;">${description}</p>
                <div style="background: linear-gradient(45deg, var(--primary-pink), var(--secondary-pink)); padding: 2rem; border-radius: 15px; margin: 1rem 0;">
                            <p style="font-size: 1.2rem; color: #f0f0f0; margin-bottom: 1rem;">📸 Photo Placeholder</p>
        <p style="opacity: 0.9; color: #f0f0f0;">Add your actual photo here by replacing the emoji with an image tag</p>
        <p style="opacity: 0.8; font-size: 0.9rem; margin-top: 1rem; color: #f0f0f0;">💡 Tip: Replace this with &lt;img src="assets/images/gallery1.jpg" style="max-width: 100%; border-radius: 10px;"&gt;</p>
                </div>
                <button class="btn" style="margin-top: 1rem;" onclick="createSparkles(event.clientX, event.clientY)">Create Sparkles ✨</button>
            </div>
        </div>
    `;

    document.body.appendChild(modal);
    
    setTimeout(() => {
        modal.classList.add('show');
    }, 10);

    const closeBtn = modal.querySelector('.modal-close');
    closeBtn.addEventListener('click', () => {
        modal.classList.remove('show');
        setTimeout(() => {
            modal.remove();
        }, 300);
    });

    modal.addEventListener('click', (e) => {
        if (e.target === modal) {
            closeBtn.click();
        }
    });
}

function showVideoModal(title, description, emoji) {
    const modal = document.createElement('div');
    modal.className = 'modal';
    modal.innerHTML = `
        <div class="modal-content">
            <button class="modal-close">&times;</button>
            <div style="text-align: center;">
                <div style="font-size: 5rem; margin-bottom: 1rem;">${emoji}</div>
                <h3>${title}</h3>
                <p style="font-size: 1.1rem; line-height: 1.6; margin: 1rem 0;">${description}</p>
                <div style="background: linear-gradient(45deg, var(--primary-pink), var(--secondary-pink)); padding: 2rem; border-radius: 15px; margin: 1rem 0;">
                            <p style="font-size: 1.2rem; color: #f0f0f0; margin-bottom: 1rem;">🎥 Video Placeholder</p>
        <p style="opacity: 0.9; color: #f0f0f0;">Add your actual video here by replacing this with a video tag</p>
        <p style="opacity: 0.8; font-size: 0.9rem; margin-top: 1rem; color: #f0f0f0;">💡 Tip: Replace this with &lt;video controls style="max-width: 100%; border-radius: 10px;"&gt;&lt;source src="assets/images/birthday_video.mp4" type="video/mp4"&gt;&lt;/video&gt;</p>
                </div>
                <button class="btn" style="margin-top: 1rem;" onclick="createSparkles(event.clientX, event.clientY)">Create Sparkles ✨</button>
            </div>
        </div>
    `;

    document.body.appendChild(modal);
    
    setTimeout(() => {
        modal.classList.add('show');
    }, 10);

    const closeBtn = modal.querySelector('.modal-close');
    closeBtn.addEventListener('click', () => {
        modal.classList.remove('show');
        setTimeout(() => {
            modal.remove();
        }, 300);
    });

    modal.addEventListener('click', (e) => {
        if (e.target === modal) {
            closeBtn.click();
        }
    });
}

function showAllPhotos() {
    // Create a slideshow of all photos
    const photos = [
        { title: 'Our First Date', emoji: '💕', desc: 'The magical evening when everything began to feel special.' },
        { title: 'Coffee Together', emoji: '☕', desc: 'Hours of talking about everything and nothing.' },
        { title: 'Sunset Walk', emoji: '🌅', desc: 'Walking hand in hand as the sun set.' },
        { title: 'Movie Night', emoji: '🎬', desc: 'Cuddled up watching our favorite movies.' },
        { title: 'Cooking Together', emoji: '👨‍🍳', desc: 'Creating delicious meals together in the kitchen.' },
        { title: 'Dance Night', emoji: '💃', desc: 'Moving together to our favorite songs.' },
        { title: 'Stargazing', emoji: '⭐', desc: 'Looking up at the stars together.' },
        { title: 'Beach Day', emoji: '🏖️', desc: 'Walking along the beach together.' },
        { title: 'Birthday Celebration', emoji: '🎂', desc: 'Celebrating your special day with love.' },
        { title: 'Holiday Together', emoji: '✈️', desc: 'Exploring new places together.' },
        { title: 'Quiet Moments', emoji: '🤫', desc: 'Peaceful moments enjoying each other\'s company.' },
        { title: 'Future Dreams', emoji: '💭', desc: 'Planning our beautiful future together.' }
    ];

    let currentPhoto = 0;

    function showPhoto() {
        const photo = photos[currentPhoto];
        showPhotoModal(photo.title, photo.desc, photo.emoji);
    }

    // Show first photo
    showPhoto();

    // Auto-advance photos every 3 seconds
    const interval = setInterval(() => {
        currentPhoto = (currentPhoto + 1) % photos.length;
        showPhoto();
    }, 3000);

    // Stop auto-advance after 30 seconds
    setTimeout(() => {
        clearInterval(interval);
    }, 30000);
}

function startQuiz() {
    const quizContainer = document.querySelector('.quiz-container');
    const surpriseContent = document.querySelector('.surprise-content');
    
    // Hide other content
    document.querySelectorAll('.surprise-content > div').forEach(div => {
        if (!div.classList.contains('quiz-container')) {
            div.style.display = 'none';
        }
    });
    
    quizContainer.style.display = 'block';
    surpriseContent.style.display = 'block';
    
    // Initialize quiz
    initializeQuiz();
}

function showMessageCarousel() {
    const carousel = document.querySelector('.message-carousel');
    const surpriseContent = document.querySelector('.surprise-content');
    
    // Hide other content
    document.querySelectorAll('.surprise-content > div').forEach(div => {
        if (!div.classList.contains('message-carousel')) {
            div.style.display = 'none';
        }
    });
    
    carousel.style.display = 'block';
    surpriseContent.style.display = 'block';
    
    // Initialize carousel
    initializeMessageCarousel();
}

function showCountdown() {
    showModal(`
        <h3>⏰ Countdown to Your Special Day ⏰</h3>
        <div id="countdown" class="countdown"></div>
        <p>Every second brings us closer to celebrating you! 💖</p>
    `);
    initializeCountdown();
}

function showTimeline() {
    showModal(`
        <h3>📖 Our Love Story Timeline 📖</h3>
        <div style="text-align: left; max-height: 400px; overflow-y: auto;">
            <p><strong>💕 First Meeting:</strong> The day our eyes met and everything changed</p>
            <p><strong>📱 First Conversation:</strong> Hours of talking that felt like minutes</p>
            <p><strong>🍽️ First Date:</strong> A magical evening that felt like a dream</p>
            <p><strong>💋 First Kiss:</strong> A moment that made time stand still</p>
            <p><strong>✈️ First Trip:</strong> Adventures that brought us closer</p>
            <p><strong>🎉 First Celebration:</strong> Every celebration with you is special</p>
            <p><strong>👨‍🍳 First Cook Together:</strong> Creating memories in the kitchen</p>
            <p><strong>🎬 First Movie:</strong> Sharing stories and emotions</p>
            <p><strong>💃 First Dance:</strong> Moving together in perfect harmony</p>
            <p><strong>🎁 First Gift:</strong> Exchanging tokens of our love</p>
            <p><strong>⭐ First Stargazing:</strong> Looking at the stars and dreaming together</p>
            <p><strong>🌅 First Sunrise:</strong> Welcoming new days together</p>
        </div>
    `);
}

function showSpecialSurprises() {
    showModal(`
        <h3>✨ Special Surprises Throughout Your Day ✨</h3>
        <div style="text-align: left;">
            <p>🌅 <strong>Morning:</strong> A special breakfast surprise</p>
            <p>☕ <strong>Mid-morning:</strong> Your favorite coffee delivered</p>
            <p>🌹 <strong>Afternoon:</strong> A beautiful bouquet of roses</p>
            <p>🎂 <strong>Evening:</strong> A magical birthday dinner</p>
            <p>🎁 <strong>Night:</strong> Special gifts and surprises</p>
            <p>💫 <strong>Throughout:</strong> Random acts of love and kindness</p>
        </div>
    `);
}

function showInteractiveCake() {
    const cakeContainer = document.querySelector('.interactive-cake');
    const surpriseContent = document.querySelector('.surprise-content');
    
    // Hide other content
    document.querySelectorAll('.surprise-content > div').forEach(div => {
        if (!div.classList.contains('interactive-cake')) {
            div.style.display = 'none';
        }
    });
    
    cakeContainer.style.display = 'block';
    surpriseContent.style.display = 'block';
}

function showLoveMessages() {
    const messagesContainer = document.querySelector('.love-messages');
    const surpriseContent = document.querySelector('.surprise-content');
    
    // Hide other content
    document.querySelectorAll('.surprise-content > div').forEach(div => {
        if (!div.classList.contains('love-messages')) {
            div.style.display = 'none';
        }
    });
    
    messagesContainer.style.display = 'block';
    surpriseContent.style.display = 'block';
}

function startBirthdayQuiz() {
    startQuiz(); // Reuse the quiz functionality
}

// Add hover effects to cards
function addCardHoverEffects() {
    // Memory cards
    document.querySelectorAll('.memory-card').forEach(card => {
        card.addEventListener('mouseenter', function() {
            this.style.transform = 'translateY(-5px)';
        });
        
        card.addEventListener('mouseleave', function() {
            this.style.transform = 'translateY(0)';
        });
    });

    // Photo cards
    document.querySelectorAll('.glass-card').forEach(card => {
        card.addEventListener('mouseenter', function() {
            this.style.transform = 'translateY(-5px) scale(1.02)';
        });
        
        card.addEventListener('mouseleave', function() {
            this.style.transform = 'translateY(0) scale(1)';
        });
    });
}

// Initialize hover effects when DOM is loaded
document.addEventListener('DOMContentLoaded', function() {
    addCardHoverEffects();
});

// Add CSS for ripple effect
const style = document.createElement('style');
style.textContent = `
    @keyframes ripple {
        to {
            transform: scale(4);
            opacity: 0;
        }
    }
`;
document.head.appendChild(style);

// Enhanced Smooth Scroll Functionality
function initializeSmoothScroll() {
    // Smooth scroll for all internal links
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
        anchor.addEventListener('click', function (e) {
            e.preventDefault();
            const target = document.querySelector(this.getAttribute('href'));
            if (target) {
                target.scrollIntoView({
                    behavior: 'smooth',
                    block: 'start',
                    inline: 'nearest'
                });
            }
        });
    });

    // Smooth scroll for navigation links
    document.querySelectorAll('.header-nav a').forEach(link => {
        link.addEventListener('click', function(e) {
            // Add smooth transition effect
            this.style.transition = 'all 0.3s ease';
            this.style.transform = 'scale(0.95)';
            
            setTimeout(() => {
                this.style.transform = 'scale(1)';
            }, 150);
        });
    });

    // Enhanced scroll behavior for all elements
    document.addEventListener('scroll', function() {
        // Add smooth scroll effects to elements as they come into view
        const elements = document.querySelectorAll('.glass-card, .nav-card, .timeline-item');
        elements.forEach(element => {
            const elementTop = element.getBoundingClientRect().top;
            const elementVisible = 150;
            
            if (elementTop < window.innerHeight - elementVisible) {
                element.classList.add('smooth-fade-in');
            }
        });
    }, { passive: true });
}

// Scroll to Top Button Functionality
function initializeScrollToTop() {
    // Create scroll to top button
    const scrollToTopBtn = document.createElement('button');
    scrollToTopBtn.className = 'scroll-to-top';
    scrollToTopBtn.innerHTML = '↑';
    scrollToTopBtn.setAttribute('aria-label', 'Scroll to top');
    document.body.appendChild(scrollToTopBtn);

    // Show/hide scroll to top button based on scroll position
    window.addEventListener('scroll', function() {
        if (window.pageYOffset > 300) {
            scrollToTopBtn.classList.add('visible');
        } else {
            scrollToTopBtn.classList.remove('visible');
        }
    }, { passive: true });

    // Smooth scroll to top when button is clicked
    scrollToTopBtn.addEventListener('click', function() {
        window.scrollTo({
            top: 0,
            behavior: 'smooth'
        });
        
        // Add click animation
        this.style.transform = 'scale(0.9)';
        setTimeout(() => {
            this.style.transform = 'scale(1)';
        }, 150);
    });

    // Enhanced smooth scroll for all buttons
    document.querySelectorAll('.btn').forEach(btn => {
        btn.addEventListener('click', function(e) {
            // Add smooth click effect
            this.style.transition = 'all 0.2s ease';
            this.style.transform = 'scale(0.95)';
            
            setTimeout(() => {
                this.style.transform = 'scale(1)';
            }, 200);
        });
    });
} 