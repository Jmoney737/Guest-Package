<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Welcome to Our Home</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Bodoni+Moda:wght@400;600&display=swap');
        @import url('https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css');

        * { margin: 0; padding: 0; box-sizing: border-box; }
        body { font-family: 'Open Sans', sans-serif; line-height: 1.6; color: #333; background-color: #FAF9F6; padding: 20px; }
        header { text-align: center; margin-bottom: 30px; }
        header h1 {
            font-family: 'Bodoni Moda', serif;
            font-size: 9rem;
            color: #A88C7D;
        }
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
            font-family: 'Bodoni Moda', serif;
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
        ol, ul { text-align: left; }
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

    <!-- Appliances & Devices -->
    <div class="section">
        <h2>
            <i class="fas fa-tv"></i> Appliances & Devices
            <button class="toggle-btn" onclick="toggleSection(this)">
                <i class="fas fa-chevron-down"></i>
            </button>
        </h2>
        <div class="section-content">
            <ul>
                <li>
                    <strong>Thermostat:</strong> Don’t Touch.
                    <img src="path/to/thermostat-image.jpg" alt="Thermostat" />
                </li>
                <li>
                    <strong>Smart TV:</strong> YouTube TV, Hulu, Netflix, Disney, Prime Video.
                    <img src="path/to/smart-tv-image.jpg" alt="Smart TV" />
                </li>
                <li>
                    <strong>Washer/Dryer:</strong> Use the AI Opti Wash & Dry Setting. Detergent is automatically dispensed. Clean filter before use.
                    <img src="path/to/washer-dryer-image.jpg" alt="Washer and Dryer" />
                    <a href="#lint-filter-cleaning" style="margin-left: 5px;">See Lint Filter Cleaning Instructions</a>
                </li>
            </ul>
        </div>
    </div>

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
                <p>
                    <strong>Note:</strong> Capsules are to the left in the jar. The automatic motor raises and lowers the machine's head when the lever is pushed up or down.
                </p>
                <li>Fill the water tank with fresh drinking water.</li>
                <img src="path/to/nespresso-water-tank.jpg" alt="Filling water tank" />
                <li>Turn on the machine by pressing the button.</li>
                <img src="path/to/nespresso-power-button.jpg" alt="Power button" />
                <li>GREEN lights will blink while the machine is heating up.</li>
                <img src="path/to/nespresso-heating.jpg" alt="Heating indicator" />
                <li>Steady GREEN light indicates the machine is ready.</li>
                <img src="path/to/nespresso-ready.jpg" alt="Ready light" />
                <li>Place a cup under the coffee outlet.</li>
                <img src="path/to/nespresso-place-cup.jpg" alt="Placing cup" />
            </ol>
        </div>
    </div>

    <div class="divider"></div>

    <!-- Lint Filter Cleaning Instructions -->
    <div class="section" id="lint-filter-cleaning">
        <h2>
            <i class="fas fa-filter"></i> Lint Filter Cleaning Instructions
            <button class="toggle-btn" onclick="toggleSection(this)">
                <i class="fas fa-chevron-down"></i>
            </button>
        </h2>
        <div class="section-content">
            <ol>
                <li>Open the lint filter cover and pull out the lint filter.</li>
                <img src="path/to/lint-filter-cover.jpg" alt="Opening lint filter cover" />
                <li>Avoid removing the rubber seal on the filter.</li>
                <img src="path/to/lint-filter-seal.jpg" alt="Rubber seal on lint filter" />
                <li>Separate the outer and inner filters.</li>
                <img src="path/to/separating-filters.jpg" alt="Separating lint filters" />
                <li>Remove lint from both filters.</li>
                <img src="path/to/cleaning-filters.jpg" alt="Cleaning lint filters" />
            </ol>
        </div>
    </div>

    <div class="divider"></div>

    <script>
        function toggleSection(button) {
            const sectionContent = button.parentElement.nextElementSibling;

            if (sectionContent.classList.contains('active')) {
                sectionContent.style.maxHeight = null;
                sectionContent.style.padding = "0";
                sectionContent.classList.remove('active');
            } else {
                sectionContent.style.maxHeight = sectionContent.scrollHeight + "px";
                sectionContent.style.padding = "10px 0";
                sectionContent.classList.add('active');
            }

            const icon = button.querySelector('i');
            if (sectionContent.classList.contains('active')) {
                icon.classList.replace('fa-chevron-down', 'fa-chevron-up');
            } else {
                icon.classList.replace('fa-chevron-up', 'fa-chevron-down');
            }
        }
    </script>
</body>
</html>
