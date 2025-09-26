# GEAInnovationStudios
Contains the shop template by GEA Innovation Studios for Minh-An Lee

Shop Template (Proprietary)

A minimal, clean, and responsive storefront template built with plain HTML/CSS/JS.
It uses localStorage for persistence and JSON files for demo data, and includes a simple in-browser cart, product modal, and a demo checkout flow.

⚠️ Important: This template is for learning and prototyping only.
Do not store real payment data, card numbers, or sensitive personal info. Use a proper backend + payment provider (e.g., Stripe) in production.

Features

Sticky nav with tabs (Home / Info / About)

Search + sort controls (relevance, price, name)

Responsive product grid + product modal

Local cart drawer with quantity edits & subtotal

Demo checkout summary (no real payments)

Login/signup demo with SHA-256 password hashing (no salt; not for production)

Editable “Info” and “About” sections with local save

Import/export JSON for accounts, items, and guest cart

Keyboard-friendly dialogs (Esc to close), ARIA labels, and semantic structure

Quick Start

Clone or download the repo/files.

(Optional) Serve locally with any static server (e.g., VS Code Live Server).
You can also just open index.html directly in your browser.

(Optional) Create a data/ folder and add:

data/shopitems.json → { "items": [...] }

data/accounts.json → { "users": [...] }
If these aren’t present, the template falls back to the embedded sample JSON.

Demo user is included via sample JSON (demo@shop.local). The password hash is set on first successful login with demo1234.

Project Structure
index.html           # All markup, styles, and app script in one file
data/
  shopitems.json     # (Optional) product catalog
  accounts.json      # (Optional) demo accounts store


If data/*.json is missing, the app uses the embedded <script type="application/json"> samples.

Persistent data (active account, items cache, info/about content, and guest cart) is stored in localStorage.

Configuration & Data

Currency: Uses the browser locale with EUR. Change the fmt function if needed.

Products: Edit data/shopitems.json or the embedded sample JSON.

Accounts: Edit data/accounts.json or use the app’s signup flow (for demo only).

Editable pages: “Info” and “About” can be edited in the UI and saved to localStorage.

Security & Privacy Notes

Do not store real card numbers, CVV, or full addresses in plaintext JSON or localStorage.

The password hashing is a basic SHA-256 demo without salt/pepper and without a server; this is not secure.
For real apps: use a backend with a modern password hasher (Argon2id/bcrypt/scrypt), sessions, TLS, and a real payment processor (Stripe/Adyen/etc.).

Accessibility

Uses semantic HTML, ARIA attributes, and focusable controls

Dialogs block background and close with Esc

Buttons have descriptive labels; images used as CSS backgrounds should also have textual context in the DOM

Browser Support

Modern evergreen browsers (Chromium, Firefox, Safari).
If you must support older browsers, polyfills may be needed for crypto.subtle, Intl.NumberFormat, etc.

Known Limitations

No real backend or authentication/session management

No inventory/stock or shipping/tax calculation

Password hashing is client-side and unsalted (demo only)

Images are demo links (e.g., Unsplash); replace with your own assets for production

Import/Export

Export: accounts, guest cart, and item catalog as JSON (via footer buttons)

Import: load accounts.json or shopitems.json to quickly seed your demo data

Third-Party Assets

Image URLs in the sample data reference Unsplash and are for demo purposes only.
Replace these before publishing, and ensure you comply with the image license/attribution requirements.

License / EULA 

Copyright © 2025 Edo. All rights reserved.

By accessing, downloading, or using this software (the “Software”), you agree to the following terms:

License Grant. You are granted a personal, non-exclusive, non-transferable, revocable license to use the Software for your own non-commercial learning and prototyping.

No Redistribution. You may not copy, publish, sublicense, sell, rent, lease, loan, distribute, or otherwise make the Software (or any derivative works) available to third parties without prior written permission from the copyright holder.

No Modification. You may not modify, adapt, translate, port, or create derivative works of the Software without prior written permission.

No Reverse Engineering. You may not reverse engineer, decompile, disassemble, or attempt to extract source code or underlying ideas/algorithms from any part of the Software.

No Data Mining / Model Training. You may not use the Software or its contents to train, fine-tune, or evaluate machine learning models, nor to create datasets for such purposes, without prior written permission.

Third-Party Services. In production, you must integrate a legitimate backend and payment provider. The author is not responsible for your use of third-party services.

Disclaimer of Warranty. THE SOFTWARE IS PROVIDED “AS IS,” WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE, AND NON-INFRINGEMENT.

Limitation of Liability. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR ANY CLAIM, DAMAGES, OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT, OR OTHERWISE, ARISING FROM, OUT OF, OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

Termination. This license automatically terminates if you breach any term. Upon termination, you must cease use and destroy all copies.

Reservation of Rights. All rights not expressly granted are reserved by the copyright holder.

If you want to publish, customize, or commercialize this project, ask for written permission first.

Contributing

Contributions are currently not accepted. Feel free to open an issue to report bugs or request permission.

Changelog

v1.0.0 (2025-09-26): Initial public release of the demo template.

Contact

For permissions or questions, contact: yes_iam2001 (discord)
