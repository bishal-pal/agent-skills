---
name: react-rag
description: Design and generate modular, accessible React.js components for Retrieval-Augmented Generation workflows and complex data visualization.
---

## react-rag

This skill is designed to assist software engineers and UI developers in creating modular and accessible React.js components that cater to Retrieval-Augmented Generation (RAG) workflows. It is particularly useful when generating front-end code for applications such as chatbots, document retrieval systems, or translating complex system architecture diagrams into functional UI components.

### Workflow Steps

1. **Identify Requirements**: Define the specific needs for the user interface components based on the RAG workflow.
2. **Select Component Type**: Choose the type of React component needed (e.g., functional, class-based, or hooks).
3. **Generate Component Code**: Create the JSX/TSX code for the component, ensuring it meets modern usability standards.
4. **Implement State Management**: Detail the state management strategies (e.g., useState, useContext) to manage data flow.
5. **Accessibility Considerations**: Ensure all components adhere to accessibility best practices (e.g., ARIA roles, keyboard navigation).
6. **Testing and Integration**: Provide guidance on how to integrate the generated components into existing React applications, including testing strategies.

### Output Format

The output will be structured as Markdown containing code blocks with React (JSX/TSX) code, followed by bullet points that explain state management and usability considerations. 

Example output format:

```jsx
// ExampleComponent.jsx
import React from 'react';

const ExampleComponent = () => {
    // State management logic
    const [data, setData] = useState([]);

    return (
        <div>
            {/* Render data visualization */}
        </div>
    );
};

export default ExampleComponent;
```

- Ensure the use of `useState` for managing local state.
- Implement error boundaries for error handling.
- Use semantic HTML elements for better accessibility.

### Examples

**Example 1:**  
**Input:** Create a chatbot UI component.  
**Output:**
```jsx
// ChatbotUI.jsx
import React, { useState } from 'react';

const ChatbotUI = () => {
    const [messages, setMessages] = useState([]);

    const sendMessage = (msg) => {
        // Logic to send message
    };

    return (
        <div>
            <div className="chat-window">
                {messages.map((msg, index) => <div key={index}>{msg}</div>)}
            </div>
            <input type="text" onKeyPress={(e) => e.key === 'Enter' && sendMessage(e.target.value)} />
        </div>
    );
};

export default ChatbotUI;
```
- Utilizes local state to manage messages.
- Input field listens for the Enter key to send messages.

**Example 2:**  
**Input:** Generate a document retrieval system interface.  
**Output:**
```jsx
// DocumentRetrieval.jsx
import React, { useState } from 'react';

const DocumentRetrieval = () => {
    const [documents, setDocuments] = useState([]);

    const fetchDocuments = () => {
        // Fetch logic here
    };

    return (
        <div>
            <button onClick={fetchDocuments}>Retrieve Documents</button>
            <ul>
                {documents.map((doc, index) => <li key={index}>{doc.title}</li>)}
            </ul>
        </div>
    );
};

export default DocumentRetrieval;
```
- Implements a button for document retrieval.
- Displays a list of titles fetched from a data source.

### Anti-Patterns

- Avoid hardcoding values within components; utilize props and state management.
- Do not ignore accessibility considerations; ensure all components are usable by people with disabilities.
- Refrain from using class components unless necessary; prefer functional components with hooks for state management.

### Scope

The skill aims to support software engineers and UI developers in building AI-integrated applications by generating high-quality React components that are easy to use, integrate, and adapt. Future enhancements may include:
- Support for additional libraries (e.g., Redux, MobX) for state management.
- Advanced examples for complex data visualizations.
- Integration with design systems and component libraries for consistent UI design.