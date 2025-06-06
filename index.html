<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>แชร์ตำแหน่งที่ตั้ง</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Sarabun:wght@400;500;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://unpkg.com/leaflet@1.7.1/dist/leaflet.css" />
    <style>
        :root {
            --primary-color: #2563eb;
            --primary-hover: #1d4ed8;
            --secondary-color: #10b981;
            --secondary-hover: #059669;
            --accent-color: #ef4444;
            --accent-hover: #dc2626;
            --light-bg: #f8fafc;
            --dark-text: #1e293b;
            --medium-text: #64748b;
            --light-text: #94a3b8;
            --card-shadow: 0 10px 25px -5px rgba(0, 0, 0, 0.1), 0 8px 10px -6px rgba(0, 0, 0, 0.1);
            --border-radius: 16px;
        }
        
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }
        
        body {
            font-family: 'Sarabun', sans-serif;
            margin: 0;
            padding: 0;
            background: linear-gradient(135deg, #f0f9ff 0%, #e0f2fe 100%);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            color: var(--dark-text);
        }
        
        .container {
            background: white;
            padding: 30px;
            border-radius: var(--border-radius);
            box-shadow: var(--card-shadow);
            max-width: 450px;
            width: 100%;
            text-align: center;
            position: relative;
            overflow: hidden;
            margin: 20px;
        }
        
        .page-header {
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 20px;
            gap: 12px;
        }
        
        .logo {
            width: 60px;
            height: 60px;
            object-fit: contain;
            margin-bottom: 10px;
        }
        
        .location-icon {
            width: 48px;
            height: 48px;
            margin-right: 8px;
        }
        
        h1 {
            color: var(--dark-text);
            font-size: 1.8rem;
            font-weight: 700;
            margin: 0;
        }
        
        p {
            color: var(--medium-text);
            line-height: 1.6;
            margin-bottom: 24px;
        }
        
        .steps {
            display: flex;
            justify-content: center;
            margin-bottom: 24px;
            position: relative;
        }
        
        .step {
            display: flex;
            flex-direction: column;
            align-items: center;
            width: 90px;
            z-index: 1;
        }
        
        .step-number {
            width: 28px;
            height: 28px;
            border-radius: 50%;
            background-color: var(--light-bg);
            color: var(--medium-text);
            display: flex;
            justify-content: center;
            align-items: center;
            font-weight: 500;
            margin-bottom: 8px;
            border: 2px solid #e2e8f0;
            transition: all 0.3s ease;
        }
        
        .step.active .step-number {
            background-color: var(--primary-color);
            color: white;
            border-color: var(--primary-color);
        }
        
        .step-text {
            font-size: 0.8rem;
            color: var(--medium-text);
            text-align: center;
            transition: all 0.3s ease;
        }
        
        .step.active .step-text {
            color: var(--primary-color);
            font-weight: 500;
        }
        
        .step-line {
            position: absolute;
            top: 14px;
            left: 50%;
            transform: translateX(-50%);
            height: 2px;
            background-color: #e2e8f0;
            width: 60%;
            z-index: 0;
        }
        
        .button-group {
            display: flex;
            gap: 12px;
            justify-content: center;
            margin: 24px 0;
        }
        
        .share-button {
            background: var(--primary-color);
            color: white;
            border: none;
            padding: 14px 20px;
            border-radius: 12px;
            font-size: 1rem;
            font-weight: 500;
            cursor: pointer;
            transition: all 0.3s ease;
            display: flex;
            align-items: center;
            gap: 8px;
            flex: 1;
            max-width: 200px;
            justify-content: center;
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -2px rgba(0, 0, 0, 0.1);
        }
        
        .share-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -4px rgba(0, 0, 0, 0.1);
        }
        
        .share-button:active {
            transform: translateY(0);
        }
        
        .current-location {
            background: var(--primary-color);
        }
        
        .current-location:hover {
            background: var(--primary-hover);
        }
        
        .select-location {
            background: var(--secondary-color);
        }
        
        .select-location:hover {
            background: var(--secondary-hover);
        }
        
        .send-button {
            background: var(--accent-color);
            display: none;
            width: 100%;
            margin-top: 20px;
            box-shadow: 0 4px 6px -1px rgba(239, 68, 68, 0.2), 0 2px 4px -2px rgba(239, 68, 68, 0.2);
        }
        
        .send-button:hover {
            background: var(--accent-hover);
        }
        
        #map {
            height: 300px;
            width: 100%;
            margin-top: 20px;
            border-radius: 12px;
            display: none;
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -2px rgba(0, 0, 0, 0.1);
            border: 2px solid #e2e8f0;
        }
        
        .location-info {
            margin-top: 20px;
            padding: 15px;
            border-radius: 12px;
            background: #f0f9ff;
            border: 1px solid #bae6fd;
            display: none;
            text-align: left;
        }
        
        .selected-location {
            margin-top: 20px;
            padding: 15px;
            background: var(--light-bg);
            border-radius: 12px;
            display: none;
            text-align: left;
            border: 1px solid #e2e8f0;
        }
        
        .selected-location p {
            margin-bottom: 8px;
        }
        
        .selected-location p:last-child {
            margin-bottom: 0;
        }
        
        .loading {
            display: none;
            margin-top: 15px;
            color: var(--medium-text);
            font-weight: 500;
        }
        
        .loading::after {
            content: '';
            display: inline-block;
            width: 20px;
            height: 20px;
            border: 2px solid #f3f3f3;
            border-top: 2px solid var(--primary-color);
            border-radius: 50%;
            animation: spin 1s linear infinite;
            margin-left: 10px;
            vertical-align: middle;
        }
        
        .error-message {
            color: var(--accent-color);
            margin-top: 15px;
            display: none;
            font-weight: 500;
            background: #fee2e2;
            padding: 10px;
            border-radius: 8px;
            border: 1px solid #fecaca;
        }
        
        .custom-message {
            margin-top: 20px;
            display: none;
        }
        
        .custom-message textarea {
            width: 100%;
            border: 1px solid #e2e8f0;
            border-radius: 8px;
            padding: 12px;
            font-family: 'Sarabun', sans-serif;
            resize: vertical;
            min-height: 80px;
            font-size: 1rem;
        }
        
        .location-details {
            margin-top: 10px;
            display: flex;
            gap: 10px;
        }
        
        .location-details > div {
            flex: 1;
            text-align: center;
            padding: 10px;
            background: var(--light-bg);
            border-radius: 8px;
            font-size: 0.9rem;
        }
        
        .location-details .value {
            font-weight: 500;
            color: var(--dark-text);
            font-size: 1.1rem;
            margin-top: 4px;
        }
        
        .location-details .label {
            color: var(--medium-text);
            font-size: 0.8rem;
        }
        
        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
        
        @media (max-width: 480px) {
            .container {
                padding: 20px;
                margin: 10px;
                border-radius: 12px;
            }
            
            .button-group {
                flex-direction: column;
                gap: 10px;
            }
            
            .share-button {
                max-width: none;
            }
            
            h1 {
                font-size: 1.5rem;
            }
            
            .page-header {
                flex-direction: column;
                gap: 8px;
            }
            
            .location-details {
                flex-direction: column;
                gap: 8px;
            }
        }
    </style>
