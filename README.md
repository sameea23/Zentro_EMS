# Zentro_EMS
Zentro is a web-based Event Management System designed to help organizers create and manage events, while enabling attendees to browse events, register, and purchase tickets. This system provides a smooth workflow for event creation, ticketing, and user management.

# Group Members
Sameea Amjad

Ambreen Naeem

Sadaf Fatima

## Table of Contents
Features

Technologies Used

Installation & Setup

Usage

Database Structure

## Features
## Organizer
Create, edit, cancel, or delete events.

View registrations for their events.

Set event capacity and ensure no time conflicts at the venue.

Monitor ticket sales and payments.

## Attendee

Browse upcoming events.

Register for events and select ticket types (Standard, VIP, Premium).

View registration and payment status.

Cancel registration if needed.

## Admin

Manage all users, events, venues, tickets, and payments via Django admin.

## General Features

User authentication with roles (Admin, Organizer, Attendee).

Dynamic forms: Attendees provide phone numbers, Organizers provide organization names.

Event capacity validation.

Venue scheduling conflict detection.

Payment tracking and status messages.

Flash messages for user feedback.

## Technologies Used

Backend: Django (Python)

Frontend: HTML, CSS, JavaScript, Django Templates

Database: SQL Server (Microsoft SQL Server / SSMS)

Authentication: Django built-in user model (customized)

Other: Django Messages Framework for flash messages

## Installation & Setup

## Create a virtual environment:

python -m venv venv
source venv/bin/activate      # Linux / macOS
venv\Scripts\activate         # Windows


## Install dependencies:

pip install -r requirements.txt


## Configure database:

Update settings.py with your SQL Server credentials.

## Run migrations:

python manage.py makemigrations
python manage.py migrate

## Run the development server:

python manage.py runserver

Open your browser and navigate to http://127.0.0.1:8000/.

## Usage
## For Organizers

Sign up as an Organizer.

Create events by filling in details: title, description, venue, date & time, capacity.

View event registrations and ticket status.

Cancel or delete events if necessary.

## For Attendees

Sign up as an Attendee.

Browse upcoming events.

Register for events and choose a ticket type.

Make payments for tickets and view payment status.

Cancel registrations if needed.

## Admin

Access the Django admin panel at /admin to manage all data.

## Database Structure

Users (events_users) – stores all users with roles (admin, organizer, attendee)

Organizer (events_organizer) – organizer profile linked to users

Attendee (events_attendee) – attendee profile linked to users

Event (events_event) – event details, venue, capacity, status

EventRegistration (events_eventregistration) – attendee registration for events

Ticket (events_ticket) – ticket info for registrations

Payment (events_payment) – payment info for tickets
