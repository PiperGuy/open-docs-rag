# OpenDocs RAG Widget

A beautiful, configurable AI-powered documentation widget that brings intelligent assistance to your website. Now with enhanced styling, Roboto font, and flexible question configuration.

## ✨ New Features

- **Config-driven questions**: Support for both legacy string format and new structured JSON format
- **Beautiful Roboto font**: Modern typography throughout the interface
- **Enhanced animations**: Smooth transitions and micro-interactions
- **Improved styling**: Gradient backgrounds, better shadows, and modern design
- **Better accessibility**: Focus states and keyboard navigation
- **Mobile responsive**: Optimized for all screen sizes

## 🚀 Quick Start

### Script Tag Usage

Include the widget with a simple script tag and configure it with data attributes:

```html
<script 
    src="widget.js" 
    data-website-id="your-website-id"
    data-project-name="Your Project"
    data-project-color="#007bff"
    data-project-logo="/logo.svg"
    data-modal-example-questions="What is this project about?, How do I get started?, What are the main features?"
></script>
```

### NPM Package Usage

```bash
npm install open-docs-rag-widget
```

```javascript
import { createWidget } from 'open-docs-rag-widget';

const widget = createWidget({
  websiteId: 'your-website-id',
  projectName: 'Your Project',
  projectColor: '#007bff',
  projectLogo: '/logo.svg',
  modalExampleQuestions: 'How to get started?, How to deploy?',
  apiEndpoint: '/api/chat'
});

widget.open();
```

## 📝 Configuration Options

### Required Parameters

- `websiteId`: Unique identifier for your website
- `projectName`: Name of your project
- `projectColor`: Primary color for the widget (hex code)
- `projectLogo`: URL to your project logo

### Example Questions Configuration

The widget now supports two formats for example questions:

#### 1. Legacy String Format (Backward Compatible)

```html
<script 
    data-modal-example-questions="What is this project about?, How do I get started?, What are the main features?"
></script>
```

#### 2. New Structured JSON Format

```html
<script 
    data-modal-example-questions='[
        {"text": "What is this project about?", "category": "general"},
        {"text": "How do I get started?", "category": "getting-started"},
        {"text": "What are the main features?", "category": "features"},
        {"text": "How do I configure the widget?", "category": "configuration"}
    ]'
></script>
```

The structured format allows for:
- **Categories**: Group questions by topic or purpose
- **Icons**: Add visual indicators to questions (coming soon)
- **Extensibility**: Easy to add more properties in the future

### Advanced Configuration Example

```html
<script 
    src="widget.js" 
    data-website-id="demo-site"
    data-project-name="Advanced Demo"
    data-project-color="#6366f1"
    data-project-logo="https://via.placeholder.com/32x32/6366f1/ffffff?text=A"
    data-modal-title="AI Assistant Pro"
    data-modal-example-questions-title="💡 Try asking:"
    data-modal-ask-ai-input-placeholder="Ask me anything about this project..."
    data-font-family="Roboto, sans-serif"
    data-modal-title-font-size="24px"
    data-example-question-button-font-size="15px"
    data-example-question-button-padding-x="20px"
    data-example-question-button-padding-y="12px"
    data-modal-example-questions='[
        {"text": "🚀 How do I deploy this project?", "category": "deployment"},
        {"text": "⚙️ What are the configuration options?", "category": "config"},
        {"text": "📚 Where can I find documentation?", "category": "docs"},
        {"text": "🛠️ How do I customize the widget?", "category": "customization"}
    ]'
></script>
```

## 🎨 Styling Features

### Typography
- **Roboto font**: Modern, clean typography throughout
- **Responsive font sizes**: Automatically adjusts for different screen sizes
- **Custom font support**: Override with your preferred font family

### Visual Enhancements
- **Gradient backgrounds**: Subtle gradients for depth and modern appeal
- **Improved shadows**: Better depth perception and visual hierarchy
- **Smooth animations**: Micro-interactions and transitions
- **Enhanced hover effects**: Interactive feedback for better UX

### Accessibility
- **Focus states**: Clear visual indicators for keyboard navigation
- **High contrast**: Readable text and sufficient color contrast
- **Screen reader support**: Proper ARIA labels and semantic HTML

## 📱 Mobile Responsiveness

The widget is fully responsive and optimized for:
- Desktop computers
- Tablets
- Mobile phones
- Touch interfaces

## 🔧 API Integration

The widget communicates with your backend API to provide intelligent responses. Configure the API endpoint:

```html
<script 
    data-api-endpoint="https://your-api.com/chat"
    data-api-key="your-api-key"
></script>
```

## 🛠️ Development

### Building the Widget

```bash
# Install dependencies
npm install

# Build for production
npm run build

# Build for development
npm run dev
```

### Project Structure

```
widget/
├── src/
│   ├── widget.ts          # Main widget implementation
│   ├── config.ts          # Configuration parsing
│   ├── types.ts           # TypeScript type definitions
│   ├── styles.css         # Widget styling
│   ├── example.html       # Example usage
│   └── index.ts           # Entry point
├── package.json
├── tsconfig.json
└── README.md
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## 📄 License

MIT License - see LICENSE file for details.

## 🆘 Support

For support and questions:
- Create an issue on GitHub
- Check the documentation
- Review the example files

---

**Made with ❤️ for better documentation experiences**
