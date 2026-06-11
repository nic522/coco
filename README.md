
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Free Student Drama Stream</title>
    <style>
        /* Mobile-First Dark Theme */
        body { background: #0f172a; color: #f8fafc; font-family: 'Segoe UI', system-ui, sans-serif; margin: 0; padding: 10px; }
        header { text-align: center; padding: 20px 0; border-bottom: 2px solid #1e293b; margin-bottom: 20px; }
        h1 { color: #38bdf8; margin: 0; font-size: 24px; }
        
        /* The Video Screen Section */
        .player-section { max-width: 100%; margin-bottom: 20px; display: none; background: #1e293b; padding: 10px; border-radius: 12px; }
        .video-wrapper { position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; border-radius: 8px; }
        .video-wrapper iframe { position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: none; }
        #playingTitle { margin: 10px 0 0 0; color: #38bdf8; font-size: 16px; }

        /* KissKH-Style Dynamic Grid */
        .grid { display: grid; grid-template-columns: repeat(2, 1fr); gap: 12px; }
        @media(min-width: 600px) { .grid { grid-template-columns: repeat(4, 1fr); } }
        
        /* Drama Cards */
        .card { background: #1e293b; border-radius: 10px; overflow: hidden; box-shadow: 0 4px 6px -1px rgba(0,0,0,0.5); cursor: pointer; transition: 0.2s; }
        .card img { width: 100%; height: 220px; object-fit: cover; display: block; }
        .card-info { padding: 8px; text-align: center; }
        .card-title { font-size: 14px; font-weight: bold; margin: 0 0 4px 0; white-space: nowrap; overflow: hidden; text-overflow: ellipsis; }
        .card-ep { font-size: 11px; color: #94a3b8; margin: 0; }
        
        /* Free Community Upload Button */
        .upload-btn { display: block; text-align: center; background: #2563eb; color: white; padding: 12px; border-radius: 8px; text-decoration: none; font-weight: bold; margin-top: 25px; font-size: 14px; }
    </style>
</head>
<body>

    <header>
        <h1>🍿 Student Drama Club</h1>
    </header>

    <!-- 1. THE VIDEO PLAYER SCREEN -->
    <div id="videoScreen" class="player-section">
        <div class="video-wrapper">
            <iframe id="videoPlayer" src="" allowfullscreen></iframe>
        </div>
        <p id="playingTitle">Loading...</p>
    </div>

    <!-- 2. THE KISSKH-STYLE VIDEO GRID -->
    <div class="grid">
        
        <!-- Drama Card 1 (Dailymotion Example) -->
        <div class="card" onclick="playVideo('https://dailymotion.com', 'My Secret Romance - Episode 1')">
            <img src="https://unsplash.com" alt="Drama Poster">
            <div class="card-info">
                <p class="card-title">My Secret Romance</p>
                <p class="card-ep">Episode 1 (Eng Sub)</p>
            </div>
        </div>

        <!-- Drama Card 2 (Add more cards by duplicating this block) -->
        <div class="card" onclick="playVideo('https://dailymotion.com', 'My Secret Romance - Episode 2')">
            <img src="https://unsplash.com" alt="Drama Poster">
            <div class="card-info">
                <p class="card-title">My Secret Romance</p>
                <p class="card-ep">Episode 2 (Eng Sub)</p>
            </div>
        </div>

    </div>

    <!-- 3. THE DAILYMOTION COMMUNITY UPLOAD BUTTON -->
    <a href="YOUR_GOOGLE_FORM_LINK_HERE" target="_blank" class="upload-btn">➕ Upload / Submit a Dailymotion Video Link</a>

    <script>
        // JavaScript logic to run the video player instantly
        function playVideo(embedUrl, title) {
            const screen = document.getElementById('videoScreen');
            const player = document.getElementById('videoPlayer');
            const titleText = document.getElementById('playingTitle');
            
            player.src = embedUrl;
            titleText.innerText = "🎬 Now Playing: " + title;
            screen.style.display = 'block';
            
            // Auto-scroll screen to top smoothly so the user sees the player instantly
            window.scrollTo({top: 0, behavior: 'smooth'});
        }
    </script>
</body>
</html>
