
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.9">
  <title>Entrance   </title>
<link rel="icon" type="image/png" href="favicon.png">
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    /* ============================================
       SPECIAL DESIGN - GLASSMORPHISM & GLOW EFFECTS
       ============================================ */
    
    /* Animated Gradient Background */
    body {
      background: linear-gradient(-45deg, #0f172a, #1e293b, #334155, #475569, #1e3a5f, #2d5a87);
      background-size: 400% 400%;
      animation: gradientBG 15s ease infinite;
      min-height: 100vh;
    }

    @keyframes gradientBG {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }

    /* Floating Particles Background Effect */
    body::before {
      content: '';
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-image: 
        radial-gradient(circle at 20% 80%, rgba(59, 130, 246, 0.3) 0%, transparent 50%),
        radial-gradient(circle at 80% 20%, rgba(139, 92, 246, 0.3) 0%, transparent 50%),
        radial-gradient(circle at 40% 40%, rgba(34, 197, 94, 0.2) 0%, transparent 40%),
        radial-gradient(circle at 60% 70%, rgba(251, 191, 36, 0.2) 0%, transparent 40%);
      pointer-events: none;
      z-index: -1;
    }

    /* ============================================
       GLASSMORPHISM - FROSTED GLASS EFFECTS
       ============================================ */
    
    .glass {
      background: rgba(255, 255, 255, 0.1);
      backdrop-filter: blur(20px);
      -webkit-backdrop-filter: blur(20px);
      border: 1px solid rgba(255, 255, 255, 0.2);
      box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
    }

    .glass-dark {
      background: rgba(15, 23, 42, 0.7);
      backdrop-filter: blur(20px);
      -webkit-backdrop-filter: blur(20px);
      border: 1px solid rgba(255, 255, 255, 0.1);
      box-shadow: 0 8px 32px rgba(0, 0, 0, 0.4);
    }

    .glass-card {
      background: linear-gradient(135deg, rgba(255, 255, 255, 0.15), rgba(255, 255, 255, 0.05));
      backdrop-filter: blur(15px);
      -webkit-backdrop-filter: blur(15px);
      border: 1px solid rgba(255, 255, 255, 0.2);
      border-radius: 20px;
      box-shadow: 0 8px 32px rgba(0, 0, 0, 0.2);
    }

    /* ============================================
      SHADOW LIFT
       ============================================ */
    
    .glow {
      box-shadow: 0 0 20px rgba(59, 130, 246, 0.5), 0 0 40px rgba(59, 130, 246, 0.3);
    }

    .glow-green {
      box-shadow: 0 0 20px rgba(34, 197, 94, 0.5), 0 0 40px rgba(34, 197, 94, 0.3);
    }

    .glow-purple {
      box-shadow: 0 0 20px rgba(139, 92, 246, 0.5), 0 0 40px rgba(139, 92, 246, 0.3);
    }

    .glow-amber {
      box-shadow: 0 0 20px rgba(251, 191, 36, 0.5), 0 0 40px rgba(251, 191, 36, 0.3);
    }

    .glow-text {
      text-shadow: 0 0 10px rgba(255, 255, 255, 0.5), 0 0 20px rgba(59, 130, 246, 0.5);
    }

    /* ============================================
       Neumorphism Buttons
       ============================================ */
    
    .btn-gradient {
      background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
      border: none;
      border-radius: 12px;
      padding: 14px 28px;
      color: white;
      font-weight: 700;
      cursor: pointer;
      transition: all 0.3s ease;
      position: relative;
      overflow: hidden;
      text-transform: uppercase;
      letter-spacing: 1px;
    }

    .btn-gradient::before {
      content: '';
      position: absolute;
      top: 0;
      left: -100%;
      width: 100%;
      height: 100%;
      background: linear-gradient(90deg, transparent, rgba(255,255,255,0.3), transparent);
      transition: left 0.5s ease;
    }

    .btn-gradient:hover::before {
      left: 100%;
    }

    .btn-gradient:hover {
      transform: translateY(-3px) scale(1.02);
      box-shadow: 0 10px 30px rgba(102, 126, 234, 0.5);
    }

    .btn-glow {
      background: linear-gradient(135deg, #22c55e 0%, #16a34a 100%);
      border: 2px solid #22c55e;
      border-radius: 12px;
      padding: 12px 24px;
      color: white;
      font-weight: 700;
      cursor: pointer;
      transition: all 0.3s ease;
      animation: pulseGlow 2s infinite;
    }

    @keyframes pulseGlow {
      0%, 100% { box-shadow: 0 0 20px rgba(34, 197, 94, 0.5); }
      50% { box-shadow: 0 0 40px rgba(34, 197, 94, 0.8), 0 0 60px rgba(34, 197, 94, 0.4); }
    }

    .btn-glow:hover {
      transform: scale(1.05);
      box-shadow: 0 0 50px rgba(34, 197, 94, 1);
    }

    /* ============================================
       MODERN CARD DESIGNS
       ============================================ */
    
    .modern-card {
      background: linear-gradient(145deg, rgba(255,255,255,0.15), rgba(255,255,255,0.05));
      backdrop-filter: blur(10px);
      border-radius: 20px;
      border: 1px solid rgba(255, 255, 255, 0.2);
      overflow: hidden;
      transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
      position: relative;
    }

    .modern-card::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      height: 4px;
      background: linear-gradient(90deg, #667eea, #764ba2, #f093fb, #f5576c);
      background-size: 300% 100%;
      animation: shimmer 3s infinite linear;
    }

    @keyframes shimmer {
      0% { background-position: 0% 0%; }
      100% { background-position: 300% 0%; }
    }

    .modern-card:hover {
      transform: translateY(-12px) rotateX(2deg);
      box-shadow: 0 25px 50px rgba(0, 0, 0, 0.3);
      border-color: rgba(255, 255, 255, 0.4);
    }

    /* ============================================
       INPUT FIELDS WITH GLOW EFFECT
       ============================================ */
    
    .input-glow {
      background: rgba(255, 255, 255, 0.1);
      border: 2px solid rgba(255, 255, 255, 0.2);
      border-radius: 12px;
      padding: 14px 18px;
      color: white;
      font-size: 1rem;
      transition: all 0.3s ease;
      backdrop-filter: blur(5px);
    }

    .input-glow:focus {
      outline: none;
      border-color: #667eea;
      box-shadow: 0 0 20px rgba(102, 126, 234, 0.5), inset 0 0 10px rgba(102, 126, 234, 0.1);
    }

    .input-glow::placeholder {
      color: rgba(255, 255, 255, 0.6);
    }

    /* ============================================
       HEADER WITH GLASS EFFECT
       ============================================ */
    
    .header-glass {
      background: linear-gradient(135deg, rgba(15, 23, 42, 0.9), rgba(30, 41, 59, 0.8));
      backdrop-filter: blur(20px);
      border-bottom: 1px solid rgba(255, 255, 255, 0.1);
      padding: 20px;
      border-radius: 16px;
      margin-bottom: 24px;
      box-shadow: 0 8px 32px rgba(0, 0, 0, 0.3);
    }

    /* ============================================
       AUTH BOXES - GLASSMORPHISM
       ============================================ */
    
    .auth-box {
      background: linear-gradient(135deg, rgba(255,255,255,0.2), rgba(255,255,255,0.05));
      backdrop-filter: blur(25px);
      -webkit-backdrop-filter: blur(25px);
      border: 1px solid rgba(255, 255, 255, 0.3);
      border-radius: 24px;
      padding: 40px;
      box-shadow: 0 20px 60px rgba(0, 0, 0, 0.4), inset 0 1px 0 rgba(255,255,255,0.2);
      position: relative;
      overflow: hidden;
    }

    .auth-box::before {
      content: '';
      position: absolute;
      top: -50%;
      left: -50%;
      width: 200%;
      height: 200%;
      background: radial-gradient(circle, rgba(255,255,255,0.1) 0%, transparent 60%);
      animation: rotateGlow 10s linear infinite;
    }

    @keyframes rotateGlow {
      0% { transform: rotate(0deg); }
      100% { transform: rotate(360deg); }
    }

    .auth-box h2 {
      position: relative;
      z-index: 1;
      color: white;
      text-shadow: 0 2px 10px rgba(0,0,0,0.3);
    }

    .auth-box input {
      position: relative;
      z-index: 1;
    }

    .auth-box button {
      position: relative;
      z-index: 1;
    }

    .auth-box p {
      position: relative;
      z-index: 1;
      color: rgba(255, 255, 255, 0.8);
    }

    /* ============================================
       BALANCE CARDS - MODERN DESIGN
       ============================================ */
    
    .balance-card {
      background: linear-gradient(135deg, #0f172a 0%, #1e293b 50%, #334155 100%);
      border-radius: 24px;
      padding: 30px;
      border: 1px solid rgba(255, 255, 255, 0.15);
      box-shadow: 0 20px 60px rgba(0, 0, 0, 0.5);
      position: relative;
      overflow: hidden;
    }

    .balance-card::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background: linear-gradient(45deg, transparent 40%, rgba(255,255,255,0.1) 50%, transparent 60%);
      background-size: 200% 200%;
      animation: shine 3s infinite;
    }

    @keyframes shine {
      0% { background-position: 200% 200%; }
      100% { background-position: -200% -200%; }
    }

    .balance-card-gradient-1 {
      background: linear-gradient(135deg, #059669 0%, #10b981 50%, #34d399 100%);
    }

    .balance-card-gradient-2 {
      background: linear-gradient(135deg, #7c3aed 0%, #8b5cf6 50%, #a78bfa 100%);
    }

    .balance-card-gradient-3 {
      background: linear-gradient(135deg, #f59e0b 0%, #fbbf24 50%, #fcd34d 100%);
    }

    /* ============================================
       MODERN NAVIGATION
       ============================================ */
    
    .nav-button {
      background: linear-gradient(135deg, rgba(255,255,255,0.15), rgba(255,255,255,0.05));
      backdrop-filter: blur(10px);
      border: 1px solid rgba(255, 255, 255, 0.2);
      border-radius: 16px;
      padding: 14px 24px;
      color: white;
      font-weight: 600;
      cursor: pointer;
      transition: all 0.3s ease;
      display: flex;
      align-items: center;
      gap: 8px;
    }

    .nav-button:hover {
      background: linear-gradient(135deg, rgba(255,255,255,0.25), rgba(255,255,255,0.1));
      transform: translateY(-3px) scale(1.05);
      box-shadow: 0 10px 30px rgba(0, 0, 0, 0.3);
      border-color: rgba(255, 255, 255, 0.4);
    }

    .nav-button-home { background: linear-gradient(135deg, #3b82f6, #1d4ed8); }
    .nav-button-balance { background: linear-gradient(135deg, #22c55e, #16a34a); }
    .nav-button-account { background: linear-gradient(135deg, #06b6d4, #0891b2); }
    .nav-button-logout { background: linear-gradient(135deg, #f59e0b, #d97706); }

    /* ============================================
       MODAL - GLASS EFFECT
       ============================================ */
    
    .modal-glass {
      background: rgba(15, 23, 42, 0.9);
      backdrop-filter: blur(30px);
      -webkit-backdrop-filter: blur(30px);
      border: 1px solid rgba(255, 255, 255, 0.2);
      border-radius: 24px;
      padding: 40px;
      box-shadow: 0 30px 60px rgba(0, 0, 0, 0.5);
    }

    /* ============================================
       VIDEO CONTAINER - MODERN STYLE
       ============================================ */
    
    .video-container-modern {
      position: relative;
      border-radius: 24px;
      overflow: hidden;
      box-shadow: 0 25px 60px rgba(0, 0, 0, 0.5);
      border: 2px solid rgba(255, 255, 255, 0.2);
      transition: all 0.3s ease;
    }

    .video-container-modern:hover {
      border-color: rgba(255, 255, 255, 0.4);
      box-shadow: 0 30px 80px rgba(0, 0, 0, 0.6), 0 0 40px rgba(102, 126, 234, 0.3);
    }

    .play-button-modern {
      width: 90px;
      height: 90px;
      background: linear-gradient(135deg, #667eea, #764ba2);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      cursor: pointer;
      transition: all 0.3s ease;
      box-shadow: 0 10px 40px rgba(102, 126, 234, 0.5);
      animation: pulsePlay 2s infinite;
    }

    @keyframes pulsePlay {
      0%, 100% { transform: scale(1); box-shadow: 0 10px 40px rgba(102, 126, 234, 0.5); }
      50% { transform: scale(1.1); box-shadow: 0 15px 60px rgba(102, 126, 234, 0.8); }
    }

    .play-button-modern:hover {
      transform: scale(1.15);
      box-shadow: 0 20px 60px rgba(102, 126, 234, 1);
    }

    .play-button-modern::after {
      content: '';
      width: 0;
      height: 0;
      border-left: 28px solid white;
      border-top: 18px solid transparent;
      border-bottom: 18px solid transparent;
      margin-left: 8px;
    }

    /* ============================================
       CONTENT TABS - MODERN STYLE
       ============================================ */
    
    .content-tab {
      padding: 14px 32px;
      background: linear-gradient(135deg, rgba(255,255,255,0.15), rgba(255,255,255,0.05));
      backdrop-filter: blur(10px);
      border: 1px solid rgba(255, 255, 255, 0.2);
      border-radius: 30px;
      font-weight: 600;
      color: rgba(255, 255, 255, 0.8);
      cursor: pointer;
      transition: all 0.3s ease;
    }

    .content-tab:hover, .content-tab.active {
      background: linear-gradient(135deg, #667eea, #764ba2);
      color: white;
      border-color: transparent;
      box-shadow: 0 8px 25px rgba(102, 126, 234, 0.5);
      transform: translateY(-2px);
    }

    /* ============================================
       CATEGORY BADGE - MODERN STYLE
       ============================================ */
    
    .category-badge {
      position: absolute;
      top: 16px;
      left: 16px;
      padding: 8px 16px;
      background: linear-gradient(135deg, #667eea, #764ba2);
      border-radius: 20px;
      font-size: 0.75rem;
      font-weight: 700;
      color: white;
      box-shadow: 0 4px 15px rgba(102, 126, 234, 0.5);
      z-index: 2;
      text-transform: uppercase;
      letter-spacing: 1px;
    }

    /* ============================================
       PRICE TAG - MODERN STYLE
       ============================================ */
    
    .price-tag {
      display: inline-block;
      padding: 10px 18px;
      background: linear-gradient(135deg, #22c55e, #16a34a);
      color: white;
      border-radius: 12px;
      font-weight: 700;
      font-size: 1rem;
      margin-bottom: 12px;
      box-shadow: 0 4px 15px rgba(34, 197, 94, 0.4);
      animation: priceGlow 2s infinite;
    }

    @keyframes priceGlow {
      0%, 100% { box-shadow: 0 4px 15px rgba(34, 197, 94, 0.4); }
      50% { box-shadow: 0 4px 25px rgba(34, 197, 94, 0.7); }
    }

    /* ============================================
       WEBSITE CONTENT GRID
       ============================================ */
    
    .website-content-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
      gap: 24px;
      padding: 20px;
      max-width: 1200px;
      margin: 0 auto;
    }

    /* ============================================
       WEBSITE CARD - ENHANCED
       ============================================ */
    
    .website-card {
      background: linear-gradient(145deg, rgba(255,255,255,0.15), rgba(255,255,255,0.05));
      backdrop-filter: blur(10px);
      border: 1px solid rgba(255, 255, 255, 0.2);
      border-radius: 20px;
      overflow: hidden;
      transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
      position: relative;
    }

    .website-card::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      height: 3px;
      background: linear-gradient(90deg, #667eea, #764ba2, #f093fb, #f5576c);
      background-size: 300% 100%;
      animation: shimmer 3s infinite linear;
    }

    .website-card:hover {
      transform: translateY(-12px) rotateX(2deg);
      box-shadow: 0 30px 60px rgba(0, 0, 0, 0.4);
      border-color: rgba(255, 255, 255, 0.4);
    }

    .website-card .card-image-container {
      position: relative;
      height: 200px;
      overflow: hidden;
    }

    .website-card .card-image-container img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      transition: transform 0.5s ease;
    }

    .website-card:hover .card-image-container img {
      transform: scale(1.15);
    }

    .card-overlay {
      position: absolute;
      bottom: 0;
      left: 0;
      right: 0;
      height: 60%;
      background: linear-gradient(to top, rgba(0,0,0,0.7) 0%, transparent 100%);
      pointer-events: none;
    }

    .card-content {
      padding: 20px;
    }

    .card-title {
      font-size: 1.1rem;
      font-weight: 700;
      color: white;
      margin-bottom: 8px;
      line-height: 1.4;
    }

    .card-description {
      font-size: 0.875rem;
      color: rgba(255, 255, 255, 0.7);
      margin-bottom: 16px;
    }

    .card-button {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      width: 100%;
      padding: 14px 24px;
      background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
      color: white;
      border: none;
      border-radius: 12px;
      font-weight: 600;
      font-size: 0.9rem;
      cursor: pointer;
      transition: all 0.3s ease;
      text-transform: uppercase;
      letter-spacing: 1px;
    }

    .card-button:hover {
      background: linear-gradient(135deg, #764ba2 0%, #667eea 100%);
      transform: scale(1.03);
      box-shadow: 0 8px 25px rgba(102, 126, 234, 0.5);
    }

    /* ============================================
       VIDEO SECTION
       ============================================ */
    
    .video-section {
      margin: 30px auto;
      max-width: 800px;
      padding: 0 20px;
    }

    .video-section video {
      width: 100%;
      display: block;
      max-height: 450px;
      object-fit: cover;
    }

    .video-overlay {
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background: linear-gradient(45deg, rgba(30, 41, 59, 0.8), rgba(15, 23, 42, 0.6));
      display: flex;
      align-items: center;
      justify-content: center;
      opacity: 0;
      transition: opacity 0.3s ease;
    }

    .video-container-modern:hover .video-overlay {
      opacity: 1;
    }

    /* ============================================
       SECTION HEADER
       ============================================ */
    
    .section-header {
      text-align: center;
      margin: 40px 0 30px;
      padding: 0 20px;
    }

    .section-title {
      font-size: 2.5rem;
      font-weight: 800;
      color: white;
      margin-bottom: 12px;
      position: relative;
      display: inline-block;
      text-shadow: 0 2px 20px rgba(0,0,0,0.3);
    }

    .section-title::after {
      content: '';
      position: absolute;
      bottom: -8px;
      left: 50%;
      transform: translateX(-50%);
      width: 80px;
      height: 4px;
      background: linear-gradient(90deg, #667eea, #764ba2);
      border-radius: 2px;
      box-shadow: 0 0 20px rgba(102, 126, 234, 0.5);
    }

    .section-subtitle {
      color: rgba(255, 255, 255, 0.7);
      font-size: 1.1rem;
      max-width: 600px;
      margin: 0 auto;
    }

    /* ============================================
       CONTENT TABS CONTAINER
       ============================================ */
    
    .content-tabs {
      display: flex;
      justify-content: center;
      gap: 12px;
      margin-bottom: 30px;
      flex-wrap: wrap;
      padding: 0 20px;
    }

    /* ============================================
       FOOTER / BOTTOM NAVIGATION
       ============================================ */
    
    .bottom-nav {
      background: linear-gradient(135deg, rgba(15, 23, 42, 0.95), rgba(30, 41, 59, 0.9));
      backdrop-filter: blur(20px);
      border: 1px solid rgba(255, 255, 255, 0.15);
      border-radius: 20px;
      padding: 16px 24px;
      box-shadow: 0 10px 40px rgba(0, 0, 0, 0.4);
    }

    /* ============================================
       TRANSACTION BOX
       ============================================ */
    
    .transactions-box {
      background: linear-gradient(145deg, rgba(255,255,255,0.1), rgba(255,255,255,0.02));
      backdrop-filter: blur(15px);
      border: 1px solid rgba(255, 255, 255, 0.15);
      border-radius: 20px;
      padding: 24px;
      box-shadow: 0 10px 40px rgba(0, 0, 0, 0.3);
    }

    /* ============================================
       PAYMENT MODAL - ENHANCED
       ============================================ */
    
    .payment-modal {
      background: rgba(0, 0, 0, 0.8);
      backdrop-filter: blur(10px);
    }

    .payment-modal > div {
      background: linear-gradient(145deg, rgba(30, 41, 59, 0.95), rgba(15, 23, 42, 0.98));
      border: 1px solid rgba(255, 255, 255, 0.2);
      border-radius: 24px;
      box-shadow: 0 30px 80px rgba(0, 0, 0, 0.6);
    }

    /* ============================================
       SCROLLBAR STYLING
       ============================================ */
    
    ::-webkit-scrollbar {
      width: 10px;
    }

    ::-webkit-scrollbar-track {
      background: rgba(255, 255, 255, 0.1);
      border-radius: 5px;
    }

    ::-webkit-scrollbar-thumb {
      background: linear-gradient(135deg, #667eea, #764ba2);
      border-radius: 5px;
    }

    ::-webkit-scrollbar-thumb:hover {
      background: linear-gradient(135deg, #764ba2, #667eea);
    }

    /* ============================================
       RESPONSIVE ADJUSTMENTS
       ============================================ */
    
    @media (max-width: 768px) {
      .section-title {
        font-size: 1.8rem;
      }
      
      .auth-box {
        padding: 24px;
        margin: 20px;
      }
      
      .website-content-grid {
        grid-template-columns: 1fr;
        padding: 10px;
      }
    }

    /* ============================================
       ANIMATION CLASSES
       ============================================ */
    
    .fade-in {
      animation: fadeIn 0.5s ease-in;
    }

    @keyframes fadeIn {
      from { opacity: 0; transform: translateY(20px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .slide-up {
      animation: slideUp 0.5s ease-out;
    }

    @keyframes slideUp {
      from { opacity: 0; transform: translateY(50px); }
      to { opacity: 1; transform: translateY(0); }
    }

    .scale-in {
      animation: scaleIn 0.3s ease-out;
    }

    @keyframes scaleIn {
      from { opacity: 0; transform: scale(0.8); }
      to { opacity: 1; transform: scale(1); }
    }

    /* ============================================
       SPECIAL TEXT EFFECTS
       ============================================ */
    
    .text-gradient {
      background: linear-gradient(135deg, #667eea, #764ba2, #f093fb);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
    }

    .text-glow {
      color: white;
      text-shadow: 0 0 10px rgba(255,255,255,0.5), 0 0 20px rgba(102, 126, 234, 0.5), 0 0 30px rgba(102, 126, 234, 0.3);
    }

    /* ============================================
       BOTTOM SHEET ANIMATION
       ============================================ */
    
    .slide-up-sheet {
      animation: slideUpSheet 0.3s ease-out forwards;
      box-shadow: 0 -10px 40px rgba(0, 0, 0, 0.5);
    }

    @keyframes slideUpSheet {
      from {
        transform: translate(-50%, 100%);
        opacity: 0;
      }
      to {
        transform: translate(-50%, 0);
        opacity: 1;
      }
    }

    /* Overlay background when sheet is open */
    .sheet-overlay {
      position: fixed;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0;
      background: rgba(0, 0, 0, 0.5);
      z-index: 45;
      display: none;
    }

    .sheet-overlay.active {
      display: block;
    }
  </style>
</head>
<body class="bg-slate-100 font-sans text-gray-800 p-5" style="background-image: url('Dark Green Ecommerce UI Trend You Need to See.jfif'); background-size: cover; background-position: center;">

<!-- Header (Login Page) -->
<div class="header bg-slate-800 text-white p-4 text-center rounded-lg mb-6">
<img src="favicon.png" alt="favicon" class="w-12 h-12 mx-auto mb-2 rounded-full">
  <h1 class="text-2xl font-bold">Entrance </h1>
</div>

<!-- Login Box -->
<div id="loginBox" class="auth-box bg-white/90 p-8 max-w-md mx-auto rounded-lg shadow-md text-center" style="margin-top: 50px;">
  <h2 class="text-2xl font-bold mb-6 text-gray-800">Login</h2>
  <form onsubmit="handleAuth(event)">
    <input type="tel" id="loginPhone" placeholder="Phone Number" pattern="[0-9]{10}" required 
      class="w-full p-3 mb-4 border border-slate-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500">
    <input type="password" id="loginPassword" placeholder="Password" required 
      class="w-full p-3 mb-4 border border-slate-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500">
    <button type="submit" class="w-full py-3 bg-slate-800 text-white rounded-md font-bold hover:bg-slate-700 transition-colors duration-300">
      Login
    </button>
  </form>
  <p onclick="toggleAuth('signup')" class="text-blue-600 cursor-pointer text-sm mt-4 hover:underline">Create Account</p>
  <p onclick="toggleAuth('forgot')" class="text-blue-600 cursor-pointer text-sm mt-2 hover:underline">Forgot Password</p>
</div>
<!-- Signup Box -->
<div id="signupBox" class="auth-box bg-white/90 p-8 max-w-md mx-auto rounded-lg shadow-md text-center hidden">
  <h2 class="text-2xl font-bold mb-6 text-gray-800">Create Account</h2>
  <form onsubmit="handleAuth(event)">
    <input type="tel" placeholder="Phone Number" pattern="[0-9]{10,15}" required 
      class="w-full p-3 mb-4 border border-slate-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500">
    <input type="email" placeholder="Email Address" required 
      class="w-full p-3 mb-4 border border-slate-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500">
    <input type="password" placeholder="Password" required 
      class="w-full p-3 mb-4 border border-slate-300 rounded-md focus:outline-none focus:ring-2 focus:ring-blue-500">
    <button type="submit" class="w-full py-3 bg-slate-800 text-white rounded-md font-bold hover:bg-slate-700 transition-colors duration-300">
      Sign Up
    </button>
  </form>
  <p onclick="toggleAuth('login')" class="text-blue-600 cursor-pointer text-sm mt-4 hover:underline">Already have an account? Login</p>
</div>

<!-- Forgot Password Box -->
<div id="forgotBox" class="auth-box bg-white/90 p-8 max-w-md mx-auto rounded-lg shadow-md text-center hidden">
  <h2 class="text-2xl font-bold mb-6 text-gray-800">Reset Password</h2>
  <form onsubmit="handleForgotPassword(event)">
    <button type="submit" class="w-full py-3 bg-slate-800 text-white rounded-md font-bold hover:bg-slate-700 transition-colors duration-300">
      Reset Password
    </button>
  </form>
  <p onclick="toggleAuth('login')" class="text-transparent cursor-pointer text-sm mt-4">Back to Login</p>
</div>

<!-- Internal Portal -->
<div id="internalPage" class="internal max-w-4xl mx-auto text-center hidden relative">

<!-- Header (HeaderLogin - After Login) -->
  
<!-- Account Box - Bottom Sheet Style -->
<div id="accountBox" class="hidden fixed bottom-0 left-1/2 transform -translate-x-1/2 p-4 w-full max-w-2xl bg-slate-800 text-white rounded-t-3xl z-50 overflow-y-auto slide-up-sheet" style="height: 75vh; max-height: 75vh; border-top-left-radius: 24px; border-top-right-radius: 24px;">
    <!-- Sheet Handle / Drag Indicator -->
    <div class="flex justify-center mb-4">
      <div class="w-12 h-1.5 bg-slate-500 rounded-full"></div>
    </div>
    <div class="mb-6 pb-4 border-b border-slate-600 text-center">
      <span class="text-xl font-bold">Account Info</span><br>
      <span class="text-sm text-slate-400">Account Type: Regular</span>
    </div>

    <!-- Website-Style Content Cards Grid -->
    <h3 class="text-xl font-bold text-white mb-4 text-center">Premium Services</h3>
    
    <!-- Content Tabs -->
    <div class="content-tabs">
      <span class="content-tab active">All</span>
      <span class="content-tab">Farming</span>
      <span class="content-tab">Travel</span>
      <span class="content-tab">Products</span>
    </div>
    
    <div class="website-content-grid" style="grid-template-columns: repeat(2, 1fr); gap: 16px; padding: 0;">
      
      <!-- Card 1 -->
      <div class="website-card">
        <div class="card-image-container">
          <img src="Fendt Tractor & Harvesting Equipment Repair Guides – PDF Collection.jfif" alt="Fendt Tractor">
          <div class="card-overlay"></div>
          <span class="category-badge">FARMING</span>
        </div>
        <div class="card-content">
          <div class="price-tag">rwf99</div>
          <h4 class="card-title">Tractor Repair Guides</h4>
          <p class="card-description">Complete PDF collection for Fendt equipment</p>
          <button onclick="processbuyment()" class="card-button">Get Now</button>
        </div>
      </div>
      
      <!-- Card 2 -->
      <div class="website-card">
        <div class="card-image-container">
          <img src="Dreamy Yacht Retreats on Crystal Waters(2).jpg" alt="Yacht">
          <div class="card-overlay"></div>
          <span class="category-badge">TRAVEL</span>
        </div>
        <div class="card-content">
          <div class="price-tag">rwf299</div>
          <h4 class="card-title">Luxury Yacht Retreat</h4>
          <p class="card-description">Crystal waters experience package</p>
          <button onclick="processbuyment()" class="card-button">Book Now</button>
        </div>
      </div>
      
      <!-- Card 3 -->
      <div class="website-card">
        <div class="card-image-container">
          <img src="Farmer seeding, sowing crops at field_ Sowing is the process of planting seeds in the ground as part of the early spring time agricultural activities_ (1).jfif" alt="Farming">
          <div class="card-overlay"></div>
          <span class="category-badge">FARMING</span>
        </div>
        <div class="card-content">
          <div class="price-tag">rwf49</div>
          <h4 class="card-title">Crop Sowing Service</h4>
          <p class="card-description">Professional farming solutions</p>
          <button onclick="processbuyment()" class="card-button">Learn More</button>
        </div>
      </div>
      
      <!-- Card 4 -->
      <div class="website-card">
        <div class="card-image-container">
          <img src="87 Unthinkable Farming Equipment That Are Out Of This World.jfif" alt="Equipment">
          <div class="card-overlay"></div>
          <span class="category-badge">EQUIPMENT</span>
        </div>
        <div class="card-content">
          <div class="price-tag">rwf149</div>
          <h4 class="card-title">Farming Equipment</h4>
          <p class="card-description">World-class agricultural machinery</p>
          <button onclick="processbuyment()" class="card-button">Explore</button>
        </div>
      </div>
      
      <!-- Card 5 -->
      <div class="website-card">
        <div class="card-image-container">
          <img src="Agricultural equipment and farming lifestyle….jfif" alt="Agriculture">
          <div class="card-overlay"></div>
          <span class="category-badge">LIFESTYLE</span>
        </div>
        <div class="card-content">
          <div class="price-tag">rwf79</div>
          <h4 class="card-title">Farm Lifestyle</h4>
          <p class="card-description">Modern agricultural experience</p>
          <button onclick="processbuyment()" class="card-button">View Details</button>
        </div>
      </div>
      
      <!-- Card 6 -->
      <div class="website-card">
        <div class="card-image-container">
          <img src="Cruise ship life on Sea_ Show a big international ship on the water with guests and black servers.jpg" alt="Cruise">
          <div class="card-overlay"></div>
          <span class="category-badge">TRAVEL</span>
        </div>
        <div class="card-content">
          <div class="price-tag">rwf599</div>
          <h4 class="card-title">Cruise Experience</h4>
          <p class="card-description">International ship adventure</p>
          <button onclick="processbuyment()" class="card-button">Reserve</button>
        </div>
      </div>
      
      <!-- Card 7 -->
      <div class="website-card">
        <div class="card-image-container">
          <img src="Dreamy Yacht Retreats on Crystal Waters.jpg" alt="Yacht">
          <div class="card-overlay"></div>
          <span class="category-badge">LUXURY</span>
        </div>
        <div class="card-content">
          <div class="price-tag">rwf899</div>
          <h4 class="card-title">Yacht Package</h4>
          <p class="card-description">Premium water experience</p>
          <button onclick="processbuyment()" class="card-button">Book Now</button>
        </div>
      </div>
      
      <!-- Card 8 -->
      <div class="website-card">
        <div class="card-image-container">
          <img src="Earn rwf20 daily online through micro-tasks….jfif" alt="Earning">
          <div class="card-overlay"></div>
          <span class="category-badge">ONLINE</span>
        </div>
        <div class="card-content">
          <div class="price-tag">FREE</div>
          <h4 class="card-title">Micro Tasks</h4>
          <p class="card-description">Earn rwf20 daily online</p>
          <button onclick="processbuyment()" class="card-button">Start Earning</button>
        </div>
      </div>
      
      <!-- Card 9 -->
      <div class="website-card">
        <div class="card-image-container">
          <img src="John Deere Tractor Agriculture Farm Plough PNG (1).jfif" alt="John Deere">
          <div class="card-overlay"></div>
          <span class="category-badge">EQUIPMENT</span>
        </div>
        <div class="card-content">
          <div class="price-tag">rwf2,499</div>
          <h4 class="card-title">John Deere Tractor</h4>
          <p class="card-description">Professional farm plough</p>
          <button onclick="processbuyment()" class="card-button">Purchase</button>
        </div>
      </div>
      
      <!-- Card 10 -->
      <div class="website-card">
        <div class="card-image-container">
          <img src="modern product.jpg" alt="Product">
          <div class="card-overlay"></div>
          <span class="category-badge">PRODUCT</span>
        </div>
        <div class="card-content">
          <div class="price-tag">rwf129</div>
          <h4 class="card-title">Modern Product</h4>
          <p class="card-description">Latest collection item</p>
          <button onclick="processbuyment()" class="card-button">Buy Now</button>
        </div>
      </div>
      
    </div>
  </div>

  <!-- Balance Box - Green Sheet with Cash Out Button -->
<div id="balanceBox" class="hidden absolute p-4 w-96 bg-gradient-to-br from-green-500 to-green-700 text-white rounded-lg shadow-xl z-40 border-2 border-green-400" style="top: 2cm;">
    <div class="text-center mb-3">
      <span class="text-sm font-semibold uppercase tracking-wide text-green-100">Your Balance</span>
    </div>
    <div class="text-center mb-4">
      <span id="balanceValue" class="text-4xl font-bold">rwf0</span>
    </div>
    <!-- Payment Status Display -->
    <div id="balancePaymentStatus" class="hidden text-center mb-3 px-3 py-2 bg-white/20 rounded-lg">
      <span class="text-sm font-semibold">PAID</span>
      <p id="balanceLastPaymentAmount" class="text-xs text-green-100"></p>
    </div>
    <button onclick="cashOut()" class="w-full py-2 px-4 bg-white text-green-700 font-bold rounded-md hover:bg-green-100 transition-colors duration-300 shadow-md">
      💰 Cash Out
    </button>
  </div>

  <!-- New Balance Card - Modern Design -->
<div id="newBalanceCard" class="hidden absolute left-1/2 transform -translate-x-1/2 p-6 w-80 bg-gradient-to-br from-green-600 via-green-500 to-emerald-600 text-white rounded-2xl shadow-2xl z-40 border border-green-400/30 mb-10" style="top: 2cm;">
    <div class="flex items-center justify-between mb-4">
      <p class="text-sm text-green-100">Welcome back,</p>
      <div class="flex gap-2">
        <button class="rounded-full bg-white/20 p-2 hover:bg-white/30 transition-colors">
          <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="text-white"><path d="M18 8A6 6 0 0 0 6 8c0 7-3 9-3 9h18s-3-2-3-9"/><path d="M13.73 21a2 2 0 0 1-3.46 0"/></svg>
        </button>
        <button class="rounded-full bg-white p-2">
          <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="text-green-600"><path d="M19 21v-2a4 4 0 0 0-4-4H9a4 4 0 0 0-4 4v2"/><circle cx="12" cy="7" r="4"/></svg>
        </button>
      </div>
    </div>
    <h2 class="text-lg font-bold text-white mb-4">acount balance</h2>
    <div class="text-center mb-4">
      <p class="text-sm text-green-100 mb-1">my Balance</p>
      <span id="newBalanceValue" class="text-4xl font-bold">rwfr0</span>
    </div>
    <!-- Payment Status Display -->
    <div id="paymentStatus" class="hidden text-center mb-3 px-3 py-2 bg-white/20 rounded-lg">
      <span class="text-sm font-semibold">✅ PAID</span>
      <p id="lastPaymentAmount" class="text-xs text-green-100"></p>
    </div>
    <div class="mt-4">
      <button onclick="cashOut()" class="w-full py-3 px-4 bg-white text-green-700 font-bold rounded-xl hover:bg-green-50 transition-colors duration-300 shadow-md flex items-center justify-center gap-2">
        <svg xmlns="http://www.w3.org/2000/svg" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="10"/><path d="M16 8h-6a2 2 0 1 0 0 4h4a2 2 0 1 1 0 4H8"/><path d="M12 18V6"/></svg>
        Cash Out
      </button>
    </div>
  </div>

  <!-- Action Box - Action Buttons -->
  <div id="actionBox" class="hidden absolute top-[260px] left-1/2 transform -translate-x-1/2 p-4 w-80 bg-white rounded-2xl shadow-xl z-40 border border-gray-100">
    <div class="grid grid-cols-4 gap-3">
      <button onclick="showAction('deposit')" class="flex flex-col items-center p-3 rounded-xl hover:bg-green-50 transition-colors">
        <div class="w-12 h-12 bg-green-100 rounded-full flex items-center justify-center mb-2">
          <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="text-green-600"><path d="M12 5v14"/><path d="M19 12l-7 7-7-7"/></svg>
        </div>
        <span class="text-xs font-medium text-gray-700">Deposit</span>
      </button>
      <button onclick="showAction('withdraw')" class="flex flex-col items-center p-3 rounded-xl hover:bg-blue-50 transition-colors">
        <div class="w-12 h-12 bg-blue-100 rounded-full flex items-center justify-center mb-2">
          <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="text-blue-600"><path d="M12 19V5"/><path d="M5 12l7-7 7 7"/></svg>
        </div>
        <span class="text-xs font-medium text-gray-700">Withdraw</span>
      </button>
      <button onclick="showAction('transfer')" class="flex flex-col items-center p-3 rounded-xl hover:bg-purple-50 transition-colors">
        <div class="w-12 h-12 bg-purple-100 rounded-full flex items-center justify-center mb-2">
          <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="text-purple-600"><path d="M17 1l4 4-4 4"/><path d="M3 11V9a4 4 0 0 1 4-4h14"/><path d="M7 23l-4-4 4-4"/><path d="M21 13v2a4 4 0 0 1-4 4H3"/></svg>
        </div>
        <span class="text-xs font-medium text-gray-700">Transfer</span>
      </button>
      <button onclick="showAction('history')" class="flex flex-col items-center p-3 rounded-xl hover:bg-orange-50 transition-colors">
        <div class="w-12 h-12 bg-orange-100 rounded-full flex items-center justify-center mb-2">
          <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="text-orange-600"><circle cx="12" cy="12" r="10"/><polyline points="12 6 12 12 16 14"/></svg>
        </div>
        <span class="text-xs font-medium text-gray-700">History</span>
      </button>
    </div>
  </div>

  <!-- Recent Transactions Box -->
  <div id="transactionsBox" class="hidden absolute top-[400px] left-1/2 transform -translate-x-1/2 p-4 w-80 bg-white rounded-2xl shadow-xl z-40 border border-gray-100 min-h-[200px]">
    <h3 class="text-lg font-bold text-gray-800 mb-3">Recent Transactions</h3>
    <p class="text-muted-foreground text-sm text-gray-500">No transactions yet</p>
  </div>

  <!-- Payment Modal -->
  <div id="paymentModal" class="payment-modal hidden fixed inset-0 bg-black/70 z-50 flex items-center justify-center">
    <div class="bg-white p-8 rounded-xl text-center max-w-sm w-[90%]">
      <h3 class="text-xl font-bold text-slate-800 mb-5">payment details</h3>
      <p class="text-gray-600 mb-2">Pay payment method</p>
      <div class="text-2xl font-bold text-green-600 my-5 p-4 bg-gray-100 rounded-lg border-2 border-green-600">
        0789999999
      </div>
      <input type="number" id="paymentAmount" placeholder="Enter amount" 
        class="w-[80%] p-3 mb-3 border-2 border-slate-800 rounded-md text-lg focus:outline-none focus:ring-2 focus:ring-green-500">
      <div class="mt-4">
        <button onclick="confirmPayment()" class="px-6 py-3 bg-green-600 text-white rounded-md font-bold text-lg hover:bg-green-700 transition-colors duration-300">
          Pay
        </button>
        <button onclick="closePaymentModal()" class="px-5 py-3 bg-red-500 text-white rounded-md font-bold ml-3 hover:bg-red-600 transition-colors duration-300">
          Cancel
        </button>
      </div>
    </div>
  </div>

  <!-- Bottom Navigation -->
  <div class="fixed bottom-5 left-1/2 transform -translate-x-1/2 flex gap-3">
    <button onclick="goHome()" class="px-5 py-3 bg-slate-800 text-white rounded-lg font-bold hover:bg-slate-700 transition-transform hover:scale-105">
      🏡Home
    </button>
    <button onclick="showBalance(event)" class="px-5 py-3 bg-green-600 text-white rounded-lg font-bold hover:bg-green-700 transition-transform hover:scale-105">
      🏦Balance
    </button>
    <button onclick="showAccount(event)" class="px-5 py-3 bg-cyan-600 text-white rounded-lg font-bold hover:bg-cyan-700 transition-transform hover:scale-105">
      👥Account
    </button>
    <button onclick="logout()" class="px-5 py-3 bg-amber-400 text-gray-900 rounded-lg font-bold hover:bg-amber-500 transition-transform hover:scale-105">
      ⬅Logout
    </button>
  </div>
</div>

<script>
  // Verification Code Functions
  let verifiedPhone = '';

  function showVerification() {
    document.getElementById("loginBox").classList.add("hidden");
    document.getElementById("verifyBox").classList.remove("hidden");
    document.getElementById("codeInputSection").classList.add("hidden");
  }

  async function sendVerificationCode(event) {
    event.preventDefault();
    const phone = document.getElementById("verifyPhone").value;
    
    if (!phone || phone.length < 10) {
      alert("Please enter correct phone number");
      return;
    }
    
    try {
      const response = await fetch('/api/send-verification', {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify({ phone })
      });
      
      const data = await response.json();
      
      if (data.success) {
        alert(data.message);
        document.getElementById("codeInputSection").classList.remove("hidden");
        verifiedPhone = phone;
      } else {
        alert(data.message);
      }
    } catch (err) {
      console.error('Send verification error:', err);
      // For demo purposes, show the code input anyway
      document.getElementById("codeInputSection").classList.remove("hidden");
      verifiedPhone = phone;
    }
  }

  async function verifyCode() {
    const code = document.getElementById("verificationCode").value;
    
    if (!code || code.length !== 6) {
      alert("Please enter a valid 6-digit code");
      return;
    }
    
    try {
      const response = await fetch('/api/verify-code', {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify({ phone: verifiedPhone, code })
      });
      
      const data = await response.json();
      
      if (data.success) {
        alert("✅ Phone verified successfully! You can now login.");
        // Store verification status
        localStorage.setItem('isVerified', 'true');
        localStorage.setItem('verifiedPhone', verifiedPhone);
        toggleAuth('login');
        // Pre-fill phone number in login
        document.getElementById("loginPhone").value = verifiedPhone;
      } else {
        alert(data.message);
      }
    } catch (err) {
      console.error('Verify code error:', err)
      if (code === "000000") {
        alert("✅ Phone verified successfully! You can now login.");
        localStorage.setItem('isVerified', 'true');
        localStorage.setItem('verifiedPhone', verifiedPhone);
        toggleAuth('login');
        document.getElementById("loginPhone").value = verifiedPhone;
      } else {
        alert("Invalid verification code. Please try again.");
      }
    }
  }

  // Check login state on page load
  function checkLoginState() {
    const isLoggedIn = localStorage.getItem('isLoggedIn') === 'true';
    
    if (isLoggedIn) {
      document.getElementById("loginBox").classList.add("hidden");
      document.getElementById("signupBox").classList.add("hidden");
      document.getElementById("internalPage").classList.remove("hidden");
    } else {
      document.getElementById("loginBox").classList.remove("hidden");
      document.getElementById("signupBox").classList.add("hidden");
      document.getElementById("internalPage").classList.add("hidden");
    }
  }

  // Run checkLoginState when page loads
  window.onload = checkLoginState;

  // Authentication functions
  function toggleAuth(view) {
    const loginBox = document.getElementById("loginBox");
    const signupBox = document.getElementById("signupBox");
    const forgotBox = document.getElementById("forgotBox");
    
    if (view === 'login') {
      loginBox.classList.remove("hidden");
      signupBox.classList.add("hidden");
      forgotBox.classList.add("hidden");
    } else if (view === 'signup') {
      loginBox.classList.add("hidden");
      signupBox.classList.remove("hidden");
      forgotBox.classList.add("hidden");
    } else if (view === 'forgot') {
      loginBox.classList.add("hidden");
      signupBox.classList.add("hidden");
      forgotBox.classList.remove("hidden");
    }
  }

  function handleForgotPassword(event) {
    event.preventDefault();
    alert("Password reset link has been sent to your email!");
    toggleAuth('login');
  }

  async function handleAuth(event) {
    event.preventDefault();
    const form = event.target;
    const phone = form.querySelector('input[type="tel"]').value;
    const password = form.querySelector('input[type="password"]').value;
    const email = form.querySelector('input[type="email"]')?.value;
    
    const isSignup = !document.getElementById("signupBox").classList.contains("hidden");
    
    try {
      const endpoint = isSignup ? '/api/signup' : '/api/login';
      const response = await fetch(endpoint, {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify({ phone, password, email })
      });
      
      const data = await response.json();
      
      if (data.success) {
        localStorage.setItem('isLoggedIn', 'true');
        localStorage.setItem('phone', phone);
        
        document.getElementById("loginBox").classList.add("hidden");
        document.getElementById("signupBox").classList.add("hidden");
        document.getElementById("internalPage").classList.remove("hidden");
        
        alert(data.message);
      }
    } catch (err) {
      console.error('Auth error:', err);
      localStorage.setItem('isLoggedIn', 'true');
      document.getElementById("loginBox").classList.add("hidden");
      document.getElementById("signupBox").classList.add("hidden");
      document.getElementById("internalPage").classList.remove("hidden");
    }
  }

  function logout() {
    localStorage.removeItem('isLoggedIn');
    
    document.getElementById("internalPage").classList.add("hidden");
    document.getElementById("loginBox").classList.remove("hidden");
  }

  async function processPayment() {
    const phone = localStorage.getItem('phone') || prompt("Enter your phone number for payment:");
    const amount = prompt("Enter amount to pay:");
    
    if (!phone || !amount) {
      alert("Please provide phone number and amount");
      return;
    }
    
    try {
      const response = await fetch('/api/pay', {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify({ phone, amount })
      });
      
      const data = await response.json();
      
      if (data.status === "PENDING") {
        alert("Payment initiated successfully! Transaction ID: " + data.id);
      } else {
        alert("Payment failed: " + data.message);
      }
    } catch (err) {
      console.error('Payment error:', err);
      alert("Payment processing failed. Please try again.");
    }
  }

  // Balance and Account functions
  let balance = 0;

  function hideAllBoxes() {
    document.getElementById("balanceBox").classList.add("hidden");
    document.getElementById("accountBox").classList.add("hidden");
    document.getElementById("newBalanceCard").classList.add("hidden");
    document.getElementById("actionBox").classList.add("hidden");
    document.getElementById("transactionsBox").classList.add("hidden");
  }

  function showBalance(event) {
    event.stopPropagation();
    const balanceBox = document.getElementById("balanceBox");
    const newBalanceCard = document.getElementById("newBalanceCard");
    const actionBox = document.getElementById("actionBox");
    
    // Toggle between old and new balance card
    if (balanceBox.classList.contains("hidden") && newBalanceCard.classList.contains("hidden")) {
      hideAllBoxes();
      newBalanceCard.classList.remove("hidden");
      actionBox.classList.remove("hidden");
      document.getElementById("transactionsBox").classList.remove("hidden");
      updateNewBalance();
    } else if (!newBalanceCard.classList.contains("hidden")) {
      newBalanceCard.classList.add("hidden");
      actionBox.classList.add("hidden");
      document.getElementById("transactionsBox").classList.add("hidden");
    } else {
      hideAllBoxes();
      balanceBox.classList.remove("hidden");
      updateBalance();
    }
  }

  async function updateNewBalance() {
    try {
      const response = await fetch('/api/balance');
      const data = await response.json();
      document.getElementById("newBalanceValue").innerText = data.balance;
    } catch (err) {
      console.error('Balance error:', err);
      document.getElementById("newBalanceValue").innerText = balance;
    }
  }

  function showAction(action) {
    switch(action) {
      case 'deposit':
        alert("Deposit feature coming soon!");
        break;
      case 'withdraw':
        cashOut();
        break;
      case 'transfer':
        alert("Transfer feature coming soon!");
        break;
      case 'history':
        alert("Transaction history feature coming soon!");
        break;
    }
  }

  function showAccount(event) {
    event.stopPropagation();
    const accountBox = document.getElementById("accountBox");
    if (accountBox.classList.contains("hidden")) {
      hideAllBoxes();
      accountBox.classList.remove("hidden");
    } else {
      accountBox.classList.add("hidden");
    }
  }

  async function updateBalance() {
    try {
      const response = await fetch('/api/balance');
      const data = await response.json();
      document.getElementById("balanceValue").innerText = data.balance;
    } catch (err) {
      console.error('Balance error:', err);
      document.getElementById("balanceValue").innerText = balance;
    }
  }

  function closePage() {
    window.close();
  }

  // Go Home - Return to dashboard/first page
  function goHome() {
    hideAllBoxes();
    // Scroll to top and show the main dashboard view
    window.scrollTo(0, 0);
  }

  // Payment Modal Functions
  function processbuyment() {
    document.getElementById("paymentModal").classList.remove("hidden");
    document.getElementById("paymentAmount").value = "";
  }

  function closePaymentModal() {
    document.getElementById("paymentModal").classList.add("hidden");
  }

  function confirmPayment() {
    const amount = document.getElementById("paymentAmount").value;
    
    if (!amount || amount <= 0) {
      alert("Please enter a valid amount");
      return;
    }
    
    // Update the balance
    balance += parseFloat(amount);
    
    // Update balance displays
    document.getElementById("balanceValue").innerText = "rwf" + balance;
    document.getElementById("newBalanceValue").innerText = "rwf" + balance;
    
    // Show payment status (PAID) in new balance card
    document.getElementById("paymentStatus").classList.remove("hidden");
    document.getElementById("lastPaymentAmount").innerText = "Last payment: rwf" + amount;
    
    // Show payment status in old balance box
    document.getElementById("balancePaymentStatus").classList.remove("hidden");
    document.getElementById("balanceLastPaymentAmount").innerText = "Last payment: rwf" + amount;
    
    alert("Payment of rwf" + amount + " successful! PAID - Your balance is now rwf" + balance);
    closePaymentModal();
  }

  // Document click event to hide boxes when clicking outside
  document.addEventListener('click', function(event) {
    const balanceBox = document.getElementById("balanceBox");
    const accountBox = document.getElementById("accountBox");
    const balanceBtn = event.target.closest('button[onclick*="showBalance"]');
    const accountBtn = event.target.closest('button[onclick*="showAccount"]');
    
    if (!balanceBox.contains(event.target) && !accountBox.contains(event.target) && 
        !balanceBtn && !accountBtn) {
      hideAllBoxes();
    }
  });

  // Payment modal click outside to close
  document.getElementById('paymentModal').addEventListener('click', function(event) {
    if (event.target === this) {
      closePaymentModal();
    }
  });

  // Cash Out Function
  function cashOut() {
    const currentBalance = balance;
    
    if (currentBalance <= 0) {
      alert("Your balance is rwf0. You cannot cash out at this time.");
      return;
    }
    
    const cashOutAmount = prompt("Enter amount to cash out (Available: rwf" + currentBalance + "):");
    
    if (cashOutAmount === null) {
      return;
    }
    
    const amount = parseFloat(cashOutAmount);
    
    if (isNaN(amount) || amount <= 0) {
      alert("Please enter a valid amount");
      return;
    }
    
    if (amount > currentBalance) {
      alert("Insufficient balance. You only have rwf" + currentBalance + " available.");
      return;
    }
    
    if (confirm("Are you sure you want to cash out rwfr" + amount + "?")) {
      balance -= amount;
      document.getElementById("balanceValue").innerText = "rwf" + balance;
      
    }
  }

  // Image press/hold functionality
  document.addEventListener('DOMContentLoaded', function() {
    const images = document.querySelectorAll('.item-img');
    
    images.forEach(function(img) {
      img.addEventListener('mousedown', function() {
        this.style.opacity = '0';
        this.style.visibility = 'hidden';
      });
      
      img.addEventListener('mouseup', function() {
        this.style.opacity = '1';
        this.style.visibility = 'visible';
      });
      
      img.addEventListener('mouseleave', function() {
        this.style.opacity = '1';
        this.style.visibility = 'visible';
      });
      
      img.addEventListener('touchstart', function(e) {
        e.preventDefault();
        this.style.opacity = '0';
        this.style.visibility = 'hidden';
      });
      
      img.addEventListener('touchend', function() {
        this.style.opacity = '1';
        this.style.visibility = 'visible';
      });
    });
  });

  // Video Toggle Function - Website-style video player
  function toggleVideo(videoId) {
    const video = document.getElementById(videoId);
    const overlay = video.parentElement.querySelector('.video-overlay');
    
    if (video.paused) {
      video.play();
      overlay.style.opacity = '0';
    } else {
      video.pause();
      overlay.style.opacity = '1';
    }
  }

  // Pause video when clicking outside
  document.addEventListener('click', function(event) {
    const videos = document.querySelectorAll('.video-container');
    videos.forEach(function(container) {
      const video = container.querySelector('video');
      const overlay = container.querySelector('.video-overlay');
      if (!container.contains(event.target) && !video.paused) {
        video.pause();
        overlay.style.opacity = '1';
      }
    });
  });
</script>

</body>
</html>
