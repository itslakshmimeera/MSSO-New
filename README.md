# MSSO-New: Film Production Scheduling System

A comprehensive web-based film production scheduling system that leverages advanced optimization algorithms to create efficient shooting schedules while managing actors, locations, and resource constraints.

## 🎬 Overview

MSSO-New is an intelligent film production scheduling platform designed to optimize complex film production workflows. The system analyzes screenplays, extracts scenes and character information, and creates optimal shooting schedules using state-of-the-art optimization algorithms including Ant Colony Optimization, Tabu Search, and Particle Swarm Optimization.

## ✨ Key Features

### 📋 Project Management
- **Multi-user support** with role-based access control
- **Project-based organization** for managing multiple productions
- **User roles**: Director, Production Manager, Scheduling Coordinator
- **Real-time collaboration** and notifications

### 📄 Screenplay Processing
- **PDF screenplay upload** and automatic parsing
- **Scene extraction** with location and character detection
- **Natural Language Processing** for intelligent content analysis
- **Character-scene relationship mapping**

### 🎭 Resource Management
- **Actor availability tracking** with calendar integration
- **Location availability management**
- **Conflict detection** and resolution
- **Resource optimization** for cost-effective scheduling

### 🔧 Advanced Optimization Algorithms
- **Ant Colony Optimization (ACOBM)**: Inspired by ant foraging behavior for finding optimal paths
- **Tabu Search (TSBM)**: Memory-based search to avoid local optima
- **Particle Swarm Optimization (PSOBM)**: Swarm intelligence for balanced optimization

### 📊 Visualization & Analytics
- **Interactive schedule visualization**
- **Cost analysis and estimation**
- **Resource utilization reports**
- **Timeline and Gantt chart views**

## 🛠️ Technology Stack

### Backend
- **Python 3.11+** - Core application language
- **Flask** - Web framework
- **SQLAlchemy** - Database ORM
- **Flask-Login** - User authentication
- **spaCy** - Natural language processing
- **NumPy** - Numerical computations

### Frontend
- **HTML5/CSS3** - Modern web standards
- **Bootstrap 5** - Responsive UI framework
- **JavaScript** - Interactive functionality
- **Font Awesome** - Icons and visual elements

### Database
- **SQLite** (default) - Development database
- **PostgreSQL** - Production database support

### Document Processing
- **ReportLab** - PDF generation
- **PyPDF2** - PDF text extraction

## 🚀 Quick Start

### Prerequisites
- Python 3.11 or higher
- pip or uv package manager

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd MSSO-New
   ```

2. **Install dependencies**
   ```bash
   # Using uv (recommended)
   uv sync
   
   # Or using pip
   pip install -r requirements.txt
   ```

3. **Set up the database**
   ```bash
   python -c "from app import app, db; app.app_context().push(); db.create_all()"
   ```

4. **Run the application**
   ```bash
   python main.py
   ```

5. **Access the application**
   Open your browser to `http://localhost:5000`

### Environment Variables

Create a `.env` file in the project root:

```env
SESSION_SECRET=your-secret-key-here
DATABASE_URL=sqlite:///film_production.db
```

For production, use PostgreSQL:
```env
DATABASE_URL=postgresql://username:password@localhost/film_production
```

## 📖 Usage Guide

### Getting Started

1. **Create an Account**
   - Register with your email and choose your role
   - Roles: Director, Production Manager, or Scheduling Coordinator

2. **Create a Project**
   - Set up a new film production project
   - Add project details and description

3. **Upload Screenplay**
   - Upload your screenplay in PDF format
   - The system will automatically extract scenes, characters, and locations

4. **Manage Resources**
   - Add actors and set their availability
   - Define locations and their availability windows
   - Set up any special constraints

5. **Generate Schedule**
   - Choose your preferred optimization algorithm
   - Set date ranges and parameters
   - Run the optimization engine

6. **Review and Adjust**
   - View the generated schedule
   - Make manual adjustments if needed
   - Export to various formats

### Optimization Algorithms

#### Ant Colony Optimization (ACOBM)
- **Best for**: Complex constraints and location-based scheduling
- **Approach**: Simulates ant colonies finding optimal paths
- **Strengths**: Excellent for minimizing travel between locations

#### Tabu Search (TSBM)
- **Best for**: Avoiding local optima in complex problems
- **Approach**: Uses memory to avoid revisiting recent solutions
- **Strengths**: Good for schedules with many actor/location conflicts

#### Particle Swarm Optimization (PSOBM)
- **Best for**: Balancing multiple optimization goals
- **Approach**: Inspired by bird flocking behavior
- **Strengths**: Balanced approach for various scheduling scenarios

## 🏗️ Project Structure

```
MSSO-New/
├── app.py                          # Flask application setup
├── main.py                         # Application entry point
├── models.py                       # Database models
├── routes.py                       # Web routes and API endpoints
├── forms.py                        # WTForms form definitions
├── utils.py                        # Utility functions
├── nlp_processor.py               # Natural language processing
├── optimization_algorithms.py     # Core optimization algorithms
├── simplified_ant_colony.py      # Simplified ACO implementation
├── json_encoder.py                # Custom JSON encoder
├── static/                        # Static assets (CSS, JS, images)
│   ├── css/
│   └── js/
├── templates/                     # Jinja2 templates
├── uploads/                       # Uploaded files
└── tests/                         # Test files
```

## 🔬 Testing

Run the test suite:

```bash
# Run all tests
python -m pytest

# Run specific test files
python test_screenplay_extraction.py
python test_screenplay_processing.py
```

## 📊 Performance

The optimization algorithms are designed to handle:
- **Scenes**: Up to 100+ scenes per project
- **Actors**: Unlimited actors with complex availability patterns
- **Locations**: Multiple locations with scheduling constraints
- **Processing Time**: Typically 5-30 seconds for optimization

## 🛡️ Security

- **Session management** with secure cookies
- **CSRF protection** on all forms
- **Input validation** and sanitization
- **SQL injection prevention** through ORM
- **File upload security** with type validation

## 🔄 API Documentation

### Core Endpoints

- `GET /` - Home page
- `POST /login` - User authentication
- `POST /register` - User registration
- `GET /projects` - List user projects
- `POST /projects` - Create new project
- `POST /upload_screenplay` - Upload screenplay file
- `POST /optimize` - Run schedule optimization
- `GET /schedule/<id>` - View schedule details

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/new-feature`)
3. Commit your changes (`git commit -m 'Add feature'`)
4. Push to the branch (`git push origin feature/new-feature`)
5. Open a Pull Request

### Development Setup

```bash
# Install development dependencies
uv sync --dev

# Run linting
flake8 .

# Run type checking
mypy .

# Run tests with coverage
pytest --cov=.
```

## � Contributors

We appreciate all the contributors who have helped make this project better:

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore-start -->
<!-- markdownlint-disable -->

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->

<!-- ALL-CONTRIBUTORS-LIST:END -->

### How to Contribute.

We welcome contributions! See our [Contributing Guidelines](#-contributing) section above for details on how to get started.

[![Contributors](https://contrib.rocks/image?repo=owner/MSSO-New)](https://github.com/owner/MSSO-New/graphs/contributors)

*Note: Replace `owner/MSSO-New` with your actual GitHub repository path*


### Performance Improvements
- [ ] Caching layer for faster optimization
- [ ] Parallel processing for large projects
- [ ] Real-time collaboration features
- [ ] Advanced reporting and analytics


---

**Built with ❤️ for the film production community**

*Making film production scheduling intelligent, efficient, and stress-free.*
