# ShineBay — Car Wash Service & Booking Website

A modern, responsive, multi-page website for a car wash and auto detailing business. Built with React, Vite, React Router, and Tailwind CSS, ShineBay provides an interactive platform for exploring services, comparing prices, viewing packages, and submitting booking requests.

The project focuses on a professional user experience, reusable components, responsive layouts, and a multi-step booking flow.

**Project Type:** Frontend Development  
**Application:** Car Wash & Auto Detailing  
**Architecture:** Multi-page experience using client-side routing  
**Backend:** Not included

## ✨ Features

- **Modern Homepage** — Hero section, service previews, business highlights, testimonials, and booking calls to action.
- **Service Catalog** — Browse available car wash and detailing services.
- **Vehicle Categories** — Explore the vehicle types supported by the business.
- **Pricing Matrix** — Compare service prices by vehicle type.
- **Service Packages** — View bundled services and package pricing.
- **How It Works** — Understand the five-step customer journey.
- **Gallery** — Browse a visual gallery with lightbox functionality.
- **Multi-Step Booking** — Select services, enter customer and vehicle details, choose a schedule, and review booking information.
- **Booking Validation** — Client-side validation for required fields, phone numbers, and email addresses.
- **Mock Availability** — Demonstration time slots with unavailable slots disabled.
- **Booking Confirmation** — Generate a booking reference and prepare the booking details for sharing.
- **WhatsApp & Email Integration** — Send booking details through a pre-filled WhatsApp message or email draft.
- **About Page** — Present business information, statistics, benefits, and customer reviews.
- **Contact Page** — Display contact details and an embedded Google Map.
- **Responsive Layout** — Adapt navigation, content, forms, and grids to mobile, tablet, and desktop screens.
- **Reusable Components** — Shared navigation, footer, page headers, CTA banners, and floating action buttons.
- **Custom Animations** — Design tokens, transitions, and visual effects for a polished browsing experience.
- **404 Page** — Provide a dedicated page for unknown routes.

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| React 19 | Component-based UI development |
| Vite | Development server and production build |
| JavaScript | Application logic |
| React Router | Client-side navigation |
| Tailwind CSS 3 | Styling and responsive layouts |
| Lucide React | Icons |
| Browser APIs | Client-side interactions and booking handoff |

## 🚀 Getting Started

### Prerequisites

Install the following before running the project:
- npm

### Installation

1. Clone the repository:

   ```bash
   git clone YOUR_REPOSITORY_URL
   ```

2. Navigate to the project directory:

   ```bash
   cd shinebay
   ```

3. Install dependencies:

   ```bash
   npm install
   ```

4. Start the development server:

   ```bash
   npm run dev
   ```

5. Open the local URL displayed in the terminal, usually `http://localhost:5173`.

### Production Build

Create an optimized production build:

```bash
npm run build
```

Preview the production build locally:

```bash
npm run preview
```

The generated production files are stored in the `dist/` directory.

## 📄 Pages & Routes

| Route | Description |
|---|---|
| `/` | Homepage with hero, service previews, benefits, process, and testimonials |
| `/services` | Complete car wash and detailing service catalog |
| `/vehicle-types` | Supported vehicle categories |
| `/pricing` | Vehicle-by-service pricing comparison |
| `/packages` | Bundled service packages |
| `/how-it-works` | Five-step service process |
| `/gallery` | Image gallery with lightbox |
| `/booking` | Multi-step booking form and confirmation |
| `/about` | Business introduction, statistics, and customer reviews |
| `/contact` | Contact information and Google Maps embed |
| `*` | Custom 404 page |

## 📅 Booking Workflow

The booking experience is organized into five steps.

### 1. Select a Service

Choose a car wash or detailing service, select the vehicle type, and optionally choose a service package.

### 2. Enter Details

Provide customer information, including name, phone number, email, and WhatsApp contact where applicable. Enter vehicle details such as make, model, and registration number, with optional booking notes.

### 3. Choose a Schedule

Select a preferred date and an available time slot. Unavailable slots are determined using mock availability data defined in `src/data/data.js`.

### 4. Review the Booking

