<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Travel Itinerary December 2024</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            margin: 0;
            padding: 15px;
            background-color: #f5f5f5;
        }
        h1 {
            text-align: center;
            color: #2c3e50;
            font-size: 24px;
            margin-bottom: 30px;
        }
        .menu {
            display: flex;
            flex-direction: column;
            gap: 40px;
            margin-bottom: 40px;
            max-width: 600px;
            margin: 0 auto;
            padding: 20px;
        }
        .menu-item-container {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 15px;
        }
        .menu-item {
            background-color: #2c3e50;
            color: white;
            padding: 20px 30px;
            border-radius: 10px;
            cursor: pointer;
            text-decoration: none;
            font-size: 18px;
            text-align: center;
            transition: transform 0.2s;
            width: 80%;
            display: block;
        }
        .menu-item:hover {
            background-color: #34495e;
            transform: translateY(-2px);
        }
        .map-preview {
            width: 100%;
            height: 200px;
            border-radius: 10px;
            margin-bottom: 10px;
            border: none;
        }
        .modal-overlay {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-color: rgba(0, 0, 0, 0.7);
            z-index: 1000;
            overflow-y: auto;
        }
        .modal {
            background-color: white;
            width: 90%;
            max-width: 600px;
            margin: 20px auto;
            padding: 20px;
            border-radius: 10px;
            position: relative;
            animation: slideIn 0.3s ease-out;
        }
        @keyframes slideIn {
            from { transform: translateY(-100px); opacity: 0; }
            to { transform: translateY(0); opacity: 1; }
        }
        .close-button {
            position: absolute;
            top: 10px;
            right: 10px;
            background: none;
            border: none;
            font-size: 24px;
            cursor: pointer;
            color: #2c3e50;
            padding: 5px 10px;
            border-radius: 5px;
        }
        .close-button:hover {
            background-color: #f0f0f0;
        }
        table {
            width: 100%;
            border-collapse: collapse;
            margin-bottom: 20px;
            font-size: 14px;
        }
        th, td {
            padding: 12px;
            border: 1px solid #ddd;
            text-align: left;
        }
        th {
            background-color: #f8f9fa;
        }
        .passengers {
            display: flex;
            flex-direction: column;
            gap: 20px;
            margin-top: 30px;
            align-items: center;
        }
        .passenger-btn {
            background-color: #3498db;
            color: white;
            border: none;
            padding: 20px 30px;
            border-radius: 8px;
            cursor: pointer;
            font-size: 18px;
            transition: background-color 0.2s;
            width: 80%;
            max-width: 300px;
        }
        .passenger-btn:hover {
            background-color: #2980b9;
        }
        .destination-header {
            text-align: center;
            margin: 0 0 20px 0;
            color: #2c3e50;
        }
        .pdf-modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-color: rgba(0, 0, 0, 0.8);
            z-index: 2000;
            padding: 20px;
        }
        .pdf-container {
            background: white;
            padding: 20px;
            border-radius: 10px;
            position: relative;
            width: 100%;
            height: 100%;
            max-width: 800px;
            margin: 0 auto;
        }
        .pdf-viewer {
            width: 100%;
            height: calc(100% - 40px);
            border: none;
            border-radius: 5px;
        }
        .close-pdf {
            position: absolute;
            top: 10px;
            right: 10px;
            background: white;
            border: none;
            font-size: 24px;
            cursor: pointer;
            width: 40px;
            height: 40px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 2px 5px rgba(0,0,0,0.2);
        }
        .close-pdf:hover {
            background-color: #f0f0f0;
        }
        .loading {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            color: white;
            font-size: 18px;
            text-align: center;
        }
        .loading:after {
            content: '';
            display: block;
            width: 40px;
            height: 40px;
            margin: 20px auto;
            border-radius: 50%;
            border: 4px solid #fff;
            border-top-color: transparent;
            animation: spin 1s linear infinite;
        }
        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
    </style>
