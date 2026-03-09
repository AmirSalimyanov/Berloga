# Berloga
<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Берлога — Банный комплекс в Салавате | Баня на дровах</title>
    <meta name="description" content="Банный комплекс «Берлога» в Салавате — частные домики с баней на дровах, сибирским чаном, мангалом и личной территорией. Забронировать онлайн.">
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,700;0,900;1,400&family=Montserrat:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        /* ============================================
           RESET & BASE
        ============================================ */
        *, *::before, *::after {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --black:       #0E0A06;
            --dark:        #1C1208;
            --dark-mid:    #2A1F12;
            --brown:       #3D2B1A;
            --amber:       #D97B2A;
            --amber-dark:  #B5621E;
            --amber-light: #F0A855;
            --red:         #A63D2F;
            --cream:       #F5EDD8;
            --beige:       #E8D9C0;
            --muted:       #B8A99A;
            --white:       #FFFFFF;
            --green:       #4A6741;

            --font-head: 'Playfair Display', Georgia, serif;
            --font-body: 'Montserrat', Arial, sans-serif;

            --radius: 12px;
            --radius-lg: 20px;
            --shadow: 0 8px 40px rgba(0,0,0,0.5);
            --shadow-sm: 0 4px 20px rgba(0,0,0,0.3);
            --transition: 0.3s ease;
        }

        html {
            scroll-behavior: smooth;
            font-size: 16px;
        }

        body {
            font-family: var(--font-body);
            background: var(--dark);
            color: var(--cream);
            overflow-x: hidden;
            line-height: 1.6;
        }

        img { display: block; max-width: 100%; }
        a { text-decoration: none; color: inherit; }
        ul { list-style: none; }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        .section-title {
            font-family: var(--font-head);
            font-size: clamp(2rem, 4vw, 3rem);
            color: var(--cream);
            line-height: 1.2;
            margin-bottom: 16px;
        }

        .section-title span {
            color: var(--amber);
        }

        .section-sub {
            font-size: 1.05rem;
            color: var(--muted);
            max-width: 600px;
            margin-bottom: 50px;
        }

        /* ============================================
           BUTTONS
        ============================================ */
        .btn {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            padding: 16px 32px;
            border-radius: 50px;
            font-family: var(--font-body);
            font-weight: 600;
            font-size: 0.95rem;
            letter-spacing: 0.5px;
            cursor: pointer;
            border: none;
            transition: all var(--transition);
            text-decoration: none;
            white-space: nowrap;
        }

        .btn-primary {
            background: var(--amber);
            color: var(--dark);
        }

        .btn-primary:hover {
            background: var(--amber-light);
            transform: translateY(-2px);
            box-shadow: 0 8px 30px rgba(217,123,42,0.4);
        }

        .btn-outline {
            background: transparent;
            color: var(--cream);
            border: 2px solid rgba(245,237,216,0.4);
        }

        .btn-outline:hover {
            border-color: var(--amber);
            color: var(--amber);
            transform: translateY(-2px);
        }

        .btn-ghost {
            background: rgba(217,123,42,0.15);
            color: var(--amber);
            border: 1px solid rgba(217,123,42,0.3);
        }

        .btn-ghost:hover {
            background: var(--amber);
            color: var(--dark);
        }

        .btn-green {
            background: var(--green);
            color: var(--white);
        }

        .btn-green:hover {
            background: #5a7f51;
            transform: translateY(-2px);
        }

        /* ============================================
           NAVIGATION
        ============================================ */
        .nav {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            z-index: 1000;
            padding: 16px 0;
            transition: all var(--transition);
        }

        .nav.scrolled {
            background: rgba(28, 18, 8, 0.97);
            backdrop-filter: blur(20px);
            padding: 10px 0;
            box-shadow: 0 4px 30px rgba(0,0,0,0.5);
        }

        .nav-inner {
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 20px;
        }

        .nav-logo {
            font-family: var(--font-head);
            font-size: 1.6rem;
            font-weight: 900;
            color: var(--cream);
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .nav-logo .bear {
            font-size: 1.8rem;
        }

        .nav-logo span {
            color: var(--amber);
        }

        .nav-links {
            display: flex;
            align-items: center;
            gap: 30px;
        }

        .nav-links a {
            font-size: 0.9rem;
            font-weight: 500;
            color: var(--muted);
            transition: color var(--transition);
            position: relative;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -4px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--amber);
            transition: width var(--transition);
        }

        .nav-links a:hover {
            color: var(--amber);
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        .nav-cta {
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .nav-phone {
            font-weight: 600;
            font-size: 0.95rem;
            color: var(--cream);
            display: flex;
            align-items: center;
            gap: 6px;
        }

        .burger {
            display: none;
            flex-direction: column;
            gap: 5px;
            cursor: pointer;
            padding: 8px;
            background: none;
            border: none;
        }

        .burger span {
            display: block;
            width: 26px;
            height: 2px;
            background: var(--cream);
            transition: all var(--transition);
        }

        /* Mobile menu */
        .mobile-menu {
            display: none;
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: var(--dark);
            z-index: 999;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            gap: 30px;
        }

        .mobile-menu.open {
            display: flex;
        }

        .mobile-menu a {
            font-family: var(--font-head);
            font-size: 2rem;
            color: var(--cream);
            transition: color var(--transition);
        }

        .mobile-menu a:hover {
            color: var(--amber);
        }

        .mobile-menu-close {
            position: absolute;
            top: 20px;
            right: 20px;
            background: none;
            border: none;
            color: var(--cream);
            font-size: 2rem;
            cursor: pointer;
        }

        /* ============================================
           HERO
        ============================================ */
        .hero {
            min-height: 100vh;
            position: relative;
            display: flex;
            align-items: center;
            overflow: hidden;
        }

        .hero-bg {
            position: absolute;
            inset: 0;
            background:
                linear-gradient(135deg, rgba(14,10,6,0.85) 0%, rgba(28,18,8,0.7) 50%, rgba(14,10,6,0.9) 100%),
                url('https://images.unsplash.com/photo-1542314831-068cd1dbfeeb?w=1600&q=80') center/cover no-repeat;
            z-index: 0;
        }

        .hero-particles {
            position: absolute;
            inset: 0;
            z-index: 1;
            pointer-events: none;
        }

        .particle {
            position: absolute;
            width: 3px;
            height: 3px;
            background: var(--amber);
            border-radius: 50%;
            opacity: 0;
            animation: float-particle linear infinite;
        }

        @keyframes float-particle {
            0% { opacity: 0; transform: translateY(0) scale(0); }
            10% { opacity: 0.8; }
            90% { opacity: 0.3; }
            100% { opacity: 0; transform: translateY(-100vh) scale(0.5); }
        }

        .hero-content {
            position: relative;
            z-index: 2;
            padding: 120px 0 60px;
        }

        .hero-badge {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            background: rgba(217,123,42,0.2);
            border: 1px solid rgba(217,123,42,0.4);
            border-radius: 50px;
            padding: 8px 20px;
            font-size: 0.85rem;
            color: var(--amber-light);
            font-weight: 500;
            margin-bottom: 30px;
            letter-spacing: 1px;
            text-transform: uppercase;
        }

        .hero-title {
            font-family: var(--font-head);
            font-size: clamp(2.8rem, 6vw, 5.5rem);
            font-weight: 900;
            color: var(--cream);
            line-height: 1.1;
            margin-bottom: 24px;
            max-width: 800px;
        }

        .hero-title .fire {
            color: var(--amber);
            position: relative;
        }

        .hero-title .fire::after {
            content: '';
            position: absolute;
            bottom: -4px;
            left: 0;
            right: 0;
            height: 3px;
            background: linear-gradient(90deg, var(--amber), var(--amber-light), transparent);
            border-radius: 2px;
        }

        .hero-sub {
            font-size: clamp(1rem, 2vw, 1.2rem);
            color: var(--beige);
            max-width: 580px;
            margin-bottom: 40px;
            line-height: 1.7;
        }

        .hero-cta {
            display: flex;
            gap: 16px;
            flex-wrap: wrap;
            margin-bottom: 60px;
        }

        .hero-stats {
            display: flex;
            gap: 40px;
            flex-wrap: wrap;
        }

        .hero-stat {
            text-align: left;
        }

        .hero-stat-num {
            font-family: var(--font-head);
            font-size: 2rem;
            font-weight: 700;
            color: var(--amber);
            line-height: 1;
        }

        .hero-stat-label {
            font-size: 0.8rem;
            color: var(--muted);
            margin-top: 4px;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        .hero-scroll {
            position: absolute;
            bottom: 30px;
            left: 50%;
            transform: translateX(-50%);
            z-index: 2;
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 8px;
            color: var(--muted);
            font-size: 0.75rem;
            letter-spacing: 2px;
            text-transform: uppercase;
            animation: bounce 2s ease-in-out infinite;
        }

        @keyframes bounce {
            0%, 100% { transform: translateX(-50%) translateY(0); }
            50% { transform: translateX(-50%) translateY(8px); }
        }

        .scroll-line {
            width: 1px;
            height: 40px;
            background: linear-gradient(to bottom, var(--amber), transparent);
        }

        /* ============================================
           TRUST BAR
        ============================================ */
        .trust-bar {
            background: var(--dark-mid);
            border-top: 1px solid rgba(217,123,42,0.2);
            border-bottom: 1px solid rgba(217,123,42,0.2);
            padding: 20px 0;
        }

        .trust-bar-inner {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 0;
            flex-wrap: wrap;
        }

        .trust-item {
            display: flex;
            align-items: center;
            gap: 10px;
            padding: 8px 30px;
            border-right: 1px solid rgba(245,237,216,0.1);
        }

        .trust-item:last-child {
            border-right: none;
        }

        .trust-icon {
            font-size: 1.4rem;
        }

        .trust-text strong {
            display: block;
            font-size: 1.1rem;
            color: var(--amber);
            font-weight: 700;
            line-height: 1;
        }

        .trust-text span {
            font-size: 0.75rem;
            color: var(--muted);
            letter-spacing: 0.5px;
        }

        /* ============================================
           ADVANTAGES
        ============================================ */
        .advantages {
            padding: 100px 0;
            background: var(--dark);
        }

        .adv-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 20px;
        }

        .adv-card {
            background: var(--dark-mid);
            border: 1px solid rgba(245,237,216,0.08);
            border-radius: var(--radius-lg);
            padding: 36px 30px;
            transition: all var(--transition);
            position: relative;
            overflow: hidden;
        }

        .adv-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 3px;
            background: linear-gradient(90deg, var(--amber), var(--amber-light));
            opacity: 0;
            transition: opacity var(--transition);
        }

        .adv-card:hover {
            transform: translateY(-6px);
            border-color: rgba(217,123,42,0.3);
            box-shadow: 0 20px 60px rgba(0,0,0,0.4);
        }

        .adv-card:hover::before {
            opacity: 1;
        }

        .adv-icon {
            font-size: 2.5rem;
            margin-bottom: 20px;
            display: block;
        }

        .adv-title {
            font-family: var(--font-head);
            font-size: 1.25rem;
            color: var(--cream);
            margin-bottom: 12px;
        }

        .adv-text {
            font-size: 0.9rem;
            color: var(--muted);
            line-height: 1.7;
        }

        /* ============================================
           CABINS
        ============================================ */
        .cabins {
            padding: 100px 0;
            background: linear-gradient(180deg, var(--dark) 0%, var(--dark-mid) 100%);
        }

        .cabins-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(340px, 1fr));
            gap: 24px;
        }

        .cabin-card {
            background: var(--dark);
            border-radius: var(--radius-lg);
            overflow: hidden;
            border: 1px solid rgba(245,237,216,0.08);
            transition: all var(--transition);
        }

        .cabin-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 30px 80px rgba(0,0,0,0.5);
            border-color: rgba(217,123,42,0.3);
        }

        .cabin-img {
            position: relative;
            height: 240px;
            overflow: hidden;
        }

        .cabin-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.6s ease;
        }

        .cabin-card:hover .cabin-img img {
            transform: scale(1.08);
        }

        .cabin-badge {
            position: absolute;
            top: 16px;
            left: 16px;
            background: var(--amber);
            color: var(--dark);
            font-size: 0.75rem;
            font-weight: 700;
            padding: 6px 14px;
            border-radius: 50px;
            letter-spacing: 0.5px;
            text-transform: uppercase;
        }

        .cabin-capacity {
            position: absolute;
            top: 16px;
            right: 16px;
            background: rgba(14,10,6,0.85);
            backdrop-filter: blur(10px);
            color: var(--cream);
            font-size: 0.8rem;
            font-weight: 600;
            padding: 6px 14px;
            border-radius: 50px;
            display: flex;
            align-items: center;
            gap: 4px;
        }

        .cabin-body {
            padding: 28px;
        }

        .cabin-name {
            font-family: var(--font-head);
            font-size: 1.5rem;
            color: var(--cream);
            margin-bottom: 8px;
        }

        .cabin-tagline {
            font-size: 0.85rem;
            color: var(--amber);
            margin-bottom: 20px;
            font-style: italic;
        }

        .cabin-features {
            display: flex;
            flex-direction: column;
            gap: 8px;
            margin-bottom: 24px;
        }

        .cabin-feature {
            display: flex;
            align-items: center;
            gap: 8px;
            font-size: 0.85rem;
            color: var(--muted);
        }

        .cabin-feature .dot {
            width: 6px;
            height: 6px;
            border-radius: 50%;
            background: var(--amber);
            flex-shrink: 0;
        }

        .cabin-options {
            display: flex;
            gap: 8px;
            flex-wrap: wrap;
            margin-bottom: 24px;
        }

        .cabin-option {
            display: flex;
            align-items: center;
            gap: 4px;
            background: rgba(217,123,42,0.12);
            border: 1px solid rgba(217,123,42,0.25);
            color: var(--amber-light);
            font-size: 0.78rem;
            font-weight: 500;
            padding: 5px 12px;
            border-radius: 50px;
        }

        .cabin-footer {
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding-top: 20px;
            border-top: 1px solid rgba(245,237,216,0.08);
        }

        .cabin-price {
            display: flex;
            flex-direction: column;
        }

        .cabin-price-from {
            font-size: 0.7rem;
            color: var(--muted);
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        .cabin-price-val {
            font-family: var(--font-head);
            font-size: 1.6rem;
            color: var(--amber);
            font-weight: 700;
        }

        .cabin-price-per {
            font-size: 0.75rem;
            color: var(--muted);
        }

        /* ============================================
           TUB / POOL
        ============================================ */
        .tub-section {
            padding: 100px 0;
            background: var(--dark-mid);
            position: relative;
            overflow: hidden;
        }

        .tub-section::before {
            content: '';
            position: absolute;
            top: -100px;
            right: -100px;
            width: 500px;
            height: 500px;
            background: radial-gradient(circle, rgba(217,123,42,0.08) 0%, transparent 70%);
            pointer-events: none;
        }

        .tub-inner {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            align-items: center;
        }

        .tub-visual {
            position: relative;
            border-radius: var(--radius-lg);
            overflow: hidden;
            aspect-ratio: 4/3;
        }

        .tub-visual img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .tub-visual-overlay {
            position: absolute;
            bottom: 0;
            left: 0;
            right: 0;
            padding: 30px;
            background: linear-gradient(to top, rgba(14,10,6,0.95) 0%, transparent 100%);
        }

        .tub-visual-badge {
            display: inline-flex;
            align-items: center;
            gap: 8px;
            background: var(--amber);
            color: var(--dark);
            font-weight: 700;
            font-size: 0.9rem;
            padding: 10px 20px;
            border-radius: 50px;
        }

        .tub-content {}

        .tub-standards {
            margin-top: 30px;
            display: flex;
            flex-direction: column;
            gap: 14px;
        }

        .tub-standard {
            display: flex;
            align-items: flex-start;
            gap: 14px;
            background: rgba(245,237,216,0.04);
            border: 1px solid rgba(245,237,216,0.08);
            border-radius: var(--radius);
            padding: 16px 20px;
            transition: border-color var(--transition);
        }

        .tub-standard:hover {
            border-color: rgba(217,123,42,0.3);
        }

        .tub-standard-icon {
            font-size: 1.4rem;
            flex-shrink: 0;
        }

        .tub-standard-text strong {
            display: block;
            font-size: 0.9rem;
            color: var(--cream);
            margin-bottom: 2px;
        }

        .tub-standard-text span {
            font-size: 0.8rem;
            color: var(--muted);
        }

        /* ============================================
           TERRITORY
        ============================================ */
        .territory {
            padding: 100px 0;
            background: var(--dark);
        }

        .territory-inner {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            align-items: center;
        }

        .territory-gallery {
            display: grid;
            grid-template-columns: 1fr 1fr;
            grid-template-rows: 200px 200px;
            gap: 12px;
        }

        .t-img {
            border-radius: var(--radius);
            overflow: hidden;
        }

        .t-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }

        .t-img:hover img {
            transform: scale(1.05);
        }

        .t-img.large {
            grid-row: span 2;
        }

        .territory-features {
            margin-top: 30px;
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 16px;
        }

        .territory-feat {
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .territory-feat-icon {
            width: 44px;
            height: 44px;
            border-radius: 12px;
            background: rgba(217,123,42,0.15);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.2rem;
            flex-shrink: 0;
        }

        .territory-feat-text strong {
            display: block;
            font-size: 0.9rem;
            color: var(--cream);
        }

        .territory-feat-text span {
            font-size: 0.78rem;
            color: var(--muted);
        }

        /* ============================================
           AMENITIES
        ============================================ */
        .amenities {
            padding: 100px 0;
            background: var(--dark-mid);
        }

        .amenities-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 30px;
        }

        .amenities-group {
            background: rgba(245,237,216,0.03);
            border: 1px solid rgba(245,237,216,0.06);
            border-radius: var(--radius-lg);
            padding: 28px;
        }

        .amenities-group-title {
            display: flex;
            align-items: center;
            gap: 10px;
            font-family: var(--font-head);
            font-size: 1.1rem;
            color: var(--amber);
            margin-bottom: 20px;
            padding-bottom: 14px;
            border-bottom: 1px solid rgba(217,123,42,0.2);
        }

        .amenities-list {
            display: flex;
            flex-direction: column;
            gap: 10px;
        }

        .amenities-item {
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 0.88rem;
            color: var(--beige);
        }

        .amenities-check {
            width: 18px;
            height: 18px;
            border-radius: 50%;
            background: rgba(74,103,65,0.3);
            border: 1px solid var(--green);
            display: flex;
            align-items: center;
            justify-content: center;
            flex-shrink: 0;
            font-size: 0.65rem;
            color: #7dbf72;
        }

        /* ============================================
           HOW IT WORKS
        ============================================ */
        .how {
            padding: 100px 0;
            background: var(--dark);
        }

        .how-steps {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 0;
            position: relative;
        }

        .how-steps::before {
            content: '';
            position: absolute;
            top: 40px;
            left: calc(12.5% + 10px);
            right: calc(12.5% + 10px);
            height: 2px;
            background: linear-gradient(90deg, var(--amber), var(--amber-light), var(--amber), var(--amber-light));
            z-index: 0;
        }

        .how-step {
            text-align: center;
            padding: 0 20px;
            position: relative;
            z-index: 1;
        }

        .step-num {
            width: 80px;
            height: 80px;
            border-radius: 50%;
            background: var(--amber);
            color: var(--dark);
            font-family: var(--font-head);
            font-size: 1.8rem;
            font-weight: 900;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 24px;
            position: relative;
            z-index: 1;
            box-shadow: 0 0 0 8px var(--dark), 0 0 0 10px rgba(217,123,42,0.3);
        }

        .step-title {
            font-family: var(--font-head);
            font-size: 1.1rem;
            color: var(--cream);
            margin-bottom: 12px;
        }

        .step-text {
            font-size: 0.85rem;
            color: var(--muted);
            line-height: 1.7;
        }

        .step-icon {
            font-size: 2rem;
            margin-bottom: 8px;
        }

        /* ============================================
           PRICING
        ============================================ */
        .pricing {
            padding: 100px 0;
            background: var(--dark-mid);
        }

        .pricing-table {
            width: 100%;
            border-collapse: separate;
            border-spacing: 0;
            border-radius: var(--radius-lg);
            overflow: hidden;
            border: 1px solid rgba(245,237,216,0.08);
            margin-bottom: 40px;
        }

        .pricing-table th {
            background: rgba(217,123,42,0.15);
            color: var(--amber);
            font-size: 0.8rem;
            text-transform: uppercase;
            letter-spacing: 1px;
            padding: 16px 20px;
            text-align: left;
            font-weight: 600;
            border-bottom: 1px solid rgba(217,123,42,0.2);
        }

        .pricing-table td {
            padding: 18px 20px;
            font-size: 0.9rem;
            color: var(--beige);
            border-bottom: 1px solid rgba(245,237,216,0.05);
        }

        .pricing-table tr:last-child td {
            border-bottom: none;
        }

        .pricing-table tr:hover td {
            background: rgba(245,237,216,0.03);
        }

        .price-val {
            font-weight: 700;
            color: var(--amber);
            font-size: 1rem;
        }

        .pricing-notes {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 16px;
        }

        .pricing-note {
            display: flex;
            align-items: flex-start;
            gap: 10px;
            background: rgba(245,237,216,0.04);
            border-radius: var(--radius);
            padding: 16px;
            font-size: 0.85rem;
            color: var(--muted);
        }

        .pricing-note-icon {
            font-size: 1.2rem;
            flex-shrink: 0;
        }

        /* ============================================
           SCENARIOS
        ============================================ */
        .scenarios {
            padding: 100px 0;
            background: var(--dark);
        }

        .scenarios-tabs {
            display: flex;
            gap: 8px;
            margin-bottom: 40px;
            flex-wrap: wrap;
        }

        .scenario-tab {
            padding: 10px 24px;
            border-radius: 50px;
            font-size: 0.9rem;
            font-weight: 500;
            cursor: pointer;
            border: 1px solid rgba(245,237,216,0.15);
            background: transparent;
            color: var(--muted);
            transition: all var(--transition);
            font-family: var(--font-body);
        }

        .scenario-tab.active,
        .scenario-tab:hover {
            background: var(--amber);
            color: var(--dark);
            border-color: var(--amber);
        }

        .scenarios-panels {}

        .scenario-panel {
            display: none;
        }

        .scenario-panel.active {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
        }

        .scenario-img {
            border-radius: var(--radius-lg);
            overflow: hidden;
            aspect-ratio: 4/3;
        }

        .scenario-img img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .scenario-content {}

        .scenario-icon {
            font-size: 3rem;
            margin-bottom: 20px;
        }

        .scenario-title {
            font-family: var(--font-head);
            font-size: 2rem;
            color: var(--cream);
            margin-bottom: 16px;
        }

        .scenario-text {
            font-size: 0.95rem;
            color: var(--muted);
            line-height: 1.8;
            margin-bottom: 24px;
        }

        .scenario-list {
            display: flex;
            flex-direction: column;
            gap: 10px;
            margin-bottom: 30px;
        }

        .scenario-list li {
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 0.9rem;
            color: var(--beige);
        }

        .scenario-list li::before {
            content: '✓';
            width: 22px;
            height: 22px;
            border-radius: 50%;
            background: rgba(217,123,42,0.2);
            color: var(--amber);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 0.75rem;
            font-weight: 700;
            flex-shrink: 0;
        }

        /* ============================================
           LOYALTY
        ============================================ */
        .loyalty {
            padding: 100px 0;
            background: linear-gradient(135deg, var(--dark-mid) 0%, var(--brown) 100%);
            position: relative;
            overflow: hidden;
        }

        .loyalty::before {
            content: '🐾';
            position: absolute;
            font-size: 20rem;
            opacity: 0.04;
            right: -50px;
            top: -50px;
            pointer-events: none;
        }

        .loyalty-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 24px;
        }

        .loyalty-card {
            background: rgba(245,237,216,0.05);
            border: 1px solid rgba(245,237,216,0.1);
            border-radius: var(--radius-lg);
            padding: 36px 28px;
            text-align: center;
            transition: all var(--transition);
        }

        .loyalty-card:hover {
            background: rgba(217,123,42,0.1);
            border-color: rgba(217,123,42,0.3);
            transform: translateY(-4px);
        }

        .loyalty-icon {
            font-size: 3rem;
            margin-bottom: 20px;
        }

        .loyalty-title {
            font-family: var(--font-head);
            font-size: 1.3rem;
            color: var(--amber);
            margin-bottom: 12px;
        }

        .loyalty-text {
            font-size: 0.88rem;
            color: var(--muted);
            line-height: 1.7;
        }

        /* ============================================
           REVIEWS
        ============================================ */
        .reviews {
            padding: 100px 0;
            background: var(--dark);
        }

        .reviews-slider {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 24px;
            margin-bottom: 40px;
        }

        .review-card {
            background: var(--dark-mid);
            border: 1px solid rgba(245,237,216,0.06);
            border-radius: var(--radius-lg);
            padding: 30px;
            transition: all var(--transition);
            position: relative;
        }

        .review-card:hover {
            border-color: rgba(217,123,42,0.2);
            transform: translateY(-4px);
        }

        .review-card::before {
            content: '"';
            position: absolute;
            top: 20px;
            right: 24px;
            font-family: var(--font-head);
            font-size: 5rem;
            color: rgba(217,123,42,0.15);
            line-height: 1;
        }

        .review-stars {
            display: flex;
            gap: 4px;
            margin-bottom: 16px;
        }

        .star {
            color: var(--amber);
            font-size: 1rem;
        }

        .review-text {
            font-size: 0.9rem;
            color: var(--beige);
            line-height: 1.8;
            margin-bottom: 20px;
            font-style: italic;
        }

        .review-author {
            display: flex;
            align-items: center;
            gap: 12px;
        }

        .review-avatar {
            width: 44px;
            height: 44px;
            border-radius: 50%;
            background: rgba(217,123,42,0.2);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.2rem;
            flex-shrink: 0;
        }

        .review-name {
            font-weight: 600;
            font-size: 0.9rem;
            color: var(--cream);
        }

        .review-date {
            font-size: 0.75rem;
            color: var(--muted);
        }

        .review-response {
            margin-top: 16px;
            padding: 14px 16px;
            background: rgba(217,123,42,0.08);
            border-left: 3px solid var(--amber);
            border-radius: 0 8px 8px 0;
            font-size: 0.8rem;
            color: var(--muted);
        }

        .review-response strong {
            color: var(--amber);
            font-size: 0.75rem;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        .reviews-cta {
            text-align: center;
        }

        /* ============================================
           STANDARDS
        ============================================ */
        .standards {
            padding: 100px 0;
            background: var(--dark-mid);
        }

        .standards-inner {
            display: grid;
            grid-template-columns: 1fr 1.4fr;
            gap: 60px;
            align-items: start;
        }

        .standards-visual {
            position: sticky;
            top: 100px;
        }

        .standards-img {
            border-radius: var(--radius-lg);
            overflow: hidden;
            margin-bottom: 20px;
        }

        .standards-img img {
            width: 100%;
            aspect-ratio: 4/3;
            object-fit: cover;
        }

        .standards-promise {
            background: var(--dark);
            border: 1px solid rgba(217,123,42,0.2);
            border-radius: var(--radius);
            padding: 24px;
        }

        .standards-promise p {
            font-size: 0.88rem;
            color: var(--muted);
            line-height: 1.7;
        }

        .standards-promise strong {
            color: var(--amber);
        }

        .checklist-section {
            margin-bottom: 36px;
        }

        .checklist-title {
            font-family: var(--font-head);
            font-size: 1.1rem;
            color: var(--amber);
            margin-bottom: 16px;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .checklist {
            display: flex;
            flex-direction: column;
            gap: 10px;
        }

        .check-item {
            display: flex;
            align-items: flex-start;
            gap: 12px;
            font-size: 0.875rem;
            color: var(--beige);
            padding: 10px 14px;
            background: rgba(245,237,216,0.03);
            border-radius: 8px;
            border: 1px solid rgba(245,237,216,0.05);
        }

        .check-box {
            width: 20px;
            height: 20px;
            border-radius: 6px;
            background: rgba(74,103,65,0.25);
            border: 1.5px solid var(--green);
            display: flex;
            align-items: center;
            justify-content: center;
            flex-shrink: 0;
            color: #7dbf72;
            font-size: 0.7rem;
            font-weight: 700;
        }

        /* ============================================
           FAQ
        ============================================ */
        .faq {
            padding: 100px 0;
            background: var(--dark);
        }

        .faq-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 0 40px;
        }

        .faq-col {}

        .faq-item {
            border-bottom: 1px solid rgba(245,237,216,0.08);
        }

        .faq-question {
            width: 100%;
            background: none;
            border: none;
            text-align: left;
            padding: 22px 0;
            font-family: var(--font-body);
            font-size: 0.95rem;
            font-weight: 500;
            color: var(--cream);
            cursor: pointer;
            display: flex;
            align-items: flex-start;
            gap: 14px;
            transition: color var(--transition);
        }

        .faq-question:hover {
            color: var(--amber);
        }

        .faq-icon {
            width: 24px;
            height: 24px;
            border-radius: 50%;
            background: rgba(217,123,42,0.15);
            border: 1px solid rgba(217,123,42,0.3);
            display: flex;
            align-items: center;
            justify-content: center;
            flex-shrink: 0;
            font-size: 1rem;
            color: var(--amber);
            transition: all var(--transition);
            margin-top: 2px;
        }

        .faq-item.open .faq-icon {
            background: var(--amber);
            color: var(--dark);
            transform: rotate(45deg);
        }

        .faq-answer {
            max-height: 0;
            overflow: hidden;
            transition: max-height 0.4s ease, padding 0.4s ease;
        }

        .faq-answer-inner {
            padding-bottom: 20px;
            font-size: 0.875rem;
            color: var(--muted);
            line-height: 1.8;
            padding-left: 38px;
        }

        .faq-item.open .faq-answer {
            max-height: 400px;
        }

        /* ============================================
           CONTACTS
        ============================================ */
        .contacts {
            padding: 100px 0;
            background: var(--dark-mid);
        }

        .contacts-inner {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
        }

        .contact-block {
            margin-bottom: 36px;
        }

        .contact-block-title {
            font-family: var(--font-head);
            font-size: 1.1rem;
            color: var(--amber);
            margin-bottom: 16px;
        }

        .contact-items {
            display: flex;
            flex-direction: column;
            gap: 12px;
        }

        .contact-item {
            display: flex;
            align-items: center;
            gap: 14px;
            font-size: 0.9rem;
            color: var(--beige);
        }

        .contact-item-icon {
            width: 44px;
            height: 44px;
            border-radius: 12px;
            background: rgba(217,123,42,0.12);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.2rem;
            flex-shrink: 0;
        }

        .contact-item a {
            color: var(--beige);
            transition: color var(--transition);
        }

        .contact-item a:hover {
            color: var(--amber);
        }

        .messenger-buttons {
            display: flex;
            gap: 12px;
            flex-wrap: wrap;
        }

        .messenger-btn {
            display: flex;
            align-items: center;
            gap: 8px;
            padding: 12px 20px;
            border-radius: 50px;
            font-size: 0.85rem;
            font-weight: 600;
            transition: all var(--transition);
            border: none;
            cursor: pointer;
            font-family: var(--font-body);
        }

        .whatsapp-btn {
            background: #25D366;
            color: white;
        }

        .whatsapp-btn:hover {
            background: #1ebe5a;
            transform: translateY(-2px);
        }

        .telegram-btn {
            background: #2AABEE;
            color: white;
        }

        .telegram-btn:hover {
            background: #1a9bd8;
            transform: translateY(-2px);
        }

        .vk-btn {
            background: #4C75A3;
            color: white;
        }

        .vk-btn:hover {
            background: #3d6190;
            transform: translateY(-2px);
        }

        .map-container {
            border-radius: var(--radius-lg);
            overflow: hidden;
            background: rgba(245,237,216,0.05);
            border: 1px solid rgba(245,237,216,0.08);
            height: 350px;
            display: flex;
            align-items: center;
            justify-content: center;
            flex-direction: column;
            gap: 16px;
            color: var(--muted);
            font-size: 0.9rem;
        }

        .map-placeholder {
            font-size: 3rem;
        }

        .how-to-get {
            display: flex;
            flex-direction: column;
            gap: 12px;
        }

        .how-to-item {
            display: flex;
            align-items: flex-start;
            gap: 12px;
            font-size: 0.875rem;
            color: var(--muted);
        }

        .how-to-icon {
            font-size: 1.2rem;
            flex-shrink: 0;
            margin-top: 2px;
        }

        /* ============================================
           BOOKING FORM
        ============================================ */
        .booking-section {
            padding: 100px 0;
            background: linear-gradient(135deg, var(--dark) 0%, var(--brown) 50%, var(--dark) 100%);
            position: relative;
            overflow: hidden;
        }

        .booking-section::before {
            content: '';
            position: absolute;
            inset: 0;
            background: radial-gradient(ellipse at center, rgba(217,123,42,0.08) 0%, transparent 70%);
            pointer-events: none;
        }

        .booking-inner {
            display: grid;
            grid-template-columns: 1fr 1.4fr;
            gap: 60px;
            align-items: start;
        }

        .booking-promo {}

        .booking-promo-title {
            font-family: var(--font-head);
            font-size: 2.5rem;
            color: var(--cream);
            margin-bottom: 16px;
            line-height: 1.2;
        }

        .booking-promo-title span {
            color: var(--amber);
        }

        .booking-promo-text {
            font-size: 0.95rem;
            color: var(--muted);
            line-height: 1.7;
            margin-bottom: 30px;
        }

        .booking-guarantees {
            display: flex;
            flex-direction: column;
            gap: 12px;
        }

        .booking-guarantee {
            display: flex;
            align-items: center;
            gap: 10px;
            font-size: 0.875rem;
            color: var(--beige);
        }

        .booking-guarantee-icon {
            font-size: 1.1rem;
        }

        .booking-form {
            background: var(--dark-mid);
            border: 1px solid rgba(245,237,216,0.08);
            border-radius: var(--radius-lg);
            padding: 40px;
        }

        .booking-form-title {
            font-family: var(--font-head);
            font-size: 1.6rem;
            color: var(--cream);
            margin-bottom: 6px;
        }

        .booking-form-sub {
            font-size: 0.85rem;
            color: var(--muted);
            margin-bottom: 30px;
        }

        .form-row {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 16px;
        }

        .form-group {
            margin-bottom: 16px;
        }

        .form-group.full {
            grid-column: span 2;
        }

        .form-label {
            display: block;
            font-size: 0.78rem;
            font-weight: 600;
            color: var(--muted);
            text-transform: uppercase;
            letter-spacing: 0.5px;
            margin-bottom: 8px;
        }

        .form-input,
        .form-select,
        .form-textarea {
            width: 100%;
            padding: 14px 16px;
            background: rgba(245,237,216,0.05);
            border: 1px solid rgba(245,237,216,0.12);
            border-radius: var(--radius);
            color: var(--cream);
            font-family: var(--font-body);
            font-size: 0.9rem;
            transition: all var(--transition);
            outline: none;
            -webkit-appearance: none;
        }

        .form-input::placeholder,
        .form-textarea::placeholder {
            color: rgba(184,169,154,0.5);
        }

        .form-input:focus,
        .form-select:focus,
        .form-textarea:focus {
            border-color: var(--amber);
            background: rgba(217,123,42,0.05);
            box-shadow: 0 0 0 3px rgba(217,123,42,0.1);
        }

        .form-select option {
            background: var(--dark-mid);
            color: var(--cream);
        }

        .form-textarea {
            height: 90px;
            resize: vertical;
        }

        .form-checkbox {
            display: flex;
            align-items: flex-start;
            gap: 10px;
            cursor: pointer;
            font-size: 0.8rem;
            color: var(--muted);
            margin-bottom: 20px;
        }

        .form-checkbox input {
            width: 18px;
            height: 18px;
            flex-shrink: 0;
            margin-top: 2px;
            accent-color: var(--amber);
        }

        .form-checkbox a {
            color: var(--amber);
        }

        .form-submit {
            width: 100%;
            padding: 18px;
            font-size: 1rem;
        }

        .form-note {
            text-align: center;
            font-size: 0.78rem;
            color: var(--muted);
            margin-top: 16px;
        }

        /* ============================================
           FLOATING CTA
        ============================================ */
        .floating-cta {
            position: fixed;
            bottom: 30px;
            right: 30px;
            z-index: 900;
            display: flex;
            flex-direction: column;
            gap: 10px;
            align-items: flex-end;
        }

        .floating-btn {
            width: 56px;
            height: 56px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1.4rem;
            cursor: pointer;
            border: none;
            transition: all var(--transition);
            text-decoration: none;
            box-shadow: 0 4px 20px rgba(0,0,0,0.4);
        }

        .floating-btn:hover {
            transform: scale(1.1);
        }

        .floating-main {
            width: 64px;
            height: 64px;
            font-size: 1.6rem;
            background: var(--amber);
            color: var(--dark);
        }

        .floating-wa {
            background: #25D366;
        }

        .floating-tg {
            background: #2AABEE;
        }

        .floating-call {
            background: var(--red);
        }

        .floating-sub {
            display: flex;
            flex-direction: column;
            gap: 8px;
            opacity: 0;
            transform: translateY(10px);
            transition: all var(--transition);
            pointer-events: none;
        }

        .floating-cta.expanded .floating-sub {
            opacity: 1;
            transform: translateY(0);
            pointer-events: all;
        }

        /* ============================================
           FOOTER
        ============================================ */
        footer {
            background: var(--black);
            padding: 50px 0 30px;
            border-top: 1px solid rgba(245,237,216,0.06);
        }

        .footer-inner {
            display: grid;
            grid-template-columns: 2fr 1fr 1fr 1fr;
            gap: 40px;
            margin-bottom: 40px;
        }

        .footer-brand {}

        .footer-logo {
            font-family: var(--font-head);
            font-size: 1.5rem;
            font-weight: 900;
            color: var(--cream);
            margin-bottom: 16px;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .footer-logo span {
            color: var(--amber);
        }

        .footer-desc {
            font-size: 0.85rem;
            color: var(--muted);
            line-height: 1.7;
            margin-bottom: 20px;
        }

        .footer-social {
            display: flex;
            gap: 10px;
        }

        .footer-social a {
            width: 38px;
            height: 38px;
            border-radius: 10px;
            background: rgba(245,237,216,0.06);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 1rem;
            transition: all var(--transition);
        }

        .footer-social a:hover {
            background: var(--amber);
            color: var(--dark);
        }

        .footer-col-title {
            font-weight: 700;
            font-size: 0.85rem;
            color: var(--cream);
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 16px;
        }

        .footer-links {
            display: flex;
            flex-direction: column;
            gap: 10px;
        }

        .footer-links a {
            font-size: 0.85rem;
            color: var(--muted);
            transition: color var(--transition);
        }

        .footer-links a:hover {
            color: var(--amber);
        }

        .footer-bottom {
            display: flex;
            align-items: center;
            justify-content: space-between;
            padding-top: 30px;
            border-top: 1px solid rgba(245,237,216,0.06);
            font-size: 0.78rem;
            color: var(--muted);
            flex-wrap: wrap;
            gap: 10px;
        }

        .footer-docs {
            display: flex;
            gap: 20px;
        }

        .footer-docs a {
            color: var(--muted);
            transition: color var(--transition);
        }

        .footer-docs a:hover {
            color: var(--amber);
        }

        /* ============================================
           NOTIFICATION
        ============================================ */
        .notification {
            position: fixed;
            top: 100px;
            right: 20px;
            z-index: 2000;
            background: var(--dark-mid);
            border: 1px solid rgba(217,123,42,0.3);
            border-radius: var(--radius);
            padding: 20px 24px;
            max-width: 320px;
            box-shadow: var(--shadow);
            transform: translateX(400px);
            transition: transform 0.4s ease;
        }

        .notification.show {
            transform: translateX(0);
        }

        .notification-icon {
            font-size: 2rem;
            margin-bottom: 8px;
        }

        .notification-title {
            font-weight: 700;
            color: var(--amber);
            margin-bottom: 4px;
        }

        .notification-text {
            font-size: 0.85rem;
            color: var(--muted);
        }

        /* 
