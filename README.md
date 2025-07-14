AI Resume & Cover Letter Generator
A full-stack web application that uses AI (LLMs) to generate professional resumes and cover letters based on user inputs like name, education, experience, skills, career goals, and more.
________________________________________
📌 Project Overview
This AI Resume Generator takes user-provided data and generates:
•	A professional resume
•	A personalized cover letter
These are powered by a large language model (LLM) via Groq API. The user receives well-formatted results that can be downloaded as PDF files. No login or signup required.
________________________________________
⚙️ Tech Stack
Frontend:
•	React.js (Vite)
•	Tailwind CSS
•	jsPDF (for PDF downloads)
Backend:
•	Node.js + Express
•	Groq API for LLM response
•	dotenv for environment management
Deployment:
•	Frontend: Vercel
•	Backend: Render
•	GitHub: Source Control
________________________________________
🏗 Folder Structure
resume-ai-app/
├── client/         # React frontend (Vite)
│   ├── src/components/Form.jsx
│   ├── src/components/Output.jsx
├── server/         # Express backend
│   └── index.js
├── .gitignore
├── README.md
└── .env            # not committed (for GROQ_API_KEY)
________________________________________
🛠 How to Set Up Locally
Step 1: Clone the Repo
git clone https://github.com/your-username/ai-resume-generator.git
cd resume-ai-app
Step 2: Backend Setup
cd server
npm install
Create server/.env with your API key:
GROQ_API_KEY=your_groq_key_here
Start backend server:
npm start
Step 3: Frontend Setup
cd ../client
npm install
Create client/.env with your deployed backend URL:
VITE_API_URL=https://your-backend-host/api/generate
Start frontend dev server:
npm run dev
Open in browser: http://localhost:5173
________________________________________
🔑 Environment Variables
In server/.env:
GROQ_API_KEY=your_groq_key_here
In client/.env:
VITE_API_URL=http://localhost:5000/api/generate
________________________________________
🧠 Architecture Overview
1.	User fills form in React UI
2.	On button click, frontend sends POST request to Express backend
3.	Backend constructs prompt and sends it to Groq’s LLM
4.	Groq returns resume/cover letter
5.	Frontend displays formatted response and enables PDF download
________________________________________
✨ Key Features
•	AI-generated professional resume & cover letter
•	Formatted output in browser
•	PDF download support
•	Dynamic prompt based on provided fields
•	Mobile-responsive design
•	Simple & intuitive interface
•	LLM backend can be swapped (Groq/OpenAI/OpenRouter)
________________________________________
✅ Pros
•	No authentication required
•	Works with free Groq API key
•	Easy to customize and extend
•	Quick deployment (Vercel + Render)
⚠️ Cons
•	LLM responses may vary in formatting
•	No rich text editing yet
•	Rate limits depend on API provider
________________________________________
📸 Screenshots
(add images to README)
________________________________________
📤 Deployment
Frontend:
•	Hosted on Vercel: https://your-vercel-app.vercel.app
Backend:
•	Hosted on Render: https://your-render-app.onrender.com
