---
layout: main
title: OX1Digital | Contact
---

<form action="https://api.web3forms.com/submit" method="POST" class="contact-form">
  <!-- Web3Forms Access Key -->
  <input type="hidden" name="access_key" value="8899d64b-5cf4-4b0a-8a42-aa4d8af56f6d">
  <input type="hidden" name="subject" value="New Contact / France Subscription Request">

  <!-- Honeypot Bot Trap -->
  <input type="checkbox" name="botcheck" class="hidden" style="display: none;">

  <!-- Form Fields -->
  <div class="form-group">
    <label for="name">Name</label>
    <input type="text" id="name" name="name" placeholder="Your name" required>
  </div>

  <div class="form-group">
    <label for="email">Email Address</label>
    <input type="email" id="email" name="email" placeholder="you@example.com" required>
  </div>

  <div class="form-group">
    <label for="message">Message <span class="optional">(Optional if only subscribing)</span></label>
    <textarea id="message" name="message" rows="5" placeholder="How can I help? (Leave blank if you're just subscribing to France updates)"></textarea>
  </div>

  <!-- Subscription Opt-in -->
  <div class="form-group checkbox-group">
    <label class="checkbox-label">
      <input type="checkbox" name="subscribe_to_france" value="Yes" checked>
      <span>Email me automatically whenever new France updates are published</span>
    </label>
  </div>

  <button type="submit" class="submit-btn">Send Message / Subscribe</button>
</form>
