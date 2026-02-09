# 📱 Panific Sales Receipt Generator

A mobile-first, professional receipt generator built for field sales teams in Ghana. Generate beautiful PDF receipts on-the-go with automatic Ghana Cedi conversion and instant sharing capabilities.

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?logo=tailwind-css&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)

## ✨ Features

### 🎯 Core Functionality
- **Auto-Generated Receipt Numbers** - Unique timestamp-based IDs (e.g., RCPT-2026-001234)
- **Smart Date Selection** - Editable date picker with current date pre-filled
- **Ghana Cedi Conversion** - Automatic amount-to-words conversion
  - Example: `GH₵ 150.50` → "One Hundred and Fifty Ghana Cedis and Fifty Pesewas"
- **Payment Methods** - Support for Momo, Cash, and Cheque
- **Conditional Cheque Field** - Cheque number input appears only when Cheque is selected
- **Company Branding** - Upload your company logo
- **Digital Signatures** - Pre-set salesperson signatures in stylish font

### 📤 Sharing & Export
- **PDF Generation** - Professional A4 format receipts
- **Web Share API** - Direct sharing to:
  - WhatsApp
  - Email
  - SMS
  - Any sharing-enabled app
- **Fallback Download** - Automatic download if sharing isn't supported

### 📱 Mobile-Optimized
- **Large Touch Targets** - Finger-friendly input fields
- **Fixed Bottom Actions** - Easy thumb access on mobile
- **Responsive Design** - Works perfectly on all screen sizes
- **Clean UI** - Modern Tailwind CSS styling

## 🚀 Quick Start

### Option 1: Direct Use (No Installation)

1. **Download** the `receipt-generator.html` file
2. **Open** it in any modern web browser (Chrome, Safari, Firefox, Edge)
3. **Start generating receipts** immediately!

### Option 2: Deploy to Web

#### Using GitHub Pages:

```bash
# 1. Fork this repository
# 2. Go to Settings → Pages
# 3. Select main branch as source
# 4. Your app will be live at: https://yourusername.github.io/receipt-generator
```

#### Using Netlify:

```bash
# 1. Connect your GitHub repo to Netlify
# 2. Deploy with one click
# 3. Get your custom URL
```

#### Using Vercel:

```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
vercel
```

## 📖 How to Use

### Basic Workflow

1. **Upload Company Logo** (Optional)
   - Click "Upload Logo" button
   - Select your company logo image

2. **Fill Receipt Details**
   - Customer Name *(required)*
   - Amount in GH₵ *(auto-converts to words)*
   - Date *(pre-filled, but editable)*
   - Payment Type *(Momo/Cash/Cheque)*
   - Cheque Number *(appears only if Cheque selected)*
   - Salesperson Name *(your signature)*

3. **Generate PDF**
   - Click "Generate PDF" button
   - Wait for confirmation

4. **Share Receipt**
   - Click "Share Receipt" button
   - Choose WhatsApp, Email, or other apps
   - Or download if sharing not available

### Screenshots

```
┌─────────────────────────────┐
│  SALES RECEIPT GENERATOR    │
│  📧 info@panific.com        │
├─────────────────────────────┤
│  [Upload Logo]              │
│                             │
│  Receipt: RCPT-2026-123456  │
│  Date: [09/02/2026]         │
│  Customer: [John Doe]       │
│  Amount: [150.50]           │
│  Words: One Hundred and...  │
│  Payment: [Cheque ▼]        │
│  Cheque #: [001234]         │
│  Salesperson: [Your Name]   │
├─────────────────────────────┤
│ [Generate PDF] [Share]      │
└─────────────────────────────┘
```

## 🛠️ Technical Details

### Built With
- **HTML5** - Structure
- **Tailwind CSS** - Styling (CDN)
- **JavaScript (ES6+)** - Logic
- **html2pdf.js** - PDF generation

### Browser Support
- ✅ Chrome (Android & Desktop)
- ✅ Safari (iOS & macOS)
- ✅ Firefox
- ✅ Edge
- ✅ Opera

### File Structure
```
receipt-generator/
│
├── receipt-generator.html    # Main application file
├── README.md                  # Documentation
└── LICENSE                    # MIT License
```

## 🔧 Customization

### Change Company Email
Edit line ~38 in the HTML file:
```html
<p class="text-sm text-gray-600 mb-4">📧 your-email@company.com</p>
```

### Change Receipt Number Format
Edit the `initializeReceipt()` function:
```javascript
const receiptNum = `RCPT-2026-${String(timestamp).slice(-6)}`;
// Change to your preferred format, e.g.:
const receiptNum = `PAN-${year}-${String(timestamp).slice(-6)}`;
```

### Customize PDF Layout
Edit the `receipt-preview` div section (starts around line ~150)

### Add More Payment Methods
Edit the payment type dropdown:
```html
<select id="paymentType">
    <option value="Momo">Mobile Money (Momo)</option>
    <option value="Cash">Cash</option>
    <option value="Cheque">Cheque</option>
    <option value="Bank Transfer">Bank Transfer</option> <!-- Add this -->
</select>
```

## 🚀 Future Enhancements

### Planned Features
- [ ] **PWA Support** - Offline functionality
- [ ] **Firebase Backend** - Store receipt history
- [ ] **Multi-language Support** - English, Twi, Ga, etc.
- [ ] **QR Code Generation** - For verification
- [ ] **Email Auto-send** - Direct email to customer
- [ ] **Analytics Dashboard** - Sales tracking
- [ ] **Multiple Currency Support** - USD, EUR, GBP
- [ ] **Receipt Templates** - Multiple design options

### Want to Contribute?
See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines

## 📱 Progressive Web App (PWA) Setup

To make this installable as an app:

1. Create `manifest.json`:
```json
{
  "name": "Panific Receipt Generator",
  "short_name": "Receipts",
  "start_url": "/",
  "display": "standalone",
  "background_color": "#ffffff",
  "theme_color": "#3b82f6",
  "icons": [
    {
      "src": "icon-192.png",
      "sizes": "192x192",
      "type": "image/png"
    },
    {
      "src": "icon-512.png",
      "sizes": "512x512",
      "type": "image/png"
    }
  ]
}
```

2. Create `service-worker.js` for offline support
3. Link manifest in HTML head section

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🤝 Support

- **Email**: info@panific.com
- **Issues**: [GitHub Issues](https://github.com/yourusername/receipt-generator/issues)
- **Discussions**: [GitHub Discussions](https://github.com/yourusername/receipt-generator/discussions)

## 🙏 Acknowledgments

- Built with ❤️ for field sales teams in Ghana
- Powered by [Tailwind CSS](https://tailwindcss.com/)
- PDF generation by [html2pdf.js](https://ekoopmans.github.io/html2pdf.js/)

## 📊 Stats

![GitHub stars](https://img.shields.io/github/stars/yourusername/receipt-generator?style=social)
![GitHub forks](https://img.shields.io/github/forks/yourusername/receipt-generator?style=social)

---

**Made with ❤️ in Ghana** 🇬🇭

*For sales teams who move fast and need reliable tools*
