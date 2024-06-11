<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Security Testing Checklist</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }
        .section {
            margin-bottom: 20px;
        }
        .section h2 {
            background-color: #f2f2f2;
            padding: 10px;
            border: 1px solid #ddd;
            margin: 0;
        }
        .item {
            margin-left: 20px;
        }
        .complete {
            color: green;
            font-weight: bold;
        }
        .incomplete {
            color: red;
            font-weight: bold;
        }
    </style>
</head>
<body>

<h1>Security Testing Checklist</h1>

<div id="checklist">
    <div class="section">
        <h2>Information Gathering</h2>
        <label class="item"><input type="checkbox" class="check-item"> Manually explore the site</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Spider/crawl for missed or hidden content</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Check for files that expose content, such as robots.txt, sitemap.xml, .DS_Store</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Check the caches of major search engines for publicly accessible sites</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Check for differences in content based on User Agent (eg, Mobile sites, access as a Search engine Crawler)</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Perform Web Application Fingerprinting</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Identify technologies used</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Identify user roles</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Identify application entry points</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Identify client-side code</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Identify multiple versions/channels (e.g. web, mobile web, mobile app, web services)</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Identify co-hosted and related applications</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Identify all hostnames and ports</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Identify third-party hosted content</label><br>
    </div>

    <div class="section">
        <h2>Configuration Management</h2>
        <label class="item"><input type="checkbox" class="check-item"> Check for commonly used application and administrative URLs</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Check for old, backup and unreferenced files</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Check HTTP methods supported and Cross Site Tracing (XST)</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test file extensions handling</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for security HTTP headers (e.g. CSP, X-Frame-Options, HSTS)</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for policies (e.g. Flash, Silverlight, robots)</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for non-production data in live environment, and vice-versa</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Check for sensitive data in client-side code (e.g. API keys, credentials)</label><br>
    </div>

    <div class="section">
        <h2>Secure Transmission</h2>
        <label class="item"><input type="checkbox" class="check-item"> Check SSL Version, Algorithms, Key length</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Check for Digital Certificate Validity (Duration, Signature and CN)</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Check credentials only delivered over HTTPS</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Check that the login form is delivered over HTTPS</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Check session tokens only delivered over HTTPS</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Check if HTTP Strict Transport Security (HSTS) in use</label><br>
    </div>

    <div class="section">
        <h2>Authentication</h2>
        <label class="item"><input type="checkbox" class="check-item"> Test for user enumeration</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for authentication bypass</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for bruteforce protection</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test password quality rules</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test remember me functionality</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for autocomplete on password forms/input</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test password reset and/or recovery</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test password change process</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test CAPTCHA</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test multi factor authentication</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for logout functionality presence</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for cache management on HTTP (eg Pragma, Expires, Max-age)</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for default logins</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for user-accessible authentication history</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for out-of channel notification of account lockouts and successful password changes</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for consistent authentication across applications with shared authentication schema / SSO</label><br>
    </div>

    <div class="section">
        <h2>Session Management</h2>
        <label class="item"><input type="checkbox" class="check-item"> Establish how session management is handled in the application (eg, tokens in cookies, token in URL)</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Check session tokens for cookie flags (httpOnly and secure)</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Check session cookie scope (path and domain)</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Check session cookie duration (expires and max-age)</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Check session termination after a maximum lifetime</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Check session termination after relative timeout</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Check session termination after logout</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test to see if users can have multiple simultaneous sessions</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test session cookies for randomness</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Confirm that new session tokens are issued on login, role change and logout</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for consistent session management across applications with shared session management</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for session puzzling</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for CSRF and clickjacking</label><br>
    </div>

    <div class="section">
        <h2>Authorization</h2>
        <label class="item"><input type="checkbox" class="check-item"> Test for path traversal</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for bypassing authorization schema</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for vertical Access control problems (a.k.a. Privilege Escalation)</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for horizontal Access control problems (between two users at the same privilege level)</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for missing authorization</label><br>
    </div>

    <div class="section">
        <h2>Data Validation</h2>
        <label class="item"><input type="checkbox" class="check-item"> Test for Reflected Cross Site Scripting</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for Stored Cross Site Scripting</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for DOM based Cross Site Scripting</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for Cross Site Flashing</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for HTML Injection</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for SQL Injection</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for SOQL Injection</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for LDAP Injection</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for ORM Injection</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for XML Injection</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for XXE Injection</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for SSI Injection</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for XPath Injection</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for XQuery Injection</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for IMAP/SMTP Injection</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for Code Injection</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for Expression Language Injection</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for Command Injection</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for Overflow (Stack, Heap and Integer)</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for Format String</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for incubated vulnerabilities</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for HTTP Splitting/Smuggling</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for HTTP Verb Tampering</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for Open Redirection</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for Local File Inclusion</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for Remote File Inclusion</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Compare client-side and server-side validation rules</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for NoSQL injection</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for HTTP parameter pollution</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for auto-binding</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for Mass Assignment</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for NULL/Invalid Session Cookie</label><br>
    </div>

    <div class="section">
        <h2>Denial of Service</h2>
        <label class="item"><input type="checkbox" class="check-item"> Test for anti-automation</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for account lockout</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for HTTP protocol DoS</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for SQL wildcard DoS</label><br>
    </div>

    <div class="section">
        <h2>Business Logic</h2>
        <label class="item"><input type="checkbox" class="check-item"> Test for feature misuse</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for lack of non-repudiation</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for trust relationships</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for integrity of data</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test segregation of duties</label><br>
    </div>

    <div class="section">
        <h2>Cryptography</h2>
        <label class="item"><input type="checkbox" class="check-item"> Check if data which should be encrypted is not</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Check for wrong algorithms usage depending on context</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Check for weak algorithms usage</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Check for proper use of salting</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Check for randomness functions</label><br>
    </div>

    <div class="section">
        <h2>Risky Functionality - File Uploads</h2>
        <label class="item"><input type="checkbox" class="check-item"> Test that acceptable file types are whitelisted</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test that file size limits, upload frequency and total file counts are defined and are enforced</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test that file contents match the defined file type</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test that all file uploads have Anti-Virus scanning in-place.</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test that unsafe filenames are sanitised</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test that uploaded files are not directly accessible within the web root</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test that uploaded files are not served on the same hostname/port</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test that files and other media are integrated with the authentication and authorisation schemas</label><br>
    </div>

    <div class="section">
        <h2>Risky Functionality - Card Payment</h2>
        <label class="item"><input type="checkbox" class="check-item"> Test for known vulnerabilities and configuration issues on Web Server and Web Application</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for default or guessable password</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for non-production data in live environment, and vice-versa</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for Injection vulnerabilities</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for Buffer Overflows</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for Insecure Cryptographic Storage</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for Insufficient Transport Layer Protection</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for Improper Error Handling</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for all vulnerabilities with a CVSS v2 score > 4.0</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for Authentication and Authorization issues</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for CSRF</label><br>
    </div>

    <div class="section">
        <h2>HTML 5</h2>
        <label class="item"><input type="checkbox" class="check-item"> Test Web Messaging</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Test for Web Storage SQL injection</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Check CORS implementation</label><br>
        <label class="item"><input type="checkbox" class="check-item"> Check Offline Web Application</label><br>
    </div>
</div>

<p id="status" class="incomplete">Checklist is incomplete</p>

<script>
    document.querySelectorAll('.check-item').forEach(item => {
        item.addEventListener('change', checkCompletion);
    });

    function checkCompletion() {
        const allChecked = Array.from(document.querySelectorAll('.check-item')).every(item => item.checked);
        const status = document.getElementById('status');
        if (allChecked) {
            status.textContent = 'Checklist is complete';
            status.className = 'complete';
        } else {
            status.textContent = 'Checklist is incomplete';
            status.className = 'incomplete';
        }
    }
</script>

</body>
</html>
