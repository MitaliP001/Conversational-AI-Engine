# Conversational-AI-Engine

A lightweight, customizable chatbot framework powered by Large Language Models (LLMs).  
This project provides a responsive web chat interface with dynamic FAQs, related questions, and smooth user interactions. It is designed for easy integration with any web platform or CMS via REST API endpoints.

---

## Features

- Interactive chat interface with loading animations  
- Dynamic Frequently Asked Questions (FAQs) and related questions sections  
- Asynchronous fetch requests to configurable AI API endpoints  
- User message and AI response caching for performance  
- Expandable resource accordion for additional user help  
- Contact and support links integrated into the UI  
- Easily customizable UI and backend endpoints  

---

## Architecture Overview

The chatbot frontend is built using plain JavaScript, HTML, and CSS for broad compatibility and ease of customization. It communicates with a backend AI service using REST API calls. This backend service hosts a large language model (LLM) : such as GPT or a similar transformer-based model  which generates human-like conversational responses based on the user input.

---

## How It Works

1. **User Input:** The user types a question or message in the chat input field.  
2. **Frontend Handling:** JavaScript captures the input, displays the user's message in the chat area, and shows a loading animation.  
3. **API Call:** The frontend sends a POST request with the user query and some metadata (e.g., IP address, location) to the LLM API endpoint.  
4. **LLM Processing:** The backend LLM processes the query, using natural language understanding to generate a relevant response.  
5. **Response Rendering:** The API returns a JSON response with the AI’s reply, which the frontend displays dynamically in the chat window.  
6. **Caching:** Frequently asked questions and answers are cached client-side to reduce redundant API calls and improve responsiveness.  

---

## Tech Stack

- **Frontend:**  
  - HTML5 and CSS3 for layout and styling  
  - Vanilla JavaScript for DOM manipulation, event handling, and AJAX fetch calls  
- **Backend:**  
  - REST API serving LLM-powered responses (replaceable with any AI backend supporting JSON requests)  
- **Integration:**  
  - Easily embeddable via shortcode or script in WordPress or other web frameworks  
- **Optional:**  
  - PHP for WordPress shortcode and asset enqueueing (if used within WordPress)  

---

## Setup & Usage

1. Clone or download this repository.  
2. Replace the placeholder API endpoint URL in the JavaScript (`fetch` call) with your own LLM API URL.  
3. Customize FAQ and related question lists by modifying the HTML structure in the chatbot container.  
4. Deploy your LLM API backend separately or use a hosted AI service that supports JSON-based chat requests.  

---

## Example API Request Payload

```json
{
  "ip_address": "192.168.10.88",
  "location": "Ahmedabad",
  "query": "What is the weather today?"
}
