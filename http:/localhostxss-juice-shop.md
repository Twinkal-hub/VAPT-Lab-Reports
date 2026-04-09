# Cross-Site Scripting (XSS) - OWASP Juice Shop

## Overview
Cross-Site Scripting (XSS) is a web security vulnerability that allows attackers to inject and execute malicious JavaScript in a user's browser.

## Target
OWASP Juice Shop Application

## Vulnerability Type
DOM-Based XSS

## Payload Used
<img src=x onerror=alert('XSS')>

## Steps to Reproduce
1. Open OWASP Juice Shop application
2. Navigate to search functionality
3. Inject payload via URL parameter:
   /#/search?q=<img src=x onerror=alert('XSS')>
4. Payload gets executed in browser context
5. Alert popup is triggered successfully

## Impact
- Execution of arbitrary JavaScript in user browser
- Possible session hijacking
- Data theft and manipulation

## Mitigation
- Input sanitization
- Output encoding
- Implement Content Security Policy (CSP)

## Result
Successfully demonstrated DOM-based Cross-Site Scripting (XSS) vulnerability with proof of execution.

## Note
During testing, a minor console syntax error was observed due to DOM manipulation. However, successful JavaScript execution confirms the presence of XSS vulnerability.

## Proof
![XSS Proof]()
