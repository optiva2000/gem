<html lang="ar" dir="rtl" id="html-root">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gem Travel Agencies - Explore Egypt</title>
    <style>
        :root {
            --primary-color: #0f172a;
            --accent-color: #0284c7;
            --danger-color: #dc2626;
            --bg-color: #f8fafc;
            --card-bg: #ffffff;
            --text-color: #334155;
        }
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--bg-color);
            color: var(--text-color);
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
            min-height: 100vh;
        }
        header {
            background-color: var(--primary-color);
            color: white;
            width: 100%;
            padding: 15px 20px;
            text-align: center;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
            display: flex;
            justify-content: space-between;
            align-items: center;
            box-sizing: border-box;
            border-bottom: 3px solid var(--danger-color);
        }
        .logo-area h1 {
            margin: 0;
            font-size: 18px;
            letter-spacing: 1px;
            text-align: left;
            color: #ffffff;
        }
        .logo-area p {
            margin: 2px 0 0;
            font-size: 11px;
            color: #cbd5e1;
            text-align: left;
        }
        .lang-selector select {
            background-color: #1e293b;
            color: white;
            border: 1px solid #475569;
            padding: 6px 10px;
            border-radius: 6px;
            font-size: 13px;
            cursor: pointer;
            outline: none;
        }
        .container {
            width: 100%;
            max-width: 600px;
            padding: 20px;
            box-sizing: border-box;
            flex: 1;
        }
        .section-title {
            font-size: 18px;
            font-weight: bold;
            margin-bottom: 15px;
            color: var(--primary-color);
            border-bottom: 2px solid #e2e8f0;
            padding-bottom: 5px;
        }
        .grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 15px;
            margin-bottom: 30px;
        }
        .main-menu-grid {
            display: flex;
            flex-direction: column;
            gap: 15px;
            margin-top: 20px;
        }
        .btn-card {
            background-color: var(--card-bg);
            border: 2px solid var(--accent-color);
            border-radius: 12px;
            padding: 20px 15px;
            text-align: center;
            font-size: 15px;
            font-weight: bold;
            color: var(--accent-color);
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 2px 4px rgba(0,0,0,0.05);
        }
        .btn-card:hover {
            background-color: var(--accent-color);
            color: white;
            transform: translateY(-2px);
            box-shadow: 0 4px 8px rgba(2, 132, 199, 0.3);
        }
        .main-btn {
            background-color: var(--card-bg);
            border: 2px solid var(--danger-color);
            border-radius: 12px;
            padding: 22px;
            text-align: center;
            font-size: 17px;
            font-weight: bold;
            color: var(--danger-color);
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 3px 6px rgba(0,0,0,0.08);
        }
        .main-btn:hover {
            background-color: var(--danger-color);
            color: white;
            transform: translateY(-2px);
            box-shadow: 0 5px 12px rgba(220, 38, 38, 0.3);
        }
        .info-card {
            background-color: white;
            border-radius: 12px;
            padding: 20px;
            box-shadow: 0 4px 10px rgba(0,0,0,0.05);
            margin-bottom: 20px;
            border-right: 5px solid var(--danger-color);
        }
        .info-card h3 {
            margin-top: 0;
            color: var(--primary-color);
            font-size: 19px;
        }
        .info-card p {
            line-height: 1.6;
            color: #475569;
            font-size: 15px;
        }
        .back-btn {
            background-color: #64748b;
            color: white;
            border: none;
            padding: 10px 20px;
            border-radius: 8px;
            cursor: pointer;
            margin-bottom: 20px;
            font-size: 14px;
        }
        .back-btn:hover {
            background-color: #475569;
        }
        .slideshow-container {
            position: relative;
            max-width: 100%;
            margin: auto;
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 4px 10px rgba(0,0,0,0.15);
            background: #000;
        }
        .mySlides {
            display: none;
            text-align: center;
        }
        .mySlides img {
            width: 100%;
            height: 250px;
            object-fit: cover;
        }
        .slide-caption {
            color: white;
            font-size: 15px;
            padding: 10px;
            background: rgba(0,0,0,0.6);
            position: absolute;
            bottom: 0;
            width: 100%;
            box-sizing: border-box;
        }
        .whatsapp-box {
            margin-top: 25px;
            text-align: center;
        }
        .whatsapp-btn {
            background-color: #25d366;
            color: white;
            border: none;
            padding: 15px 25px;
            border-radius: 50px;
            font-size: 15px;
            font-weight: bold;
            cursor: pointer;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
            text-decoration: none;
            box-shadow: 0 4px 10px rgba(37, 211, 102, 0.3);
            transition: background 0.3s;
            width: 100%;
            box-sizing: border-box;
        }
        .whatsapp-btn:hover {
            background-color: #20ba5a;
        }
        /* نافذة اختيار الأسماء المنبثقة */
        .modal {
            display: none;
            position: fixed;
            z-index: 1000;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0,0,0,0.5);
            justify-content: center;
            align-items: center;
        }
        .modal-content {
            background-color: white;
            padding: 20px;
            border-radius: 12px;
            width: 90%;
            max-width: 400px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0,0,0,0.3);
        }
        .modal-content h3 {
            margin-top: 0;
            color: var(--primary-color);
        }
        .wa-number-option {
            background-color: #f1f5f9;
            border: 2px solid #25d366;
            color: #1e293b;
            padding: 12px;
            margin: 10px 0;
            border-radius: 8px;
            font-weight: bold;
            display: block;
            text-decoration: none;
            transition: 0.2s;
        }
        .wa-number-option:hover {
            background-color: #25d366;
            color: white;
        }
        .close-modal {
            background-color: #64748b;
            color: white;
            border: none;
            padding: 8px 15px;
            border-radius: 6px;
            margin-top: 10px;
            cursor: pointer;
        }
        .hidden {
            display: none;
        }
    </style>