<script src="https://lib.youware.com/youware-lib.1747145198.js" id="yourware-lib"></script></head>
<body>
    <div class="container">
        <div class="page-header">
            <img src="https://img2.pic.in.th/pic/60p.png" alt="Logo" class="logo">
        </div>
        <div class="page-header">
            <img src="https://public.youware.com/users-website-assets/prod/24adcf9b-7d56-49c5-96e9-36f571aa111e/location-4496459_1280.png" alt="Location Icon" class="location-icon">
            <h1>แชร์ตำแหน่งที่ตั้ง</h1>
        </div>
        
        <p>แชร์ตำแหน่งที่ตั้งของคุณกับร้านค้าเพื่อการจัดส่งที่รวดเร็วและแม่นยำ</p>
        
        <div class="steps">
            <div class="step-line"></div>
            <div class="step active" id="step1">
                <div class="step-number">1</div>
                <div class="step-text">เลือกตำแหน่ง</div>
            </div>
            <div class="step" id="step2">
                <div class="step-number">2</div>
                <div class="step-text">ตรวจสอบ</div>
            </div>
            <div class="step" id="step3">
                <div class="step-number">3</div>
                <div class="step-text">ส่งตำแหน่ง</div>
            </div>
        </div>
        
        <div class="button-group">
            <button class="share-button current-location" onclick="getLocation()">
                📍 ตำแหน่งปัจจุบัน
            </button>
            <button class="share-button select-location" onclick="showMap()">
                🗺️ เลือกตำแหน่งเอง
            </button>
        </div>
        
        <div id="map"></div>
        
        <div id="selectedLocation" class="selected-location"></div>
        
        <div class="custom-message" id="customMessage">
            <textarea placeholder="เพิ่มข้อความหรือคำอธิบายเพิ่มเติม (เช่น สีบ้าน, จุดสังเกต)" id="messageInput"></textarea>
        </div>
        
        <button id="sendButton" class="share-button send-button" onclick="sendLocation()">
            📤 ส่งตำแหน่ง
        </button>
        
        <div id="loading" class="loading">กำลังส่งข้อมูล...</div>
        <div id="locationInfo" class="location-info"></div>
        <div id="errorMessage" class="error-message"></div>
    </div>

    <script src="https://unpkg.com/leaflet@1.7.1/dist/leaflet.js"></script>
    <script>
        let map;
        let marker;
        let selectedLocation = false;
        let currentLatLng = null;
        
        // Step management
        function setActiveStep(stepNumber) {
            document.querySelectorAll('.step').forEach((step, index) => {
                if (index < stepNumber) {
                    step.classList.add('active');
                } else {
                    step.classList.remove('active');
                }
            });
        }

        function initMap() {
            // ถ้าแผนที่ถูกสร้างแล้ว ไม่ต้องสร้างใหม่
            if (map) {
                document.getElementById('map').style.display = 'block';
                return;
            }
            
            map = L.map('map').setView([13.7563, 100.5018], 13);
            
            // ใช้ OpenStreetMap รุ่นที่มีการออกแบบที่สวยงามมากขึ้น
            L.tileLayer('https://{s}.tile.openstreetmap.fr/hot/{z}/{x}/{y}.png', {
                attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors',
                maxZoom: 19
            }).addTo(map);

            // เพิ่มตัวควบคุมซูม
            map.zoomControl.setPosition('bottomright');
            
            // เพิ่ม event handler สำหรับการคลิกบนแผนที่
            map.on('click', function(e) {
                if (marker) {
                    map.removeLayer(marker);
                }
                
                // สร้างมาร์กเกอร์ด้วยไอคอนที่กำหนดเอง
                marker = L.marker(e.latlng, {
                    draggable: true, // ให้มาร์กเกอร์สามารถลากได้
                    autoPan: true
                }).addTo(map);
                
                // อัปเดตตำแหน่งเมื่อมีการลากมาร์กเกอร์
                marker.on('dragend', function(event) {
                    updateLocationDisplay(event.target.getLatLng());
                });
                
                selectedLocation = true;
                currentLatLng = e.latlng;
                
                updateLocationDisplay(e.latlng);
                
                // แสดงขั้นตอนที่ 2
                setActiveStep(2);
            });
            
            document.getElementById('map').style.display = 'block';
        }
        
        function updateLocationDisplay(latLng) {
            document.getElementById('selectedLocation').style.display = 'block';
            document.getElementById('customMessage').style.display = 'block';
            
            // แสดงข้อมูลตำแหน่งในรูปแบบที่อ่านง่ายขึ้น
            document.getElementById('selectedLocation').innerHTML = `
                <p><strong>📍 ตำแหน่งที่เลือก:</strong></p>
                <div class="location-details">
                    <div>
                        <div class="label">ละติจูด</div>
                        <div class="value">${latLng.lat.toFixed(6)}</div>
                    </div>
                    <div>
                        <div class="label">ลองจิจูด</div>
                        <div class="value">${latLng.lng.toFixed(6)}</div>
                    </div>
                </div>
                <p style="margin-top: 12px; font-size: 0.9rem; color: var(--medium-text);">
                    <a href="https://www.google.com/maps?q=${latLng.lat},${latLng.lng}" target="_blank" style="color: var(--primary-color);">
                        ดูใน Google Maps
                    </a>
                </p>
            `;
            
            document.getElementById('sendButton').style.display = 'block';
        }

        function showMap() {
            document.getElementById('errorMessage').style.display = 'none';
            initMap();
            setActiveStep(1);
        }

        function getLocation() {
            document.getElementById('errorMessage').style.display = 'none';
            
            if (navigator.geolocation) {
                document.getElementById('loading').style.display = 'block';
                document.getElementById('loading').textContent = 'กำลังค้นหาตำแหน่งปัจจุบัน...';
                
                navigator.geolocation.getCurrentPosition(
                    function(position) {
                        document.getElementById('loading').style.display = 'none';
                        
                        const latitude = position.coords.latitude;
                        const longitude = position.coords.longitude;
                        currentLatLng = { lat: latitude, lng: longitude };
                        
                        // แสดงแผนที่และซูมไปที่ตำแหน่งปัจจุบัน
                        initMap();
                        map.setView([latitude, longitude], 16);
                        
                        if (marker) {
                            map.removeLayer(marker);
                        }
                        
                        marker = L.marker([latitude, longitude], {
                            draggable: true,
                            autoPan: true
                        }).addTo(map);
                        
                        // อัปเดตตำแหน่งเมื่อมีการลากมาร์กเกอร์
                        marker.on('dragend', function(event) {
                            updateLocationDisplay(event.target.getLatLng());
                        });
                        
                        updateLocationDisplay(currentLatLng);
                        
                        // แสดงขั้นตอนที่ 2
                        setActiveStep(2);
                    },
                    function(error) {
                        document.getElementById('loading').style.display = 'none';
                        
                        let errorMessage = '';
                        switch(error.code) {
                            case error.PERMISSION_DENIED:
                                errorMessage = 'กรุณาอนุญาตให้เข้าถึงตำแหน่งที่ตั้งของคุณ';
                                break;
                            case error.POSITION_UNAVAILABLE:
                                errorMessage = 'ไม่สามารถเข้าถึงตำแหน่งที่ตั้งได้';
                                break;
                            case error.TIMEOUT:
                                errorMessage = 'หมดเวลาการร้องขอตำแหน่งที่ตั้ง';
                                break;
                            default:
                                errorMessage = 'เกิดข้อผิดพลาดที่ไม่ทราบสาเหตุ';
                                break;
                        }
                        document.getElementById('errorMessage').style.display = 'block';
                        document.getElementById('errorMessage').textContent = errorMessage;
                    },
                    {
                        enableHighAccuracy: true,
                        timeout: 10000,
                        maximumAge: 0
                    }
                );
            } else {
                document.getElementById('errorMessage').style.display = 'block';
                document.getElementById('errorMessage').textContent = 'เบราว์เซอร์ของคุณไม่รองรับการเข้าถึงตำแหน่งที่ตั้ง';
            }
        }

        async function sendLocation() {
            if (!currentLatLng) {
                document.getElementById('errorMessage').style.display = 'block';
                document.getElementById('errorMessage').textContent = 'กรุณาเลือกตำแหน่งก่อนส่ง';
                return;
            }

            // แสดง loading
            document.getElementById('loading').style.display = 'block';
            document.getElementById('sendButton').style.display = 'none';
            document.getElementById('errorMessage').style.display = 'none';
            
            // แสดงขั้นตอนที่ 3
            setActiveStep(3);

            try {
                // รับข้อความเพิ่มเติมจาก textarea
                const additionalMessage = document.getElementById('messageInput').value.trim();
                
                // สร้าง URL สำหรับ LINE OA
                let messageText = `ตำแหน่งที่ตั้ง: ${currentLatLng.lat.toFixed(6)}, ${currentLatLng.lng.toFixed(6)}\nGoogle Maps: https://www.google.com/maps?q=${currentLatLng.lat},${currentLatLng.lng}`;
                
                // เพิ่มข้อความเพิ่มเติมถ้ามี
                if (additionalMessage) {
                    messageText += `\n\nข้อความเพิ่มเติม: ${additionalMessage}`;
                }
                
                const lineOAUrl = `https://line.me/R/oaMessage/@laemtong2/?${encodeURIComponent(messageText)}`;

                // เปิด LINE OA ในหน้าต่างใหม่
                window.open(lineOAUrl, '_blank');

                // แสดงข้อความยืนยัน
                document.getElementById('locationInfo').style.display = 'block';
                document.getElementById('locationInfo').innerHTML = `
                    <p style="margin-bottom: 8px; font-weight: 500;">✅ ตำแหน่งของคุณถูกส่งให้ร้านค้าเรียบร้อยแล้ว</p>
                    <p style="margin-bottom: 0;">กรุณาตรวจสอบข้อความในแชท LINE OA เพื่อติดตามสถานะการจัดส่ง</p>
                `;

            } catch (error) {
                document.getElementById('errorMessage').style.display = 'block';
                document.getElementById('errorMessage').textContent = 'เกิดข้อผิดพลาดในการส่งข้อมูล กรุณาลองใหม่อีกครั้ง';
                document.getElementById('sendButton').style.display = 'block';
                setActiveStep(2);
            } finally {
                document.getElementById('loading').style.display = 'none';
            }
        }
    </script>
</body>
</html>
