
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
  <title>TYSON HACK — Premium Subscription Plans</title>
  <!-- Google Fonts + Font Awesome 6 (same as original) -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    :root {
      --primary: #dc2626;
      --primary-dark: #b91c1c;
      --primary-light: #fef2f2;
      --accent: #1e293b;
      --text: #334155;
      --text-light: #64748b;
      --white: #ffffff;
      --gray-light: #f8fafc;
      --border: #e2e8f0;
      --success: #10b981;
    }

    body {
      font-family: 'Inter', sans-serif;
      background: linear-gradient(135deg, #fef2f2 0%, #fff 100%);
      color: var(--text);
      line-height: 1.5;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      padding: 32px 20px;
    }

    /* main container — fixed max-width, consistent height behavior */
    .container {
      max-width: 500px;
      width: 100%;
      background: var(--white);
      border-radius: 28px;
      box-shadow: 0 20px 35px -12px rgba(0, 0, 0, 0.1);
      overflow: hidden;
      margin-bottom: 28px;
      transition: all 0.2s ease;
    }

    .header {
      background: linear-gradient(135deg, var(--primary) 0%, var(--primary-dark) 100%);
      color: var(--white);
      padding: 32px 24px;
      text-align: center;
    }

    .logo {
      font-size: 30px;
      font-weight: 700;
      letter-spacing: -0.3px;
      margin-bottom: 10px;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 10px;
    }

    .logo i {
      font-size: 28px;
    }

    .subtitle {
      font-size: 16px;
      font-weight: 400;
      opacity: 0.92;
    }

    .content {
      padding: 32px 26px;
    }

    .section-title {
      font-size: 20px;
      font-weight: 700;
      color: var(--accent);
      margin-bottom: 24px;
      text-align: center;
      letter-spacing: -0.2px;
    }

    .plans {
      display: flex;
      flex-direction: column;
      gap: 20px;
      margin-bottom: 32px;
    }

    /* plan cards — fixed consistent height and good breath */
    .plan-card {
      background: var(--white);
      border: 1.5px solid var(--border);
      border-radius: 20px;
      padding: 22px 20px;
      transition: all 0.25s ease;
      cursor: pointer;
      position: relative;
      min-height: 210px;
      display: flex;
      flex-direction: column;
    }

    .plan-card:hover {
      transform: translateY(-4px);
      box-shadow: 0 20px 25px -12px rgba(220, 38, 38, 0.2);
      border-color: var(--primary);
    }

    .plan-card.selected {
      border-color: var(--primary);
      background: var(--primary-light);
      box-shadow: 0 8px 18px rgba(220, 38, 38, 0.08);
    }

    .plan-card h3 {
      font-size: 20px;
      font-weight: 700;
      color: var(--accent);
      margin-bottom: 6px;
    }

    .plan-card .price {
      font-size: 28px;
      font-weight: 800;
      color: var(--primary);
      margin-bottom: 4px;
      letter-spacing: -0.3px;
    }

    .plan-card .validity {
      font-size: 14px;
      color: var(--text-light);
      margin-bottom: 12px;
      font-weight: 500;
    }

    .plan-card .features {
      font-size: 13px;
      color: var(--text-light);
      margin-top: 6px;
    }

    .plan-card .features ul {
      list-style-type: none;
      padding-left: 0;
    }

    .plan-card .features li {
      margin-bottom: 6px;
      display: flex;
      align-items: center;
      gap: 10px;
    }

    .plan-card .features i {
      color: var(--success);
      font-size: 13px;
      width: 16px;
    }

    .highlight-badge {
      position: absolute;
      top: 16px;
      right: 18px;
      background: var(--primary);
      color: white;
      padding: 5px 12px;
      border-radius: 40px;
      font-size: 11px;
      font-weight: 700;
      letter-spacing: 0.3px;
      box-shadow: 0 2px 6px rgba(0,0,0,0.05);
    }

    .contact-section {
      text-align: center;
      margin-top: 8px;
      padding-top: 18px;
      border-top: 1px solid var(--border);
    }

    .contact-btn {
      background: var(--primary);
      color: var(--white);
      padding: 14px 28px;
      border-radius: 40px;
      font-size: 16px;
      font-weight: 600;
      text-decoration: none;
      display: inline-flex;
      align-items: center;
      gap: 10px;
      transition: all 0.25s ease;
      box-shadow: 0 6px 14px rgba(220, 38, 38, 0.25);
    }

    .contact-btn:hover {
      background: var(--primary-dark);
      transform: translateY(-2px);
      box-shadow: 0 10px 20px rgba(220, 38, 38, 0.3);
    }

    .footer {
      padding: 18px 24px;
      text-align: center;
      font-size: 12px;
      color: var(--text-light);
      background: var(--gray-light);
      border-top: 1px solid var(--border);
    }

    /* bottom section: consistent width and better inner spacing */
    .bottom-section {
      max-width: 500px;
      width: 100%;
      background: linear-gradient(135deg, var(--accent) 0%, #1e2a3a 100%);
      border-radius: 28px;
      padding: 32px 28px;
      color: var(--white);
      text-align: center;
      margin-bottom: 20px;
      box-shadow: 0 18px 30px -12px rgba(0, 0, 0, 0.2);
    }

    .bottom-section h3 {
      font-size: 22px;
      font-weight: 700;
      margin-bottom: 12px;
      letter-spacing: -0.2px;
    }

    .bottom-section p {
      font-size: 15px;
      margin-bottom: 24px;
      opacity: 0.9;
      line-height: 1.5;
      max-width: 380px;
      margin-left: auto;
      margin-right: auto;
    }

    .join-btn {
      background: var(--white);
      color: var(--accent);
      padding: 14px 32px;
      border-radius: 40px;
      font-size: 15px;
      font-weight: 700;
      text-decoration: none;
      display: inline-flex;
      align-items: center;
      gap: 10px;
      transition: all 0.25s ease;
      margin-bottom: 22px;
      box-shadow: 0 6px 12px rgba(0,0,0,0.1);
    }

    .join-btn:hover {
      background: var(--primary-light);
      transform: translateY(-2px);
      color: var(--primary-dark);
    }

    .bottom-footer {
      font-size: 11px;
      opacity: 0.75;
      line-height: 1.5;
    }

    /* MODAL - perfect height and scroll on small devices */
    .modal {
      display: none;
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0.6);
      align-items: center;
      justify-content: center;
      z-index: 1000;
      padding: 20px;
      backdrop-filter: blur(3px);
    }

    .modal-content {
      background: var(--white);
      border-radius: 32px;
      padding: 32px 28px;
      max-width: 460px;
      width: 100%;
      max-height: 90vh;
      overflow-y: auto;
      text-align: left;
      box-shadow: 0 30px 40px -20px rgba(0, 0, 0, 0.3);
      position: relative;
    }

    .close {
      position: absolute;
      top: 20px;
      right: 24px;
      font-size: 28px;
      cursor: pointer;
      color: var(--text-light);
      transition: color 0.2s;
      line-height: 1;
    }

    .close:hover {
      color: var(--primary);
    }

    .modal-title {
      font-size: 26px;
      font-weight: 700;
      color: var(--accent);
      margin-bottom: 6px;
    }

    .modal-subtitle {
      font-size: 15px;
      color: var(--text-light);
      margin-bottom: 24px;
    }

    .payment-details {
      background: var(--primary-light);
      border-radius: 20px;
      padding: 20px;
      margin-bottom: 24px;
    }

    .payment-details p {
      margin-bottom: 12px;
      display: flex;
      justify-content: space-between;
      font-size: 15px;
    }

    .payment-details strong {
      color: var(--accent);
      font-weight: 700;
    }

    .upi-section {
      background: var(--gray-light);
      border-radius: 20px;
      padding: 20px;
      margin-bottom: 24px;
      text-align: center;
    }

    .upi-id {
      font-size: 20px;
      font-weight: 800;
      color: var(--primary);
      margin: 12px 0;
      padding: 12px;
      background: var(--white);
      border-radius: 60px;
      border: 1px dashed var(--primary);
      letter-spacing: 0.3px;
      word-break: break-all;
    }

    .form-group {
      margin-bottom: 24px;
    }

    .form-group label {
      display: block;
      margin-bottom: 10px;
      font-weight: 600;
      color: var(--accent);
      font-size: 15px;
    }

    .form-group input {
      width: 100%;
      padding: 14px 18px;
      border: 1.5px solid var(--border);
      border-radius: 60px;
      font-size: 16px;
      transition: all 0.2s;
      background: white;
    }

    .form-group input:focus {
      border-color: var(--primary);
      outline: none;
      box-shadow: 0 0 0 3px rgba(220, 38, 38, 0.15);
    }

    .submit-btn {
      background: var(--primary);
      color: var(--white);
      width: 100%;
      padding: 16px;
      border: none;
      border-radius: 60px;
      font-size: 17px;
      font-weight: 700;
      cursor: pointer;
      transition: all 0.2s ease;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 12px;
      box-shadow: 0 5px 12px rgba(220, 38, 38, 0.3);
    }

    .submit-btn:hover {
      background: var(--primary-dark);
      transform: translateY(-2px);
    }

    .note {
      font-size: 12px;
      color: var(--text-light);
      margin-top: 20px;
      line-height: 1.45;
    }

    .transaction-id {
      font-weight: 700;
      color: var(--primary);
      background: rgba(220,38,38,0.08);
      padding: 4px 8px;
      border-radius: 30px;
    }

    .success-message {
      display: none;
      background: var(--success);
      color: white;
      padding: 14px 20px;
      border-radius: 60px;
      margin-bottom: 24px;
      text-align: center;
      font-weight: 600;
      font-size: 14px;
    }

    /* responsive: breath and dimension fix for smaller screens */
    @media (max-width: 550px) {
      body {
        padding: 20px 16px;
      }
      .content {
        padding: 24px 18px;
      }
      .plan-card {
        padding: 18px 16px;
        min-height: auto;
      }
      .modal-content {
        padding: 24px 20px;
      }
      .modal-title {
        font-size: 22px;
      }
      .upi-id {
        font-size: 17px;
      }
      .header {
        padding: 26px 20px;
      }
      .bottom-section {
        padding: 28px 20px;
      }
    }
  </style>
</head>
<body>

  <!-- MAIN PAYMENT CONTAINER (consistent width/height, balanced padding) -->
  <div class="container">
    <div class="header">
      <div class="logo">
        <i class="fas fa-shield-alt"></i>
        TYSON HACK
      </div>
      <div class="subtitle">Premium Subscription Plans</div>
    </div>
    
    <div class="content">
      <h2 class="section-title">Select Your Plan</h2>
      
      <div class="plans">
        <!-- PRO PLAN CARD -->
        <div class="plan-card" data-plan="PRO PLAN" data-price="999" data-validity="7 Days">
          <div class="highlight-badge">MOST POPULAR</div>
          <h3>PRO PLAN</h3>
          <div class="price">₹999</div>
          <div class="validity">Valid for 7 Days</div>
          <div class="features">
            <ul>
              <li><i class="fas fa-check"></i> Full access to all features</li>
              <li><i class="fas fa-check"></i> Priority customer support</li>
              <li><i class="fas fa-check"></i> Advanced analytics</li>
            </ul>
          </div>
        </div>
        
        <!-- ULTIMATE PLAN CARD -->
        <div class="plan-card" data-plan="ULTIMATE PLAN" data-price="1499" data-validity="30 Days">
          <div class="highlight-badge">BEST VALUE</div>
          <h3>ULTIMATE PLAN</h3>
          <div class="price">₹1499</div>
          <div class="validity">Valid for 30 Days</div>
          <div class="features">
            <ul>
              <li><i class="fas fa-check"></i> All PRO features included</li>
              <li><i class="fas fa-check"></i> Exclusive premium tools</li>
              <li><i class="fas fa-check"></i> 24/7 dedicated support</li>
            </ul>
          </div>
        </div>
      </div>
      
      <div class="contact-section">
        <a href="https://t.me/TYSON_OWNER" target="_blank" class="contact-btn">
          <i class="fas fa-headset"></i> Contact Support
        </a>
      </div>
    </div>
    
    <div class="footer">
      © 2025 TYSON HACK. All rights reserved.
    </div>
  </div>

  <!-- BOTTOM COMMUNITY SECTION (width aligned, inner breath increased) -->
  <div class="bottom-section">
    <h3>Launch Your Prediction Journey</h3>
    <p>Join TYSON HACK and unlock the power of AI-driven insights for better decision making.</p>
    <a href="https://t.me/addlist/brybA4P0A8xlYjI1" target="_blank" class="join-btn">
      <i class="fas fa-users"></i> Join Our Community
    </a>
    <div class="bottom-footer">
      TYSON HACK is designed for educational and informational purposes.<br />
      Use at your own discretion. © 2025 TYSON HACK.
    </div>
  </div>

  <!-- PAYMENT MODAL (fully functional, improved vertical scrolling & spacing) -->
  <div id="paymentModal" class="modal">
    <div class="modal-content">
      <span class="close">&times;</span>
      <h3 class="modal-title">Complete Your Payment</h3>
      <p class="modal-subtitle">Follow the instructions below to complete your purchase</p>
      
      <div class="success-message" id="successMessage">
        <i class="fas fa-check-circle"></i> Payment submitted successfully!
      </div>
      
      <div class="payment-details">
        <p><span>Selected Plan:</span> <strong id="modalPlan"></strong></p>
        <p><span>Amount:</span> <strong id="modalPrice"></strong></p>
        <p><span>Validity:</span> <strong id="modalValidity"></strong></p>
        <p><span>Transaction ID:</span> <strong class="transaction-id" id="transactionId"></strong></p>
      </div>
      
      <div class="upi-section">
        <p>Please use the following UPI ID to complete your payment:</p>
        <div class="upi-id" id="upiIdDisplay">8092043236@ybl</div>
        <p>If the UPI app doesn't open automatically, please copy this ID and paste it in your payment app.</p>
      </div>
      
      <div class="form-group">
        <label for="utrInput">UTR Number <small>(After completing payment)</small></label>
        <input type="text" id="utrInput" placeholder="Enter your UTR number" autocomplete="off" />
        <div class="note">Your UTR number is a 10-20 digit reference number provided by your bank after successful payment.</div>
      </div>
      
      <button class="submit-btn" id="submitPaymentBtn">
        <i class="fas fa-paper-plane"></i> Submit Payment Details
      </button>
      
      <div class="note">
        <strong>Note:</strong> Your payment will be verified by our team within 24 hours. Please save your Transaction ID for reference.
      </div>
    </div>
  </div>

  <script>
    // DOM elements - exact same logic but improved readability
    const modal = document.getElementById('paymentModal');
    const closeBtn = document.querySelector('.close');
    const planCards = document.querySelectorAll('.plan-card');
    const modalPlan = document.getElementById('modalPlan');
    const modalPrice = document.getElementById('modalPrice');
    const modalValidity = document.getElementById('modalValidity');
    const utrInput = document.getElementById('utrInput');
    const upiIdDisplay = document.getElementById('upiIdDisplay');
    const transactionIdDisplay = document.getElementById('transactionId');
    const successMessageDiv = document.getElementById('successMessage');
    const submitBtn = document.getElementById('submitPaymentBtn');

    // constants
    const upiId = '8092043236@ybl';
    const merchantName = 'TYSON HACK';

    // generate transaction ID (same format as original)
    function generateTransactionId() {
      return 'TXN' + Math.random().toString(36).substring(2, 11).toUpperCase();
    }

    // plan selection & upi intent trigger
    planCards.forEach(card => {
      card.addEventListener('click', () => {
        // remove selected class from all cards
        planCards.forEach(c => c.classList.remove('selected'));
        card.classList.add('selected');

        const plan = card.getAttribute('data-plan');
        const price = card.getAttribute('data-price');
        const validity = card.getAttribute('data-validity');
        const transactionId = generateTransactionId();

        // populate modal fields
        modalPlan.textContent = plan;
        modalPrice.textContent = `₹${price}`;
        modalValidity.textContent = validity;
        upiIdDisplay.textContent = upiId;
        transactionIdDisplay.textContent = transactionId;

        // reset input & success message
        utrInput.value = '';
        successMessageDiv.style.display = 'none';

        // open UPI app (payment intent)
        const upiLink = `upi://pay?pa=${upiId}&pn=${encodeURIComponent(merchantName)}&am=${price}&cu=INR&tn=${encodeURIComponent(`Payment for ${plan} - ${transactionId}`)}`;
        window.location.href = upiLink;

        // show modal after triggering UPI (user will see it on return)
        modal.style.display = 'flex';
      });
    });

    // close modal (X button)
    closeBtn.addEventListener('click', () => {
      modal.style.display = 'none';
      utrInput.value = '';
      successMessageDiv.style.display = 'none';
    });

    // close modal when clicking outside
    window.addEventListener('click', (e) => {
      if (e.target === modal) {
        modal.style.display = 'none';
        utrInput.value = '';
        successMessageDiv.style.display = 'none';
      }
    });

    // submit payment details to telegram (identical validation & message)
    function submitPaymentHandler() {
      const plan = modalPlan.textContent;
      const priceRaw = modalPrice.textContent.replace('₹', '');
      const utr = utrInput.value.trim();
      const transactionId = transactionIdDisplay.textContent;

      // UTR validation: 10-20 alphanumeric chars
      if (!utr || !/^[A-Za-z0-9]{10,20}$/.test(utr)) {
        alert('Please enter a valid UTR number (10–20 alphanumeric characters).');
        utrInput.focus();
        return;
      }

      // show success feedback
      successMessageDiv.style.display = 'block';

      // build telegram message exactly as original
      const message = `New Payment Received!%0A%0ATransaction ID: ${transactionId}%0APlan: ${plan}%0APrice: ₹${priceRaw}%0AUTR: ${utr}%0A%0A~Please verify the payment. Thank you!`;
      const telegramUrl = `https://t.me/TYSON_OWNER?text=${encodeURIComponent(message)}`;
      window.open(telegramUrl, '_blank');

      // auto close modal after 3 seconds and reset selection
      setTimeout(() => {
        modal.style.display = 'none';
        utrInput.value = '';
        successMessageDiv.style.display = 'none';
        // remove selected highlight from any plan card
        planCards.forEach(c => c.classList.remove('selected'));
      }, 3000);
    }

    // attach event listener to submit button
    submitBtn.addEventListener('click', submitPaymentHandler);
  </script>
</body>
</html>
