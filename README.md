# GIA Energy Website

Live site: `https://www.giaenergy.com/`

## Overview

This project is a corporate website for GIA Energy, a company focused on solar energy solutions in Colombia.

I built it as a clear, conversion-focused website with two main goals:

- present the company and its services in a professional way;
- make it easy for potential clients to get in touch and request a quote.

Even though the project is simple by nature, I approached it with the same mindset I use in larger products: make good technical decisions, keep the code maintainable, and avoid adding complexity that does not create real value.

## What I Built

The website includes:

- a landing page with brand messaging, service highlights, and calls to action;
- a services page with categorized solar and energy-related solutions;
- a results page to showcase completed projects and build trust;
- a contact page with a validated lead capture form;
- reusable UI components such as header, footer, cards, labels, and shared sections.

## Skills Demonstrated

This project is small, but it reflects how I apply my knowledge in real business scenarios.

- Frontend architecture: I structured the app with reusable components, separated static content into data modules, and kept the code organized around maintainability.
- React and Next.js: I used the Next.js App Router, component-based composition, client-side interactivity where needed, and static export for a lightweight production build.
- TypeScript: I defined interfaces for component props and data models to keep the implementation safer and easier to scale.
- UI engineering: I built a responsive interface with SCSS, reusable styles, and a consistent visual structure across pages.
- Form handling and validation: I implemented client-side validation and input sanitization for the contact form to improve data quality before submission.
- Integration thinking: I connected the contact flow to an AWS Lambda function using Amazon SES through the AWS SDK, keeping the website simple while still supporting a real business process.
- Deployment: I prepared the project for production and deployed it on Vercel.
- Infrastructure basics: I configured the domain setup with Route 53 for a GoDaddy-registered domain and implemented SSL so the site is served securely over HTTPS.
- Product judgment: I intentionally avoided overengineering and chose a solution proportional to the actual needs of the project.

## Technical Decisions

One of the things I wanted to show in this project is that good development is not only about adding features. It is also about knowing when not to complicate a solution.

For this website, I decided to:

- avoid global state management because the project does not need it;
- keep most content in local data files instead of adding a CMS too early;
- use a simple service layer for the email submission flow;
- configure the project for static export to keep deployment simple;
- focus on clarity, readability, and maintainability over unnecessary abstractions.

That decision-making is part of my engineering approach. I try to build systems that match the real scope of the product instead of forcing patterns that only add noise.

## Contact Flow

The contact section is one of the most important parts of the site because it supports lead generation.

Users can submit:

- full name;
- city;
- phone number;
- email;
- estimated monthly energy cost range.

On the frontend, I added validation and sanitization to improve the quality of the submitted data. For the email delivery flow, I used an AWS Lambda function integrated with Amazon SES through the AWS SDK.

## Tech Stack

- Next.js 15
- React 19
- TypeScript
- Sass (SCSS)
- Swiper
- AWS Lambda
- Amazon SES
- Route 53
- SSL / HTTPS
- Vercel

## Project Structure

```text
src/
  app/          # Pages and app-level configuration
  components/   # Reusable UI components
  lib/          # Static data for content sections
  services/     # External service integrations
  styles/       # Shared Sass variables and mixins
  utils/        # Small helper utilities

public/         # Images, icons, video, and static assets
```

## Running The Project

```bash
npm install
npm run dev
```

Local development runs at:

```bash
http://localhost:3000
```

## Build And Deployment

This project is configured for static export and production deployment.

```bash
npm run build
npm run export
```

The live version is deployed on Vercel:

`https://www.giaenergy.com/`

For production setup, I also configured the domain connection for a GoDaddy-registered domain through Route 53 and ensured the site was served over HTTPS with SSL enabled.
