# WorkTree

WorkTree is a booking platform for office and coworking spaces, like Airbnb but for places to work. Owners list their spaces, renters request dates, and owners accept or decline each request from their dashboard.

Built in a 5-day sprint at the [Le Wagon Amsterdam](https://www.lewagon.com/amsterdam) Full Stack Web Development bootcamp (March 2025), by a team of three.

## Screenshots

<p align="center">
  <img src="docs/screenshots/home.png" width="240" alt="WorkTree home page with coworking spaces">
  <img src="docs/screenshots/space.png" width="240" alt="Space details and booking form">
  <img src="docs/screenshots/dashboard.png" width="240" alt="Owner dashboard with listed spaces">
</p>
<p align="center">
  <img src="docs/screenshots/requests.png" width="240" alt="Booking requests with accept and decline actions">
  <img src="docs/screenshots/sign-in.png" width="240" alt="Sign in page">
</p>

## Features

- **Two user roles**: every user starts as a renter and becomes an owner by listing a space.
- **Space listings**: owners create and delete listings with photos (uploaded to Cloudinary), price per hour and per day, capacity and availability.
- **Booking requests**: renters choose start and end dates; dates in the past are rejected.
- **Approval workflow**: each booking moves through three states: pending, accepted or declined.
- **Role-based dashboard**: owners see incoming requests for their spaces, and renters see the status of their own bookings.

## Tech stack

- **Backend:** Ruby 3.3, Ruby on Rails 7.1, PostgreSQL
- **Frontend:** Hotwire (Turbo + Stimulus), Bootstrap 5, Flatpickr
- **Other:** Devise (authentication), Active Storage with Cloudinary (image uploads), Docker

## My role

I built the dashboard and the booking flow behind it:

- Built the dashboard that shows different content to owners and renters.
- Built the accept and decline actions in the bookings controller, so a renter's request appears in the owner's dashboard.
- Added the delete action for spaces, and buttons that only owners can see.
- Worked on the booking and space models, the routes and the dashboard styling.

## Run it locally

Requirements: Ruby 3.3.5, PostgreSQL.

```bash
git clone https://github.com/ozgekuzhan/worktree.git
cd worktree
bundle install
rails db:create db:migrate db:seed
rails server
```

Image uploads need a Cloudinary account. Add it to a `.env` file:

```
CLOUDINARY_URL=cloudinary://API_KEY:API_SECRET@CLOUD_NAME
```

## Team

- [Ozge Kuzhan](https://github.com/ozgekuzhan)
- [paucotan](https://github.com/paucotan)
- Artem Zemskov