Check the selected services, vehicle details, customer information, schedule, and estimated pricing. Confirm the booking or return to edit the details.

### 5. Confirm and Share

Generate a booking reference and prepare the booking details for sending through WhatsApp or an email draft.

**Important:** Confirming the booking is a frontend demonstration. It does not create a persistent server-side booking or guarantee a real appointment.

## 📁 Project Structure

```text
src/
├── components/
│   ├── Layout.jsx
│   ├── Navbar.jsx
│   ├── PageHeader.jsx
│   ├── CTABanner.jsx
│   ├── Hero.jsx
│   ├── Services.jsx
│   ├── VehicleTypes.jsx
│   ├── Pricing.jsx
│   ├── Packages.jsx
│   ├── HowItWorks.jsx
│   ├── Booking.jsx
│   ├── Gallery.jsx
│   ├── WhyChooseUs.jsx
│   ├── Testimonials.jsx
│   ├── About.jsx
│   ├── Contact.jsx
│   ├── Footer.jsx
│   └── FloatingButtons.jsx
├── data/
│   └── data.js
├── pages/
│   ├── Home.jsx
│   ├── ServicesPage.jsx
│   ├── VehicleTypesPage.jsx
│   ├── PricingPage.jsx
│   ├── PackagesPage.jsx
│   ├── HowItWorksPage.jsx
│   ├── GalleryPage.jsx
│   ├── BookingPage.jsx
│   ├── AboutPage.jsx
│   ├── ContactPage.jsx
│   └── NotFound.jsx
├── App.jsx
├── main.jsx
└── index.css

tailwind.config.js
public/
  _redirects
```

*The structure highlights the main files described for the project. Your actual repository may contain additional configuration files or assets.*

## ⚙️ Customization

### Business Information

Update the `BUSINESS` object at the top of `src/data/data.js` to customize:

- Business name
- Phone and WhatsApp numbers
- Email address
- Business address
- Opening hours
- Google Maps embed URL

### Services, Pricing & Packages

Edit the corresponding data arrays and objects in `src/data/data.js` to update:

- Available car wash and detailing services
- Vehicle categories
- Vehicle-specific pricing
- Service packages
- Gallery content
- Testimonials
- Mock time-slot availability

### Styling & Branding

Customize the visual identity using:

- `tailwind.config.js` for Tailwind theme configuration
- `src/index.css` for design tokens, fonts, and animations

### Adding a New Page

1. Create a page component inside `src/pages/`.
2. Register its route in `src/App.jsx`.
3. Add navigation links in `src/components/Navbar.jsx` or `src/components/Footer.jsx`.
4. Test the page on mobile and desktop.

## 🌐 Deployment

The project can be deployed to a static hosting provider such as Netlify or Vercel.

Because the application uses React Router, configure the hosting platform to serve `index.html` for client-side routes. Otherwise, refreshing a route such as `/booking` may return a 404.

### Netlify

The project includes `public/_redirects` for SPA fallback, as described in the project configuration:

```text
/* /index.html 200
```

### Vercel

If required, create a `vercel.json` file in the project root:

```json
{
  "rewrites": [
    {
      "source": "/(.*)",
      "destination": "/"
    }
  ]
}
```

Verify the rewrite behavior with your Vite deployment configuration.

## ⚠️ Project Scope & Limitations

ShineBay is a **frontend-only project**. The following are not included:

- Backend server or database
- Persistent booking storage
- Real-time appointment availability
- User authentication
- Admin dashboard
- Automated booking notifications
- Online payment processing
- Server-side customer or vehicle records

Bookings are prepared for WhatsApp or email handoff, while availability and booking confirmation are demonstrated on the client side.

## 🎯 Project Objective

ShineBay demonstrates modern frontend development practices through a complete car wash service website, combining reusable React components, responsive styling, multi-page navigation, interactive forms, mock scheduling, and customer-friendly booking handoff.

---

**ShineBay — Car Wash Service & Booking Website**  
*Explore services. Compare packages. Book with ease.*

#   c a r - w a s h - f r o n t - e n d - a p p l i c a t i o n  
 #   c a r - w a s h - f r o n t - e n d - a p p l i c a t i o n  
 