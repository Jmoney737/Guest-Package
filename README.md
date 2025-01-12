<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Welcome to Our Home</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Great+Vibes&family=Open+Sans:wght@400;600&display=swap');
        @import url('https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css');

        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { font-family: 'Open Sans', sans-serif; line-height: 1.6; color: #333; background-color: #FAF9F6; padding: 20px; }
        header { text-align: center; margin-bottom: 30px; }
        header h1 { font-family: 'Great Vibes', cursive; font-size: 3rem; color: #A88C7D; }
        header p { font-size: 1.2rem; color: #555; }
        .smart-home-link {
            display: inline-block;
            margin-top: 10px;
            padding: 10px 20px;
            background-color: #A88C7D;
            color: #FFF;
            font-weight: bold;
            text-decoration: none;
            border-radius: 5px;
            transition: background-color 0.3s ease;
        }
        .smart-home-link:hover { background-color: #946b5d; }
        .section { 
            background: linear-gradient(135deg, #FFF, #F7F2EE); 
            border-radius: 10px; 
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1); 
            margin-bottom: 20px; 
            padding: 20px; 
            max-width: 800px; 
            margin-left: auto; 
            margin-right: auto; 
        }
        .section h2 {
            font-family: 'Great Vibes', cursive;
            font-size: 2rem;
            color: #A88C7D;
            margin-bottom: 10px;
            text-align: center;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .section h2 i {
            margin-right: 10px;
            transition: transform 0.3s ease, color 0.3s ease;
        }
        .section h2:hover i {
            transform: scale(1.2);
            color: #946b5d;
        }
        .section-content {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.5s ease-out, padding 0.3s ease-out;
        }
        .section-content.active {
            max-height: 1000px;
            padding: 10px 0;
            background-color: #FFF3E6;
            border-radius: 5px;
            box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
        }
        ol, ul { text-align: left; margin-left: 20px; }
        img { max-width: 100%; border-radius: 5px; margin: 10px 0; }
        .toggle-btn {
            background: none;
            border: none;
            font-size: 1.5rem;
            cursor: pointer;
            color: #A88C7D;
            transition: transform 0.2s ease, color 0.3s ease;
        }
        .toggle-btn:active {
            transform: scale(0.95);
        }
        .toggle-btn:hover { color: #946b5d; }
        .divider {
            border-top: 2px solid #DDD;
            margin: 20px 0;
        }
    </style>
</head>
<body>
    <header>
        <h1>Welcome to Our Home</h1>
        <p>We’re so glad to have you here. Click on the icons for quick navigation.</p>
        <a href="https://jmoney737.github.io/Routine-Activator/" target="_blank" class="smart-home-link">Smart Home Control</a>
    </header>

    <div class="divider"></div>

    <!-- Nespresso Coffee Preparation Guide -->
    <div class="section">
        <h2>
            <i class="fas fa-coffee"></i> Nespresso Coffee Preparation Guide
            <button class="toggle-btn" onclick="toggleSection(this)">
                <i class="fas fa-chevron-down"></i>
            </button>
        </h2>
        <div class="section-content">
            <ol>
                <li>Fill the water tank with fresh drinking water.</li>
                <img src="https://github.com/user-attachments/assets/b2e02e7d-1c8a-4cee-84ad-52ac8514c588" alt="Filling the water tank">
                <li>Turn on the machine by pressing the button.</li>
                <img src="https://github.com/user-attachments/assets/797a5710-f9b1-4916-a2c6-cb403407c967" alt="Power Button">
                <li>Wait for the GREEN light to stop blinking (heating up).</li>
                <li>Place a cup under the coffee outlet and brew!</li>
                <img src="https://github.com/user-attachments/assets/4472e73a-19de-4921-9d1b-0a32f4deea4a" alt="Ready to Brew">
            </ol>
        </div>
    </div>

    <div class="divider"></div>

    <!-- Lint Filter Cleaning Instructions -->
    <div class="section">
        <h2>
            <i class="fas fa-filter"></i> Lint Filter Cleaning Instructions
            <button class="toggle-btn" onclick="toggleSection(this)">
                <i class="fas fa-chevron-down"></i>
            </button>
        </h2>
        <div class="section-content">
            <ol>
                <li>Remove the lint filter from the machine.</li>
                <img src="https://github.com/user-attachments/assets/c313bb1f-ce18-4d0c-ac06-67d153dbc521" alt="Lint Filter Removal">
                <li>Clean out any lint and reassemble.</li>
                <img src="https://github.com/user-attachments/assets/3a84ba9e-9ddf-4e19-8328-884cf31cc6ca" alt="Clean Lint Filter">
            </ol>
        </div>
    </div>

    <div class="divider"></div>

    <!-- Organized Office Storage -->
    <div class="section">
        <h2>
            <i class="fas fa-folder"></i> Organized Office Storage
            <button class="toggle-btn" onclick="toggleSection(this)">
                <i class="fas fa-chevron-down"></i>
            </button>
        </h2>
        <div class="section-content">
            <h3>Left Office Drawer</h3>
            <ul>
                <li>Writing Supplies, Office Tools, Batteries</li>
            </ul>
            <img src="path/to/left-office-drawer.jpg" alt="Left Drawer">
        </div>
    </div>

    <script>
        function toggleSection(button) {
            const sectionContent = button.parentElement.nextElementSibling;

            if (sectionContent.classList.contains('active')) {
                sectionContent.style.maxHeight = null;
                sectionContent.classList.remove('active');
            } else {
                sectionContent.style.maxHeight = sectionContent.scrollHeight + "px";
                sectionContent.classList.add('active');
            }
        }
    </script>
</body>
</html>
