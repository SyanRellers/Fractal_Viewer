# Interactive Fractal Explorer

An interactive web application that generates high-resolution, colorful fractals that you can explore by clicking to zoom in.

## Features
- Real-time fractal generation with progressive loading
- Click-to-zoom interaction for fractal exploration
- Colorful visualization using matplotlib colormaps
- Responsive design that fills the browser window

## Prerequisites
- Python 3.7 or higher
- pip (Python package installer)

## Installation

1. **Check Python Installation:**
```bash
# Verify Python version
python --version  # Should be 3.7 or higher

# If python command not found, try:
python3 --version
```

2. **Clone the repository:**
```bash
git clone git@github.com:SyanRellers/fractal-app.git
cd fractal-app
```

3. **Set up a virtual environment (recommended):**
```bash
# Create virtual environment
python -m venv venv

# Activate virtual environment
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate
```

4. **Install required packages:**
```bash
# Install all dependencies
pip install fastapi uvicorn jinja2 numpy pillow matplotlib numba

# Verify installations
pip list | grep -E "fastapi|uvicorn|jinja2|numpy|pillow|matplotlib|numba"
```

If you encounter any permission errors, try:
```bash
pip install --user fastapi uvicorn jinja2 numpy pillow matplotlib numba
```

## Running the Application

1. Start the server:
```bash
uvicorn app:app --reload
```

2. Open your web browser and navigate to:
```bash
http://localhost:8000/view
```

## Usage
- Click anywhere on the fractal to zoom in at that point
- The application uses progressive loading: first a quick low-resolution preview, then a high-quality render
- The fractal automatically resizes to fill your browser window

## Project Structure
```
fractal-app/
├── app.py              # Main application with FastAPI routes and fractal generation
└── templates/
    └── index.html      # Frontend interface with zoom controls
```

## Technical Stack
- FastAPI: Web framework
- Numba: JIT compilation for faster fractal computation
- Matplotlib: Color mapping
- Pillow: Image processing
- NumPy: Numerical computations
