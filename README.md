# CAD Viewer Application

A basic web-based CAD viewer that can import, display, and manipulate simple 3D models (e.g., STL or OBJ files). This full-stack project was developed as a technical assignment for a Full-Stack Engineering Intern role at insyde.io.

## Features

- **File Upload:**  
  - Upload STL or OBJ files using a simple React-based UI.
  
- **3D Model Viewing:**  
  - Render 3D models in the browser using Three.js.
  - Use OrbitControls for rotating, zooming, and panning the model.
  
- **Model Conversion:**  
  - Convert models between STL and OBJ formats (both STL → OBJ and OBJ → STL).
  - Download the converted file directly from the interface.
  
- **User-Friendly Interface:**  
  - Clean design with clear instructions.
  - Responsive viewer area with a frame and helpful notes.

- **Backend API:**  
  - Built with Flask to handle file upload, retrieval, and conversion.
  - Endpoints include `/upload`, `/model/<filename>`, and `/convert`.
  - Use CAD Viewer.postman_collection file and import it in Postman tool ( Home -> Workspaces -> select your workspace -> import option [top-left] -> select this file and upload )
- **Instruction to use Postman for testing backend API:**
    - /upload (POST method)
        - Go to Body section and set key value as **model** and type as **file**
        - Upload the .obj or .stl file as value
    - /convert (GET method) [format represents the target file extension]
        - GO to Params section and set below keys-values
        - For key **filename** , value is **fileName**
        - For key **format**, value is **stl** or **obj**
    - /model/filename (GET method)
      - Enter filename after /model like /model/Cottage_FREE.stl        

## Demo Picture

Watch the demo picture explaining the approach and key features of this project:
![WhatsApp Image 2025-03-12 at 01 23 05_4fc704b6](https://github.com/user-attachments/assets/c1de77c8-3295-4683-994a-57ff9b32019f)


## Local Setup Instructions

### Prerequisites

Make sure you have installed:
- **Python 3.x**
- **Node.js and npm**
- **Git (Optional)**

## 🛠️ Tech Stack

| Component    | Technology |
|-------------|------------|
| **Frontend** | React, Three.js, OrbitControls |
| **Backend**  | Django, Django REST Framework |
| **Database** | SQLite |

### Open command prompt and perform below steps
### Backend Setup (Flask API)
1. **Clone the repository and navigate to folder:**
   ```cmd
   git clone https://github.com/Anilpurrum2011/3D-CAD-Viewer
   ```
   ```cmd
   cd CAD-Viewer/cad-backend
   ```

2. **Set up a virtual environment:**
   ```
     python -m venv venv
   ```
3. **Activate the virtual environment:** 
      ```
      Windows : venv\Scripts\activate
      ```
      ```
      macOS/Linux : source venv/bin/activate
      ```
4. **Install required packages:**
    ```
       pip install -r requirements.txt
    ```
5. **Run the Flask server:**
     ```
       python app.py
     ```
   
### Frontend Setup (React Application)
1. **Navigate to the React project folder:**
   ```
     cd ../cad-frontend
   ```
2. **Install dependencies:**
     ```
       npm install
     ```
3. **Start the React application:** (Install nodemon if you are using nodemon or just use npm instead of nodemon)
   ```
     nodemon start
   ``` 
   ```
     npm start
   ```

### Project Structure
    #3D CAD-Viewer-WebApp/
    ├── cad-backend/
    │   ├── app.py
    │   ├── requirements.txt
    │   └── uploads/
    └── cad-frontend/
        ├── public/
        ├── src/
        │   ├── App.js
        │   ├── App.test.js
        │   ├── App.css
        │   ├── index.js
        │   ├── index.css
        │   ├── CADViewer.js
        │   ├── FileUpload.js
        │   └── ConvertDownload.js
        ├── package-lock.json
        └── package.json


