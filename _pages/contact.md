---
title: "Contact"
layout: page
permalink: /contact/
---
<h1>Contact</h1>

<div class="section-card-container3">
<div class="section-card">
<section class="contact-card">
<h2>Office</h2>
<p>
<!-- Add your room number here, if desired. -->
First Floor, <br>
Mehta Family School of Data Science and Artificial Intelligence<br>
Indian Institute of Technology Roorkee<br>
Roorkee, Uttarakhand 247667, India
</p>
</section>
</div>
<div class="section-card">
<section class="contact-card">
<h2>Email</h2>
<a href="mailto:jagnyashini@cs.iitr.ac.in">
        jagnyashini@cs.iitr.ac.in
</a>
<h2>Phone</h2>
Land Line: +91-1332-285925
</section>
</div>
</div>

<h1>Get in Touch</h1>

<div class="section-card">
<section class="contact-card contact-message">
<h2>Send a message</h2>
<p class="contact-form-note">
This button opens your email application with the message prepared.
</p>

<form id="contactForm">
<label for="contactName">Name</label>
<input id="contactName" name="name" type="text" autocomplete="name" required>

<label for="contactEmail">Email</label>
<input id="contactEmail" name="email" type="email" autocomplete="email" required>

<label for="contactMessage">Message</label>
<textarea
  id="contactMessage"
  name="message"
  rows="7"
  required
  style="display:block; width:700px; max-width:100%; height:180px; padding:12px; box-sizing:border-box;"
></textarea>
<button type="submit">Send message</button>
</form>
</section>
</div>

<script>
  document.getElementById('contactForm').addEventListener('submit', function (event) {
    event.preventDefault();

    if (!this.reportValidity()) return;

    const name = document.getElementById('contactName').value.trim();
    const email = document.getElementById('contactEmail').value.trim();
    const message = document.getElementById('contactMessage').value.trim();

    const subject = encodeURIComponent('Website enquiry from ' + name);
    const body = encodeURIComponent(
      message + '\n\n' +
      'From: ' + name + '\n' +
      'Reply-to: ' + email
    );

    window.location.href =
      'mailto:jagnyashini@cs.iitr.ac.in?subject=' + subject + '&body=' + body;
  });
</script>