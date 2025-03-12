# 🏗️ CAD Viewer Application

A web-based CAD viewer that allows users to upload, view, manipulate, and convert 3D models (STL and OBJ files). This full-stack project was developed as part of a technical assignment for a Full-Stack Engineering Intern role.

---

## 🚀 Features

- **📂 File Upload:** Upload STL or OBJ files via a React-based UI.
- **🖥️ 3D Model Rendering:** Render models using Three.js with OrbitControls for rotation, zoom, and pan.
- **🔄 Model Conversion:** Convert STL to OBJ and vice versa with direct file download.
- **🛠️ Backend API:** Django backend for file handling and conversion.
- **🎯 User-Friendly Interface:** Clean and intuitive UI for a smooth experience.

---

## 🛠️ Tech Stack

| Component    | Technology |
|-------------|------------|
| **Frontend** | React, Three.js, OrbitControls |
| **Backend**  | Django, Django REST Framework |
| **Database** | SQLite |
| **Deployment** | Docker (Optional) |

---

## 📌 API Endpoints

| Method | Endpoint           | Description                              |
|--------|-------------------|------------------------------------------|
| `POST` | `/upload`         | Uploads a 3D model file                 |
| `GET`  | `/model/<filename>` | Retrieves the uploaded model            |
| `GET`  | `/convert?filename=<>&format=<stl/obj>` | Converts between formats |

---

## 🎬 Demo Video

[![Watch Demo](https://img.youtube.com/vi/your_video_id/0.jpg)](https://drive.google.com/file/d/your_google_drive_video_link/view)

---

## ⚙️ Installation & Setup

### 1️⃣ Clone Repository
```sh
git clone https://github.com/your-repo/cad-viewer.git
cd cad-viewer
