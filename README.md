
Mohit | Portfolio
Personal portfolio website of Mohit, a frontend developer based in New Delhi, India. The site presents my projects, skills, education and contact details in a fast, responsive, single-page layout.

Live site: https://your-domain.com (replace after deployment)

Table of Contents
Overview
Features
Tech Stack
Project Structure
Getting Started
Available Scripts
Environment Variables
Customization
Deployment
Roadmap
Contact
License
Overview
This portfolio is built to show what I work with every day: JavaScript, TypeScript, React, Next.js, Node.js and Tailwind CSS. The goal is a clean, accessible and quick website that a recruiter or client can scan in under a minute.

Main sections:

Hero with a short introduction and call to action
About me and education
Skills grouped by area
Selected projects with links to source code and live demos
Contact form
Resume download
Features
Fully responsive layout for mobile, tablet and desktop
Light and dark theme with system preference detection
Server-side rendering and static generation with Next.js
Type-safe codebase using TypeScript
Utility-first styling with Tailwind CSS
Contact form handled by a Node.js API route with validation
Project data stored in a single typed file for easy updates
Semantic HTML, keyboard navigation and visible focus states
SEO metadata and Open Graph tags configured per page
Optimized images with the Next.js image component
Tech Stack
Area	Technology
Language	JavaScript (ES2022), TypeScript
Framework	Next.js (App Router)
UI library	React
Styling	Tailwind CSS
Backend	Node.js (Next.js API routes)
Linting	ESLint, Prettier
Version control	Git and GitHub
Hosting	Vercel
Project Structure
portfolio/
├── public/
│   ├── images/              Project screenshots and profile photo
│   └── resume.pdf           Downloadable resume
├── src/
│   ├── app/
│   │   ├── layout.tsx       Root layout, fonts and metadata
│   │   ├── page.tsx         Home page composing all sections
│   │   ├── globals.css      Tailwind directives and base styles
│   │   └── api/
│   │       └── contact/
│   │           └── route.ts Contact form handler
│   ├── components/
│   │   ├── Navbar.tsx
│   │   ├── Hero.tsx
│   │   ├── About.tsx
│   │   ├── Skills.tsx
│   │   ├── Projects.tsx
│   │   ├── ProjectCard.tsx
│   │   ├── Contact.tsx
│   │   ├── Footer.tsx
│   │   └── ThemeToggle.tsx
│   ├── data/
│   │   ├── projects.ts      Project list
│   │   └── skills.ts        Skill groups
│   ├── lib/
│   │   └── validators.ts    Contact form validation
│   └── types/
│       └── index.ts         Shared TypeScript types
├── .env.example
├── next.config.js
├── tailwind.config.ts
├── tsconfig.json
├── package.json
└── README.md
Getting Started
Prerequisites
Node.js 18 or later
npm, yarn or pnpm
Git
Installation
bash
# Clone the repository
git clone https://github.com/your-username/portfolio.git

# Move into the project folder
cd portfolio

# Install dependencies
npm install

# Create your environment file
cp .env.example .env.local

# Start the development server
npm run dev
Open http://localhost:3000 in your browser.

Available Scripts
Command	Description
npm run dev	Start the development server
npm run build	Create an optimized production build
npm run start	Run the production build locally
npm run lint	Check code with ESLint
npm run format	Format code with Prettier
npm run typecheck	Run the TypeScript compiler without emitting files
Environment Variables
Create a .env.local file in the project root:

# Address that receives contact form messages
CONTACT_RECEIVER_EMAIL=

# SMTP settings used by the contact API route
SMTP_HOST=
SMTP_PORT=
SMTP_USER=
SMTP_PASS=

# Public site URL used for metadata
NEXT_PUBLIC_SITE_URL=http://localhost:3000
Never commit .env.local to the repository.

Customization
Update personal details
Edit the content in src/components/Hero.tsx and src/components/About.tsx.

Add or edit projects
Open src/data/projects.ts and add an entry:

ts
{
  title: "Project Name",
  description: "One or two lines about what the project does.",
  tags: ["React", "TypeScript", "Tailwind CSS"],
  github: "https://github.com/your-username/project",
  live: "https://project-demo.com",
  image: "/images/project-name.png",
}
Update skills
Edit src/data/skills.ts to add, remove or regroup skills.

Change colors and fonts
Edit tailwind.config.ts under theme.extend to change the color palette and font families.

Replace the resume
Replace public/resume.pdf with your latest file, keeping the same name.

Deployment
The easiest way to deploy is Vercel.

Push the repository to GitHub.
Import the repository in Vercel.
Add the environment variables from the section above.
Click Deploy.
Every push to the main branch will trigger a new production deployment automatically.

Roadmap
Blog section using MDX
Case study pages for major projects
Page transition animations
Analytics integration
Unit tests for components and the contact API
Contact
Name: Mohit Sharma
Location: New Delhi, India
GitHub: https://github.com/your-username
LinkedIn: https://linkedin.com/in/your-username
Email: your-email@example.com
License
This project is licensed under the MIT License. You are free to use the code as a reference, but please do not reuse the personal content, images or resume.
