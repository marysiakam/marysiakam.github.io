---
title: "Contact"
layout: single
permalink: /contact/
author_profile: true
---

<p class="page-subheading">Have a question or just want to say hi? Send me a note below.</p>

<form class="contact-form" id="contact-form">
  <label for="contact-subject">Subject</label>
  <input type="text" id="contact-subject" name="subject" required>

  <label for="contact-message">Message</label>
  <textarea id="contact-message" name="message" rows="6" required></textarea>

  <button type="submit" class="page-cta">Send email</button>
</form>

<script>
document.getElementById('contact-form').addEventListener('submit', function (e) {
  e.preventDefault();
  var subject = encodeURIComponent(document.getElementById('contact-subject').value);
  var body = encodeURIComponent(document.getElementById('contact-message').value);
  window.location.href = 'mailto:{{ site.email }}?subject=' + subject + '&body=' + body;
});
</script>
