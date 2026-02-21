---
title: Build UI using Syncfusion UI Builder
description: Step-by-step tutorial to build a customer dashboard in React using Syncfusion UI Builder in Code Studio. Includes data grid, charts, and export features.
platform: syncfusion-code-studio
keywords: tutorial, ui-builder, syncfusion-components, dashboard, data-grid, charts
---

# Build UI Using Syncfusion UI Builder

## Overview

Ever wanted to build a professional dashboard with minimal code? In this tutorial, we'll do exactly that! We'll use the powerful **UI Builder tool** in Code Studio to create a stunning customer dashboard complete with interactive data grids, charts, and export functionality—all powered by Syncfusion components.

The best part? You won't spend hours writing boilerplate code. UI Builder does the heavy lifting, and you focus on making it yours. By the end of this tutorial, you'll have a fully functional dashboard that looks great and works seamlessly.

## Prerequisites

Let's make sure you have everything you need:

- **Syncfusion Code Studio** installed and ready to go. (Not there yet? Check out [Install and Configure](/code-studio/getting-started/install-and-configuration) first!)
- **UI Builder tool enabled** in Code Studio (we'll verify this together in Step 1)
- [Node.js](https://nodejs.org/en/download) and npm.
- **A Syncfusion license key** ready. ([Learn how to generate one](https://help.syncfusion.com/common/essential-studio/licensing/how-to-generate))



## What You'll Learn

By following this tutorial, you'll gain these skills:

- Build professional dashboards with AI-generated UI code
- Use UI Builder to create data grids and charts effortlessly
- Write effective UI Builder requests to create full features
- Customize generated Syncfusion components
- Wire up real functionality like exports in minutes
- Set up licensing and themes correctly
- Deploy a fully working React dashboard

## Let's Build!

### Step 1: Set Up Your React Project

First things first—let's create a fresh React project that we'll transform into a dashboard.

1. **Open your terminal** and create a new React app using Vite (it's super fast!):
   ```bash
   npm create vite@latest customer-dashboard -- --template react
   cd customer-dashboard
   ```

   **What's happening here?** We're creating a React project with Vite. Think of it as the starting foundation for your dashboard.

2. **Open the project folder** in Syncfusion Code Studio. You should see your project structure on the left side.

3. **Now, let's verify UI Builder is ready:**
   - Look for the **Configure Tools** option in Code Studio
   - Make sure **UI Builder** is enabled (you should see a checkmark)
   
   <img src="tutorials-images/tool.png" alt="UI Builder Tool" />
   <img src="tutorials-images/toolenable.png" alt="UI Builder Tool Enable" />

   **Why do we need UI Builder enabled?** This tool unlocks the ability for Code Studio to generate professional dashboard code for us. Without it, we'd be writing lots of boilerplate by hand!

**Your foundation is ready!** You now have a blank React project and UI Builder standing by. Let's move to the fun part—generating your dashboard.



### Step 2: Generate Dashboard With UI Builder

This is where the magic happens. We'll describe what we want, and UI Builder will generate the code for us.

1. **In the chat input field**, paste this request:
   ```
   Create a customer dashboard for React using Syncfusion components with data grid, charts, and export functionality.

   ```

   > **Note:** Being specific helps! Instead of just "create a dashboard," we told UI Builder exactly what components we need: data grid, specific charts, and export features. The more detail, the better the result.

2. **Press Enter and watch the magic** happen! Code Studio will:
   - Analyze your request
   - Generate React components with Syncfusion elements
   - Wire up the data grid with sample data
   - Create chart components 
  

   <img src="tutorials-images/context.png" alt="UI Builder Context" />

  



### Step 3: Register Syncfusion License and Theme

1. Ensure required Syncfusion packages are installed. Code Studio typically installs dependencies automatically when generating components.

2. [Register](https://help.syncfusion.com/common/essential-studio/licensing/how-to-register-in-an-application#reactjs) your Syncfusion license key in your app entry (for example, in index.js):
   ```javascript
   import { registerLicense } from '@syncfusion/ej2-base';
   registerLicense('YOUR_LICENSE_KEY');
   ```
   
3. Confirm that a Syncfusion theme CSS import is present in your entry styles.


**Great!** Your dashboard is now licensed and themed. Time to see it in action.


### Step 4: Launch Your Dashboard

It's time to see your dashboard come to life!

1. **Start the development server:**
   ```bash
   npm run dev
   ```
   
   

2. **Open your browser** and navigate to the URL shown in your terminal (example: `http://localhost:5173`)

3. **Take a moment to admire your work!** You should see:
   - A professional-looking customer dashboard
   - A data grid with customer information (sortable and filterable)
   - Charts showing sales trends and customer growth
   - Export buttons ready to convert your data to PDF or Excel

 **Your dashboard is live!** This is a fully functional React app with real Syncfusion components. Pretty cool, right?



**You've created a production-ready dashboard!** .


### Step 5: Make It Your Own (Optional)

UI Builder gave us a great starting point, but now we can personalize it. Here are some ideas:

- Adjust grid columns, sorting, filtering, and pagination settings
- Update chart types, series, and data sources
- Add toolbar items such as Excel/PDF export and wire them to handlers
- Replace sample data with API-backed data as needed

**The foundation is yours to build on!** Each change you make will feel smoother now that you understand the structure.



## Verify: Did Everything Work?

Let's verify your dashboard is working as expected. Here's what success looks like:

<img src="tutorials-images/customer-dashboard-output.png" alt="Customer Dashboard Output" />

Validate the following:

- Data Grid
  - Columns support sorting and filtering
  - Pagination works and data renders correctly
- Charts
  - Sales by Region (bar) and Customer Growth (line) show expected values
  - Tooltips and interactions work; layout is responsive
- Export
  - Grid exports to Excel and PDF successfully
  - Exported files contain correct data and formatting
- Integration
  - No runtime errors; acceptable load and render performance
  - License key is registered and no license popups appear

If something fails:
- Ensure all Syncfusion packages and peer dependencies are installed
- Verify theme CSS imports
- Check data shapes against component requirements

## What's Next? Keep Building!

You've just created your first professional dashboard. The journey doesn't stop here—here are some exciting directions you can go:

**Want to understand UI Builder better?**
→ Visit the [UI Builder Guide](/code-studio/ui-builder) to learn advanced techniques and discover what other platforms you can build for.