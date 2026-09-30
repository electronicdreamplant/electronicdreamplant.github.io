---
layout: main
title: OX1Digital | Contact
---

<form action="https://api.web3forms.com/submit" method="POST" class="contact-form" novalidate>
  <!-- Web3Forms Config -->
  <input type="hidden" name="access_key" value="8899d64b-5cf4-4b0a-8a42-aa4d8af56f6d">
  <input type="hidden" name="subject" value="New Contact / France Subscription Request">

  <!-- Honeypot Bot Trap -->
  <input type="checkbox" name="botcheck" class="visually-hidden" tabindex="-1" autocomplete="off">

  <!-- Name Field -->
  <div class="form-group">
    <label class="form-label" for="name">
      Full name
    </label>
    <input class="form-control" id="name" name="name" type="text" autocomplete="name" required>
  </div>

  <!-- Email Field -->
  <div class="form-group">
    <label class="form-label" for="email">
      Email address
    </label>
    <span id="email-hint" class="form-hint">
      We’ll only use this to respond to your message or send published updates.
    </span>
    <input class="form-control" id="email" name="email" type="email" spellcheck="false" aria-describedby="email-hint" autocomplete="email" required>
  </div>

  <!-- Message Field -->
  <div class="form-group">
    <label class="form-label" for="message">
      Message <span class="form-hint-inline">(optional)</span>
    </label>
    <span id="message-hint" class="form-hint">
      Leave this blank if you are only signing up for email updates.
    </span>
    <textarea class="form-control" id="message" name="message" rows="5" aria-describedby="message-hint"></textarea>
  </div>

  <!-- Checkbox / Opt-in Component -->
  <div class="form-group">
    <div class="checkboxes__item">
      <input class="checkboxes__input" id="subscribe_to_france" name="subscribe_to_france" type="checkbox" value="Yes" checked>
      <label class="form-label checkboxes__label" for="subscribe_to_france">
        Email me automatically whenever new France updates are published
      </label>
    </div>
  </div>

  <!-- Button Component -->
  <button type="submit" class="submit-btn">
    Send message
  </button>
</form>
