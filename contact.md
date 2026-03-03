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

    </form>
    
<script>
  (function () {
    const form = document.getElementById("contactForm");
    if (!form) return;

    form.addEventListener("submit", async function (e) {
      e.preventDefault();

      const formData = new FormData(form);

      try {
        const res = await fetch(form.action, {
          method: "POST",
          body: formData,
          headers: { "Accept": "application/json" }
        });

        if (res.ok) {
          window.location.href = "/thank-you/";
          return;
        }

        const data = await res.json().catch(() => null);
        const msg = data && data.errors && data.errors.length
          ? data.errors.map(x => x.message).join(" | ")
          : "Submission failed. Please try again.";

        alert(msg);
      } catch (err) {
        alert("Network error. Please try again.");
      }
    });
  })();
</script>
