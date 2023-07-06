<!DOCTYPE html>
<html>
<head>
</head>
<body>
  <header>
    <h1 style="text-align: center; font-size: 24px; margin: 20px;">Web Application Security</h1>
  </header>

  <section>
    <h2 style="font-size: 20px;">Installation and Setup</h2>
    <p>To practice and apply my knowledge, I will be installing Owasp Juice Shop, a vulnerable full JavaScript web application designed by Owasp.</p>
    <ol>
      <li>Clone the repository: <code>git clone https://github.com/juice-shop/juice-shop</code></li>
      <li>Navigate to the project directory: <code>cd juice-shop</code></li>
      <li>Install the required dependencies: <code>npm install</code></li>
      <li>Start the application: <code>npm start</code></li>
    </ol>
    <img src="https://th.bing.com/th/id/R.12ee318566a8850abfea46d0129f6fe3?rik=TOem1fxrHz3OWg&pid=ImgRaw&r=0" alt="Owasp Juice Shop Screenshot">
  </section>

  <section>
    <h2 style="font-size: 20px;">Web Application Security Topics</h2>
    <p>During my learning journey, I will be covering various topics related to web application security. Some of the key areas include:</p>
    <ol>
      <li>Cross-Site Scripting (XSS)</li>
      <li>SQL Injection Fundamentals</li>
      <li>SQLMap</li>
      <li>Command Injections</li>
      <li>File Upload Attacks</li>
      <li>Broken Authentication</li>
      <li>File Inclusion</li>
      <li>XML Attacks</li>
      <li>XXE (XML External Entity) Attacks</li>
      <li>Insecure Direct Object References (IDOR)</li>
      <li>API Attacks</li>
    </ol>
  </section>

  <section>
    <h1 style="font-size: 24px;">Cross-Site Scripting (XSS)</h1>
    <h2 style="font-size: 20px;">DOM-Based XSS Vulnerability</h2>
    <p>Unlike reflected XSS and stored XSS, the DOM-Based XSS vulnerability occurs on the client side. This means that an attacker can send a URL that contains some malicious JavaScript code. This code will be executed on the client's browser.</p>
    <p>On the Juice Shop app, let's try searching for something, like "Apple" for example.</p>
    <img src="https://github.com/msfcode/WebAppSec/assets/74313566/b501b49d-00bc-4723-92a6-444fd0bd48e1)">
    <p>Try to inspect the elements of the website:</p>
    <p>As we can see here, whatever we enter in the search input appears in the code:</p>
    <p>Another example, what if we try to inject an &lt;img&gt; tag and replace the link with an image link like "https://i.imgflip.com/u9pv5.jpg":</p>
    <img src="https://i.imgflip.com/u9pv5.jpg" alt="Injected Image">
    <p>But we can try to execute some JavaScript code using the &lt;iframe&gt; tag:</p>
    <iframe src="javascript:alert('DOMED')"></iframe>
    <p>You can, of course, search for another payload to test DOM-Based vulnerability on the
