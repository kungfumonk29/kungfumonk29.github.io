---
layout: default
title: Contact
permalink: /contact/
---

# Get in Touch

<div class="contact-grid">

  <div class="contact-left">
    <h2>Contact</h2>
    <p>
      For consulting opportunities, strategic discussions, or collaborations,
      feel free to reach out using the form.
    </p>

    <p><strong>Current Location</strong><br>
    Canary Wharf, London</p>

    <div class="map">
      <iframe
        src="https://www.google.com/maps?q=Canary+Wharf,+London&output=embed"
        loading="lazy">
      </iframe>
    </div>
  </div>

  <div class="contact-right">
    <form action="https://formspree.io/f/xpqjgwwq" method="POST">

      <label>Name</label>
      <input type="text" name="name" required>

      <label>Company</label>
      <input type="text" name="company">

      <label>Reason for Contact</label>
      <input type="text" name="reason">

      <label>Message</label>
      <textarea name="message" required></textarea>

      <button class="button" type="submit">Send</button>

      <input type="hidden" name="_redirect" value="https://aryamangupta.co/thank-you/">

    </form>
  </div>

</div>
