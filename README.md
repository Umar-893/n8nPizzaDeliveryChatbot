# n8nPizzaDeliveryChatbot
A chatbot developed in n8n to be shared.
🍕 AI-Powered Pizza Delivery Chatbot (n8n Workflow)
Order Management | Menu API | Real-Time Order Status | WhatsApp/Chat Integration

This repository contains a complete n8n workflow for building an AI-powered pizza delivery chatbot that can:

✅ Take pizza orders
✅ Fetch menu dynamically
✅ Create orders
✅ Track order status
✅ Collect customer information
✅ Integrate with WhatsApp or website chat
✅ Fully automated using AI + JavaScript tools

Perfect for restaurants who want an intelligent chatbot without coding.

🚀 Features
🤖 AI Chatbot Agent

Powered by OpenAI GPT-4.1-mini

Understands natural language (e.g., "I want a large pepperoni pizza")

Extracts structured data (pizza type, quantity, name, address, phone)

Calls internal tools for:

Menu fetching

Order creation

Order status checking

📦 Order Management System

Includes:

Order API webhook (takes new orders)

Order status logic (pending, confirmed, out for delivery, delivered)

Javascript node to maintain order records

Response node to return order confirmation JSON

🧾 Dynamic Menu API

Menu Webhook that exposes pizza menu

Works as a real API

Chatbot gets menu from this API instead of hardcoding it

📱 Connect to WhatsApp or any chat

You can use:

Meta WhatsApp (recommended)

Twilio WhatsApp

n8n Chat Trigger (built-in)

Website chat widgets

📂 Workflow Overview
Chat Trigger → Pizza Chatbot Agent → Tools:
   → Get Menu Tool
   → Create Order Tool
   → Check Order Status Tool
Conversation Memory
Menu API Webhook → Menu Data → Return Menu
Order API Webhook → Order Management Logic → Return Order Response

🧠 Tool Details
🔧 Create Order Tool

JavaScript function that:

Validates required fields

Generates unique order ID

Sends order data to the Order API Webhook

Returns confirmation JSON

🔧 Get Menu Tool

Calls internal Menu API Webhook

Returns structured pizza menu

🔧 Check Order Status Tool

Looks up order status based on orderId

Returns current status

🕵️‍♂️ How It Works (Flow)

User sends a message:
"I want 1 medium pepperoni pizza"

AI agent extracts:

pizzaType

quantity

customerName

customerAddress

customerPhone

Agent calls Create Order Tool

Order is stored via Order Management Logic

Chatbot replies with:

Your order ORD-12345 is confirmed!


User asks:
"Where is my order?"

Agent calls Check Order Status Tool

Response:

Your order ORD-12345 is now Out for Delivery 🚗💨

📥 Installation Instructions
1️⃣ Download/Copy Workflow JSON

Export from your n8n workflow or use repo file.

2️⃣ Import into n8n

Go to:

n8n → Workflows → Import from File

3️⃣ Add API Key

Set:

OpenAI API key

Webhook URLs

4️⃣ Connect to WhatsApp (Optional)

Use:

Meta Business Suite, OR

Twilio WhatsApp

5️⃣ Run the Workflow

Click Execute Workflow or Open Chat.

⚙️ Customization
Change Pizza Menu

Modify inside Menu Data node.

Add More Pizzas

Just edit the menu JSON:

{
  "name": "BBQ Chicken Pizza",
  "price": 12.99
}

Add Delivery Fee / Tax

Modify Order Management Logic.

🧪 Testing Order Creation

Inside Create Order Tool → Test Tool:

Paste this sample input:

{
  "pizzaType": "Medium Pepperoni Pizza",
  "quantity": 1,
  "customerName": "Umar",
  "customerAddress": "Street 34, Jhang",
  "customerPhone": "342187903"
}

🎯 Ideal For

Restaurants

Cloud kitchens

Food delivery startups

Agencies offering AI automation

n8n developers

📞 Support

If you need:

Custom WhatsApp chatbot

Restaurant automation

AI agent development

n8n workflows

Just open an issue or contact the developer.
