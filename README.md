🌱 LinkPlant
A simple link-in-bio application built with Django. Create profiles, add multiple links, and share your personal link page with others.

✨ Features
Profile Management - Create profiles with customizable background colors

Link Management - Add, edit, and delete links for each profile

Public Profile Pages - Beautiful, mobile-friendly link pages with color themes

Admin Interface - Full Django admin support for easy management

Responsive Design - Built with Tailwind CSS for modern, responsive UI

🚀 Quick Start
Prerequisites
Python 3.8+

Django 4.0+

pip

Installation
Clone the repository

bash
git clone https://github.com/yourusername/linkplant.git
cd linkplant
Create a virtual environment

bash
python -m venv venv
Activate the virtual environment

bash
# Windows
venv\Scripts\activate

# macOS/Linux
source venv/bin/activate
Install dependencies

bash
pip install django django-crispy-forms crispy-tailwind
Apply migrations

bash
python manage.py migrate
Create a superuser (optional but recommended)

bash
python manage.py createsuperuser
Run the development server

bash
python manage.py runserver
Visit http://127.0.0.1:8000 in your browser

📁 Project Structure
text
linkplant/
├── link_plant/
│   ├── admin.py          # Admin configuration
│   ├── apps.py           # App configuration
│   ├── models.py         # Profile & Link models
│   ├── tests.py          # Test cases
│   ├── urls.py           # URL routing
│   └── views.py          # View logic
├── templates/
│   └── link_plant/
│       ├── _base.html    # Base template
│       ├── link_form.html    # Link create/update form
│       ├── link_list.html    # Links dashboard
│       ├── link_confirm_delete.html  # Delete confirmation
│       └── profile.html  # Public profile page
├── manage.py
└── requirements.txt
🎨 Usage
Creating a Profile
Access the Django admin panel at /admin/

Add a new Profile with:

Name: Your display name

Slug: URL-friendly identifier (e.g., john-doe)

Background Color: Choose from Blue, Green, or Yellow

Adding Links
Visit the main dashboard at /

Click "Add Link"

Fill in:

Text: Display text for the link

URL: The destination URL

Profile: Select which profile this link belongs to

Sharing Your Profile
Your public profile URL will be: http://yoursite.com/your-slug/

Share this URL with others to showcase your links

🔧 Models
Profile
Field	Type	Description
name	CharField	Profile display name
slug	SlugField	URL identifier
bg_color	CharField	Background color choice
Link
Field	Type	Description
text	CharField	Link display text
url	URLField	Destination URL
profile	ForeignKey	Related Profile
🎨 Customization
Adding Background Colors
Edit models.py in the BG_CHOICES tuple:

python
BG_CHOICES = (
    ("blue", "Blue"),
    ("green", "Green"),
    ("yellow", "Yellow"),
    ("purple", "Purple"),  # Add new colors here
)
Styling
All templates use Tailwind CSS. Customize the appearance by:

Editing _base.html for global layout

Modifying profile.html for public page design

Adjusting colors in the header/navbar

🔒 Security
CSRF protection enabled on all forms

Django's built-in security features active

URL validation on link fields

📱 Responsive Design
The application is fully responsive:

Desktop: Grid layout with table view for links

Mobile: Stacked layout optimized for small screens

Public profiles: Centered, mobile-first design

🤝 Contributing
Fork the repository

Create a feature branch (git checkout -b feature/AmazingFeature)

Commit your changes (git commit -m 'Add some AmazingFeature')

Push to the branch (git push origin feature/AmazingFeature)

Open a Pull Request

📝 License
This project is open source and available under the MIT License.

🙏 Acknowledgments
Built with Django

Styled with Tailwind CSS

Inspired by link-in-bio services like Linktree

Made by Meher Labidi
