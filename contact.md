---
layout: default
title: Contact
permalink: https://builtbyg.github.io/contact/
---
* * *
## [Home](./index.md)
* * *
## Let's Connect!

<style>
  form {
    max-width: 600px;
    margin: 0 auto;
    font-family: Arial, sans-serif;
  }

  .form-group {
    display: flex;
    flex-direction: column;
    margin-bottom: 1.5em;
  }

  label {
    font-weight: bold;
    margin-bottom: 0.5em;
  }

  input,
  textarea {
    padding: 0.75em;
    font-size: 1em;
    border: 1px solid #ccc;
    border-radius: 6px;
    width: 100%;
    box-sizing: border-box;
  }

  textarea {
    resize: vertical;
    min-height: 120px;
  }

  button {
    background-color: #007bff;
    color: white;
    padding: 0.75em 1.5em;
    border: none;
    border-radius: 6px;
    font-size: 1em;
    cursor: pointer;
    transition: background-color 0.3s ease;
  }

  button:hover {
    background-color: #0056b3;
  }
</style>

<form action="https://formspree.io/f/xyzwqder" method="POST">
  <div class="form-group">
    <label for="firstName">First Name:</label>
    <input type="text" id="firstName" name="First Name" required>
  </div>

  <div class="form-group">
    <label for="surname">Surname:</label>
    <input type="text" id="surname" name="Surname" required>
  </div>

  <div class="form-group">
    <label for="email">Your Email:</label>
    <input type="email" id="email" name="email" required>
  </div>

  <div class="form-group">
    <label for="message">Your Message:</label>
    <textarea id="message" name="message" required></textarea>
  </div>

  <button type="submit">Send</button>
</form>
