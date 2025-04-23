# 📝 Rich Text to Markdown Converter

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=flat&logo=tailwind-css&logoColor=white)
![Markdown](https://img.shields.io/badge/Markdown-000000?style=flat&logo=markdown&logoColor=white)
![DOMPurify](https://img.shields.io/badge/DOMPurify-8B0000?style=flat&logo=javascript&logoColor=white)
![Font Awesome](https://img.shields.io/badge/Font_Awesome-339AF0?style=flat&logo=font-awesome&logoColor=white)

A sleek, modern web application that instantly converts rich text content into clean, well-formatted Markdown. Perfect for developers, writers, and content creators who work with Markdown.

![Rich Text to Markdown Converter](screenshot.png)



## ✨ Features

- 🚀 **Instant Conversion**: Paste rich text content and see the Markdown conversion in real-time
- 👁️ **Live Preview**: See how your Markdown will render instantly
- 🔒 **Secure**: Built-in HTML sanitization using DOMPurify
- 📋 **Easy Copying**: One-click copy to clipboard functionality
- 🎨 **Beautiful UI**: Modern, responsive design using Tailwind CSS
- 🔌 **No Backend Required**: Purely client-side implementation
- 🌟 **GitHub Flavored Markdown**: Supports tables, strikethrough, and more

## 🏗️ Architecture

The application follows a clean, event-driven architecture with clear separation of concerns:

```mermaid
graph TD
    A[User Input/Paste] --> B[Event Handler]
    B --> C[HTML Sanitizer]
    C --> D[Markdown Converter]
    D --> E[Output Display]
    E --> F[Preview Renderer]
    
    style A fill:#f9f,stroke:#333,stroke-width:4px
    style B fill:#bbf,stroke:#333,stroke-width:2px
    style C fill:#dfd,stroke:#333,stroke-width:2px
    style D fill:#dfd,stroke:#333,stroke-width:2px
    style E fill:#fdd,stroke:#333,stroke-width:2px
    style F fill:#fdd,stroke:#333,stroke-width:2px
```

### 🔄 Data Flow

```mermaid
sequenceDiagram
    participant User
    participant PasteHandler
    participant DOMPurify
    participant TurndownService
    participant MarkedJS
    participant UI

    User->>PasteHandler: Paste Content
    PasteHandler->>DOMPurify: Sanitize HTML
    DOMPurify->>TurndownService: Clean HTML
    TurndownService->>UI: Convert to Markdown
    UI->>MarkedJS: Request Preview
    MarkedJS->>UI: Render HTML Preview
```

## 🛠️ Technical Components

### Core Libraries

- **TurndownJS**: Converts HTML to Markdown
- **DOMPurify**: Sanitizes HTML input
- **MarkedJS**: Renders Markdown preview
- **TailwindCSS**: Handles styling
- **Font Awesome**: Provides icons

### Component Structure

```mermaid
classDiagram
    class EventHandler {
        +handlePaste()
        +handleRender()
        +handleCopy()
        +handleClear()
    }
    class TurndownService {
        +turndown(html)
        +use(plugin)
    }
    class DOMPurify {
        +sanitize(html)
    }
    class UIManager {
        +updateButtonStates()
        +showMessage()
        +clearMessage()
    }
    class MarkdownRenderer {
        +render(markdown)
    }

    EventHandler --> TurndownService
    EventHandler --> DOMPurify
    EventHandler --> UIManager
    EventHandler --> MarkdownRenderer
```

## 🚀 Getting Started

1. Clone the repository
2. Open `index.html` in a modern web browser
3. Start pasting rich text content!

No build process or installation required - it just works!

## 🔧 Browser Support

- ✅ Chrome/Edge (Latest)
- ✅ Firefox (Latest)
- ✅ Safari (Latest)
- ✅ Opera (Latest)

## 🔐 Security Features

- HTML sanitization using DOMPurify
- Script tag removal
- Safe attribute filtering
- XSS protection

## 🎯 Use Cases

1. Converting Word documents to Markdown
2. Cleaning up formatted text for GitHub
3. Converting HTML newsletter content
4. Preparing documentation from rich text

## 🤝 Contributing

Feel free to:
- Open issues
- Submit Pull Requests
- Suggest new features
- Report bugs

## 📜 License

MIT License - feel free to use in your own projects!

---

Made with ❤️ for the Markdown community
