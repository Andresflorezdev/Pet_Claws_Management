# 🐾 Pet Claws Management - Garras

Pet store management system developed with Django and MySQL.

## 📋 Description

**Garras** is a web application for comprehensive management of a pet store.  It allows managing users, staff, and roles within the organization, with different profile types such as veterinarians, assistants, receptionists, and administrators. 

## ✨ Features

- 🔐 **User authentication system**
- 👥 **People management** (full CRUD)
- 💼 **Job position/user type management**:  
  - Veterinarian
  - Veterinary assistant
  - Receptionist
  - Administrator
  - Veterinary surgeon
  - Wildlife specialist
  - Zootechnician
- 👤 **User management** with role assignment
- 🎨 Modern and responsive interface with custom CSS
- 📊 Dashboard with company mission and vision

## 🛠️ Technologies

- **Backend**: Django 5.2.5
- **Database**: MySQL
- **Frontend**: HTML5, CSS3 (with effects and animations)
- **Python**: 3.x

## 📦 Dependencies

```txt
Django==5.2.5
mysqlclient==2.2.7
asgiref==3.9.1
sqlparse==0.5.3
tzdata==2025.2
```

## 🚀 Installation

### 1. Clone the repository

```bash
git clone https://github.com/Andresflorezdev/Pet_Claws_Management.git
cd Pet_Claws_Management
```

### 2. Create and activate virtual environment

```bash
python -m venv env
```

**Windows:**
```bash
.\env\Scripts\activate
```

**Linux/Mac:**
```bash
source env/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure database

Create the MySQL database by executing the `estructura_mysql.sql` file:

```bash
mysql -u root -p < estructura_mysql. sql
```

Or from MySQL:  
```sql
source estructura_mysql.sql;
```

This script will create:  
- Database `garras`
- Tables: `tipo`, `persona`, `usuario`
- Test data (7 sample users)

### 5. Configure database connection

Edit `mascota/mascota/settings.py` with your MySQL credentials:

```python
DATABASES = {
    'default':  {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'garras',
        'USER': 'your_username',
        'PASSWORD':  'your_password',
        'HOST': 'localhost',
        'PORT': '3306'
    }
}
```

### 6. Run migrations (optional)

```bash
cd mascota
python manage.py migrate
```

### 7. Run development server

```bash
python manage.py runserver
```

Access:  `http://127.0.0.1:8000/`

## 👤 Test Users

The system comes with 7 sample users:

| Username | Password | Role |
|---------|-----------|-------|
| sofia_vet | vet123 | Veterinarian |
| marco_aux | aux234 | Veterinary assistant |
| lucia_recep | recep345 | Receptionist |
| esteban_admin | admin456 | Administrator |
| natalia_ciru | ciru567 | Veterinary surgeon |
| julian_fauna | fauna678 | Wildlife specialist |
| caro_zoo | zoo789 | Zootechnician |

## 📁 Project Structure

```
Pet_Claws_Management/
├── mascota/                          # Main Django project
│   ├── manage.py                     # Command-line utility
│   ├── mascota/                      # Project configuration
│   │   ├── settings.py              # Settings
│   │   ├── urls. py                  # Main URLs
│   │   ├── wsgi.py                  # WSGI configuration
│   │   └── asgi.py                  # ASGI configuration
│   └── aplicacion_garras/           # Main application
│       ├── models.py                # Models: Persona, Tipo, Usuario
│       ├── views.py                 # Views and business logic
│       ├── urls.py                  # Application routes
│       ├── forms. py                 # Django forms
│       ├── static/                  # Static files (CSS, images)
│       │   └── aplicacion_garras/
│       │       ├── base.css
│       │       └── home.css
│       └── templates/               # HTML templates
│           └── aplicacion_garras/
│               ├── base. html
│               ├── home.html
│               ├── ingreso.html
│               ├── cargos.html
│               ├── personas.html
│               └── ...  
├── estructura_mysql. sql             # Database script
├── requirements.txt                 # Python dependencies
└── README. md                        # This file
```

## 🔧 Features by Module

### 🏠 Home
- User login
- Main dashboard with navigation
- Logout

### 💼 Job Positions
- List all job positions
- Create new position
- Edit existing position
- Delete position

### 👥 People
- List all people
- Register new person
- Edit person information
- Delete person

### 👤 Users
- List system users
- Create user and assign position
- Edit user
- Delete user

## 🌐 Main Routes

- `/` - Login
- `/inicio/` - Home page
- `/logout/` - Logout
- `/cargos/` - Job positions management
- `/personas/` - People management
- `/usuarios/` - Users management
- `/admin/` - Django admin panel

## 🎨 Design Features

- Responsive design with CSS Grid
- Modern gradients and visual effects
- Sidebar navigation
- CSS animations
- Corporate blue theme (#1e40af)

## 🔒 Security

⚠️ **Important**: This project is configured for development.  For production:

1. Set `DEBUG = False` in `settings.py`
2. Change `SECRET_KEY` to a secure key
3. Configure `ALLOWED_HOSTS`
4. Use environment variables for credentials
5. Implement HTTPS
6. Use hashed passwords (currently plain text in DB)


## 📝 License

This is an open source project.

## 👨‍💻 Author

**Andrés Flórez** - [Andresflorezdev](https://github.com/Andresflorezdev)

## 📧 Contact

For questions or suggestions, please open an issue in the repository.

---

⭐️ If you like this project, give it a star! 
