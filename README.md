# Comiccraft-AI-Comic-Story-Creator-Using-Gemini-ModelsComicCraft - AI Comic Story Creator using Gemini Models
Project Description
ComicCraft is a web-based application that uses AI to generate personalized comic book stories and illustrations from user-provided prompts.
The application uses Google Gemini models for story generation and Stable Diffusion for comic-style image generation. It provides an interactive web interface where users can enter a story prompt, character name, setting, story tone, and art style.
ComicCraft generates a panel-by-panel storyline with narration, character dialogues, and illustrations. Users can preview the generated comic and export it as a downloadable PDF.
Features
Generate a structured 5-panel comic outline.
Generate comic narration and character dialogues.
Generate comic-style illustrations using Stable Diffusion.
Customize the main character, setting, tone, and art style.
Preview the generated comic panel-by-panel.
Export the complete comic as a PDF.
Provides browser-based frontend and FastAPI backend.
Supports API-based comic generation.
Technologies Used
Python
FastAPI
Uvicorn
HTML
CSS
Jinja2
Google Gemini Flash
Google Gemini Pro
Hugging Face Diffusers
Stable Diffusion
PyTorch
FPDF
Pillow
AI Models
Gemini Flash
Used for fast and structured generation of the 5-panel comic outline.
Gemini Pro
Used for detailed comic narration and character dialogues.
Stable Diffusion
Used to generate comic-style illustrations from image prompts.
Project Architecture
ComicCraft consists of three main components:
Frontend - HTML, CSS, and Jinja2 templates for collecting user input and displaying the generated comic.
Backend - FastAPI for routing, processing user input, coordinating AI generation, and exporting the comic.
AI Integration - Google Gemini APIs and Hugging Face Diffusers for text and image generation.
User Inputs
The application accepts:
Story Prompt
Main Character Name
Setting
Story Tone
Art Style
Project Workflow
User enters the comic story details.
Gemini Flash generates a structured 5-panel outline.
Gemini Pro generates narration and character dialogues.
Stable Diffusion generates illustrations for each panel.
The generated images and story are organized into a comic layout.
The comic is exported as a PDF.
The user can preview and download the completed comic.
Project Structure
A project structure based on the application workflow includes:
ComicCraft/
├── app/
│   └── main.py
├── templates/
│   ├── index.html
│   ├── comic_preview.html
│   └── export_success.html
├── static/
│   ├── panels/
│   └── exports/
├── gemini_flash.py
├── gemini_pro.py
├── image_generator.py
├── layout_builder.py
├── exporters.py
├── routes.py
├── requirements.txt
└── README.md
Main Functions
generate_outline()
File: gemini_flash.py
Generates a structured 5-panel comic outline containing panel information, scene descriptions, and image-generation prompts.
generate_story()
File: gemini_pro.py
Expands the panel outline into a complete comic story with narration and character dialogue.
generate_image()
File: image_generator.py
Generates comic-style illustrations using Stable Diffusion and saves the images in the static/panels directory.
build_comic_layout()
File: layout_builder.py
Combines the generated images and story content into a structured comic layout.
save_pdf()
File: exporters.py
Creates a multi-page PDF containing the comic images and narration and saves it in the static/exports directory.
Installation
1. Install Python and pip
Make sure Python and pip are installed on the system.
2. Create a Virtual Environment
python -m venv comiccraft-env
For Windows:
comiccraft-env\Scripts\activate
3. Install Dependencies
pip install fastapi uvicorn jinja2 python-multipart google-generativeai diffusers transformers fpdf Pillow accelerate
Or, if a requirements.txt file is available:
pip install -r requirements.txt
Environment Variables
The application requires API credentials for the AI services.
Example:
GEMINI_API_KEY=your_gemini_api_key_here
HF_API_KEY=your-huggingface-api-key-here
Keep API keys private and do not commit them to a public repository.
Running the Application
From the project root, start the FastAPI server:
uvicorn app.main:app --reload
Open the application in a browser:
http://127.0.0.1:8000
FastAPI API documentation is available at:
http://127.0.0.1:8000/docs
API Routes
/
Loads the ComicCraft homepage.
/generate
Accepts form input, generates the comic, and displays the comic preview.
/generate-comic/json
Accepts JSON input and returns comic layout information and the generated PDF path.
/test-image
Tests image generation using a custom prompt.
/export-success
Displays the successful comic export confirmation page.
Frontend Pages
index.html
Collects the story prompt, character name, setting, tone, and art style.
comic_preview.html
Displays the generated comic panels, images, descriptions, captions, and narration.
export_success.html
Displays a confirmation message after the comic is exported.
PDF Export
The generated comic can be downloaded as a PDF. The PDF contains the comic panel images, panel titles, scene descriptions, captions, and narration.
Example
A user can enter a prompt such as:
A brave fox exploring an enchanted forest.
The application processes the prompt and generates a personalized comic with multiple panels, narration, dialogue, and illustrations.
Conclusion
ComicCraft demonstrates how generative AI can be used to create personalized comic stories and illustrations. By combining Gemini models for storytelling with Stable Diffusion for image generation, the application provides an end-to-end workflow from a simple story prompt to a downloadable comic PDF.ComicCraft - AI Comic Story Creator using Gemini Models
Project Description
ComicCraft is a web-based application that uses AI to generate personalized comic book stories and illustrations from user-provided prompts.
The application uses Google Gemini models for story generation and Stable Diffusion for comic-style image generation. It provides an interactive web interface where users can enter a story prompt, character name, setting, story tone, and art style.
ComicCraft generates a panel-by-panel storyline with narration, character dialogues, and illustrations. Users can preview the generated comic and export it as a downloadable PDF.
Features
Generate a structured 5-panel comic outline.
Generate comic narration and character dialogues.
Generate comic-style illustrations using Stable Diffusion.
Customize the main character, setting, tone, and art style.
Preview the generated comic panel-by-panel.
Export the complete comic as a PDF.
Provides browser-based frontend and FastAPI backend.
Supports API-based comic generation.
Technologies Used
Python
FastAPI
Uvicorn
HTML
CSS
Jinja2
Google Gemini Flash
Google Gemini Pro
Hugging Face Diffusers
Stable Diffusion
PyTorch
FPDF
Pillow
AI Models
Gemini Flash
Used for fast and structured generation of the 5-panel comic outline.
Gemini Pro
Used for detailed comic narration and character dialogues.
Stable Diffusion
Used to generate comic-style illustrations from image prompts.
Project Architecture
ComicCraft consists of three main components:
Frontend - HTML, CSS, and Jinja2 templates for collecting user input and displaying the generated comic.
Backend - FastAPI for routing, processing user input, coordinating AI generation, and exporting the comic.
AI Integration - Google Gemini APIs and Hugging Face Diffusers for text and image generation.
User Inputs
The application accepts:
Story Prompt
Main Character Name
Setting
Story Tone
Art Style
Project Workflow
User enters the comic story details.
Gemini Flash generates a structured 5-panel outline.
Gemini Pro generates narration and character dialogues.
Stable Diffusion generates illustrations for each panel.
The generated images and story are organized into a comic layout.
The comic is exported as a PDF.
The user can preview and download the completed comic.
Project Structure
A project structure based on the application workflow includes:
ComicCraft/
├── app/
│   └── main.py
├── templates/
│   ├── index.html
│   ├── comic_preview.html
│   └── export_success.html
├── static/
│   ├── panels/
│   └── exports/
├── gemini_flash.py
├── gemini_pro.py
├── image_generator.py
├── layout_builder.py
├── exporters.py
├── routes.py
├── requirements.txt
└── README.md
Main Functions
generate_outline()
File: gemini_flash.py
Generates a structured 5-panel comic outline containing panel information, scene descriptions, and image-generation prompts.
generate_story()
File: gemini_pro.py
Expands the panel outline into a complete comic story with narration and character dialogue.
generate_image()
File: image_generator.py
Generates comic-style illustrations using Stable Diffusion and saves the images in the static/panels directory.
build_comic_layout()
File: layout_builder.py
Combines the generated images and story content into a structured comic layout.
save_pdf()
File: exporters.py
Creates a multi-page PDF containing the comic images and narration and saves it in the static/exports directory.
Installation
1. Install Python and pip
Make sure Python and pip are installed on the system.
2. Create a Virtual Environment
python -m venv comiccraft-env
For Windows:
comiccraft-env\Scripts\activate
3. Install Dependencies
pip install fastapi uvicorn jinja2 python-multipart google-generativeai diffusers transformers fpdf Pillow accelerate
Or, if a requirements.txt file is available:
pip install -r requirements.txt
Environment Variables
The application requires API credentials for the AI services.
Example:
GEMINI_API_KEY=your_gemini_api_key_here
HF_API_KEY=your-huggingface-api-key-here
Keep API keys private and do not commit them to a public repository.
Running the Application
From the project root, start the FastAPI server:
uvicorn app.main:app --reload
Open the application in a browser:
http://127.0.0.1:8000
FastAPI API documentation is available at:
http://127.0.0.1:8000/docs
API Routes
/
Loads the ComicCraft homepage.
/generate
Accepts form input, generates the comic, and displays the comic preview.
/generate-comic/json
Accepts JSON input and returns comic layout information and the generated PDF path.
/test-image
Tests image generation using a custom prompt.
/export-success
Displays the successful comic export confirmation page.
Frontend Pages
index.html
Collects the story prompt, character name, setting, tone, and art style.
comic_preview.html
Displays the generated comic panels, images, descriptions, captions, and narration.
export_success.html
Displays a confirmation message after the comic is exported.
PDF Export
The generated comic can be downloaded as a PDF. The PDF contains the comic panel images, panel titles, scene descriptions, captions, and narration.
Example
A user can enter a prompt such as:
A brave fox exploring an enchanted forest.
The application processes the prompt and generates a personalized comic with multiple panels, narration, dialogue, and illustrations.
Conclusion
ComicCraft demonstrates how generative AI can be used to create personalized comic stories and illustrations. By combining Gemini models for storytelling with Stable Diffusion for image generation, the application provides an end-to-end workflow from a simple story prompt to a downloadable comic PDF.
