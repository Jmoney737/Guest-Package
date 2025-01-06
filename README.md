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
        .search-bar {
            max-width: 800px;
            margin: 20px auto;
            display: flex;
            justify-content: center;
        }
        .search-bar input {
            width: 100%;
            padding: 10px;
            border: 2px solid #A88C7D;
            border-radius: 5px 0 0 5px;
        }
        .search-bar button {
            padding: 10px;
            background-color: #A88C7D;
            color: #FFF;
            border: none;
            border-radius: 0 5px 5px 0;
            cursor: pointer;
        }
        .search-bar button:hover { background-color: #946b5d; }
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
            max-height: 1000px; /* Arbitrarily large value */
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

    <!-- Additional Sections -->
    <!-- Omitted for brevity -->

    <script>
        function toggleSection(button) {
            const sectionContent = button.parentElement.nextElementSibling;

            if (sectionContent.style.maxHeight) {
                // Collapse section
                sectionContent.style.maxHeight = null;
                sectionContent.style.padding = "0";
                sectionContent.classList.remove('active');
            } else {
                // Expand section
                sectionContent.style.maxHeight = sectionContent.scrollHeight + "px";
                sectionContent.style.padding = "10px 0";
                sectionContent.classList.add('active');
            }

            const icon = button.querySelector('i');
            if (sectionContent.style.maxHeight) {
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
                    section.style.border = '2px solid #A88C7D'; // Highlight match
                } else {
                    section.style.display = 'none';
                }
            });
        }
    </script>
</body>
</html>
