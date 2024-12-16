https://t.me/@imp3ratorrr

Welcome to the Evilginx Imperator House
Imperator House serves as a collaborative and educational platform for exploring the powerful capabilities of Evilginx, a modern reverse proxy tool. This repository is designed to assist users in understanding, customizing, and enhancing Evilginx, with a focus on Phishlet creation, software modification, and troubleshooting common issues.

Whether you’re new to Evilginx or an experienced user, Imperator House offers resources and guidance to help you master reverse proxy concepts, develop robust configurations, and tackle advanced use cases.

What is Evilginx?
Evilginx is an advanced reverse proxy framework designed primarily for penetration testing and security research. It intercepts and manipulates HTTP/HTTPS requests, enabling powerful capabilities such as session hijacking and phishing through man-in-the-middle techniques. Evilginx can bypass multi-factor authentication (MFA) and other advanced security mechanisms, making it a critical tool for security professionals.

Originally developed by @kgretzky, Evilginx offers a modular architecture centered around Phishlets, YAML configuration files that define how the proxy interacts with specific web services. Evilginx is ideal for simulating sophisticated attacks in controlled environments to test the resilience of authentication systems and security measures.

Why Imperator House?
In the current landscape, misinformation and poorly executed materials have flooded the community. Imperator House was created to provide a professional, educational, and collaborative environment where users can:

Understand Evilginx Concepts: Learn about reverse proxies, session handling, and multi-factor authentication bypass techniques.
Develop Phishlets: Create, customize, and troubleshoot YAML configurations tailored to specific services.
Collaborate and Innovate: Share insights, solve problems together, and push the boundaries of Evilginx’s capabilities.
Our mission is to equip users with the knowledge and tools they need to responsibly and effectively utilize Evilginx.

Features of Evilginx
Session Hijacking
Evilginx intercepts authentication tokens during a phishing attack, allowing attackers to bypass MFA without needing the victim’s credentials.

Phishlets
These YAML-based configuration files define the reverse proxy’s behavior, including URL paths, headers, cookies, and injection scripts. Phishlets are modular, enabling customization for different target services.

JavaScript Injection
Evilginx supports injecting custom JavaScript into proxied pages, allowing dynamic interactions and automation, such as autofilling forms or manipulating page content.

Domain Blacklisting
Evilginx can block or redirect specific domains to avoid detection or disrupt unwanted traffic.

Integration with Puppeteer
Evilginx can integrate with Puppeteer for advanced automation, simulating user actions such as completing captchas or submitting forms.

Session Replay and Debugging
The tool captures session data, providing valuable insights for analysis and debugging.

Modularity
Evilginx’s architecture allows users to expand functionality with custom modules and scripts.

Getting Started with Evilginx
1. Installation Guide
Follow these steps to install Evilginx locally or on a remote server:

Local Installation: Set up Evilginx on your development machine.
Remote Deployment: Install Evilginx on a VPS or cloud server for real-world testing.
Dependencies: Install required packages and libraries, including Nginx, OpenSSL, and GoLang.
2. Configuration
Set up domain names and DNS records for phishing campaigns.
Configure SSL/TLS certificates for secure communications.
3. Quick Start
Run your first phishing campaign by deploying a preconfigured Phishlet. Learn how to manage:

Lures: URLs that victims will visit during an attack.
Redirectors: Fallback pages to maintain stealth.
Sessions: Captured authentication tokens.
Phishlets: The Core of Evilginx
Phishlets are the backbone of Evilginx’s functionality. These YAML files control how Evilginx interacts with web services.

Key Elements of a Phishlet:
Triggers: Define domains, paths, and parameters to determine when actions occur.
Headers: Specify HTTP/HTTPS headers to pass through the proxy.
Cookies: Manage session cookies to maintain stealth.
JavaScript Injection (js_inject): Inject scripts into proxied pages to manipulate behavior dynamically.

Example Phishlet Configuration:
js_inject:
  - trigger_domains: ["www.example.com"]
    trigger_paths: ["/login"]
    script: |
      document.querySelector('#username').value = "{email}";
      document.querySelector('#password').focus();

    Advanced Features
1. JavaScript Injection
Evilginx supports injecting scripts to customize victim interactions. For example, autofill fields or dynamically manipulate page content.

2. Evilpuppet Integration (For Pro Users)
Evilpuppet introduces interactive browser sessions that mimic user behavior to bypass captchas, simulate clicks, and forge tokens.

Example Configuration:
evilpuppet:
  triggers:
    - domains: ["www.example.com"]
      actions:
        - selector: '#email'
          value: '{username}'
        - selector: '#password'
          value: '{password}'
          click: true
  interceptors:
    - token: "session_token"
      url_re: "/sessions"
      abort: true
3. Puppeteer Automation
Integrate Evilginx with Puppeteer for advanced workflows, including headless browsing, form submissions, and debugging.

Security Best Practices
While Evilginx is a powerful tool, it should be used responsibly. Ethical guidelines include:

Using Evilginx solely for educational and penetration testing purposes.
Respecting privacy laws and obtaining explicit permission before running tests.
Avoiding malicious or illegal activities.
Community and Resources
Official Documentation: Learn the fundamentals from the Evilginx GitHub repository.
Forum Discussions: Engage with experts on technical forums.
Imperator House Support: Collaborate with like-minded professionals to overcome challenges and share knowledge.
Disclaimer: Imperator House is an educational platform. Any misuse of Evilginx for illegal or malicious purposes is strictly prohibited and punishable under applicable laws. Users are fully responsible for their actions.

Explore, innovate, and master the capabilities of Evilginx responsibly. Welcome to the Imperator House!
