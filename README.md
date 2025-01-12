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
        .weather-widget {
            display: flex;
            justify-content: space-between;
            align-items: center;
            background: linear-gradient(135deg, #FFF, #F7F2EE);
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            padding: 15px;
            margin-bottom: 20px;
        }
        .weather-widget i {
            font-size: 3rem;
            color: #A88C7D;
        }
        .weather-widget div {
            font-size: 1.2rem;
            color: #555;
        }
        .weather-widget div strong {
            color: #A88C7D;
        }
        .search-bar {
            display: flex;
            justify-content: center;
            margin-bottom: 20px;
        }
        .search-bar input {
            padding: 10px;
            font-size: 1rem;
            border: 1px solid #ccc;
            border-radius: 5px 0 0 5px;
            width: 70%;
        }
        .search-bar button {
            padding: 10px 20px;
            font-size: 1rem;
            background-color: #A88C7D;
            color: #FFF;
            border: none;
            border-radius: 0 5px 5px 0;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }
        .search-bar button:hover { background-color: #946b5d; }
        .divider {
            height: 1px;
            background-color: #ccc;
            margin: 20px 0;
        }
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
        .section-content {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.5s ease-out, padding 0.3s ease-out;
        }
        .section-content.active {
            max-height: 1000px;
            padding: 10px 0;
        }
    </style>
</head>
<body>
    <header>
        <h1>Welcome to Our Home</h1>
        <p>We’re so glad to have you here. Click on the icons for quick navigation.</p>
        <a href="https://jmoney737.github.io/Routine-Activator/" target="_blank" class="smart-home-link">Smart Home Control</a>
    </header>

    <!-- Weather Widget -->
    <div class="weather-widget" id="weather-widget">
        <i class="fas fa-cloud-sun"></i>
        <div id="weather-data">
            <p>Loading weather data...</p>
        </div>
    </div>

    <!-- Search Bar -->
    <div class="search-bar">
        <input type="text" id="search-input" placeholder="Search for a section..." aria-label="Search for a section">
        <button onclick="searchSections()">Search</button>
    </div>

    <div class="divider"></div>

    <!-- Example Section -->
    <div class="section" id="appliances">
        <h2>
            <i class="fas fa-tv"></i> Appliances & Devices
            <button class="toggle-btn" onclick="toggleSection(this, 'appliances')" aria-label="Toggle section">
                <i class="fas fa-chevron-down"></i>
            </button>
        </h2>
        <div class="section-content">
            <ul>
                <li><strong>Thermostat:</strong> Don’t Touch.</li>
                <li><strong>Smart TV:</strong> YouTube TV, Hulu, Netflix, Disney, Prime Video.</li>
                <li>
                    <strong>Washer/Dryer:</strong> Use the AI Opti Wash & Dry Setting. Detergent is automatically dispensed. Clean filter before use.
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
            <button class="toggle-btn" onclick="toggleSection(this)" aria-label="Toggle section">
                <i class="fas fa-chevron-down"></i>
            </button>
        </h2>
        <div class="section-content">
            <ol>
                <p><strong>Note:</strong> Capsules are to the left in the jar. The automatic motor raises and lowers the machine's head when the lever is pushed up or down.</p>
                <li>Fill the water tank with fresh drinking water.</li>
                <li>Turn on the machine by pressing the button.</li>
                <li>GREEN lights will blink while the machine is heating up.</li>
                <li>Steady GREEN light indicates the machine is ready.</li>
                <li>Place a cup under the coffee outlet.</li>
                <li>Open the machine head by pushing the lever up.</li>
                <li>Insert a capsule, dome side down.</li>
                <li>Close the lid by pressing the lever down, then press the button to start brewing.</li>
            </ol>
        </div>
    </div>

    <div class="divider"></div>

    <!-- Lint Filter Cleaning Instructions -->
    <div class="section" id="lint-filter-cleaning">
        <h2>
            <i class="fas fa-filter"></i> Lint Filter Cleaning Instructions
            <button class="toggle-btn" onclick="toggleSection(this)" aria-label="Toggle section">
                <i class="fas fa-chevron-down"></i>
            </button>
        </h2>
        <div class="section-content">
            <ol>
                <li>Open the lint filter cover and pull out the lint filter.</li>
                <li>Avoid removing the rubber seal on the filter.</li>
                <li>Separate the outer and inner filters.</li>
                <li>Remove lint from both filters.</li>
                <li>Reassemble the filters and insert them back in place.</li>
            </ol>
        </div>
    </div>

    <div class="divider"></div>

    <!-- Guide to Local Bars and Restaurants -->
    <div class="section">
        <h2>
            <i class="fas fa-utensils"></i> Guide to Local Bars and Restaurants
            <button class="toggle-btn" onclick="toggleSection(this)" aria-label="Toggle section">
                <i class="fas fa-chevron-down"></i>
            </button>
        </h2>
        <div class="section-content">
            <ul>
                <li>
                    <strong>GreenHouse Restaurant and Bar</strong><br>
                    Enjoy New American cuisine and an award-winning bar. 
                    <a href="https://greenhouserestaurantdenton.com/" target="_blank">Visit Website</a>
                </li>
                <li>
                    <strong>Rooster's Roadhouse</strong><br>
                    Casual BBQ and burgers in a relaxed atmosphere. 
                    <a href="https://roosters-roadhouse.com/" target="_blank">Visit Website</a>
                </li>
                <li>
                    <strong>Barley & Board</strong><br>
                    A gastropub with craft beers and elevated comfort food. 
                    <a href="https://www.barleyandboard.com/" target="_blank">Visit Website</a>
                </li>
            </ul>
        </div>
    </div>

    <div class="divider"></div>

    <!-- Local Attractions -->
    <div class="section">
        <h2>
            <i class="fas fa-map-marker-alt"></i> Local Attractions
            <button class="toggle-btn" onclick="toggleSection(this)" aria-label="Toggle section">
                <i class="fas fa-chevron-down"></i>
            </button>
        </h2>
        <div class="section-content">
            <ul>
                <li>
                    <strong>Denton Courthouse-on-the-Square Museum</strong><br>
                    Learn about local history in this iconic courthouse. 
                    <a href="https://dentoncounty.gov/Departments/Courthouse-on-the-Square" target="_blank">Visit Website</a>
                </li>
                <li>
                    <strong>Ray Roberts Lake State Park</strong><br>
                    A haven for nature enthusiasts with hiking, biking, and fishing. 
                    <a href="https://tpwd.texas.gov/state-parks/ray-roberts-lake" target="_blank">Visit Website</a>
                </li>
                <li>
                    <strong>Arts & Jazz Festival</strong><br>
                    An annual festival featuring live music, art, and local food. 
                    <a href="https://dentonjazzfest.com/" target="_blank">Visit Website</a>
                </li>
            </ul>
        </div>
    </div>

    <div class="divider"></div>

    <!-- Combined Section for Drawers and Cabinets -->
    <div class="section">
        <h2>
            <i class="fas fa-drawer"></i> Office Storage
        </h2>
        <div class="drawer-buttons">
            <button class="drawer-button" onclick="toggleDrawer('left-drawer')">Left Office Drawer</button>
            <button class="drawer-button" onclick="toggleDrawer('right-drawer')">Right Office Drawer</button>
            <button class="drawer-button" onclick="toggleDrawer('left-cabinet')">Left Office Cabinet</button>
            <button class="drawer-button" onclick="toggleDrawer('right-cabinet')">Right Office Cabinet</button>
        </div>
        <div id="left-drawer" class="section-content">
            <h3>Left Office Drawer:</h3>
            <ul>
                <li>Sharpie markers (various colors)</li>
                <li>Ballpoint pens (blue and black)</li>
                <li>Highlighters (multiple colors)</li>
                <li>Stapler</li>
                <li>Small plastic containers for organization</li>
            </ul>
        </div>
        <div id="right-drawer" class="section-content">
            <h3>Right Office Drawer:</h3>
            <ul>
                <li>USB, USB-C, and Lightning cables</li>
                <li>HDMI or auxiliary cables</li>
                <li>White power adapters/plugs</li>
                <li>Markers (e.g., Sharpie)</li>
                <li>JBL portable speaker</li>
            </ul>
        </div>
        <div id="left-cabinet" class="section-content">
            <h3>Left Office Cabinet:</h3>
            <ul>
                <li>Woven basket (contains small items)</li>
                <li>Aerosol can (compressed air or cleaner)</li>
                <li>Stacked black trays or storage cases</li>
                <li>Electronics (e.g., microprocessor tuner/amplifier)</li>
            </ul>
        </div>
        <div id="right-cabinet" class="section-content">
            <h3>Right Office Cabinet:</h3>
            <ul>
                <li>TP-Link Deco Wi-Fi 7 BE10000 (mesh system boxes)</li>
                <li>Circular Deco devices (mesh system)</li>
                <li>Projector or similar device (silver-gray with vents and cables)</li>
                <li>Stacked board games: Monopoly Builder, Out of Line, puzzles</li>
            </ul>
        </div>
    </div>

    <script>
        function toggleDrawer(drawerId) {
            const drawer = document.getElementById(drawerId);
            const isActive = drawer.classList.contains('active');

            document.querySelectorAll('.section-content').forEach(content => {
                content.classList.remove('active');
            });

            if (!isActive) {
                drawer.classList.add('active');
            }
        }

        function searchSections() {
            const query = document.getElementById('search-input').value.toLowerCase();
            document.querySelectorAll('.section').forEach(section => {
                const text = section.textContent.toLowerCase();
                if (text.includes(query)) {
                    section.style.display = '';
                } else {
                    section.style.display = 'none';
                }
            });
        }

        // Fetch weather data on page load
        async function fetchWeather() {
            const apiKey = '7841816e864c04d9b862cb645522ca43';
            const city = 'Denton';
            const url = `https://api.openweathermap.org/data/2.5/weather?q=${city}&units=imperial&appid=${apiKey}`;
            const weatherDataDiv = document.getElementById('weather-data');

            try {
                const response = await fetch(url);
                if (!response.ok) throw new Error('Weather data not found');
                const data = await response.json();

                weatherDataDiv.innerHTML = `
                    <p><strong>City:</strong> ${data.name}</p>
                    <p><strong>Temperature:</strong> ${data.main.temp} &deg;F</p>
                    <p><strong>Weather:</strong> ${data.weather[0].description}</p>
                    <p><strong>Humidity:</strong> ${data.main.humidity}%</p>
                    <p><strong>Wind Speed:</strong> ${data.wind.speed} mph</p>
                `;
            } catch (error) {
                weatherDataDiv.innerHTML = `<p>Error fetching weather data: ${error.message}</p>`;
            }
        }

        window.onload = () => {
            fetchWeather();
        };
    </script>
</body>
</html>
