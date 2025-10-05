# INF Website Code with Blog & News Section

## Overview
This is the complete React-based code structure for the **Inua Nurse Footprint (INF)** website — a professional, medical-themed platform showcasing INF’s mission, programs, events, impact, and news. It uses **dark blue, white, and light blue** brand colors and integrates responsive design for both desktop and mobile.

### Theme
We use the **“Minimal Mistakes” GitHub Pages theme**, a free, elegant, and customizable theme suitable for medical or NGO-style organizations.

---

## Pages and Structure

### 1. **Home Page (`Home.jsx`)**
- Hero section with INF slogan: *“Uplift the Nurse to Uplift the Community.”*
- Brief introduction to INF.
- Buttons linking to *About, Programs,* and *Join Us* sections.
- Rotating banner for key highlights (e.g., medical camps, trainings, and mental health initiatives).

### 2. **About Page (`About.jsx`)**
- Overview of INF as an **organization**, not just a project.
- Mission, Vision, and Core Values.
- INF slogans displayed creatively with nursing visuals.
- Leadership section with profiles (photos, titles, short bios).

### 3. **Programs Page (`Programs.jsx`)**
- Sections for each core area: mentorship, community outreach, welfare, training, and leadership development.
- Each section features icons, short descriptions, and relevant images.

### 4. **Events Page (`Events.jsx`)**
- Dynamic list of upcoming and past events (medical camps, trainings, webinars).
- Event cards include date, location, brief summary, and photos.
- Integrated calendar view for scheduled activities.

### 5. **Impact Page (`Impact.jsx`)**
- Showcases measurable outcomes and testimonials.
- Infographics showing number of students mentored, patients served, and trainings conducted.
- Embedded map showing outreach locations.

### 6. **Gallery Page (`Gallery.jsx`)**
- Professional image gallery showcasing events, trainings, and community service.
- Filter by category (e.g., Medical Camps, Webinars, Mentorship).
- Lightbox feature for enlarged photo viewing.

### 7. **Blog & News Page (`Blog.jsx`)** 📰
- Dedicated space for sharing INF updates, nursing news, and public health insights.
- Sections:
  - **Latest Updates:** Quick news posts with featured images.
  - **From the Field:** Articles written by nursing students and mentors.
  - **Announcements:** Opportunities, scholarships, and event notices.
- Comment or feedback option via embedded Google Form or Disqus.

### 8. **Contact Page (`Contact.jsx`)**
- Contact form for partnership inquiries or membership.
- Display INF email, phone, and social media links.
- Embedded Google Map of main location (University of Nairobi).

---

## Additional Features
- **Responsive Navbar & Footer** across all pages.
- **Animated transitions** using Framer Motion.
- **SEO-friendly structure** and clean typography.
- Integration with **GitHub Pages** for free hosting.

---

## Recommended File Structure
```
INF-Website/
├── public/
│   ├── index.html
│   ├── images/
├── src/
│   ├── components/
│   │   ├── Navbar.jsx
│   │   ├── Footer.jsx
│   │   ├── Hero.jsx
│   ├── pages/
│   │   ├── Home.jsx
│   │   ├── About.jsx
│   │   ├── Programs.jsx
│   │   ├── Events.jsx
│   │   ├── Impact.jsx
│   │   ├── Gallery.jsx
│   │   ├── Blog.jsx
│   │   ├── Contact.jsx
│   ├── App.jsx
│   ├── index.js
├── package.json
├── README.md
```

---

## Deployment Instructions
1. Push this repository to **GitHub**.
2. Go to *Settings → Pages → Branch: main → /root*.
3. Save and deploy to activate your free GitHub Pages website.

---

**INF – Inua Nurse Footprint**  
*#TheNextGenerationOfNurses*  
*#UpliftTheNurseToUpliftTheCommunity*  
*#LeaveNoNurseBehind*
