# Networkwalks-B084-week3-password-cracking
<!DOCTYPE html>

<html lang="en">

<head>


</head>

<body>



<header>

<div>

<span class="badge">🔐 CYBERSECURITY LAB</span>

<span class="badge">KALI LINUX</span>

<span class="badge">ETHICAL HACKING</span>

</div>

<h1>Password Cracking<br>with John The Ripper (JTR)</h1>

<p>Cracking a password-protected PDF in a controlled lab to learn why strong passwords matter.</p>

</header>



<div class="container">



<div class="card">

<h2>📌 Project Overview</h2>

<p><b>Task:</b> Crack the password of a protected PDF file <code>My Locked PDF1.pdf</code> using JTR John and JTR Johnny.</p>

<p style="margin-top:10px">This was done in a <b>lab environment only</b> for learning password security, auditing, and penetration testing fundamentals.</p>

<div class="grid" style="margin-top:15px">

<div class="mini"><b>OS:</b> Kali Linux<br><b>Tools:</b> John the Ripper Jumbo, Johnny (GUI), pdf2john</div>

<div class="mini"><b>Target:</b> My Locked PDF.pdf<br><b>Attack Type:</b> Wordlist Attack<br><b>Wordlist:</b> rockyou.txt</div>

</div>

</div>



<div class="card">

<h2>🧠 Background</h2>

<p>John the Ripper (JTR) is a popular password cracking tool used by security professionals to test how strong passwords are. It started for Unix systems but now works on Windows, Linux, and Mac.</p>

<p style="margin-top:10px">It can check many types of password hashes and also unlock password-protected files like PDF, ZIP, and Office documents.</p>

<p style="margin-top:10px"><b>Johnny</b> is the graphical version of John the Ripper. It gives a simple point-and-click screen, so beginners can use JTR without typing long commands.</p>

</div>



<div class="card">

<h2>🛠️ Tools Used</h2>

<ul>

<li><b>John the Ripper (Jumbo):</b> Command-line password cracker</li>

<li><b>Johnny:</b> GUI for John the Ripper</li>

<li><b>pdf2john:</b> Extracts hash from PDF file</li>

<li><b>rockyou.txt:</b> Common passwords wordlist on Kali</li>

<li><b>Kali Linux Terminal:</b> For running all commands</li>

</ul>

</div>



<div class="card">

<h2>⚙️ Step-by-Step Process</h2>



<h3>1. Extract Hash From PDF</h3>

<pre>pdf2john "My Locked PDF1.pdf" > hash.txt

cat hash.txt</pre>

<p>Result: 1 password hash loaded - PDF [MD5 SHA2 RC4/AES 32/64]</p>



<h3>2. Prepare Wordlist on Kali</h3>

<pre>sudo gzip -d /usr/share/wordlists/rockyou.txt.gz

ls -lh /usr/share/wordlists/rockyou.txt</pre>



<h3>3. Start Wordlist Attack</h3>

<pre>john --wordlist=/usr/share/wordlists/rockyou.txt hash.txt</pre>



<h3>4. Show Cracked Password</h3>

<pre>john --show hash.txt</pre>



<h3>5. If Needed - Clear Old Session</h3>

<pre>rm ~/.john/john.pot

john --wordlist=/usr/share/wordlists/rockyou.txt hash.txt</pre>

</div>



<div class="card success">

<h2>✅ What I Learned</h2>

<ul>

<li>Weak / common passwords in rockyou.txt can be cracked in seconds</li>

<li>PDF protection is only as strong as the password behind it</li>

<li>Password cracking is for testing defences, not for breaking into real accounts</li>

<li>Johnny makes the same attack easier for beginners with a GUI</li>

</ul>

</div>



<div class="card warn">

<h2>🛡️ Security Takeaway</h2>

<p>Use long, unique, and complex passwords. Enable MFA wherever possible. What takes you 5 seconds to type could take an attacker 5 seconds to crack if it is weak.</p>

<p style="margin-top:10px"><b>Best Practice:</b> 14+ characters, mix of upper, lower, numbers, symbols, and never reuse passwords.</p>

</div>



<div class="card">

<h2>⚠️ Disclaimer</h2>

<p>This project was completed for educational purposes in a controlled lab. Do not use these techniques on systems or files you do not own or do not have permission to test.</p>

</div>



<div class="card" style="text-align:center">

<h2>Connect With Me</h2>

<p>Interested in Cybersecurity, Ethical Hacking & Penetration Testing?</p>

<p style="margin-top:10px"><a href="#">LinkedIn</a> https://www.linkedin.com/in/vincent-goodluck-43754636a/?lipi=urn%3Ali%3Apage%3Ad_flagship3_profile_view_base_contact_details%3Bp1jdZLoiSG65%2BH79tPkGlg%3D%3D • 

<p style="margin-top:12px">#Cybersecurity #EthicalHacking #JohnTheRipper #KaliLinux #PenetrationTesting</p>

</div>



</div>



<footer>Built for learning | Password Cracking with JTR Lab • 2026</footer>



</body>

</html>