</head>
<body>
    <h1>Travel Itinerary December 2024</h1>
    
    <div class="menu">
        <div class="menu-item-container">
            <iframe class="map-preview" src="https://www.google.com/maps/embed/v1/place?key=AIzaSyBMJpBlQLdRY0XhvHftWxR4kSPpxmHjkk0&q=Madrid,Spain" frameborder="0"></iframe>
            <a href="#" class="menu-item" onclick="showItinerary('dec1')">
                December 1: Guatemala - Madrid
            </a>
        </div>
        
        <div class="menu-item-container">
            <iframe class="map-preview" src="https://www.google.com/maps/embed/v1/place?key=AIzaSyBMJpBlQLdRY0XhvHftWxR4kSPpxmHjkk0&q=Rovaniemi,Finland" frameborder="0"></iframe>
            <a href="#" class="menu-item" onclick="showItinerary('dec3')">
                December 3: Madrid - Rovaniemi
            </a>
        </div>
        
        <div class="menu-item-container">
            <iframe class="map-preview" src="https://www.google.com/maps/embed/v1/place?key=AIzaSyBMJpBlQLdRY0XhvHftWxR4kSPpxmHjkk0&q=Basel,Switzerland" frameborder="0"></iframe>
            <a href="#" class="menu-item" onclick="showItinerary('dec5')">
                December 5: Rovaniemi - Basel
            </a>
        </div>
        
        <div class="menu-item-container">
            <iframe class="map-preview" src="https://www.google.com/maps/embed/v1/place?key=AIzaSyBMJpBlQLdRY0XhvHftWxR4kSPpxmHjkk0&q=Strasbourg,France" frameborder="0"></iframe>
            <a href="#" class="menu-item" onclick="showItinerary('dec6')">
                December 6: Basel - Strasbourg
            </a>
        </div>
        
        <div class="menu-item-container">
            <iframe class="map-preview" src="https://www.google.com/maps/embed/v1/place?key=AIzaSyBMJpBlQLdRY0XhvHftWxR4kSPpxmHjkk0&q=Paris,France" frameborder="0"></iframe>
            <a href="#" class="menu-item" onclick="showItinerary('dec8')">
                December 8: Strasbourg - Paris
            </a>
        </div>
    </div>

    <!-- Modal Overlay -->
    <div id="modalOverlay" class="modal-overlay">
        <div class="modal">
            <button class="close-button" onclick="closeModal()">&times;</button>
            <div id="modalContent">
                <!-- Content will be inserted here -->
            </div>
        </div>
    </div>

    <!-- PDF Modal -->
    <div id="pdfModal" class="pdf-modal">
        <div id="loading" class="loading">Loading PDF...</div>
        <div class="pdf-container">
            <button class="close-pdf" onclick="closePdfViewer()">&times;</button>
            <iframe id="pdfViewer" class="pdf-viewer"></iframe>
        </div>
    </div>

    <!-- Templates -->
    <template id="dec1-template">
        <h2 class="destination-header">December 1: Guatemala - Madrid</h2>
        <table>
            <tr>
                <th>Time</th>
                <th>From</th>
                <th>To</th>
                <th>Transport</th>
            </tr>
            <tr>
                <td>6:45 AM</td>
                <td>Guatemala</td>
                <td>Miami</td>
                <td>Flight</td>
            </tr>
            <tr>
                <td>3:35 PM</td>
                <td>Miami</td>
                <td>Madrid</td>
                <td>Flight</td>
            </tr>
        </table>
        <div class="passengers">
            <button class="passenger-btn" onclick="showPdf('1Q8YGpie-9vOYVKgOzl9aONCaZTd1tzXB')">Nancy's Ticket</button>
            <button class="passenger-btn" onclick="showPdf('1dCGVtU7EXFAMlD0eAWCRkWVs8RD7UnRv')">Daniel's Ticket</button>
            <button class="passenger-btn" onclick="showPdf('1V_kDOlynZZbL9v8MXqfXWD4OIERpx9Hc')">Emilio's Ticket</button>
        </div>
    </template>



<template id="dec3-template">
    <h2 class="destination-header">December 3: Madrid - Rovaniemi</h2>
    <table>
        <tr>
            <th>Time</th>
            <th>From</th>
            <th>To</th>
            <th>Transport</th>
        </tr>
        <tr>
            <td>10:20 AM</td>
            <td>Madrid</td>
            <td>Helsinki</td>
            <td>Flight</td>
        </tr>
        <tr>
            <td>9:14 PM</td>
            <td>Helsinki</td>
            <td>Rovaniemi</td>
            <td>Train</td>
        </tr>
    </table>
    <div class="trip-buttons">
        <button class="trip-btn" onclick="showTicketsModal('flight')">Flight Tickets: Madrid - Helsinki</button>
        <button class="trip-btn" onclick="showTicketsModal('train')">Train Tickets: Helsinki - Rovaniemi</button>
    </div>
</template>

<!-- Add new tickets modal -->
<div id="ticketsModal" class="modal-overlay">
    <div class="modal">
        <button class="close-button" onclick="closeTicketsModal()">&times;</button>
        <div id="ticketsModalContent">
            <!-- Content will be inserted here -->
        </div>
    </div>
</div>

