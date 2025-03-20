# Introduction to Next.js: Getting Started

## What is Next.js

Next.js is a React-based framework for building hybrid applications. It enables you to create anything from static websites to fully dynamic web apps at scale—or any combination of the two. Built and maintained by Vercel, Next.js comes packed with a set of simple, opinionated conventions designed to streamline development and make sophisticated React features easier to adopt.

### 🚀 Getting Started: Setting up your Development Environment

Let's get your development environment ready! Follow these steps to set up the project:

1. **Install Node.js 20+:**

   - Ensure you have Node.js version 20 or higher installed. You can check your version by running `node -v` in your terminal.
   - If you need to install or upgrade Node.js, you can download it from [nodejs.org](https://nodejs.org/).

2. **Clone the Repository:**

   - Clone the project repository to your local machine using Git. Replace `[repo]` with the actual repository URL provided for this lesson.
     ```bash
     git clone https://github.com/Hendrixer/next.js-fundamentals
     cd next.js-fundamentals
     ```

3. **Install Dependencies:**

   - Navigate into the cloned repository directory in your terminal.
   - Install project dependencies using npm:
     ```bash
     npm install
     ```
     or the shorthand:
     ```bash
     npm i
     ```

4. **Checkout the Starting Branch:**

   - For this lesson, we'll start with the code from lesson 3. Checkout to the `03` branch:
     ```bash
     git checkout 03
     ```
     This branch contains the starting point for this lesson's exercises.

5. **Configure Environment Variables:**

   - Look at the `.env.example` file in the project root. This file provides a template for the environment variables your application needs.
   - Create a new file named `.env` in the project root.
   - Copy the contents of `.env.example` into your new `.env` file.
   - **JWT Secret:** For `JWT_SECRET`, you can use any random string for development purposes. This secret is used to sign and verify JSON Web Tokens.
   - **Database URL:** You'll need a PostgreSQL database.
     - **Option 1: Local PostgreSQL:** If you have PostgreSQL running locally, configure `DATABASE_URL` to connect to your local database.
     - **Option 2: Hosted PostgreSQL (Instagres/NeonDB):** For a quick setup, you can use [Instagres](https://www.instagres.com/) (powered by NeonDB) to get a temporary hosted PostgreSQL database.
       - Go to [Instagres](https://www.instagres.com/) and create a new database.
       - Copy the provided database URL.
       - Paste this URL as the value for `DATABASE_URL` in your `.env` file.
       - **Important:** Instagres databases expire after one hour. You can create a new one when needed or consider creating a free Neon account for a more persistent database.

6. **Run Database Migrations:**

   - To set up the database schema, you need to run database migrations. This will create the necessary tables in your PostgreSQL database.
   - Run the following command in your terminal:
     ```bash
     npm run db:push
     ```
     This command uses Dirzzle ORM to push your database schema to the configured database.

7. **Start Development Server (Optional):**
   - While not strictly necessary for setup, you can start the development server to verify everything is working:
     ```bash
     npm run dev
     ```
     Then, open your browser and navigate to `http://localhost:3000`.

🎉 **You're all set!** You've successfully set up your Next.js development environment and are ready to start exploring the code in lesson 3.
