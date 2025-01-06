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
        body {
            font-family: 'Open Sans', sans-serif;
            line-height: 1.6;
            color: #2c3e50;
            background-color: #e8f5e9;
            background-image: url('https://www.transparenttextures.com/patterns/green-dust.png');
            padding: 20px;
            background-size: cover;
        }
        header {
            text-align: center;
            margin-bottom: 30px;
        }
        header h1 {
            font-family: 'Great Vibes', cursive;
            font-size: 3.5rem;
            color: #2e7d32;
        }
        header p {
            font-size: 1.3rem;
            color: #4caf50;
        }
        .smart-home-link {
            display: inline-block;
            margin-top: 10px;
            padding: 10px 20px;
            background-color: #388e3c;
            color: #FFF;
            font-weight: bold;
            text-decoration: none;
            border-radius: 5px;
            transition: background-color 0.3s ease, transform 0.2s ease;
        }
        .smart-home-link:hover {
            background-color: #2e7d32;
            transform: scale(1.05);
        }
        .search-bar {
            max-width: 800px;
            margin: 20px auto;
            display: flex;
            justify-content: center;
            padding: 10px;
            background-color: #f1f8e9;
            border: 1px solid #c8e6c9;
            border-radius: 10px;
            box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
        }
        .search-bar input {
            width: 100%;
            padding: 12px;
            border: 1px solid #a5d6a7;
            border-radius: 5px 0 0 5px;
            outline: none;
        }
        .search-bar button {
            padding: 10px;
            background-color: #66bb6a;
            color: #FFF;
            border: none;
            border-radius: 0 5px 5px 0;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }
        .search-bar button:hover {
            background-color: #43a047;
        }
        .section {
            background: linear-gradient(135deg, #e8f5e9, #c8e6c9);
            border-radius: 15px;
            padding: 20px;
            margin-bottom: 20px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
        }
        .section h2 {
            font-family: 'Great Vibes', cursive;
            font-size: 2.2rem;
            color: #2e7d32;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        .section h2 i {
            margin-right: 10px;
        }
        .section-content {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.5s ease-out, padding 0.3s ease-out;
            background-color: #f1f8e9;
            border: 1px solid #c8e6c9;
            border-radius: 10px;
            padding: 15px;
            margin-top: 10px;
        }
        .section-content.active {
            max-height: 1000px; /* Arbitrarily large value */
            padding: 15px;
        }
        ol, ul {
            text-align: left;
        }
        img {
            max-width: 100%;
            border-radius: 10px;
            margin: 10px 0;
            border: 2px solid #a5d6a7;
            box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
        }
        .toggle-btn {
            background: none;
            border: none;
            font-size: 1.5rem;
            cursor: pointer;
            color: #2e7d32;
            transition: color 0.3s ease, transform 0.2s ease;
        }
        .toggle-btn:hover {
            color: #43a047;
            transform: rotate(180deg);
        }
        .divider {
            border-top: 2px solid #a5d6a7;
            margin: 20px 0;
        }
    </style>
</head>
<body>
    <header>
        <h1>Welcome to Out House</h1>
        <p>We’re so glad to have you here. Click on the icons for quick navigation.</p>
        <a href="https://jmoney737.github.io/Routine-Activator/" target="_blank" class="smart-home-link">Smart Home Control</a>
    </header>

    <div class="search-bar">
        <input type="text" id="search-input" placeholder="Search for a section...">
        <button onclick="searchSections()">Search</button>
    </div>

    <div class="section">
        <h2>
            <i class="fas fa-wifi"></i> Wi-Fi Information
            <button class="toggle-btn" onclick="toggleSection(this)">
                <i class="fas fa-chevron-down"></i>
            </button>
        </h2>
        <div class="section-content">
            <ul>
                <li><span>Network Name:</span> KRESS</li>
                <li><span>Password:</span> 9403950691</li>
            </ul>
        </div>
    </div>

    <div class="divider"></div>

    <div class="section">
        <h2>
            <i class="fas fa-tv"></i> Appliances & Devices
            <button class="toggle-btn" onclick="toggleSection(this)">
                <i class="fas fa-chevron-down"></i>
            </button>
        </h2>
        <div class="section-content">
            <ul>
                <li><span>Thermostat:</span> Don’t Touch.</li>
                <li><span>Smart TV:</span> YouTube TV, Hulu, Netflix, Disney, Prime Video.</li>
                <li>
                    <span>Washer/Dryer:</span> Use the AI Opti Wash & Dry Setting. Detergent is automatically dispensed. Clean filter before use.
                    <a href="#lint-filter-cleaning" style="margin-left: 5px;">See Lint Filter Cleaning Instructions</a>
                </li>
            </ul>
        </div>
    </div>

    <div class="divider"></div>

    <div class="section">
        <h2>
            <i class="fas fa-coffee"></i> Nespresso Coffee Preparation Guide
            <button class="toggle-btn" onclick="toggleSection(this)">
                <i class="fas fa-chevron-down"></i>
            </button>
        </h2>
        <div class="section-content">
            <ol>
                <p><strong>Note:</strong> Capsules are to the left in the jar. The automatic motor raises and lowers the machine's head when the lever is pushed up or down.</p>
                <li>Fill the water tank with fresh drinking water.</li>
                <img src="https://github.com/user-attachments/assets/86c020a1-06a2-4be8-96a1-266d78b99be7" alt="Fill Water Tank">
                <li>Turn on the machine by pressing the button.</li>
                <img src="https://github.com/user-attachments/assets/f7567056-b9fc-41e4-ac14-42b3ab688ac4" alt="Machine Button">
                <li>GREEN lights will blink while the machine is heating up.</li>
                <img src="https://github.com/user-attachments/assets/6f4657a4-f898-407a-a7f9-fbbedf789aaa" alt="Heating Indicator">
                <li>Steady GREEN light indicates the machine is ready.</li>
                <img src="https://github.com/user-attachments/assets/630486de-987a-46c1-aa82-49bba329979e" alt="Ready Light">
                <li>Place a cup under the coffee outlet.</li>
                <img src="https://github.com/user-attachments/assets/de2290fc-bbe8-4b6f-a813-af8dfccd1d18" alt="Place Cup">
                <li>Open the machine head by pushing the lever up.</li>
                <img src="https://github.com/user-attachments/assets/0ace38f7-f21d-4584-b473-c1c80103d78e" alt="Open Machine Head">
                <li>Insert a capsule, dome side down.</li>
                <img src="https://github.com/user-attachments/assets/4a29b12b-bcb2-4196-bdeb-0783ce745da5" alt="Insert Capsule">
                <li>Close the lid by pressing the lever down, then press the button to start brewing.</li>
            </ol>
        </div>
    </div>

    <div class="divider"></div>

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
                <img src="https://github.com/user-attachments/assets/35a86890-8764-4d1c-bd83-26feb01498a6" alt="Lint Filter Cover">
                <li>Avoid removing the rubber seal on the filter.</li>
                <img src="https://github.com/user-attachments/assets/3ae2f8d5-a2de-4f92-b5c9-357d0fa376c9" alt="Rubber Seal">
                <li>Separate the outer and inner filters.</li>
                <img src="https://github.com/user-attachments/assets/0ace38f7-f21d-4584-b473-c1c80103d78e" alt="Separate Filters">
                <li>Remove lint from both filters.</li>
                <li>Reassemble the filters and insert them back in place.</li>
            </ol>
        </div>
    </div>

    <script>
        function toggleSection(button) {
            const sectionContent = button.parentElement.nextElementSibling;
            sectionContent.classList.toggle('active');

            const icon = button.querySelector('i');
            if (sectionContent.classList.contains('active')) {
                icon.classList.replace('fa-chevron-down', 'fa-chevron-up');
            } else {
                icon.classList.replace('fa-chevron-up', 'fa-chevron-down');
            }
        }

        function searchSections() {
            const query = document.getElementById('search-input').value.toLowerCase();
            const sections = document.querySelectorAll('.section');

            sections.forEach(section => {
                const text = section.textContent.toLowerCase();
                if (text.includes(query)) {
                    section.style.display = 'block';
                } else {
                    section.style.display = 'none';
                }
            });
        }
    </script>
</body>
</html>
