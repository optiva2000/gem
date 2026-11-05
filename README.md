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
            gap: 10px;
            text-decoration: none;
            box-shadow: 0 4px 10px rgba(37, 211, 102, 0.3);
            transition: background 0.3s;
        }
        .whatsapp-btn:hover {
            background-color: #20ba5a;
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

            <!-- زرار الواتساب الإضافي في الواجهة الرئيسية -->
            <div class="whatsapp-box" style="margin-top: 30px;">
                <a id="wa-home-link" href="#" target="_blank" class="whatsapp-btn" style="width: 100%; justify-content: center; box-sizing: border-box;">💬 <span id="txt-home-wa">For More Information & Booking</span></a>
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
                <a id="wa-car-link" href="#" target="_blank" class="whatsapp-btn">💬 Book Car & Driver via WhatsApp</a>
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
                <a id="wa-airport-link" href="#" target="_blank" class="whatsapp-btn">💬 Book Airport Transfer via WhatsApp</a>
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
                <a id="wa-link" href="#" target="_blank" class="whatsapp-btn">💬 Contact for Details & Reservation</a>
            </div>
        </div>
    </div>

    <script>
        const primaryWhatsApp = "201062519011";

        const translations = {
            ar: {
                subtitle: "اكتشف مصر",
                mainTitle: "مرحباً بك في Gem Travel - اختر الخدمة المطلوبة",
                sightseeing: "🏛️ الجولات السياحية والرحلات",
                carRental: "🚗 تأجير سيارات مع سائق",
                airportTransfer: "✈️ انتقالات المطار",
                homeWa: "لمزيد من المعلومات والحجز العام",
                backMain: "← القائمة الرئيسية",
                backDest: "← العودة للوجهات",
                backPlaces: "← رجوع للأماكن",
                chooseGov: "اختر الوجهة السياحية",
                placeDetails: "تفاصيل المكان",
                waBtn: "💬 احجز واستعلم عبر الواتساب",
                carTitle: "🚗 تأجير سيارات مع سائق محترف",
                carDesc: "استمتع براحة الحرية والاستكشاف على طريقتك الخاصة! نوفر لك سيارات حديثة ومكيفة بالكامل مع نخبة من السائقين المحترفين.",
                carWa: "💬 احجز سيارة مع سائق عبر الواتساب",
                airportTitle: "✈️ انتقالات المطار بكل سهولة وأمان",
                airportDesc: "ابدأ رحلتك بلا إرهاق! نحن في انتظارك لحظة هبوط طائرتك لضمان وصولك بكل أمان وراحة.",
                airportWa: "💬 احجز انتقالات المطار عبر الواتساب",
                cairo: "القاهرة",
                alex: "الإسكندرية",
                aswan: "أسوان",
                luxor: "الأقصر"
            },
            en: {
                subtitle: "Travel Agencies - Explore Egypt",
                mainTitle: "Welcome to Gem Travel - Select Service",
                sightseeing: "🏛️ Sightseeing & Excursions",
                carRental: "🚗 Car Rental with Driver",
                airportTransfer: "✈️ Airport Transfers",
                homeWa: "For More Information & Booking",
                backMain: "← Main Menu",
                backDest: "← Back to Destinations",
                backPlaces: "← Back to Places",
                chooseGov: "Select Destination",
                placeDetails: "Place Details",
                waBtn: "💬 Contact for Details & Reservation",
                carTitle: "🚗 Car Rental with Professional Driver",
                carDesc: "Enjoy freedom and exploration at your own pace! We offer modern, fully air-conditioned cars with professional drivers.",
                carWa: "💬 Book Car & Driver via WhatsApp",
                airportTitle: "✈️ Seamless Airport Transfers",
                airportDesc: "Start your trip without any fatigue! We will be waiting for you the moment your plane lands.",
                airportWa: "💬 Book Airport Transfer via WhatsApp",
                cairo: "Cairo",
                alex: "Alexandria",
                aswan: "Aswan",
                luxor: "Luxor"
            },
            fr: {
                subtitle: "Agences de Voyage - Explorer l'Égypte",
                mainTitle: "Bienvenue chez Gem Travel - Choisissez un service",
                sightseeing: "🏛️ Excursions et Tourisme",
                carRental: "🚗 Location de voiture avec chauffeur",
                airportTransfer: "✈️ Transferts Aéroport",
                homeWa: "Pour plus d'informations et réservations",
                backMain: "← Menu Principal",
                backDest: "← Retour aux destinations",
                backPlaces: "← Retour aux lieux",
                chooseGov: "Sélectionnez la destination",
                placeDetails: "Détails du lieu",
                waBtn: "💬 Contact & Réservation WhatsApp",
                carTitle: "🚗 Location de voiture avec chauffeur",
                carDesc: "Profitez de la liberté et de l'exploration à votre rythme avec des voitures modernes.",
                carWa: "💬 Réserver via WhatsApp",
                airportTitle: "✈️ Transferts aéroport",
                airportDesc: "Commencez votre voyage sans fatigue ! Nous vous attendons dès l'atterrissage.",
                airportWa: "💬 Réserver le transfert via WhatsApp",
                cairo: "Le Caire",
                alex: "Alexandrie",
                aswan: "Assouan",
                luxor: "Louxor"
            },
            es: {
                subtitle: "Agencias de Viajes - Explorar Egipto",
                mainTitle: "Bienvenido a Gem Travel - Seleccione servicio",
                sightseeing: "🏛️ Excursiones y Turismo",
                carRental: "🚗 Alquiler de autos con chofer",
                airportTransfer: "✈️ Traslados al Aeropuerto",
                homeWa: "Para más información y reservas",
                backMain: "← Menú Principal",
                backDest: "← Volver a destinos",
                backPlaces: "← Volver a lugares",
                chooseGov: "Seleccionar destino",
                placeDetails: "Detalles del lugar",
                waBtn: "💬 Contacto y Reserva por WhatsApp",
                carTitle: "🚗 Alquiler de autos con chofer",
                carDesc: "¡Disfruta de la libertad y exploración a tu ritmo con vehículos modernos!",
                carWa: "💬 Reservar por WhatsApp",
                airportTitle: "✈️ Traslados al aeropuerto",
                airportDesc: "¡Comienza tu viaje sin fatiga! Te esperamos en cuanto aterrice tu avión.",
                airportWa: "💬 Reservar traslado por WhatsApp",
                cairo: "El Cairo",
                alex: "Alejandría",
                aswan: "Asuán",
                luxor: "Luxor"
            },
            zh: {
                subtitle: "旅行社 - 探索埃及",
                mainTitle: "欢迎来到 Gem Travel - 请选择服务",
                sightseeing: "🏛️ 观光与游览",
                carRental: "🚗 带有司机的汽车租赁",
                airportTransfer: "✈️ 机场接送服务",
                homeWa: "获取更多信息与预订",
                backMain: "← 主菜单",
                backDest: "← 返回目的地",
                backPlaces: "← 返回地点",
                chooseGov: "选择目的地",
                placeDetails: "地点详情",
                waBtn: "💬 WhatsApp 咨询与预订",
                carTitle: "🚗 专业司机租车服务",
                carDesc: "按照您自己的节奏享受自由与探索！",
                carWa: "💬 通过 WhatsApp 预订",
                airportTitle: "✈️ 无忧机场接送服务",
                airportDesc: "开启轻松旅程！",
                airportWa: "💬 预订接机服务",
                cairo: "开罗",
                alex: "亚历山大",
                aswan: "阿斯旺",
                luxor: "卢克索"
            },
            ja: {
                subtitle: "旅行代理店 - エジプトを探索",
                mainTitle: "Gem Travelへようこそ - サービスを選択",
                sightseeing: "🏛️ 観光＆エクスカーション",
                carRental: "🚗 ドライバー付きレンタカー",
                airportTransfer: "✈️ 空港送迎サービス",
                homeWa: "詳細情報とご予約について",
                backMain: "← メインメニュー",
                backDest: "← 目的地に戻る",
                backPlaces: "← 場所に戻る",
                chooseGov: "目的地を選択",
                placeDetails: "場所の詳細",
                waBtn: "💬 WhatsAppで予約・問い合わせ",
                carTitle: "🚗 プロドライバー付きレンタカー",
                carDesc: "快適な観光をお楽しみください。",
                carWa: "💬 WhatsAppで予約",
                airportTitle: "✈️ スムーズな空港送迎",
                airportDesc: "旅の始まりをストレスフリーに！",
                airportWa: "💬 空港送迎を予約",
                cairo: "カイロ",
                alex: "アレクサンドリア",
                aswan: "アスワン",
                luxor: "ルクソール"
            }
        };

        let currentLang = 'en';

        function changeLanguage(lang) {
            currentLang = lang;
            const t = translations[lang];
            const htmlRoot = document.getElementById('html-root');
            
            if (lang === 'ar') {
                htmlRoot.setAttribute('dir', 'rtl');
                htmlRoot.setAttribute('lang', 'ar');
            } else {
                htmlRoot.setAttribute('dir', 'ltr');
                htmlRoot.setAttribute('lang', lang);
            }

            document.getElementById('header-subtitle').innerText = t.subtitle;
            document.getElementById('txt-main-title').innerText = t.mainTitle;
            document.getElementById('btn-sightseeing').innerText = t.sightseeing;
            document.getElementById('btn-car-rental').innerText = t.carRental;
            document.getElementById('btn-airport-transfer').innerText = t.airportTransfer;
            document.getElementById('txt-home-wa').innerText = t.homeWa;
            
            document.getElementById('btn-back-main1').innerText = t.backMain;
            document.getElementById('btn-back-main2').innerText = t.backMain;
            document.getElementById('btn-back-main3').innerText = t.backMain;
            document.getElementById('btn-back-sightseeing').innerText = t.backDest;
            document.getElementById('txt-choose-gov').innerText = t.chooseGov;
            
            document.getElementById('car-title').innerText = t.carTitle;
            document.getElementById('car-desc').innerText = t.carDesc;
            document.getElementById('wa-car-link').innerText = t.carWa;
            
            document.getElementById('airport-title').innerText = t.airportTitle;
            document.getElementById('airport-desc').innerText = t.airportDesc;
            document.getElementById('wa-airport-link').innerText = t.airportWa;

            document.getElementById('wa-home-link.href') // dummy
            document.getElementById('wa-home-link').href = `https://wa.me/${primaryWhatsApp}?text=${encodeURIComponent('Hello Gem Travel, I would like more information and general booking.')}`;
            document.getElementById('wa-car-link').href = `https://wa.me/${primaryWhatsApp}?text=${encodeURIComponent('Hello Gem Travel, I want to inquire about Car Rental with Driver.')}`;
            document.getElementById('wa-airport-link').href = `https://wa.me/${primaryWhatsApp}?text=${encodeURIComponent('Hello Gem Travel, I want to book an Airport Transfer.')}`;

            const buttons = document.querySelectorAll('#sightseeing-screen .btn-card');
            const keys = ['Cairo', 'Alex', 'Aswan', 'Luxor'];
            buttons.forEach((btn, index) => {
                let keyName = keys[index].toLowerCase();
                btn.innerText = t[keyName] || keys[index];
            });
        }

        function openScreen(screenId) {
            document.getElementById('main-hub-screen').classList.add('hidden');
            document.getElementById('sightseeing-screen').classList.add('hidden');
            document.getElementById('car-rental-screen').classList.add('hidden');
            document.getElementById('airport-transfer-screen').classList.add('hidden');
            document.getElementById('gov-screen').classList.add('hidden');
            document.getElementById('detail-screen').classList.add('hidden');

            document.getElementById(screenId).classList.remove('hidden');
        }

        function goMainHub() {
            openScreen('main-hub-screen');
        }

        const tourData = {
            Cairo: {
                title: { ar: "رحلات القاهرة", en: "Cairo Tours", fr: "Excursions au Caire", es: "Tours por El Cairo", zh: "开罗旅游", ja: "カイロツアー" },
                subsections: [
                    {
                        category: { ar: "رحلات نهارية", en: "Cairo Day Trips", fr: "Visites diurnes", es: "Tours diurnos", zh: "日间游", ja: "日帰りツアー" },
                        items: [
                            { name: "Pyramids of Giza", images: ["https://images.unsplash.com/photo-1539650116574-8efeb43e2750", "https://images.unsplash.com/photo-1568322445760-727c66798c8c"] },
                            { name: "Cairo Citadel", images: ["https://images.unsplash.com/photo-1572252009286-268acec5ca0a"] },
                            { name: "Grand Egyptian Museum", images: ["https://images.unsplash.com/photo-1564507592333-c60657eea523"] }
                        ]
                    }
                ]
            },
            Alex: {
                title: { ar: "الإسكندرية", en: "Alexandria", fr: "Alexandrie", es: "Alejandría", zh: "亚历山大", ja: "アレクサンドリア" },
                subsections: [
                    {
                        category: { ar: "معالم الإسكندرية", en: "Alexandria Landmarks", fr: "Monuments", es: "Monumentos", zh: "地标", ja: "ランドマーク" },
                        items: [
                            { name: "Qaitbay Castle", images: ["https://images.unsplash.com/photo-1568605117036-5fe5e7bab0b7"] },
                            { name: "Alexandria Library", images: ["https://images.unsplash.com/photo-1541872703-74c5e44368f9"] }
                        ]
                    }
                ]
            },
            Aswan: {
                title: { ar: "أسوان", en: "Aswan", fr: "Assouan", es: "Asuán", zh: "阿斯旺", ja: "アスワン" },
                subsections: [
                    {
                        category: { ar: "معالم أسوان", en: "Aswan Highlights", fr: "Sites d'Assouan", es: "Sitios de Asuán", zh: "阿斯旺景点", ja: "アスワンの見どころ" },
                        items: [
                            { name: "Abu Simbel", images: ["https://images.unsplash.com/photo-1564507592333-c60657eea523"] },
                            { name: "Nubian Village", images: ["https://images.unsplash.com/photo-1544816155-12df9643f363"] }
                        ]
                    }
                ]
            },
            Luxor: {
                title: { ar: "الأقصر", en: "Luxor", fr: "Louxor", es: "Luxor", zh: "卢克索", ja: "ルクソール" },
                subsections: [
                    {
                        category: { ar: "معالم الأقصر", en: "Luxor Temples & Valley", fr: "Temples de Louxor", es: "Templos de Luxor", zh: "卢克索神庙与河谷", ja: "ルクソールの神殿と渓谷" },
                        items: [
                            { name: "Karnak Temple", images: ["https://images.unsplash.com/photo-1608953151270-2495edab4fb6"] },
                            { name: "Valley of the Kings", images: ["https://images.unsplash.com/photo-1568322445760-727c66798c8c"] }
                        ]
                    }
                ]
            }
        };

        function openGov(govKey) {
            document.getElementById('sightseeing-screen').classList.add('hidden');
            document.getElementById('gov-screen').classList.remove('hidden');
            
            const data = tourData[govKey];
            let govTitle = data.title[currentLang] || data.title['en'];
            let html = `<div class="section-title">${govTitle}</div>`;
            
            data.subsections.forEach(sub => {
                let catName = sub.category[currentLang] || sub.category['en'];
                if(catName) html += `<h4 style="color:#0284c7; margin-top:20px;">${catName}</h4>`;
                html += `<div class="grid">`;
                sub.items.forEach(item => {
                    html += `<div class="btn-card" onclick='openPlace(${JSON.stringify(item.name)}, ${JSON.stringify(item.images)})'>${item.name}</div>`;
                });
                html += `</div>`;
            });
            document.getElementById('gov-content').innerHTML = html;
        }

        let slideInterval;
        function backToGov() {
            clearInterval(slideInterval);
            document.getElementById('detail-screen').classList.add('hidden');
            document.getElementById('gov-screen').classList.remove('hidden');
        }

        function openPlace(placeName, images) {
            document.getElementById('gov-screen').classList.add('hidden');
            document.getElementById('detail-screen').classList.remove('hidden');
            document.getElementById('place-title').innerText = placeName;

            let sliderHtml = '';
            images.forEach((img, index) => {
                sliderHtml += `
                    <div class="mySlides" style="display: ${index === 0 ? 'block' : 'none'}">
                        <img src="${img}" alt="${placeName}">
                        <div class="slide-caption">${placeName} - Photo ${index + 1}</div>
                    </div>
                `;
            });
            document.getElementById('slider-container').innerHTML = sliderHtml;

            let waText = encodeURIComponent(`Hello Gem Travel, I would like to inquire and reserve for: ${placeName}`);
            document.getElementById('wa-link').href = `https://wa.me/${primaryWhatsApp}?text=${waText}`;

            if (images.length > 1) {
                let sIndex = 0;
                clearInterval(slideInterval);
                slideInterval = setInterval(() => {
                    let slides = document.querySelectorAll('.mySlides');
                    slides.forEach(s => s.style.display = 'none');
                    sIndex = (sIndex + 1) % slides.length;
                    slides[sIndex].style.display = 'block';
                }, 3000);
            }
        }

        changeLanguage('en');
    </script>
</body>
</html>