</head>
<body>

    <header>
        <div class="logo-area">
            <div class="logo-text">
                <h1>GEM TRAVEL</h1>
                <p id="header-subtitle">Travel Agencies - Explore Egypt</p>
            </div>
        </div>
        <div class="lang-selector">
            <select id="languageSelect" onchange="changeLanguage(this.value)">
                <option value="ar">العربية</option>
                <option value="en" selected>English</option>
                <option value="fr">Français</option>
                <option value="es">Español</option>
                <option value="zh">中文</option>
                <option value="ja">日本語</option>
            </select>
        </div>
    </header>

    <div class="container">
        <!-- Main Hub -->
        <div id="main-hub-screen">
            <div class="section-title" id="txt-main-title">Welcome to Gem Travel - Select Service</div>
            <div class="main-menu-grid">
                <div class="main-btn" onclick="openScreen('sightseeing-screen')" id="btn-sightseeing">🏛️ Sightseeing & Excursions</div>
                <div class="main-btn" onclick="openScreen('car-rental-screen')" id="btn-car-rental">🚗 Car Rental with Driver</div>
                <div class="main-btn" onclick="openScreen('airport-transfer-screen')" id="btn-airport-transfer">✈️ Airport Transfer</div>
            </div>

            <!-- زرار الواتساب في الواجهة الرئيسية -->
            <div class="whatsapp-box" style="margin-top: 30px;">
                <button onclick="openWhatsAppModal('Hello Gem Travel, I would like more information and general booking.')" class="whatsapp-btn">
                    💬 <span id="txt-home-wa">For More Information & Booking</span>
                </button>
            </div>
        </div>

        <!-- Sightseeing Destinations -->
        <div id="sightseeing-screen" class="hidden">
            <button class="back-btn" id="btn-back-main1" onclick="goMainHub()">← Main Menu</button>
            <div class="section-title" id="txt-choose-gov">Select Destination</div>
            <div class="grid">
                <div class="btn-card" onclick="openGov('Cairo')">Cairo (القاهرة)</div>
                <div class="btn-card" onclick="openGov('Alex')">Alexandria (الإسكندرية)</div>
                <div class="btn-card" onclick="openGov('Aswan')">Aswan (أسوان)</div>
                <div class="btn-card" onclick="openGov('Luxor')">Luxor (الأقصر)</div>
                <div class="btn-card" onclick="openGov('Sharm')">Sharm El Sheikh (شرم الشيخ)</div>
                <div class="btn-card" onclick="openGov('Hurghada')">Hurghada (الغردقة)</div>
            </div>
        </div>

        <!-- Car Rental -->
        <div id="car-rental-screen" class="hidden">
            <button class="back-btn" id="btn-back-main2" onclick="goMainHub()">← Main Menu</button>
            <div class="info-card">
                <h3 id="car-title">🚗 Car Rental with Professional Driver</h3>
                <p id="car-desc">Enjoy freedom and exploration at your own pace! We offer modern, fully air-conditioned cars with professional drivers for a stress-free journey.</p>
            </div>
            <div class="whatsapp-box">
                <button onclick="openWhatsAppModal('Hello Gem Travel, I want to inquire about Car Rental with Driver.')" class="whatsapp-btn">
                    💬 <span id="txt-car-wa">Book Car & Driver via WhatsApp</span>
                </button>
            </div>
        </div>

        <!-- Airport Transfer -->
        <div id="airport-transfer-screen" class="hidden">
            <button class="back-btn" id="btn-back-main3" onclick="goMainHub()">← Main Menu</button>
            <div class="info-card">
                <h3 id="airport-title">✈️ Seamless Airport Transfers</h3>
                <p id="airport-desc">Start your trip without any fatigue! We will be waiting for you the moment your plane lands to ensure a smooth arrival.</p>
            </div>
            <div class="whatsapp-box">
                <button onclick="openWhatsAppModal('Hello Gem Travel, I want to book an Airport Transfer.')" class="whatsapp-btn">
                    💬 <span id="txt-airport-wa">Book Airport Transfer via WhatsApp</span>
                </button>
            </div>
        </div>

        <!-- Governorate Content -->
        <div id="gov-screen" class="hidden">
            <button class="back-btn" id="btn-back-sightseeing" onclick="openScreen('sightseeing-screen')">← Back to Destinations</button>
            <div id="gov-content"></div>
        </div>

        <!-- Detail Screen & Slideshow -->
        <div id="detail-screen" class="hidden">
            <button class="back-btn" id="btn-back-gov" onclick="backToGov()">← Back to Places</button>
            <div class="section-title" id="place-title">Place Details</div>
            
            <div class="slideshow-container" id="slider-container"></div>

            <div class="whatsapp-box">
                <button id="detail-wa-btn" onclick="" class="whatsapp-btn">
                    💬 <span id="txt-detail-wa">Contact for Details & Reservation</span>
                </button>
            </div>
        </div>
    </div>

    <!-- نافذة اختيار الأسماء -->
    <div id="waModal" class="modal">
        <div class="modal-content">
            <h3 id="modal-title">اختر الشخص المناسب لمراسلته عبر الواتساب</h3>
            <div id="wa-options-container"></div>
            <button class="close-modal" onclick="closeWhatsAppModal()" id="modal-close-btn">إغلاق</button>
        </div>
    </div>

    <script>
        // الأرقام مرتبطة بالأسماء المباشرة (استبدل الأرقام والأسماء بما يناسبكم)
        const teamContacts = [
            { name: "باسل سعيد", number: "00201062519011" },
            { name: "أمجد حلمي", number: "201284234111" }, 
        ];

        let currentModalText = "";

        function openWhatsAppModal(text) {
            currentModalText = text;
            const container = document.getElementById('wa-options-container');
            container.innerHTML = "";

            teamContacts.forEach(item => {
                let encodedText = encodeURIComponent(currentModalText);
                let link = `https://wa.me/${item.number}?text=${encodedText}`;
                
                let btn = document.createElement('a');
                btn.href = link;
                btn.target = "_blank";
                btn.className = "wa-number-option";
                btn.innerHTML = `🟢 ${item.name} (${item.number})`;
                btn.onclick = () => closeWhatsAppModal();
                container.appendChild(btn);
            });

            document.getElementById('waModal').style.display = 'flex';
        }

        function closeWhatsAppModal() {
            document.getElementById('waModal').style.display = 'none';
        }

        const translations = {
            ar: {
                subtitle: "اكتشف مصر",
                mainTitle: "مرحباً بك في Gem Travel - اختر الخدمة المطلوبة",
                sightseeing: "🏛️ الجولات السياحية والرحلات",
                carRental: "🚗 تأجير سيارات مع سائق",
                airportTransfer: "✈️ انتقالات المطار",
                homeWa: "لمزيد من المعلومات والحجز العام",
                carWa: "احجز سيارة مع سائق عبر الواتساب",
                airportWa: "احجز انتقالات المطار عبر الواتساب",
                detailWa: "احجز واستعلم عبر الواتساب",
                modalTitle: "اختر الشخص المناسب لمراسلته عبر الواتساب",
                closeBtn: "إغلاق",
                backMain: "← القائمة الرئيسية",
                backDest: "← العودة للوجهات",
                backPlaces: "← رجوع للأماكن",
                chooseGov: "اختر الوجهة السياحية",
                placeDetails: "تفاصيل المكان",
                carTitle: "🚗 تأجير سيارات مع سائق محترف",
                carDesc: "استمتع براحة الحرية والاستكشاف على طريقتك الخاصة! نوفر لك سيارات حديثة ومكيفة بالكامل مع نخبة من السائقين المحترفين.",
                airportTitle: "✈️ انتقالات المطار بكل سهولة وأمان",
                airportDesc: "ابدأ رحلتك بلا إرهاق! نحن في انتظارك لحظة هبوط طائرتك لضمان وصولك بكل أمان وراحة.",
                cairo: "القاهرة",
                alex: "الإسكندرية",
                aswan: "أسوان",
                luxor: "الأقصر",
                sharm: "شرم الشيخ",
                hurghada: "الغردقة"
            },
            en: {
                subtitle: "Travel Agencies - Explore Egypt",
                mainTitle: "Welcome to Gem Travel - Select Service",
                sightseeing: "🏛️ Sightseeing & Excursions",
                carRental: "🚗 Car Rental with Driver",
                airportTransfer: "✈️ Airport Transfers",
                homeWa: "For More Information & Booking",
                carWa: "Book Car & Driver via WhatsApp",
                airportWa: "Book Airport Transfer via WhatsApp",
                detailWa: "Contact for Details & Reservation",
                modalTitle: "Select Team Member to Contact via WhatsApp",
                closeBtn: "Close",
                backMain: "← Main Menu",
                backDest: "← Back to Destinations",
                backPlaces: "← Back to Places",
                chooseGov: "Select Destination",
                placeDetails: "Place Details",
                carTitle: "🚗 Car Rental with Professional Driver",
                carDesc: "Enjoy freedom and exploration at your own pace! We offer modern, fully air-conditioned cars with professional
