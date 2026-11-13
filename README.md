# Full-Stack MERN URL Shortener

A scalable, modular URL shortener web application built with the MERN stack. It follows a clean layered backend architecture (**Routes → Controllers → Services → DAO**) and uses **TanStack Router & TanStack Query** on the frontend.

## Tech Stack
- **Frontend:** React (Vite), Tailwind CSS, Redux Toolkit, TanStack React Query, TanStack React Router, Axios
- **Backend:** Node.js, Express.js (ES Modules), NanoID (7-character collision-resistant IDs)
- **Database:** MongoDB & Mongoose (with B-Tree indexing on short_url)
- **Authentication & Security:** Stateless JWT Authentication stored in HTTP-Only Cookies, bcrypt password hashing, CORS with credentials

## Key Features
- **Instant URL Shortening:** Generates unique 7-character short links using 
anoid with direct backend redirection (GET /:id) to minimize frontend load.
- **Custom Slugs (Authenticated Users):** Logged-in users can create custom vanity URLs with duplicate-slug validation.
- **Click Analytics Dashboard:** Tracks total clicks per link atomically using MongoDB \ and auto-refreshes stats on the user dashboard via TanStack Query cache invalidation.
- **Layered Backend Architecture:** Decoupled Data Access Objects (dao/), business logic (services/), request handlers (controller/), centralized AppError classes, and async 	ryCatchWrapper.
