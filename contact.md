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
      please use the form.
    </p>

    <p>
      <strong>Current Location</strong><br>
      Canary Wharf, London
    </p>

    <div class="map">
      <iframe
        src="https://www.google.com/maps?q=Canary+Wharf,+London&output=embed"
        loading="lazy">
      </iframe>
    </div>
  </div>

  <div class="contact-right">

    <form id="contactForm">

      <!-- Honeypot (anti-spam) -->
      <input type="text" name="website" style="display:none" tabindex="-1" autocomplete="off">

      <label>Name</label>
      <input type="text" name="name" required>

      <label>Email</label>
      <input type="email" name="email" required>

      <label>Company</label>
      <input type="text" name="company">

      <label>Reason for Contact</label>
      <input type="text" name="reason">

      <label>Message</label>
      <textarea name="message" required></textarea>

      <button class="button" type="submit">Send</button>

    </form>

  </div>

</div>

<script>
(function () {
  const form = document.getElementById("contactForm");
  if (!form) return;

  const ENDPOINT = "https://billowing-dew-f772.aryaman-gupta.workers.dev/contact";

  form.addEventListener("submit", async (e) => {
    e.preventDefault();

    const button = form.querySelector("button");
    button.disabled = true;
    button.textContent = "Sending...";

    const payload = Object.fromEntries(new FormData(form).entries());

    try {
      const res = await fetch(ENDPOINT, {
        method: "POST",
        headers: { "Content-Type": "application/json" },
        body: JSON.stringify(payload),
      });

      if (res.ok) {
        window.location.href = "/thank-you/";
        return;
      }

      const text = await res.text().catch(() => "");
      alert("Failed to send. " + (text || "Please try again."));
    } catch {
      alert("Network error. Please try again.");
    }

    button.disabled = false;
    button.textContent = "Send";
  });
})();
</script>
