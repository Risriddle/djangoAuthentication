Django Authentication System
This is a simple user authentication system built with Django, allowing users to sign up, log in, reset passwords, view profiles, and change passwords. Users can log in using either their email or username.

Features
Sign Up: Users register with a unique username, email, and password.
Login: Login using either username or email.
Password Reset: Users can reset passwords via email (currently displayed in the console).
Profile & Dashboard: View and update user information.
Password Change: Authenticated users can change their passwords.
Logout: Ends the user session.


Email Configuration
Currently, emails for password resets are shown in the console. In production, you can switch to using services like Brevo (formerly Sendinblue) by configuring the email backend in settings.py:


EMAIL_BACKEND = 'django.core.mail.backends.smtp.EmailBackend'
EMAIL_HOST = 'smtp-relay.brevo.com'
EMAIL_PORT = 587
EMAIL_USE_TLS = True
EMAIL_HOST_USER = 'your_brevo_account_email'
EMAIL_HOST_PASSWORD = 'your_brevo_api_key'
