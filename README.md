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
        .search-bar {
            max-width: 800px;
            margin: 0 auto 20px;
            display: flex;
            justify-content: center;
            gap: 10px;
        }
        #search-input {
            padding: 10px;
            border: 1px solid #CCC;
            border-radius: 5px;
            flex: 1;
        }
        button {
            background-color: #A88C7D;
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 5px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }
        button:hover {
            background-color: #946b5d;
        }
    </style>
</head>
<body>
    <header>
        <h1>Welcome to Our Home</h1>
        <p>We’re so glad to have you here. Click on the icons for quick navigation.</p>
        <a href="https://jmoney737.github.io/Routine-Activator/" target="_blank" class="smart-home-link">Smart Home Control</a>
    </header>

    <div class="search-bar">
        <input type="text" id="search-input" placeholder="Search for a section...">
        <button onclick="searchSections()">Search</button>
    </div>

    <div class="divider"></div>

    <!-- Wi-Fi Information -->
    <div class="section">
        <h2>
            <i class="fas fa-wifi"></i> Wi-Fi Information
            <button class="toggle-btn" onclick="toggleSection(this)">
                <i class="fas fa-chevron-down"></i>
            </button>
        </h2>
        <div class="section-content">
            <ul>
                <li><strong>Network Name:</strong> KRESS</li>
                <li><strong>Password:</strong> 9403950691</li>
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
                <p><strong>Note:</strong> Capsules are to the left in the jar. The automatic motor raises and lowers the machine's head when the lever is pushed up or down.</p>
                <li>Fill the water tank with fresh drinking water.</li>
                <img src="path/to/nespresso-fill-water-tank.jpg" alt="Fill Water Tank">
                <li>Turn on the machine by pressing the button.</li>
                <img src="path/to/nespresso-power-button.jpg" alt="Power Button">
                <li>GREEN lights will blink while the machine is heating up.</li>
                <img src="path/to/nespresso-heating-up.jpg" alt="Heating Up">
                <li>Steady GREEN light indicates the machine is ready.</li>
                <img src="path/to/nespresso-ready-light.jpg" alt="Ready Light">
                <li>Place a cup under the coffee outlet.</li>
                <img src="path/to/nespresso-place-cup.jpg" alt="Place Cup">
                <li>Open the machine head by pushing the lever up.</li>
                <img src="path/to/nespresso-open-head.jpg" alt="Open Machine Head">
                <li>Insert a capsule, dome side down.</li>
                <li>Close the lid by pressing the lever down, then press the button to start brewing.</li>
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
                <li>Open the lint filter cover and pull out the lint filter.</li>
                <img src="path/to/lint-filter-cover.jpg" alt="Lint Filter Cover">
                <li>Avoid removing the rubber seal on the filter.</li>
                <img src="path/to/lint-filter-seal.jpg" alt="Rubber Seal">
                <li>Separate the outer and inner filters.</li>
                <img src="path/to/separate-filters.jpg" alt="Separate Filters">
                <li>Remove lint from both filters.</li>
                <li>Reassemble the filters and insert them back in place.</li>
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
                sectionContent.classList.remove('active');
            } else {
                sectionContent.classList.add('active');
            }
        }
    </script>
</body>
</html>![IMG_4701](https://github.com/user-attachments/assets/160a3dee-5f8f-4d3f-9020-dbcac42ab020)
![IMG_4704](https://github.com/user-attachments/assets/ba7611c7-8c7c-4910-9c4f-641251812e09)
![IMG_4705](https://github.com/user-attachments/assets/efd384f8-e732-4376-9a04-c35c24e7d7ef)
![IMG_4706](https://github.com/user-attachments/assets/c313bb1f-ce18-4d0c-ac06-67d153dbc521)
![IMG_4707](https://github.com/user-attachments/assets/3a84ba9e-9ddf-4e19-8328-884cf31cc6ca)