<!-- Add templates for ticket types -->
<template id="flight-tickets-template">
    <h3 class="ticket-type-header">Madrid - Helsinki Flight Tickets</h3>
    <div class="passengers">
        <button class="passenger-btn" onclick="showPdf('1f9LfonydJOP4J-tITkUDR8s0TtIqsHu2')">Nancy's Flight Ticket</button>
        <button class="passenger-btn" onclick="showPdf('1jBZ_Riaub-e5Qyx5Qojbpb_F1Tm4ew-G')">Daniel's Flight Ticket</button>
        <button class="passenger-btn" onclick="showPdf('1wBVkY0UwdQtDALqq9003FeKs1dt2pb2o')">Emilio's Flight Ticket</button>
    </div>
</template>
<template id="train-tickets-template">
    <h3 class="ticket-type-header">Helsinki - Rovaniemi Train Tickets</h3>
    <div class="passengers">
        <button class="passenger-btn" onclick="showPdf('1aFq8k4ZmyPBE3azFsMaZmBo_hIbtWcEc')">Nancy's Train Ticket</button>
        <button class="passenger-btn" onclick="showPdf('1GZ-ZSwdjz303UIOcw1LIuLuxy14T_-YK')">Daniel's Train Ticket</button>
        <button class="passenger-btn" onclick="showPdf('1Ek2aarYK_Qc79acqmktZcbfQnPzUbWLp')">Emilio's Train Ticket</button>
    </div>
</template>

<style>
    /* Add to existing styles */
    .trip-buttons {
        display: flex;
        flex-direction: column;
        gap: 15px;
        margin: 20px 0;
        align-items: center;
    }

    .trip-btn {
        background-color: #2c3e50;
        color: white;
        border: none;
        padding: 15px 25px;
        border-radius: 8px;
        cursor: pointer;
        font-size: 16px;
        transition: all 0.2s;
        width: 80%;
        max-width: 300px;
    }

    .trip-btn:hover {
        background-color: #34495e;
        transform: translateY(-2px);
    }

    .ticket-type-header {
        text-align: center;
        color: #2c3e50;
        margin-bottom: 20px;
        font-size: 20px;
    }
</style>

<script>
    // Add to existing JavaScript
    function showTicketsModal(type) {
        const ticketsModal = document.getElementById('ticketsModal');
        const modalContent = document.getElementById('ticketsModalContent');
        const template = document.getElementById(`${type}-tickets-template`);
        
        modalContent.innerHTML = template.innerHTML;
        ticketsModal.style.display = 'block';
        document.body.style.overflow = 'hidden';
    }

    function closeTicketsModal() {
        const ticketsModal = document.getElementById('ticketsModal');
        ticketsModal.style.display = 'none';
        document.body.style.overflow = 'auto';
    }

    // Add click outside listener for tickets modal
    document.getElementById('ticketsModal').addEventListener('click', function(e) {
        if (e.target === this) {
            closeTicketsModal();
        }
    });
</script>

    <script>
        function showItinerary(id) {
            const modalOverlay = document.getElementById('modalOverlay');
            const modalContent = document.getElementById('modalContent');
            const template = document.getElementById(`${id}-template`);
            
            modalContent.innerHTML = template.innerHTML;
            modalOverlay.style.display = 'block';
            document.body.style.overflow = 'hidden';
        }

        function closeModal() {
            const modalOverlay = document.getElementById('modalOverlay');
            modalOverlay.style.display = 'none';
            document.body.style.overflow = 'auto';
        }

        function showPdf(fileId) {
            const pdfModal = document.getElementById('pdfModal');
            const pdfViewer = document.getElementById('pdfViewer');
            const loading = document.getElementById('loading');
            
            pdfModal.style.display = 'block';
            loading.style.display = 'block';
            
            const pdfUrl = `https://drive.google.com/file/d/${fileId}/preview`;
            
            pdfViewer.onload = function() {
                loading.style.display = 'none';
            };
            
            pdfViewer.src = pdfUrl;
            document.body.style.overflow = 'hidden';
        }

        function closePdfViewer() {
            const pdfModal = document.getElementById('pdfModal');
            const pdfViewer = document.getElementById('pdfViewer');
            pdfModal.style.display = 'none';
            pdfViewer.src = '';
            document.body.style.overflow = 'auto';
        }

        // Close modals when clicking outside
        document.getElementById('modalOverlay').addEventListener('click', function(e) {
            if (e.target === this) {
                closeModal();
            }
        });

        document.getElementById('pdfModal').addEventListener('click', function(e) {
            if (e.target === this) {
                closePdfViewer();
            }
        });
    </script>
</body>
</html>
