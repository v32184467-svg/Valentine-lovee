
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>For Devi Jii ❤️</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
    <script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,700;1,700&family=Satoshi:wght@300;400;700&display=swap" rel="stylesheet">

    <style>
        :root {
            --aurora-1: hsla(333, 70%, 55%, 0.4);
            --aurora-2: hsla(282, 82%, 54%, 0.3);
            --aurora-3: hsla(210, 89%, 60%, 0.3);
            --aurora-4: hsla(35, 90%, 60%, 0.3);
        }

        body {
            margin: 0;
            padding: 0;
            background-color: #0c0a09;
            color: #f5f5f5;
            font-family: 'Satoshi', sans-serif;
            overflow: hidden;
            height: 100vh;
        }

        /* Layer 1: Animated Aurora Gradient */
        .aurora-container {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -2;
            filter: blur(100px);
            animation: drift 20s ease-in-out infinite alternate;
        }

        .aurora-blob {
            position: absolute;
            width: 60vw;
            height: 60vw;
            border-radius: 50%;
            mix-blend-mode: screen;
        }

        @keyframes drift {
            from { transform: scale(1) rotate(0deg); }
            to { transform: scale(1.2) rotate(10deg); }
        }

        /* Step Styling */
        .glass-card {
            background: rgba(12, 10, 9, 0.6);
            backdrop-filter: blur(20px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 24px;
            box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.5);
            display: none;
            opacity: 0;
            transform: translateY(30px);
        }

        .glass-card.active {
            display: block;
        }

        .text-gradient {
            background: linear-gradient(to right, #ffffff, #f472b6, #fb7185);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            font-family: 'Playfair Display', serif;
        }

        .btn-primary {
            background: linear-gradient(135deg, #ec4899, #e11d48);
            box-shadow: 0 10px 20px -5px rgba(225, 29, 72, 0.5);
            transition: all 0.3s cubic-bezier(0.175, 0.885, 0.32, 1.275);
        }

        .btn-primary:hover {
            transform: translateY(-4px) scale(1.05);
            box-shadow: 0 15px 25px -5px rgba(225, 29, 72, 0.7);
        }

        .btn-primary:active {
            transform: translateY(1px);
        }

        .progress-track {
            position: fixed;
            top: 20px;
            left: 50%;
            transform: translateX(-50%);
            width: 200px;
            height: 6px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            overflow: hidden;
            z-index: 100;
        }

        #progress-bar {
            width: 20%;
            height: 100%;
            background: linear-gradient(to right, #ec4899, #e11d48);
            transition: width 0.6s ease;
        }

        .polaroid {
            background: white;
            padding: 10px 10px 30px 10px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.4);
            transform: rotate3d(1, 1, 1, 10deg);
            transition: transform 0.1s ease-out;
        }

        .final-pop {
            position: fixed;
            font-weight: 900;
            color: #e11d48;
            pointer-events: none;
            z-index: 1000;
            text-shadow: 0 0 10px rgba(255,255,255,0.5);
        }
    </style>
</head>
<body>

    <div class="aurora-container">
        <div class="aurora-blob" style="background: var(--aurora-1); top: -10%; left: -10%;"></div>
        <div class="aurora-blob" style="background: var(--aurora-2); bottom: -10%; right: -10%;"></div>
        <div class="aurora-blob" style="background: var(--aurora-3); top: 20%; right: 20%;"></div>
        <div class="aurora-blob" style="background: var(--aurora-4); bottom: 10%; left: 30%;"></div>
