!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gangadhar Experience Line - Premium Bus Booking</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 25%, #f093fb 50%, #4facfe 75%, #00f2fe 100%);
            min-height: 100vh;
            animation: gradientShift 15s ease infinite;
            background-size: 400% 400%;
        }

        @keyframes gradientShift {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        /* Header */
        .header {
            background: linear-gradient(135deg, #ff0844 0%, #ffb199 25%, #ffd89b 50%, #19dcea 75%, #b721ff 100%);
            color: white;
            padding: 0;
            box-shadow: 0 4px 20px rgba(0,0,0,0.15);
            position: sticky;
            top: 0;
            z-index: 1000;
            background-size: 300% 300%;
            animation: rainbowFlow 10s ease infinite;
        }

        @keyframes rainbowFlow {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        .header-content {
            max-width: 1400px;
            margin: 0 auto;
            padding: 20px 30px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo-section {
            display: flex;
            align-items: center;
            gap: 15px;
        }

        .logo {
            font-size: 2em;
        }

        .brand-name h1 {
            font-size: 1.8em;
            font-weight: 700;
            letter-spacing: -0.5px;
        }

        .brand-name p {
            font-size: 0.9em;
            opacity: 0.9;
            font-weight: 300;
        }

        .header-actions {
            display: flex;
            gap: 15px;
            align-items: center;
        }

        .header-btn {
            background: rgba(255,255,255,0.2);
            border: 1px solid rgba(255,255,255,0.3);
            color: white;
            padding: 10px 20px;
            border-radius: 8px;
            cursor: pointer;
            font-weight: 500;
            transition: all 0.3s;
        }

        .header-btn:hover {
            background: rgba(255,255,255,0.3);
        }

        /* Hero Section */
        .hero {
            background: linear-gradient(135deg, #fa709a 0%, #fee140 25%, #30cfd0 50%, #a8edea 75%, #ff6a88 100%);
            padding: 60px 30px;
            color: white;
            position: relative;
            overflow: hidden;
            background-size: 400% 400%;
            animation: rainbowHero 12s ease infinite;
        }

        @keyframes rainbowHero {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url('data:image/svg+xml,<svg width="100" height="100" xmlns="http://www.w3.org/2000/svg"><circle cx="50" cy="50" r="40" fill="rgba(255,255,255,0.1)"/></svg>');
            opacity: 0.3;
            animation: pulse 4s ease infinite;
        }

        @keyframes pulse {
            0%, 100% { opacity: 0.3; }
            50% { opacity: 0.5; }
        }

        .hero-content {
            max-width: 1400px;
            margin: 0 auto;
            text-align: center;
            position: relative;
            z-index: 1;
        }

        .hero h2 {
            font-size: 3em;
            margin-bottom: 15px;
            font-weight: 700;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.2);
        }

        .hero p {
            font-size: 1.3em;
            opacity: 0.95;
            margin-bottom: 40px;
        }

        .search-box {
            background: white;
            border-radius: 15px;
            padding: 30px;
            box-shadow: 0 20px 60px rgba(0,0,0,0.2);
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            max-width: 1200px;
            margin: 0 auto;
        }

        .search-field {
            display: flex;
            flex-direction: column;
            gap: 8px;
        }

        .search-field label {
            color: #64748b;
            font-size: 0.9em;
            font-weight: 600;
        }

        .search-field input, .search-field select {
            padding: 15px;
            border: 2px solid #e2e8f0;
            border-radius: 10px;
            font-size: 1em;
            transition: all 0.3s;
        }

        .search-field input:focus, .search-field select:focus {
            outline: none;
            border-color: #3b82f6;
        }

        .search-btn {
            background: linear-gradient(135deg, #ff0844 0%, #ffb199 25%, #ffd89b 50%, #19dcea 75%, #b721ff 100%);
            color: white;
            border: none;
            padding: 15px 40px;
            border-radius: 10px;
            font-size: 1.1em;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
            align-self: flex-end;
            box-shadow: 0 4px 15px rgba(255, 8, 68, 0.4);
            background-size: 300% 300%;
            animation: rainbowButton 8s ease infinite;
        }

        @keyframes rainbowButton {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        .search-btn:hover {
            transform: translateY(-2px) scale(1.05);
            box-shadow: 0 10px 30px rgba(255, 8, 68, 0.5);
        }

        /* Container */
        .container {
            max-width: 1400px;
            margin: 0 auto;
            padding: 40px 30px;
            background: white;
            border-radius: 20px 20px 0 0;
            margin-top: -30px;
            position: relative;
            z-index: 10;
        }

        /* Bus Card */
        .bus-card {
            background: linear-gradient(145deg, #ffffff 0%, #f8fafc 100%);
            border-radius: 20px;
            padding: 30px;
            margin-bottom: 25px;
            box-shadow: 0 8px 25px rgba(0,0,0,0.1);
            border: 2px solid transparent;
            transition: all 0.3s;
            position: relative;
            overflow: hidden;
        }

        .bus-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 5px;
            background: linear-gradient(90deg, #ff0844 0%, #ffb199 14%, #ffd89b 28%, #30cfd0 42%, #19dcea 57%, #b721ff 71%, #f093fb 85%, #ff0844 100%);
            background-size: 200% 100%;
            animation: rainbowSlide 3s linear infinite;
        }

        @keyframes rainbowSlide {
            0% { background-position: 0% 0%; }
            100% { background-position: 200% 0%; }
        }

        .bus-card:hover {
            box-shadow: 0 12px 35px rgba(102, 126, 234, 0.2);
            transform: translateY(-5px);
            border-color: #667eea;
        }

        .bus-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 25px;
            padding-bottom: 20px;
            border-bottom: 2px solid #f1f5f9;
        }

        .bus-info h3 {
            font-size: 1.5em;
            color: #1e293b;
            margin-bottom: 8px;
        }

        .bus-type {
            display: inline-block;
            background: linear-gradient(135deg, #ff6a88 0%, #ffb199 25%, #ffd89b 50%, #a8edea 75%, #30cfd0 100%);
            color: #1e293b;
            padding: 6px 15px;
            border-radius: 20px;
            font-size: 0.85em;
            font-weight: 600;
            background-size: 200% 200%;
            animation: rainbowShimmer 5s ease infinite;
        }

        @keyframes rainbowShimmer {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        .bus-rating {
            text-align: right;
        }

        .rating-stars {
            color: #fbbf24;
            font-size: 1.2em;
            margin-bottom: 5px;
            text-shadow: 0 0 10px rgba(251, 191, 36, 0.6);
            animation: starGlow 2s ease-in-out infinite;
        }

        @keyframes starGlow {
            0%, 100% { text-shadow: 0 0 10px rgba(251, 191, 36, 0.6); }
            50% { text-shadow: 0 0 20px rgba(251, 191, 36, 0.9), 0 0 30px rgba(251, 191, 36, 0.6); }
        }

        .rating-count {
            color: #64748b;
            font-size: 0.9em;
        }

        .journey-details {
            display: grid;
            grid-template-columns: 1fr auto 1fr;
            gap: 30px;
            align-items: center;
            margin-bottom: 25px;
        }

        .journey-point {
            text-align: center;
        }

        .journey-time {
            font-size: 2em;
            font-weight: 700;
            color: #1e293b;
        }

        .journey-location {
            color: #64748b;
            margin-top: 5px;
            font-size: 1.1em;
        }

        .journey-duration {
            text-align: center;
            position: relative;
        }

        .duration-line {
            width: 100%;
            height: 2px;
            background: #cbd5e1;
            position: relative;
            margin: 15px 0;
        }

        .duration-line::before,
        .duration-line::after {
            content: '';
            position: absolute;
            width: 12px;
            height: 12px;
            background: linear-gradient(135deg, #ff0844 0%, #ffb199 50%, #19dcea 100%);
            border-radius: 50%;
            top: -5px;
            box-shadow: 0 0 15px rgba(255, 8, 68, 0.6);
            animation: dotPulse 2s ease-in-out infinite;
        }

        @keyframes dotPulse {
            0%, 100% { transform: scale(1); box-shadow: 0 0 15px rgba(255, 8, 68, 0.6); }
            50% { transform: scale(1.2); box-shadow: 0 0 25px rgba(255, 8, 68, 0.9); }
        }

        .duration-line::before {
            left: 0;
        }

        .duration-line::after {
            right: 0;
        }

        .duration-text {
            font-weight: 600;
            color: #64748b;
        }

        .amenities {
            display: flex;
            gap: 15px;
            flex-wrap: wrap;
            margin-bottom: 25px;
        }

        .amenity {
            display: flex;
            align-items: center;
            gap: 8px;
            padding: 8px 15px;
            background: linear-gradient(135deg, #ffecd2 0%, #fcb69f 25%, #ffd89b 50%, #a8edea 75%, #fed6e3 100%);
            border-radius: 20px;
            font-size: 0.9em;
            color: #7c2d12;
            font-weight: 500;
            box-shadow: 0 2px 8px rgba(252, 182, 159, 0.3);
            background-size: 200% 200%;
            animation: amenityShine 6s ease infinite;
        }

        @keyframes amenityShine {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        .bus-footer {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .price-section {
            display: flex;
            align-items: baseline;
            gap: 10px;
        }

        .price {
            font-size: 2.2em;
            font-weight: 700;
            background: linear-gradient(135deg, #ff0844 0%, #ffb199 20%, #ffd89b 40%, #30cfd0 60%, #b721ff 80%, #ff0844 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            background-size: 300% 300%;
            animation: rainbowText 5s linear infinite;
        }

        @keyframes rainbowText {
            0% { background-position: 0% 50%; }
            100% { background-position: 300% 50%; }
        }

        .price-label {
            color: #64748b;
            font-size: 0.95em;
        }

        .seats-available {
            color: #059669;
            font-weight: 600;
            margin-bottom: 5px;
            text-shadow: 0 1px 2px rgba(5, 150, 105, 0.2);
        }

        .view-seats-btn {
            background: linear-gradient(135deg, #ff0844 0%, #ffb199 25%, #ffd89b 50%, #19dcea 75%, #b721ff 100%);
            color: white;
            border: none;
            padding: 15px 40px;
            border-radius: 12px;
            font-size: 1.1em;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
            box-shadow: 0 4px 15px rgba(240, 147, 251, 0.4);
            background-size: 300% 300%;
            animation: rainbowButton 8s ease infinite;
        }

        .view-seats-btn:hover {
            transform: translateY(-3px) scale(1.05);
            box-shadow: 0 8px 25px rgba(240, 147, 251, 0.5);
        }

        /* Seat Selection Modal */
        .modal {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0,0,0,0.7);
            z-index: 2000;
            overflow-y: auto;
        }

        .modal.active {
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 20px;
        }

        .modal-content {
            background: white;
            border-radius: 20px;
            max-width: 1200px;
            width: 100%;
            max-height: 90vh;
            overflow-y: auto;
            box-shadow: 0 25px 80px rgba(0,0,0,0.3);
        }

        .modal-header {
            background: linear-gradient(135deg, #ff0844 0%, #ffb199 20%, #ffd89b 40%, #30cfd0 60%, #19dcea 80%, #b721ff 100%);
            color: white;
            padding: 30px;
            border-radius: 20px 20px 0 0;
            display: flex;
            justify-content: space-between;
            align-items: center;
            background-size: 300% 300%;
            animation: rainbowHeader 10s ease infinite;
        }

        @keyframes rainbowHeader {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        .close-modal {
            background: rgba(255,255,255,0.2);
            border: none;
            color: white;
            font-size: 2em;
            cursor: pointer;
            width: 45px;
            height: 45px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: all 0.3s;
        }

        .close-modal:hover {
            background: rgba(255,255,255,0.3);
        }

        .modal-body {
            padding: 40px;
        }

        .seat-layout-section {
            display: grid;
            grid-template-columns: 1fr 350px;
            gap: 40px;
        }

        .seat-legend {
            display: flex;
            gap: 25px;
            margin-bottom: 30px;
            flex-wrap: wrap;
        }

        .legend-item {
            display: flex;
            align-items: center;
            gap: 10px;
            font-weight: 500;
        }

        .legend-seat {
            width: 35px;
            height: 35px;
            border-radius: 6px;
            border: 2px solid;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 0.8em;
        }

        .legend-seat.available {
            background: white;
            border-color: #cbd5e1;
            color: #64748b;
        }

        .legend-seat.selected {
            background: linear-gradient(135deg, #ff0844 0%, #ffd89b 50%, #19dcea 100%);
            border-color: #ff0844;
            color: white;
        }

        .legend-seat.booked {
            background: #e2e8f0;
            border-color: #cbd5e1;
            color: #94a3b8;
        }

        .bus-layout {
            background: #f8fafc;
            padding: 25px;
            border-radius: 15px;
            border: 2px solid #e2e8f0;
        }

        .deck-label {
            font-weight: 600;
            color: #1e293b;
            margin-bottom: 15px;
            font-size: 1.05em;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .deck-info {
            font-size: 0.85em;
            color: #64748b;
            font-weight: 500;
        }

        .seats-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 8px;
            margin-bottom: 20px;
        }

        .seat {
            width: 45px;
            height: 45px;
            border: 2px solid #cbd5e1;
            border-radius: 6px;
            background: white;
            cursor: pointer;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 600;
            font-size: 0.85em;
            transition: all 0.3s;
            color: #64748b;
        }

        .seat:hover:not(.booked):not(.driver) {
            transform: scale(1.08);
            border-color: #3b82f6;
        }

        .seat.selected {
            background: linear-gradient(135deg, #ff0844 0%, #ffb199 33%, #ffd89b 66%, #19dcea 100%);
            border-color: #ff0844;
            color: white;
            transform: scale(1.05);
            box-shadow: 0 4px 12px rgba(255, 8, 68, 0.6);
            animation: seatPulse 1.5s ease-in-out infinite;
        }

        @keyframes seatPulse {
            0%, 100% { box-shadow: 0 4px 12px rgba(255, 8, 68, 0.6); }
            50% { box-shadow: 0 6px 20px rgba(255, 8, 68, 0.9); }
        }

        .seat.booked {
            background: #e2e8f0;
            border-color: #cbd5e1;
            color: #94a3b8;
            cursor: not-allowed;
        }

        .seat.driver {
            background: #1e293b;
            color: white;
            cursor: default;
            font-size: 1.2em;
        }

        .seat.empty {
            background: transparent;
            border: none;
            cursor: default;
        }

        .booking-summary {
            background: #f8fafc;
            padding: 30px;
            border-radius: 15px;
            border: 2px solid #e2e8f0;
            position: sticky;
            top: 20px;
        }

        .summary-title {
            font-size: 1.4em;
            font-weight: 700;
            color: #1e293b;
            margin-bottom: 20px;
        }

        .summary-row {
            display: flex;
            justify-content: space-between;
            padding: 15px 0;
            border-bottom: 1px solid #e2e8f0;
        }

        .summary-row:last-child {
            border-bottom: none;
        }

        .summary-label {
            color: #64748b;
        }

        .summary-value {
            font-weight: 600;
            color: #1e293b;
        }

        .selected-seats {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
        }

        .seat-badge {
            background: linear-gradient(135deg, #ff0844 0%, #ffb199 25%, #ffd89b 50%, #30cfd0 75%, #b721ff 100%);
            color: white;
            padding: 6px 12px;
            border-radius: 8px;
            font-size: 0.9em;
            font-weight: 600;
            box-shadow: 0 2px 8px rgba(240, 147, 251, 0.3);
            background-size: 200% 200%;
            animation: badgeShimmer 4s ease infinite;
        }

        @keyframes badgeShimmer {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        .total-amount {
            background: linear-gradient(135deg, #ff0844 0%, #ffb199 20%, #ffd89b 40%, #30cfd0 60%, #19dcea 80%, #b721ff 100%);
            color: white;
            padding: 20px;
            border-radius: 12px;
            margin: 20px 0;
            text-align: center;
            box-shadow: 0 8px 20px rgba(255, 8, 68, 0.4);
            background-size: 300% 300%;
            animation: totalAmountGlow 8s ease infinite;
        }

        @keyframes totalAmountGlow {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        .total-label {
            font-size: 0.9em;
            opacity: 0.8;
            margin-bottom: 5px;
        }

        .total-price {
            font-size: 2.5em;
            font-weight: 700;
        }

        .proceed-btn {
            width: 100%;
            background: linear-gradient(135deg, #ff0844 0%, #ffb199 20%, #ffd89b 40%, #30cfd0 60%, #19dcea 80%, #b721ff 100%);
            color: white;
            border: none;
            padding: 18px;
            border-radius: 12px;
            font-size: 1.2em;
            font-weight: 700;
            cursor: pointer;
            transition: all 0.3s;
            box-shadow: 0 6px 20px rgba(250, 112, 154, 0.4);
            background-size: 300% 300%;
            animation: proceedRainbow 8s ease infinite;
        }

        @keyframes proceedRainbow {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        .proceed-btn:hover:not(:disabled) {
            transform: translateY(-3px) scale(1.02);
            box-shadow: 0 10px 30px rgba(250, 112, 154, 0.6);
        }

        .proceed-btn:disabled {
            background: #cbd5e1;
            cursor: not-allowed;
        }

        .travel-tab {
            background: rgba(255,255,255,0.2);
            border: 2px solid rgba(255,255,255,0.3);
            color: white;
            padding: 15px 35px;
            border-radius: 12px;
            font-size: 1.1em;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
            backdrop-filter: blur(10px);
        }

        .travel-tab:hover {
            background: rgba(255,255,255,0.3);
            transform: translateY(-2px);
            box-shadow: 0 4px 12px rgba(255,255,255,0.2);
        }

        .travel-tab.active {
            background: white;
            color: #ff0844;
            border-color: white;
            box-shadow: 0 4px 15px rgba(255, 255, 255, 0.5);
            font-weight: 700;
        }

        .flight-class, .train-class {
            display: inline-block;
            background: linear-gradient(135deg, #ffecd2 0%, #fcb69f 33%, #ffd89b 66%, #a8edea 100%);
            color: #7c2d12;
            padding: 6px 15px;
            border-radius: 20px;
            font-size: 0.85em;
            font-weight: 600;
            background-size: 200% 200%;
            animation: classShimmer 5s ease infinite;
        }

        @keyframes classShimmer {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        .hotel-badge {
            display: inline-block;
            background: linear-gradient(135deg, #a8edea 0%, #fed6e3 33%, #ffd89b 66%, #ffb199 100%);
            color: #1e293b;
            padding: 6px 15px;
            border-radius: 20px;
            font-size: 0.85em;
            font-weight: 600;
            margin-right: 8px;
            background-size: 200% 200%;
            animation: hotelBadgeGlow 5s ease infinite;
        }

        @keyframes hotelBadgeGlow {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        .hotel-image {
            width: 100%;
            height: 250px;
            object-fit: cover;
            border-radius: 12px;
            margin-bottom: 20px;
        }

        .hotel-features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
            gap: 15px;
            margin: 20px 0;
        }

        .feature-box {
            background: #f8fafc;
            padding: 15px;
            border-radius: 10px;
            text-align: center;
            border: 1px solid #e2e8f0;
        }

        .feature-icon {
            font-size: 2em;
            margin-bottom: 8px;
        }

        .feature-label {
            font-size: 0.9em;
            color: #64748b;
            font-weight: 600;
        }

        .hotel-location {
            color: #64748b;
            margin: 10px 0;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .night-price {
            font-size: 0.9em;
            color: #64748b;
        }

        .flight-logo {
            width: 50px;
            height: 50px;
            background: #f1f5f9;
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.8em;
            margin-right: 15px;
        }

        @media (max-width: 968px) {
            .seat-layout-section {
                grid-template-columns: 1fr;
            }

            .booking-summary {
                position: static;
            }

            .hero h2 {
                font-size: 2em;
            }

            .search-box {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header class="header">
        <div class="header-content">
            <div class="logo-section">
                <div class="logo">🚌</div>
                <div class="brand-name">
                    <h1>Gangadhar Experience Line</h1>
                    <p>Premium Travel, Trusted Service</p>
                </div>
            </div>
            <div class="header-actions">
                <button class="header-btn" onclick="showMyBookings()">My Bookings</button>
                <button class="header-btn">Login</button>
            </div>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="heroSection">
        <div class="hero-content">
            <h2>Your Journey, Our Priority</h2>
            <p>Book Buses, Trains & Flights with India's most trusted travel partner</p>
            
            <!-- Travel Mode Tabs -->
            <div style="display: flex; gap: 15px; justify-content: center; margin-bottom: 30px; flex-wrap: wrap;">
                <button class="travel-tab active" onclick="switchTravelMode('bus')" id="busTab">
                    🚌 Buses
                </button>
                <button class="travel-tab" onclick="switchTravelMode('train')" id="trainTab">
                    🚆 Trains
                </button>
                <button class="travel-tab" onclick="switchTravelMode('flight')" id="flightTab">
                    ✈️ Flights
                </button>
                <button class="travel-tab" onclick="switchTravelMode('hotel')" id="hotelTab">
                    🏨 Hotels
                </button>
            </div>

            <div class="search-box" id="transportSearch">
                <div class="search-field">
                    <label>From</label>
                    <select id="fromCity" style="width: 100%; padding: 15px; border: 2px solid #e2e8f0; border-radius: 10px; font-size: 1em;">
                        <option value="Bangalore">Bangalore</option>
                        <option value="Mumbai">Mumbai</option>
                        <option value="Delhi">Delhi</option>
                        <option value="Chennai">Chennai</option>
                        <option value="Hyderabad">Hyderabad</option>
                        <option value="Pune">Pune</option>
                        <option value="Kolkata">Kolkata</option>
                        <option value="Ahmedabad">Ahmedabad</option>
                        <option value="Jaipur">Jaipur</option>
                        <option value="Goa">Goa</option>
                    </select>
                </div>
                <div class="search-field">
                    <label>To</label>
                    <select id="toCity" style="width: 100%; padding: 15px; border: 2px solid #e2e8f0; border-radius: 10px; font-size: 1em;">
                        <option value="Mumbai">Mumbai</option>
                        <option value="Bangalore">Bangalore</option>
                        <option value="Delhi">Delhi</option>
                        <option value="Chennai">Chennai</option>
                        <option value="Hyderabad">Hyderabad</option>
                        <option value="Pune">Pune</option>
                        <option value="Kolkata">Kolkata</option>
                        <option value="Ahmedabad">Ahmedabad</option>
                        <option value="Jaipur">Jaipur</option>
                        <option value="Goa">Goa</option>
                    </select>
                </div>
                <div class="search-field">
                    <label>Journey Date</label>
                    <input type="date" value="2025-11-05" id="journeyDate">
                </div>
                <div class="search-field" id="returnDateField" style="display: none;">
                    <label>Return Date</label>
                    <input type="date" value="2025-11-12" id="returnDate">
                </div>
                <button class="search-btn" onclick="searchResults()">
                    <span id="searchBtnText">Search Buses</span>
                </button>
            </div>

            <!-- Hotel Search Box -->
            <div class="search-box" id="hotelSearch" style="display: none;">
                <div class="search-field">
                    <label>City / Location</label>
                    <select id="hotelCity" style="width: 100%; padding: 15px; border: 2px solid #e2e8f0; border-radius: 10px; font-size: 1em;">
                        <option value="Mumbai">Mumbai</option>
                        <option value="Bangalore">Bangalore</option>
                        <option value="Delhi">Delhi</option>
                        <option value="Chennai">Chennai</option>
                        <option value="Hyderabad">Hyderabad</option>
                        <option value="Pune">Pune</option>
                        <option value="Kolkata">Kolkata</option>
                        <option value="Ahmedabad">Ahmedabad</option>
                        <option value="Jaipur">Jaipur</option>
                        <option value="Goa">Goa</option>
                        <option value="Udaipur">Udaipur</option>
                        <option value="Agra">Agra</option>
                    </select>
                </div>
                <div class="search-field">
                    <label>Check-in Date</label>
                    <input type="date" value="2025-11-05" id="checkInDate">
                </div>
                <div class="search-field">
                    <label>Check-out Date</label>
                    <input type="date" value="2025-11-07" id="checkOutDate">
                </div>
                <div class="search-field">
                    <label>Rooms & Guests</label>
                    <select id="roomsGuests" style="width: 100%; padding: 15px; border: 2px solid #e2e8f0; border-radius: 10px; font-size: 1em;">
                        <option value="1-1">1 Room, 1 Guest</option>
                        <option value="1-2">1 Room, 2 Guests</option>
                        <option value="1-3">1 Room, 3 Guests</option>
                        <option value="2-4">2 Rooms, 4 Guests</option>
                        <option value="3-6">3 Rooms, 6 Guests</option>
                    </select>
                </div>
                <button class="search-btn" onclick="searchResults()">
                    Search Hotels
                </button>
            </div>
        </div>
    </section>

    <!-- Bus Listings -->
    <div class="container" id="busListings">
        <div class="bus-card">
            <div class="bus-header">
                <div class="bus-info">
                    <h3>Gangadhar Volvo Multi-Axle</h3>
                    <span class="bus-type">AC Sleeper (2+1)</span>
                </div>
                <div class="bus-rating">
                    <div class="rating-stars">★★★★★</div>
                    <div class="rating-count">4.8 (2,450 ratings)</div>
                </div>
            </div>

            <div class="journey-details">
                <div class="journey-point">
                    <div class="journey-time">22:30</div>
                    <div class="journey-location" id="busFrom1">Bangalore</div>
                </div>
                <div class="journey-duration">
                    <div class="duration-line"></div>
                    <div class="duration-text" id="busDuration1">14h 30m</div>
                </div>
                <div class="journey-point">
                    <div class="journey-time">13:00</div>
                    <div class="journey-location" id="busTo1">Mumbai</div>
                </div>
            </div>

            <div class="amenities">
                <div class="amenity">❄️ Air Conditioning</div>
                <div class="amenity">📺 Entertainment</div>
                <div class="amenity">🔌 Charging Point</div>
                <div class="amenity">💺 Reclining Seats</div>
                <div class="amenity">🛏️ Sleeper Berths</div>
                <div class="amenity">🚻 Clean Washroom</div>
            </div>

            <div class="bus-footer">
                <div>
                    <div class="seats-available">18 seats available</div>
                    <div class="price-section">
                        <span class="price" id="busPrice1">₹1,000</span>
                        <span class="price-label">onwards</span>
                    </div>
                </div>
                <button class="view-seats-btn" onclick="openSeatModal()">View Seats</button>
            </div>
        </div>

        <div class="bus-card">
            <div class="bus-header">
                <div class="bus-info">
                    <h3>Gangadhar Express Deluxe</h3>
                    <span class="bus-type">Semi-Sleeper</span>
                </div>
                <div class="bus-rating">
                    <div class="rating-stars">★★★★☆</div>
                    <div class="rating-count">4.5 (1,890 ratings)</div>
                </div>
            </div>

            <div class="journey-details">
                <div class="journey-point">
                    <div class="journey-time">20:00</div>
                    <div class="journey-location" id="busFrom2">Bangalore</div>
                </div>
                <div class="journey-duration">
                    <div class="duration-line"></div>
                    <div class="duration-text" id="busDuration2">15h 00m</div>
                </div>
                <div class="journey-point">
                    <div class="journey-time">11:00</div>
                    <div class="journey-location" id="busTo2">Mumbai</div>
                </div>
            </div>

            <div class="amenities">
                <div class="amenity">❄️ Air Conditioning</div>
                <div class="amenity">🔌 Charging Point</div>
                <div class="amenity">💺 Reclining Seats</div>
                <div class="amenity">📱 WiFi</div>
            </div>

            <div class="bus-footer">
                <div>
                    <div class="seats-available">25 seats available</div>
                    <div class="price-section">
                        <span class="price" id="busPrice2">₹700</span>
                        <span class="price-label">onwards</span>
                    </div>
                </div>
                <button class="view-seats-btn" onclick="openSeatModal()">View Seats</button>
            </div>
        </div>

        <div class="bus-card">
            <div class="bus-header">
                <div class="bus-info">
                    <h3>Gangadhar Luxury Coach</h3>
                    <span class="bus-type">AC Seater (2+2)</span>
                </div>
                <div class="bus-rating">
                    <div class="rating-stars">★★★★☆</div>
                    <div class="rating-count">4.4 (1,200 ratings)</div>
                </div>
            </div>

            <div class="journey-details">
                <div class="journey-point">
                    <div class="journey-time">06:00</div>
                    <div class="journey-location" id="busFrom3">Bangalore</div>
                </div>
                <div class="journey-duration">
                    <div class="duration-line"></div>
                    <div class="duration-text" id="busDuration3">12h 30m</div>
                </div>
                <div class="journey-point">
                    <div class="journey-time">18:30</div>
                    <div class="journey-location" id="busTo3">Mumbai</div>
                </div>
            </div>

            <div class="amenities">
                <div class="amenity">❄️ Air Conditioning</div>
                <div class="amenity">🔌 Charging Point</div>
                <div class="amenity">💺 Push Back Seats</div>
                <div class="amenity">📱 WiFi</div>
                <div class="amenity">🍽️ Snacks</div>
            </div>

            <div class="bus-footer">
                <div>
                    <div class="seats-available">32 seats available</div>
                    <div class="price-section">
                        <span class="price" id="busPrice3">₹550</span>
                        <span class="price-label">onwards</span>
                    </div>
                </div>
                <button class="view-seats-btn" onclick="openSeatModal()">View Seats</button>
            </div>
        </div>
    </div>

    <!-- My Bookings Section -->
    <div class="container" id="myBookingsSection" style="display: none;">
        <div style="margin-bottom: 30px;">
            <h2 style="color: #1e293b; font-size: 2em; margin-bottom: 10px;">My Bookings</h2>
            <p style="color: #64748b;">View and manage all your travel bookings</p>
        </div>

        <div id="bookingsList">
            <!-- Bookings will be dynamically added here -->
        </div>
    </div>

    <!-- Booking Details Modal -->
    <div class="modal" id="bookingDetailsModal">
        <div class="modal-content" style="max-width: 800px;">
            <div class="modal-header">
                <div>
                    <h2>Booking Details</h2>
                    <p>Complete information about your booking</p>
                </div>
                <button class="close-modal" onclick="closeBookingDetails()">×</button>
            </div>
            <div class="modal-body">
                <div id="bookingDetailsContent"></div>
            </div>
        </div>
    </div>

    <!-- Hotel Listings -->
    <div class="container" id="hotelListings" style="display: none;">
        <div class="bus-card">
            <img src="https://images.unsplash.com/photo-1566073771259-6a8506099945?w=800&h=400&fit=crop" alt="Hotel" class="hotel-image" onerror="this.src='data:image/svg+xml,%3Csvg xmlns=%22http://www.w3.org/2000/svg%22 width=%22800%22 height=%22400%22%3E%3Crect fill=%22%23ddd%22 width=%22800%22 height=%22400%22/%3E%3Ctext x=%2250%25%22 y=%2250%25%22 text-anchor=%22middle%22 dy=%22.3em%22 fill=%22%23999%22 font-size=%2224%22%3ELuxury Hotel%3C/text%3E%3C/svg%3E'">
            <div class="bus-header">
                <div class="bus-info">
                    <h3>The Grand Taj Palace</h3>
                    <div class="hotel-location">
                        📍 Colaba, South Mumbai • 2.5 km from Gateway of India
                    </div>
                    <div style="margin-top: 10px;">
                        <span class="hotel-badge">5 Star</span>
                        <span class="hotel-badge">Luxury</span>
                        <span class="hotel-badge">Sea View</span>
                    </div>
                </div>
                <div class="bus-rating">
                    <div class="rating-stars">★★★★★</div>
                    <div class="rating-count">4.9 (5,600 ratings)</div>
                    <div style="margin-top: 8px; font-size: 0.95em; color: #16a34a; font-weight: 600;">Excellent</div>
                </div>
            </div>

            <div class="hotel-features">
                <div class="feature-box">
                    <div class="feature-icon">🏊</div>
                    <div class="feature-label">Swimming Pool</div>
                </div>
                <div class="feature-box">
                    <div class="feature-icon">🍽️</div>
                    <div class="feature-label">Restaurant</div>
                </div>
                <div class="feature-box">
                    <div class="feature-icon">💪</div>
                    <div class="feature-label">Gym & Spa</div>
                </div>
                <div class="feature-box">
                    <div class="feature-icon">🅿️</div>
                    <div class="feature-label">Free Parking</div>
                </div>
                <div class="feature-box">
                    <div class="feature-icon">📱</div>
                    <div class="feature-label">Free WiFi</div>
                </div>
                <div class="feature-box">
                    <div class="feature-icon">🛎️</div>
                    <div class="feature-label">Room Service</div>
                </div>
            </div>

            <div class="amenities">
                <div class="amenity">❄️ Air Conditioning</div>
                <div class="amenity">📺 Smart TV</div>
                <div class="amenity">☕ Mini Bar</div>
                <div class="amenity">🛁 Jacuzzi</div>
                <div class="amenity">🧺 Laundry Service</div>
                <div class="amenity">🚖 Airport Transfer</div>
            </div>

            <div class="bus-footer">
                <div>
                    <div class="seats-available">Only 3 rooms left at this price!</div>
                    <div class="price-section">
                        <span class="price">₹8,500</span>
                        <span class="night-price">per night + taxes</span>
                    </div>
                </div>
                <button class="view-seats-btn" onclick="bookHotel('The Grand Taj Palace', 8500)">Book Now</button>
            </div>
        </div>

        <div class="bus-card">
            <img src="https://images.unsplash.com/photo-1542314831-068cd1dbfeeb?w=800&h=400&fit=crop" alt="Hotel" class="hotel-image" onerror="this.src='data:image/svg+xml,%3Csvg xmlns=%22http://www.w3.org/2000/svg%22 width=%22800%22 height=%22400%22%3E%3Crect fill=%22%23ddd%22 width=%22800%22 height=%22400%22/%3E%3Ctext x=%2250%25%22 y=%2250%25%22 text-anchor=%22middle%22 dy=%22.3em%22 fill=%22%23999%22 font-size=%2224%22%3EBoutique Hotel%3C/text%3E%3C/svg%3E'">
            <div class="bus-header">
                <div class="bus-info">
                    <h3>Oberoi Trident Business Hotel</h3>
                    <div class="hotel-location">
                        📍 Nariman Point, Mumbai • 1 km from Marine Drive
                    </div>
                    <div style="margin-top: 10px;">
                        <span class="hotel-badge">4 Star</span>
                        <span class="hotel-badge">Business Hotel</span>
                        <span class="hotel-badge">City View</span>
                    </div>
                </div>
                <div class="bus-rating">
                    <div class="rating-stars">★★★★☆</div>
                    <div class="rating-count">4.6 (3,850 ratings)</div>
                    <div style="margin-top: 8px; font-size: 0.95em; color: #16a34a; font-weight: 600;">Very Good</div>
                </div>
            </div>

            <div class="hotel-features">
                <div class="feature-box">
                    <div class="feature-icon">💼</div>
                    <div class="feature-label">Business Center</div>
                </div>
                <div class="feature-box">
                    <div class="feature-icon">🍽️</div>
                    <div class="feature-label">Breakfast Included</div>
                </div>
                <div class="feature-box">
                    <div class="feature-icon">🏋️</div>
                    <div class="feature-label">Fitness Center</div>
                </div>
                <div class="feature-box">
                    <div class="feature-icon">🅿️</div>
                    <div class="feature-label">Parking</div>
                </div>
                <div class="feature-box">
                    <div class="feature-icon">📱</div>
                    <div class="feature-label">Free WiFi</div>
                </div>
                <div class="feature-box">
                    <div class="feature-icon">🛎️</div>
                    <div class="feature-label">24/7 Concierge</div>
                </div>
            </div>

            <div class="amenities">
                <div class="amenity">❄️ Air Conditioning</div>
                <div class="amenity">📺 LED TV</div>
                <div class="amenity">☕ Tea/Coffee Maker</div>
                <div class="amenity">🛏️ King Size Bed</div>
                <div class="amenity">🧺 Daily Housekeeping</div>
                <div class="amenity">🔒 Safe Deposit Box</div>
            </div>

            <div class="bus-footer">
                <div>
                    <div class="seats-available">12 rooms available</div>
                    <div class="price-section">
                        <span class="price">₹5,200</span>
                        <span class="night-price">per night + taxes</span>
                    </div>
                </div>
                <button class="view-seats-btn" onclick="bookHotel('Oberoi Trident Business Hotel', 5200)">Book Now</button>
            </div>
        </div>

        <div class="bus-card">
            <img src="https://images.unsplash.com/photo-1551882547-ff40c63fe5fa?w=800&h=400&fit=crop" alt="Hotel" class="hotel-image" onerror="this.src='data:image/svg+xml,%3Csvg xmlns=%22http://www.w3.org/2000/svg%22 width=%22800%22 height=%22400%22%3E%3Crect fill=%22%23ddd%22 width=%22800%22 height=%22400%22/%3E%3Ctext x=%2250%25%22 y=%2250%25%22 text-anchor=%22middle%22 dy=%22.3em%22 fill=%22%23999%22 font-size=%2224%22%3EBudget Hotel%3C/text%3E%3C/svg%3E'">
            <div class="bus-header">
                <div class="bus-info">
                    <h3>FabHotel Prime Comfort Inn</h3>
                    <div class="hotel-location">
                        📍 Andheri East, Mumbai • 5 km from Airport
                    </div>
                    <div style="margin-top: 10px;">
                        <span class="hotel-badge">3 Star</span>
                        <span class="hotel-badge">Budget Friendly</span>
                        <span class="hotel-badge">Near Airport</span>
                    </div>
                </div>
                <div class="bus-rating">
                    <div class="rating-stars">★★★★☆</div>
                    <div class="rating-count">4.3 (2,240 ratings)</div>
                    <div style="margin-top: 8px; font-size: 0.95em; color: #16a34a; font-weight: 600;">Good</div>
                </div>
            </div>

            <div class="hotel-features">
                <div class="feature-box">
                    <div class="feature-icon">🍽️</div>
                    <div class="feature-label">Complimentary Breakfast</div>
                </div>
                <div class="feature-box">
                    <div class="feature-icon">🅿️</div>
                    <div class="feature-label">Free Parking</div>
                </div>
                <div class="feature-box">
                    <div class="feature-icon">📱</div>
                    <div class="feature-label">Free WiFi</div>
                </div>
                <div class="feature-box">
                    <div class="feature-icon">🛎️</div>
                    <div class="feature-label">Front Desk</div>
                </div>
                <div class="feature-box">
                    <div class="feature-icon">🚖</div>
                    <div class="feature-label">Airport Shuttle</div>
                </div>
                <div class="feature-box">
                    <div class="feature-icon">🧳</div>
                    <div class="feature-label">Luggage Storage</div>
                </div>
            </div>

            <div class="amenities">
                <div class="amenity">❄️ Air Conditioning</div>
                <div class="amenity">📺 TV</div>
                <div class="amenity">🚿 Hot Water</div>
                <div class="amenity">🛏️ Comfortable Beds</div>
                <div class="amenity">🧺 Laundry</div>
                <div class="amenity">☕ In-room Dining</div>
            </div>

            <div class="bus-footer">
                <div>
                    <div class="seats-available">18 rooms available</div>
                    <div class="price-section">
                        <span class="price">₹2,800</span>
                        <span class="night-price">per night + taxes</span>
                    </div>
                </div>
                <button class="view-seats-btn" onclick="bookHotel('FabHotel Prime Comfort Inn', 2800)">Book Now</button>
            </div>
        </div>
    </div>

    <!-- Train Listings -->
    <div class="container" id="trainListings" style="display: none;">
        <div class="bus-card">
            <div class="bus-header">
                <div class="bus-info">
                    <div style="display: flex; align-items: center;">
                        <div class="flight-logo">🚆</div>
                        <div>
                            <h3>Udyan Express (11301)</h3>
                            <span class="train-class">3AC • 2AC • 1AC</span>
                        </div>
                    </div>
                </div>
                <div class="bus-rating">
                    <div class="rating-stars">★★★★☆</div>
                    <div class="rating-count">4.6 (3,200 ratings)</div>
                </div>
            </div>

            <div class="journey-details">
                <div class="journey-point">
                    <div class="journey-time">07:40</div>
                    <div class="journey-location">Bangalore (SBC)</div>
                </div>
                <div class="journey-duration">
                    <div class="duration-line"></div>
                    <div class="duration-text">23h 55m</div>
                </div>
                <div class="journey-point">
                    <div class="journey-time">07:35</div>
                    <div class="journey-location">Mumbai (CSMT)</div>
                </div>
            </div>

            <div class="amenities">
                <div class="amenity">🍽️ Pantry Service</div>
                <div class="amenity">🔌 Charging Point</div>
                <div class="amenity">🛏️ Berths Available</div>
                <div class="amenity">❄️ Air Conditioning</div>
                <div class="amenity">🚻 Clean Washrooms</div>
            </div>

            <div class="bus-footer">
                <div>
                    <div class="seats-available">Available: 3AC (24) • 2AC (15) • 1AC (8)</div>
                    <div class="price-section">
                        <span class="price">₹850</span>
                        <span class="price-label">3AC onwards</span>
                    </div>
                </div>
                <button class="view-seats-btn" onclick="openSeatModal()">Check Availability</button>
            </div>
        </div>

        <div class="bus-card">
            <div class="bus-header">
                <div class="bus-info">
                    <div style="display: flex; align-items: center;">
                        <div class="flight-logo">🚆</div>
                        <div>
                            <h3>Rajdhani Express (12430)</h3>
                            <span class="train-class">2AC • 1AC</span>
                        </div>
                    </div>
                </div>
                <div class="bus-rating">
                    <div class="rating-stars">★★★★★</div>
                    <div class="rating-count">4.9 (5,600 ratings)</div>
                </div>
            </div>

            <div class="journey-details">
                <div class="journey-point">
                    <div class="journey-time">20:00</div>
                    <div class="journey-location">Bangalore (SBC)</div>
                </div>
                <div class="journey-duration">
                    <div class="duration-line"></div>
                    <div class="duration-text">17h 15m</div>
                </div>
                <div class="journey-point">
                    <div class="journey-time">13:15</div>
                    <div class="journey-location">Mumbai (CSMT)</div>
                </div>
            </div>

            <div class="amenities">
                <div class="amenity">🍽️ Meals Included</div>
                <div class="amenity">🔌 Charging Point</div>
                <div class="amenity">🛏️ Premium Berths</div>
                <div class="amenity">❄️ Air Conditioning</div>
                <div class="amenity">📱 WiFi</div>
                <div class="amenity">📰 Newspapers</div>
            </div>

            <div class="bus-footer">
                <div>
                    <div class="seats-available">Available: 2AC (20) • 1AC (12)</div>
                    <div class="price-section">
                        <span class="price">₹1,450</span>
                        <span class="price-label">2AC onwards</span>
                    </div>
                </div>
                <button class="view-seats-btn" onclick="openSeatModal()">Check Availability</button>
            </div>
        </div>
    </div>

    <!-- Flight Listings -->
    <div class="container" id="flightListings" style="display: none;">
        <div class="bus-card">
            <div class="bus-header">
                <div class="bus-info">
                    <div style="display: flex; align-items: center;">
                        <div class="flight-logo">✈️</div>
                        <div>
                            <h3>IndiGo • 6E-5314</h3>
                            <span class="flight-class">Economy • Business</span>
                        </div>
                    </div>
                </div>
                <div class="bus-rating">
                    <div class="rating-stars">★★★★☆</div>
                    <div class="rating-count">4.5 (8,900 ratings)</div>
                </div>
            </div>

            <div class="journey-details">
                <div class="journey-point">
                    <div class="journey-time">06:30</div>
                    <div class="journey-location">Bangalore (BLR)</div>
                </div>
                <div class="journey-duration">
                    <div class="duration-line"></div>
                    <div class="duration-text">1h 45m • Non-stop</div>
                </div>
                <div class="journey-point">
                    <div class="journey-time">08:15</div>
                    <div class="journey-location">Mumbai (BOM)</div>
                </div>
            </div>

            <div class="amenities">
                <div class="amenity">🎒 7kg Cabin Bag</div>
                <div class="amenity">💼 15kg Check-in</div>
                <div class="amenity">🍽️ Paid Meals</div>
                <div class="amenity">💺 Standard Seats</div>
                <div class="amenity">🔌 USB Charging</div>
            </div>

            <div class="bus-footer">
                <div>
                    <div class="seats-available">12 seats left at this price</div>
                    <div class="price-section">
                        <span class="price">₹4,250</span>
                        <span class="price-label">per person</span>
                    </div>
                </div>
                <button class="view-seats-btn" onclick="openSeatModal()">Book Now</button>
            </div>
        </div>

        <div class="bus-card">
            <div class="bus-header">
                <div class="bus-info">
                    <div style="display: flex; align-items: center;">
                        <div class="flight-logo">✈️</div>
                        <div>
                            <h3>Air India • AI-503</h3>
                            <span class="flight-class">Economy • Business</span>
                        </div>
                    </div>
                </div>
                <div class="bus-rating">
                    <div class="rating-stars">★★★★★</div>
                    <div class="rating-count">4.7 (6,400 ratings)</div>
                </div>
            </div>

            <div class="journey-details">
                <div class="journey-point">
                    <div class="journey-time">14:20</div>
                    <div class="journey-location">Bangalore (BLR)</div>
                </div>
                <div class="journey-duration">
                    <div class="duration-line"></div>
                    <div class="duration-text">1h 50m • Non-stop</div>
                </div>
                <div class="journey-point">
                    <div class="journey-time">16:10</div>
                    <div class="journey-location">Mumbai (BOM)</div>
                </div>
            </div>

            <div class="amenities">
                <div class="amenity">🎒 7kg Cabin Bag</div>
                <div class="amenity">💼 25kg Check-in</div>
                <div class="amenity">🍽️ Complimentary Meals</div>
                <div class="amenity">💺 Reclining Seats</div>
                <div class="amenity">📺 Entertainment</div>
                <div class="amenity">📱 WiFi</div>
            </div>

            <div class="bus-footer">
                <div>
                    <div class="seats-available">18 seats available</div>
                    <div class="price-section">
                        <span class="price">₹5,890</span>
                        <span class="price-label">per person</span>
                    </div>
                </div>
                <button class="view-seats-btn" onclick="openSeatModal()">Book Now</button>
            </div>
        </div>

        <div class="bus-card">
            <div class="bus-header">
                <div class="bus-info">
                    <div style="display: flex; align-items: center;">
                        <div class="flight-logo">✈️</div>
                        <div>
                            <h3>Vistara • UK-864</h3>
                            <span class="flight-class">Premium Economy • Business</span>
                        </div>
                    </div>
                </div>
                <div class="bus-rating">
                    <div class="rating-stars">★★★★★</div>
                    <div class="rating-count">4.9 (12,300 ratings)</div>
                </div>
            </div>

            <div class="journey-details">
                <div class="journey-point">
                    <div class="journey-time">19:45</div>
                    <div class="journey-location">Bangalore (BLR)</div>
                </div>
                <div class="journey-duration">
                    <div class="duration-line"></div>
                    <div class="duration-text">1h 40m • Non-stop</div>
                </div>
                <div class="journey-point">
                    <div class="journey-time">21:25</div>
                    <div class="journey-location">Mumbai (BOM)</div>
                </div>
            </div>

            <div class="amenities">
                <div class="amenity">🎒 10kg Cabin Bag</div>
                <div class="amenity">💼 30kg Check-in</div>
                <div class="amenity">🍽️ Gourmet Meals</div>
                <div class="amenity">💺 Premium Seats</div>
                <div class="amenity">📺 Entertainment</div>
                <div class="amenity">📱 WiFi</div>
                <div class="amenity">🎧 Noise Cancelling</div>
            </div>

            <div class="bus-footer">
                <div>
                    <div class="seats-available">Only 6 seats left!</div>
                    <div class="price-section">
                        <span class="price">₹7,650</span>
                        <span class="price-label">per person</span>
                    </div>
                </div>
                <button class="view-seats-btn" onclick="openSeatModal()">Book Now</button>
            </div>
        </div>
    </div>

    <!-- Seat Selection Modal -->
    <div class="modal" id="seatModal">
        <div class="modal-content">
            <div class="modal-header">
                <div>
                    <h2>Select Your Seats</h2>
                    <p>Bangalore → Mumbai | 05 Nov 2025 | 22:30</p>
                </div>
                <button class="close-modal" onclick="closeSeatModal()">×</button>
            </div>
            <div class="modal-body">
                <div class="seat-legend">
                    <div class="legend-item">
                        <div class="legend-seat available">1</div>
                        <span>Available</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-seat selected">1</div>
                        <span>Selected</span>
                    </div>
                    <div class="legend-item">
                        <div class="legend-seat booked">1</div>
                        <span>Booked</span>
                    </div>
                </div>

                <div class="seat-layout-section">
                    <div>
                        <div class="bus-layout">
                            <div class="deck-label">
                                <span>Lower Deck</span>
                                <span class="deck-info">Seats 1-20</span>
                            </div>
                            <div style="display: flex; gap: 15px; align-items: flex-start;">
                                <div style="flex: 1;">
                                    <div style="text-align: center; font-size: 0.75em; color: #64748b; margin-bottom: 8px; font-weight: 600;">Left Side</div>
                                    <div class="seats-grid" id="lowerDeckLeft" style="grid-template-columns: repeat(2, 1fr);"></div>
                                </div>
                                <div style="width: 40px; display: flex; flex-direction: column; align-items: center; justify-content: center; gap: 10px;">
                                    <div style="writing-mode: vertical-rl; font-size: 0.75em; color: #94a3b8; font-weight: 600;">AISLE</div>
                                </div>
                                <div style="flex: 1;">
                                    <div style="text-align: center; font-size: 0.75em; color: #64748b; margin-bottom: 8px; font-weight: 600;">Right Side</div>
                                    <div class="seats-grid" id="lowerDeckRight" style="grid-template-columns: repeat(2, 1fr);"></div>
                                </div>
                            </div>
                        </div>
                        <div class="bus-layout" style="margin-top: 20px;">
                            <div class="deck-label">
                                <span>Upper Deck (Sleeper)</span>
                                <span class="deck-info">Seats 21-40</span>
                            </div>
                            <div style="display: flex; gap: 15px; align-items: flex-start;">
                                <div style="flex: 1;">
                                    <div style="text-align: center; font-size: 0.75em; color: #64748b; margin-bottom: 8px; font-weight: 600;">Left Side</div>
                                    <div class="seats-grid" id="upperDeckLeft" style="grid-template-columns: repeat(2, 1fr);"></div>
                                </div>
                                <div style="width: 40px; display: flex; flex-direction: column; align-items: center; justify-content: center; gap: 10px;">
                                    <div style="writing-mode: vertical-rl; font-size: 0.75em; color: #94a3b8; font-weight: 600;">AISLE</div>
                                </div>
                                <div style="flex: 1;">
                                    <div style="text-align: center; font-size: 0.75em; color: #64748b; margin-bottom: 8px; font-weight: 600;">Right Side</div>
                                    <div class="seats-grid" id="upperDeckRight" style="grid-template-columns: repeat(2, 1fr);"></div>
                                </div>
                            </div>
                        </div>
                    </div>

                    <div class="booking-summary">
                        <h3 class="summary-title">Booking Summary</h3>
                        <div class="summary-row">
                            <span class="summary-label">Selected Seats</span>
                            <div class="selected-seats" id="selectedSeats">
                                <span style="color: #94a3b8;">No seats selected</span>
                            </div>
                        </div>
                        <div class="summary-row">
                            <span class="summary-label">Seat Type</span>
                            <span class="summary-value">AC Sleeper</span>
                        </div>
                        <div class="summary-row">
                            <span class="summary-label">Base Fare</span>
                            <span class="summary-value" id="baseFare">₹0</span>
                        </div>
                        <div class="summary-row">
                            <span class="summary-label">GST (5%)</span>
                            <span class="summary-value" id="gst">₹0</span>
                        </div>

                        <div class="total-amount">
                            <div class="total-label">Total Amount</div>
                            <div class="total-price" id="totalAmount">₹0</div>
                        </div>

                        <button class="proceed-btn" id="proceedBtn" disabled onclick="showPassengerForm()">
                            Proceed to Book
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Passenger Details Modal -->
    <div class="modal" id="passengerModal">
        <div class="modal-content">
            <div class="modal-header">
                <div>
                    <h2>Passenger Details</h2>
                    <p>Please provide your contact information</p>
                </div>
                <button class="close-modal" onclick="closePassengerModal()">×</button>
            </div>
            <div class="modal-body">
                <div style="max-width: 600px; margin: 0 auto;">
                    <div class="booking-summary" style="position: static;">
                        <h3 class="summary-title">Enter Your Details</h3>
                        
                        <div style="margin-bottom: 20px;">
                            <label style="display: block; margin-bottom: 8px; color: #64748b; font-weight: 600;">Full Name *</label>
                            <input type="text" id="passengerName" placeholder="Enter your full name" 
                                style="width: 100%; padding: 15px; border: 2px solid #e2e8f0; border-radius: 10px; font-size: 1em;">
                        </div>

                        <div style="margin-bottom: 20px;">
                            <label style="display: block; margin-bottom: 8px; color: #64748b; font-weight: 600;">Primary Phone Number *</label>
                            <input type="tel" id="passengerPhone" placeholder="Enter 10 digit mobile number" 
                                maxlength="10" pattern="[0-9]{10}"
                                style="width: 100%; padding: 15px; border: 2px solid #e2e8f0; border-radius: 10px; font-size: 1em;">
                        </div>

                        <div style="margin-bottom: 20px;">
                            <label style="display: block; margin-bottom: 8px; color: #64748b; font-weight: 600;">Alternate Phone Number (Optional)</label>
                            <input type="tel" id="alternatePhone" placeholder="Enter alternate mobile number" 
                                maxlength="10" pattern="[0-9]{10}"
                                style="width: 100%; padding: 15px; border: 2px solid #e2e8f0; border-radius: 10px; font-size: 1em;">
                        </div>

                        <div style="margin-bottom: 20px;">
                            <label style="display: block; margin-bottom: 8px; color: #64748b; font-weight: 600;">Emergency Contact Number (Optional)</label>
                            <input type="tel" id="emergencyPhone" placeholder="Enter emergency contact number" 
                                maxlength="10" pattern="[0-9]{10}"
                                style="width: 100%; padding: 15px; border: 2px solid #e2e8f0; border-radius: 10px; font-size: 1em;">
                            <small style="color: #64748b; font-size: 0.85em;">In case of emergency, we'll contact this number</small>
                        </div>

                        <div style="margin-bottom: 20px;">
                            <label style="display: block; margin-bottom: 8px; color: #64748b; font-weight: 600;">Email Address *</label>
                            <input type="email" id="passengerEmail" placeholder="Enter your email address" 
                                style="width: 100%; padding: 15px; border: 2px solid #e2e8f0; border-radius: 10px; font-size: 1em;">
                        </div>

                        <div style="margin-bottom: 20px;">
                            <label style="display: block; margin-bottom: 8px; color: #64748b; font-weight: 600;">Age *</label>
                            <input type="number" id="passengerAge" placeholder="Enter your age" min="1" max="120"
                                style="width: 100%; padding: 15px; border: 2px solid #e2e8f0; border-radius: 10px; font-size: 1em;">
                        </div>

                        <div style="margin-bottom: 20px;">
                            <label style="display: block; margin-bottom: 8px; color: #64748b; font-weight: 600;">Gender *</label>
                            <select id="passengerGender" style="width: 100%; padding: 15px; border: 2px solid #e2e8f0; border-radius: 10px; font-size: 1em;">
                                <option value="">Select Gender</option>
                                <option value="Male">Male</option>
                                <option value="Female">Female</option>
                                <option value="Other">Other</option>
                            </select>
                        </div>

                        <div style="background: #dbeafe; border: 2px solid #3b82f6; border-radius: 10px; padding: 15px; margin-bottom: 20px;">
                            <div style="display: flex; align-items: start; gap: 10px;">
                                <div style="font-size: 1.5em;">💡</div>
                                <div style="font-size: 0.9em; color: #1e40af;">
                                    <strong>Multiple Numbers:</strong> SMS confirmations will be sent to your primary number. Alternate numbers are for backup contact purposes.
                                </div>
                            </div>
                        </div>

                        <div class="summary-row" style="margin-top: 30px; padding-top: 20px; border-top: 2px solid #e2e8f0;">
                            <span class="summary-label">Selected Seats</span>
                            <div class="selected-seats" id="finalSelectedSeats"></div>
                        </div>

                        <div class="total-amount">
                            <div class="total-label">Total Amount Payable</div>
                            <div class="total-price" id="finalTotalAmount">₹0</div>
                        </div>

                        <button class="proceed-btn" onclick="confirmBooking()" style="margin-top: 20px;">
                            Confirm & Pay
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Booking Confirmation Modal -->
    <div class="modal" id="confirmationModal">
        <div class="modal-content">
            <div class="modal-header" style="background: linear-gradient(135deg, #16a34a 0%, #15803d 100%);">
                <div>
                    <h2>🎉 Booking Confirmed!</h2>
                    <p>Your tickets have been booked successfully</p>
                </div>
                <button class="close-modal" onclick="closeConfirmationModal()">×</button>
            </div>
            <div class="modal-body">
                <div style="max-width: 700px; margin: 0 auto;">
                    <!-- Success Icon -->
                    <div style="text-align: center; margin-bottom: 30px;">
                        <div style="width: 100px; height: 100px; background: #dcfce7; border-radius: 50%; display: inline-flex; align-items: center; justify-content: center; font-size: 3em;">
                            ✓
                        </div>
                    </div>

                    <!-- Confirmation Message -->
                    <div class="booking-summary" style="position: static; background: #dcfce7; border-color: #16a34a;">
                        <div style="text-align: center; margin-bottom: 25px;">
                            <h3 style="color: #16a34a; font-size: 1.5em; margin-bottom: 10px;">Booking Successful!</h3>
                            <p style="color: #15803d; font-size: 1.1em;">Your seat has been confirmed</p>
                        </div>

                        <div style="background: white; padding: 25px; border-radius: 10px; margin-bottom: 20px;">
                            <div class="summary-row">
                                <span class="summary-label">Booking ID</span>
                                <span class="summary-value" id="bookingId">GEL2025110512345</span>
                            </div>
                            <div class="summary-row">
                                <span class="summary-label">Passenger Name</span>
                                <span class="summary-value" id="confirmName"></span>
                            </div>
                            <div class="summary-row">
                                <span class="summary-label">Phone Number</span>
                                <span class="summary-value" id="confirmPhone"></span>
                            </div>
                            <div class="summary-row">
                                <span class="summary-label">Email</span>
                                <span class="summary-value" id="confirmEmail"></span>
                            </div>
                            <div class="summary-row">
                                <span class="summary-label">Seat Numbers</span>
                                <div class="selected-seats" id="confirmSeats"></div>
                            </div>
                            <div class="summary-row">
                                <span class="summary-label">Journey Date</span>
                                <span class="summary-value">05 Nov 2025, 22:30</span>
                            </div>
                            <div class="summary-row">
                                <span class="summary-label">Route</span>
                                <span class="summary-value">Bangalore → Mumbai</span>
                            </div>
                            <div class="summary-row" style="border-bottom: none; padding-top: 20px; margin-top: 15px; border-top: 2px solid #e2e8f0;">
                                <span class="summary-label" style="font-size: 1.2em;">Total Paid</span>
                                <span class="summary-value" style="color: #16a34a; font-size: 1.4em;" id="confirmAmount"></span>
                            </div>
                        </div>

                        <!-- SMS/Email Notification -->
                        <div style="background: #fff7ed; border: 2px solid #fb923c; border-radius: 10px; padding: 20px; margin-bottom: 20px;">
                            <div style="display: flex; align-items: center; gap: 15px; margin-bottom: 15px;">
                                <div style="font-size: 2em;">📱</div>
                                <div>
                                    <h4 style="color: #ea580c; margin-bottom: 5px;">SMS Sent Successfully!</h4>
                                    <p style="color: #9a3412; font-size: 0.95em; margin: 0;">A confirmation message has been sent to your mobile</p>
                                </div>
                            </div>
                            <div style="background: white; padding: 15px; border-radius: 8px; font-family: monospace; font-size: 0.9em; color: #1e293b;">
                                <strong>Gangadhar Experience Line</strong><br>
                                Dear <span id="smsName"></span>, your booking is confirmed!<br>
                                Seats: <span id="smsSeats"></span><br>
                                Journey: BLR → MUM on 05-Nov-2025<br>
                                Amount: <span id="smsAmount"></span><br>
                                Booking ID: <span id="smsBookingId"></span><br>
                                Happy Journey! 🚌
                            </div>
                        </div>

                        <div style="background: #dbeafe; border: 2px solid #3b82f6; border-radius: 10px; padding: 20px;">
                            <div style="display: flex; align-items: center; gap: 15px; margin-bottom: 15px;">
                                <div style="font-size: 2em;">📧</div>
                                <div>
                                    <h4 style="color: #1e40af; margin-bottom: 5px;">Email Sent Successfully!</h4>
                                    <p style="color: #1e3a8a; font-size: 0.95em; margin: 0;">Booking details sent to your email address</p>
                                </div>
                            </div>
                            <div style="background: white; padding: 15px; border-radius: 8px; font-size: 0.9em; color: #1e293b;">
                                <strong>To:</strong> <span id="emailTo"></span><br>
                                <strong>Subject:</strong> Booking Confirmation - Gangadhar Experience Line<br><br>
                                Your e-ticket and journey details have been sent to your email. Please carry a valid ID proof during travel.
                            </div>
                        </div>
                    </div>

                    <div style="display: flex; gap: 15px; margin-top: 20px;">
                        <button class="view-seats-btn" onclick="downloadTicket()" style="flex: 1;">
                            📄 Download Ticket
                        </button>
                        <button class="proceed-btn" onclick="closeConfirmationModal()" style="flex: 1;">
                            Done
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        const seatPrice = 1000;
        let selectedSeats = [];
        let bookedSeats = [5, 9, 15, 22, 28, 35];
        let currentTravelMode = 'bus';
        let allBookings = []; // Store all bookings

        // Route data with pricing and duration
        const routeData = {
            'Bangalore-Mumbai': { duration: '14h 30m', busPrice: 1000, trainPrice: 850, flightPrice: 4250 },
            'Bangalore-Delhi': { duration: '32h 00m', busPrice: 1800, trainPrice: 1450, flightPrice: 5800 },
            'Bangalore-Chennai': { duration: '6h 30m', busPrice: 450, trainPrice: 320, flightPrice: 3200 },
            'Bangalore-Hyderabad': { duration: '9h 00m', busPrice: 650, trainPrice: 480, flightPrice: 3800 },
            'Bangalore-Pune': { duration: '11h 00m', busPrice: 750, trainPrice: 650, flightPrice: 4100 },
            'Mumbai-Delhi': { duration: '26h 00m', busPrice: 1500, trainPrice: 1200, flightPrice: 5200 },
            'Mumbai-Goa': { duration: '10h 00m', busPrice: 700, trainPrice: 580, flightPrice: 4500 },
            'Delhi-Jaipur': { duration: '5h 30m', busPrice: 400, trainPrice: 280, flightPrice: 3500 },
            'Delhi-Agra': { duration: '3h 30m', busPrice: 350, trainPrice: 250, flightPrice: 3200 },
            'Chennai-Hyderabad': { duration: '8h 00m', busPrice: 550, trainPrice: 420, flightPrice: 3600 },
            'Hyderabad-Pune': { duration: '10h 30m', busPrice: 680, trainPrice: 520, flightPrice: 3900 },
            'Kolkata-Delhi': { duration: '28h 00m', busPrice: 1600, trainPrice: 1300, flightPrice: 5500 },
            'default': { duration: '12h 00m', busPrice: 800, trainPrice: 600, flightPrice: 4000 }
        };

        function getRouteInfo(from, to) {
            const key = `${from}-${to}`;
            return routeData[key] || routeData['default'];
        }

        function updateListingsWithRoute() {
            const from = document.getElementById('fromCity').value;
            const to = document.getElementById('toCity').value;
            
            if (from === to) {
                alert('Source and destination cannot be the same!');
                return;
            }

            const route = getRouteInfo(from, to);

            // Update bus listings
            if (currentTravelMode === 'bus') {
                document.getElementById('busFrom1').textContent = from;
                document.getElementById('busFrom2').textContent = from;
                document.getElementById('busFrom3').textContent = from;
                document.getElementById('busTo1').textContent = to;
                document.getElementById('busTo2').textContent = to;
                document.getElementById('busTo3').textContent = to;
                document.getElementById('busDuration1').textContent = route.duration;
                document.getElementById('busDuration2').textContent = route.duration;
                document.getElementById('busDuration3').textContent = route.duration;
                document.getElementById('busPrice1').textContent = '₹' + route.busPrice;
                document.getElementById('busPrice2').textContent = '₹' + Math.round(route.busPrice * 0.7);
                document.getElementById('busPrice3').textContent = '₹' + Math.round(route.busPrice * 0.55);
            }
        }

        function switchTravelMode(mode) {
            currentTravelMode = mode;
            
            // Update tabs
            document.querySelectorAll('.travel-tab').forEach(tab => tab.classList.remove('active'));
            document.getElementById(mode + 'Tab').classList.add('active');
            
            // Update search button text
            const searchBtn = document.getElementById('searchBtnText');
            if (mode === 'bus') searchBtn.textContent = 'Search Buses';
            else if (mode === 'train') searchBtn.textContent = 'Search Trains';
            else if (mode === 'flight') searchBtn.textContent = 'Search Flights';
            else searchBtn.textContent = 'Search Hotels';
            
            // Show/hide search boxes
            const transportSearch = document.getElementById('transportSearch');
            const hotelSearch = document.getElementById('hotelSearch');
            
            if (mode === 'hotel') {
                transportSearch.style.display = 'none';
                hotelSearch.style.display = 'grid';
            } else {
                transportSearch.style.display = 'grid';
                hotelSearch.style.display = 'none';
                
                // Show/hide return date for flights
                const returnField = document.getElementById('returnDateField');
                returnField.style.display = mode === 'flight' ? 'block' : 'none';
            }
            
            // Show respective listings
            document.getElementById('busListings').style.display = mode === 'bus' ? 'block' : 'none';
            document.getElementById('trainListings').style.display = mode === 'train' ? 'block' : 'none';
            document.getElementById('flightListings').style.display = mode === 'flight' ? 'block' : 'none';
            document.getElementById('hotelListings').style.display = mode === 'hotel' ? 'block' : 'none';
        }

        function searchResults() {
            if (currentTravelMode === 'hotel') {
                const city = document.getElementById('hotelCity').value;
                const checkIn = document.getElementById('checkInDate').value;
                const checkOut = document.getElementById('checkOutDate').value;
                
                if (!city || !checkIn || !checkOut) {
                    alert('Please fill all search fields');
                    return;
                }
                
                const nights = Math.ceil((new Date(checkOut) - new Date(checkIn)) / (1000 * 60 * 60 * 24));
                alert(`Searching hotels in ${city}\nCheck-in: ${checkIn}\nCheck-out: ${checkOut}\nTotal Nights: ${nights}\n\nShowing available hotels below!`);
            } else {
                const from = document.getElementById('fromCity').value;
                const to = document.getElementById('toCity').value;
                const date = document.getElementById('journeyDate').value;
                
                if (!from || !to || !date) {
                    alert('Please fill all search fields');
                    return;
                }

                if (from === to) {
                    alert('Source and destination cannot be the same!');
                    return;
                }

                updateListingsWithRoute();
                
                let message = `Searching ${currentTravelMode}s from ${from} to ${to} on ${date}`;
                if (currentTravelMode === 'flight' && document.getElementById('returnDate').value) {
                    message += ` (Return: ${document.getElementById('returnDate').value})`;
                }
                
                alert(message + '\n\nShowing available results below!');
            }
        }

        function bookHotel(hotelName, pricePerNight) {
            const checkIn = document.getElementById('checkInDate').value;
            const checkOut = document.getElementById('checkOutDate').value;
            const nights = Math.ceil((new Date(checkOut) - new Date(checkIn)) / (1000 * 60 * 60 * 24));
            const totalPrice = pricePerNight * nights;
            const gst = Math.round(totalPrice * 0.12);
            const finalPrice = totalPrice + gst;
            
            // Show passenger modal with hotel details
            document.getElementById('passengerModal').classList.add('active');
            document.getElementById('finalTotalAmount').textContent = `₹${finalPrice}`;
            
            const detailsHtml = `
                <span class="seat-badge">${hotelName}</span>
                <span class="seat-badge">${nights} Night${nights > 1 ? 's' : ''}</span>
            `;
            document.getElementById('finalSelectedSeats').innerHTML = detailsHtml;
            
            // Store hotel booking details for confirmation
            window.currentHotelBooking = {
                name: hotelName,
                checkIn: checkIn,
                checkOut: checkOut,
                nights: nights,
                price: finalPrice
            };
        }

        function openSeatModal() {
            document.getElementById('seatModal').classList.add('active');
            renderSeats();
        }

        function closeSeatModal() {
            document.getElementById('seatModal').classList.remove('active');
            selectedSeats = [];
            updateSummary();
        }

        function renderSeats() {
            const lowerDeckLeft = document.getElementById('lowerDeckLeft');
            const lowerDeckRight = document.getElementById('lowerDeckRight');
            const upperDeckLeft = document.getElementById('upperDeckLeft');
            const upperDeckRight = document.getElementById('upperDeckRight');
            
            if (!lowerDeckLeft) return;
            
            lowerDeckLeft.innerHTML = '';
            lowerDeckRight.innerHTML = '';
            upperDeckLeft.innerHTML = '';
            upperDeckRight.innerHTML = '';

            // Driver seat in lower left first position
            lowerDeckLeft.appendChild(createSeat('driver', '🚗'));
            
            // Lower deck left (seats 2-5)
            for (let i = 2; i <= 5; i++) {
                lowerDeckLeft.appendChild(createSeat(i, i));
            }
            
            // Lower deck right (seats 6-10)
            for (let i = 6; i <= 10; i++) {
                lowerDeckRight.appendChild(createSeat(i, i));
            }

            // Upper deck left (seats 11-20)
            for (let i = 11; i <= 20; i++) {
                upperDeckLeft.appendChild(createSeat(i, i));
            }
            
            // Upper deck right (seats 21-40)
            for (let i = 21; i <= 40; i++) {
                upperDeckRight.appendChild(createSeat(i, i));
            }
        }

        function createSeat(id, label) {
            const seat = document.createElement('div');
            seat.className = 'seat';
            
            if (id === 'driver') {
                seat.classList.add('driver');
            } else if (bookedSeats.includes(id)) {
                seat.classList.add('booked');
            } else if (selectedSeats.includes(id)) {
                seat.classList.add('selected');
            }

            seat.textContent = label;
            
            if (id !== 'driver' && !bookedSeats.includes(id)) {
                seat.onclick = () => toggleSeat(id);
            }

            return seat;
        }

        function toggleSeat(seatId) {
            const index = selectedSeats.indexOf(seatId);
            if (index > -1) {
                selectedSeats.splice(index, 1);
            } else {
                if (selectedSeats.length < 6) {
                    selectedSeats.push(seatId);
                } else {
                    alert('Maximum 6 seats can be selected at a time');
                    return;
                }
            }
            renderSeats();
            updateSummary();
        }

        function updateSummary() {
            const seatsContainer = document.getElementById('selectedSeats');
            const baseFare = selectedSeats.length * seatPrice;
            const gstAmount = Math.round(baseFare * 0.05);
            const total = baseFare + gstAmount;

            if (selectedSeats.length === 0) {
                seatsContainer.innerHTML = '<span style="color: #94a3b8;">No seats selected</span>';
            } else {
                seatsContainer.innerHTML = selectedSeats
                    .sort((a, b) => a - b)
                    .map(seat => `<span class="seat-badge">${seat}</span>`)
                    .join('');
            }

            document.getElementById('baseFare').textContent = `₹${baseFare}`;
            document.getElementById('gst').textContent = `₹${gstAmount}`;
            document.getElementById('totalAmount').textContent = `₹${total}`;
            document.getElementById('proceedBtn').disabled = selectedSeats.length === 0;
        }

        function showPassengerForm() {
            document.getElementById('passengerModal').classList.add('active');
            const total = document.getElementById('totalAmount').textContent;
            document.getElementById('finalTotalAmount').textContent = total;
            
            const seatsHtml = selectedSeats
                .sort((a, b) => a - b)
                .map(seat => `<span class="seat-badge">${seat}</span>`)
                .join('');
            document.getElementById('finalSelectedSeats').innerHTML = seatsHtml;
        }

        function closePassengerModal() {
            document.getElementById('passengerModal').classList.remove('active');
        }

        function confirmBooking() {
            const name = document.getElementById('passengerName').value.trim();
            const phone = document.getElementById('passengerPhone').value.trim();
            const alternatePhone = document.getElementById('alternatePhone').value.trim();
            const emergencyPhone = document.getElementById('emergencyPhone').value.trim();
            const email = document.getElementById('passengerEmail').value.trim();
            const age = document.getElementById('passengerAge').value.trim();
            const gender = document.getElementById('passengerGender').value;

            // Validation
            if (!name || !phone || !email || !age || !gender) {
                alert('Please fill all required fields (marked with *)');
                return;
            }

            if (phone.length !== 10 || !/^\d+$/.test(phone)) {
                alert('Please enter a valid 10-digit primary phone number');
                return;
            }

            // Validate alternate phone if provided
            if (alternatePhone && (alternatePhone.length !== 10 || !/^\d+$/.test(alternatePhone))) {
                alert('Alternate phone number must be 10 digits');
                return;
            }

            // Validate emergency phone if provided
            if (emergencyPhone && (emergencyPhone.length !== 10 || !/^\d+$/.test(emergencyPhone))) {
                alert('Emergency contact number must be 10 digits');
                return;
            }

            // Check if alternate or emergency is same as primary
            if (alternatePhone && alternatePhone === phone) {
                alert('Alternate phone number cannot be same as primary number');
                return;
            }

            if (emergencyPhone && emergencyPhone === phone) {
                alert('Emergency contact cannot be same as primary number');
                return;
            }

            if (!email.includes('@') || !email.includes('.')) {
                alert('Please enter a valid email address');
                return;
            }

            // Generate booking ID
            const bookingId = 'GEL' + Date.now().toString().slice(-10);
            const total = document.getElementById('finalTotalAmount').textContent;

            // Update confirmation modal
            document.getElementById('bookingId').textContent = bookingId;
            document.getElementById('confirmName').textContent = name;
            
            // Show all phone numbers
            let phoneDisplay = '+91 ' + phone;
            if (alternatePhone) {
                phoneDisplay += ' (Alt: +91 ' + alternatePhone + ')';
            }
            if (emergencyPhone) {
                phoneDisplay += ' (Emergency: +91 ' + emergencyPhone + ')';
            }
            document.getElementById('confirmPhone').textContent = phoneDisplay;
            
            document.getElementById('confirmEmail').textContent = email;
            document.getElementById('confirmAmount').textContent = total;
            
            const seatsText = selectedSeats.sort((a, b) => a - b).join(', ');
            const confirmSeatsHtml = selectedSeats
                .sort((a, b) => a - b)
                .map(seat => `<span class="seat-badge">${seat}</span>`)
                .join('');
            document.getElementById('confirmSeats').innerHTML = confirmSeatsHtml;

            // SMS Content - Primary number
            document.getElementById('smsName').textContent = name.split(' ')[0];
            document.getElementById('smsSeats').textContent = seatsText;
            document.getElementById('smsAmount').textContent = total;
            document.getElementById('smsBookingId').textContent = bookingId;

            // Email Content
            document.getElementById('emailTo').textContent = email;

            // Mark seats as booked
            bookedSeats.push(...selectedSeats);
            
            // Save booking to history
            const bookingData = {
                id: bookingId,
                name: name,
                phone: phone,
                alternatePhone: alternatePhone,
                emergencyPhone: emergencyPhone,
                email: email,
                age: age,
                gender: gender,
                seats: [...selectedSeats],
                amount: total,
                date: new Date().toLocaleDateString(),
                bookingDate: new Date().toLocaleString(),
                travelDate: document.getElementById('journeyDate').value,
                from: document.getElementById('fromCity').value,
                to: document.getElementById('toCity').value,
                mode: currentTravelMode,
                status: 'confirmed'
            };
            allBookings.push(bookingData);
            
            // Close passenger modal and show confirmation
            closePassengerModal();
            closeSeatModal();
            document.getElementById('confirmationModal').classList.add('active');

            // Simulate sending messages to all numbers
            console.log('SMS sent to Primary: +91' + phone);
            if (alternatePhone) {
                console.log('Backup SMS sent to Alternate: +91' + alternatePhone);
            }
            if (emergencyPhone) {
                console.log('Emergency contact notified: +91' + emergencyPhone);
            }
            console.log('Email sent to ' + email);
        }

        function closeConfirmationModal() {
            document.getElementById('confirmationModal').classList.remove('active');
            selectedSeats = [];
            
            // Clear form
            document.getElementById('passengerName').value = '';
            document.getElementById('passengerPhone').value = '';
            document.getElementById('alternatePhone').value = '';
            document.getElementById('emergencyPhone').value = '';
            document.getElementById('passengerEmail').value = '';
            document.getElementById('passengerAge').value = '';
            document.getElementById('passengerGender').value = '';
        }

        function downloadTicket() {
            alert('Ticket download functionality would be implemented here!\nIn real application, this would generate a PDF ticket.');
        }

        function showMyBookings() {
            // Hide all other sections
            document.getElementById('heroSection').style.display = 'none';
            document.getElementById('busListings').style.display = 'none';
            document.getElementById('trainListings').style.display = 'none';
            document.getElementById('flightListings').style.display = 'none';
            document.getElementById('hotelListings').style.display = 'none';
            
            // Show bookings section
            document.getElementById('myBookingsSection').style.display = 'block';
            
            // Render bookings
            renderBookings();
        }

        function hideMyBookings() {
            document.getElementById('myBookingsSection').style.display = 'none';
            document.getElementById('heroSection').style.display = 'block';
            
            // Show current travel mode listings
            if (currentTravelMode === 'bus') {
                document.getElementById('busListings').style.display = 'block';
            } else if (currentTravelMode === 'train') {
                document.getElementById('trainListings').style.display = 'block';
            } else if (currentTravelMode === 'flight') {
                document.getElementById('flightListings').style.display = 'block';
            } else if (currentTravelMode === 'hotel') {
                document.getElementById('hotelListings').style.display = 'block';
            }
        }

        function renderBookings() {
            const bookingsList = document.getElementById('bookingsList');
            
            if (allBookings.length === 0) {
                bookingsList.innerHTML = `
                    <div class="no-bookings">
                        <div class="no-bookings-icon">🎫</div>
                        <h3 style="color: #64748b; margin-bottom: 10px;">No Bookings Yet</h3>
                        <p style="color: #94a3b8; margin-bottom: 20px;">Start your journey by booking tickets now!</p>
                        <button class="view-seats-btn" onclick="hideMyBookings()">Book Now</button>
                    </div>
                `;
                return;
            }
            
            bookingsList.innerHTML = allBookings
                .sort((a, b) => new Date(b.bookingDate) - new Date(a.bookingDate))
                .map(booking => `
                    <div class="booking-card ${booking.status === 'cancelled' ? 'cancelled' : ''}">
                        <span class="booking-status ${booking.status === 'confirmed' ? 'status-confirmed' : 'status-cancelled'}">
                            ${booking.status === 'confirmed' ? '✓ Confirmed' : '✗ Cancelled'}
                        </span>
                        
                        <div class="booking-id-section">
                            <strong style="color: #64748b;">Booking ID:</strong>
                            <span class="booking-id-badge">${booking.id}</span>
                        </div>
                        
                        <div class="booking-header">
                            <div>
                                <h3 style="color: #1e293b; margin-bottom: 8px;">
                                    ${getModeIcon(booking.mode)} ${booking.from} → ${booking.to}
                                </h3>
                                <p style="color: #64748b; margin-bottom: 5px;">
                                    <strong>Passenger:</strong> ${booking.name}
                                </p>
                                <p style="color: #64748b; margin-bottom: 5px;">
                                    <strong>Travel Date:</strong> ${new Date(booking.travelDate).toLocaleDateString('en-IN', { weekday: 'short', year: 'numeric', month: 'short', day: 'numeric' })}
                                </p>
                                <p style="color: #64748b; margin-bottom: 5px;">
                                    <strong>Booked On:</strong> ${booking.bookingDate}
                                </p>
                            </div>
                        </div>
                        
                        <div style="background: #f8fafc; padding: 15px; border-radius: 10px; margin-bottom: 15px;">
                            <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); gap: 15px;">
                                <div>
                                    <p style="color: #64748b; font-size: 0.9em; margin-bottom: 5px;">Seats/Rooms</p>
                                    <p style="color: #1e293b; font-weight: 600;">${booking.seats.join(', ')}</p>
                                </div>
                                <div>
                                    <p style="color: #64748b; font-size: 0.9em; margin-bottom: 5px;">Contact</p>
                                    <p style="color: #1e293b; font-weight: 600;">+91 ${booking.phone}</p>
                                </div>
                                <div>
                                    <p style="color: #64748b; font-size: 0.9em; margin-bottom: 5px;">Email</p>
                                    <p style="color: #1e293b; font-weight: 600;">${booking.email}</p>
                                </div>
                                <div>
                                    <p style="color: #64748b; font-size: 0.9em; margin-bottom: 5px;">Total Amount</p>
                                    <p style="color: #16a34a; font-weight: 700; font-size: 1.2em;">${booking.amount}</p>
                                </div>
                            </div>
                        </div>
                        
                        <div class="booking-actions">
                            <button class="btn-small btn-view" onclick="viewBookingDetails('${booking.id}')">
                                📋 View Details
                            </button>
                            <button class="btn-small btn-download" onclick="downloadBookingTicket('${booking.id}')">
                                📄 Download Ticket
                            </button>
                            ${booking.status === 'confirmed' ? `
                                <button class="btn-small btn-cancel" onclick="cancelBooking('${booking.id}')">
                                    ❌ Cancel Booking
                                </button>
                            ` : '<button class="btn-small btn-disabled" disabled>Cancelled</button>'}
                        </div>
                    </div>
                `).join('');
        }

        function getModeIcon(mode) {
            const icons = {
                'bus': '🚌 Bus',
                'train': '🚆 Train',
                'flight': '✈️ Flight',
                'hotel': '🏨 Hotel'
            };
            return icons[mode] || '🎫 ' + mode;
        }

        function viewBookingDetails(bookingId) {
            const booking = allBookings.find(b => b.id === bookingId);
            if (!booking) return;
            
            const detailsContent = document.getElementById('bookingDetailsContent');
            detailsContent.innerHTML = `
                <div class="booking-summary" style="position: static;">
                    <h3 class="summary-title">Booking Information</h3>
                    
                    <div style="background: ${booking.status === 'confirmed' ? '#dcfce7' : '#fee2e2'}; padding: 15px; border-radius: 10px; margin-bottom: 20px; text-align: center;">
                        <h3 style="color: ${booking.status === 'confirmed' ? '#166534' : '#991b1b'}; font-size: 1.3em;">
                            ${booking.status === 'confirmed' ? '✓ Booking Confirmed' : '✗ Booking Cancelled'}
                        </h3>
                        <p style="color: ${booking.status === 'confirmed' ? '#15803d' : '#7f1d1d'}; margin-top: 5px;">
                            Booking ID: <strong>${booking.id}</strong>
                        </p>
                    </div>
                    
                    <div class="summary-row">
                        <span class="summary-label">Travel Type</span>
                        <span class="summary-value">${getModeIcon(booking.mode)}</span>
                    </div>
                    <div class="summary-row">
                        <span class="summary-label">Route</span>
                        <span class="summary-value">${booking.from} → ${booking.to}</span>
                    </div>
                    <div class="summary-row">
                        <span class="summary-label">Passenger Name</span>
                        <span class="summary-value">${booking.name}</span>
                    </div>
                    <div class="summary-row">
                        <span class="summary-label">Age / Gender</span>
                        <span class="summary-value">${booking.age} years / ${booking.gender}</span>
                    </div>
                    <div class="summary-row">
                        <span class="summary-label">Primary Phone</span>
                        <span class="summary-value">+91 ${booking.phone}</span>
                    </div>
                    ${booking.alternatePhone ? `
                    <div class="summary-row">
                        <span class="summary-label">Alternate Phone</span>
                        <span class="summary-value">+91 ${booking.alternatePhone}</span>
                    </div>
                    ` : ''}
                    ${booking.emergencyPhone ? `
                    <div class="summary-row">
                        <span class="summary-label">Emergency Contact</span>
                        <span class="summary-value">+91 ${booking.emergencyPhone}</span>
                    </div>
                    ` : ''}
                    <div class="summary-row">
                        <span class="summary-label">Email</span>
                        <span class="summary-value">${booking.email}</span>
                    </div>
                    <div class="summary-row">
                        <span class="summary-label">Seats/Rooms</span>
                        <div class="selected-seats">
                            ${booking.seats.map(seat => `<span class="seat-badge">${seat}</span>`).join('')}
                        </div>
                    </div>
                    <div class="summary-row">
                        <span class="summary-label">Travel Date</span>
                        <span class="summary-value">${new Date(booking.travelDate).toLocaleDateString('en-IN', { weekday: 'long', year: 'numeric', month: 'long', day: 'numeric' })}</span>
                    </div>
                    <div class="summary-row">
                        <span class="summary-label">Booking Date</span>
                        <span class="summary-value">${booking.bookingDate}</span>
                    </div>
                    <div class="summary-row" style="border-top: 2px solid #e2e8f0; padding-top: 15px; margin-top: 10px; border-bottom: none;">
                        <span class="summary-label" style="font-size: 1.2em;">Total Amount Paid</span>
                        <span class="summary-value" style="color: #16a34a; font-size: 1.5em;">${booking.amount}</span>
                    </div>
                </div>
            `;
            
            document.getElementById('bookingDetailsModal').classList.add('active');
        }

        function closeBookingDetails() {
            document.getElementById('bookingDetailsModal').classList.remove('active');
        }
