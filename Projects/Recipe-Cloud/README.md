Recipe Cloud
Overview

Recipe Cloud is a personal project designed as a small digital cooking book for phone and tablet use. The goal was to build an application that could store recipes, support user authentication, and experiment with OCR for extracting recipe content from images.

The project combined backend development, local infrastructure setup, authentication testing, and troubleshooting across a Linux-based environment.
Project Goals

    Build a lightweight recipe application for mobile and tablet use
    Store and manage recipe data
    Experiment with OCR for reading recipe text from images
    Test authentication and user access flows
    Run the project in a self-managed local environment

    ## Architecture

- [Architecture Notes](./architecture-notes.md)
- [Lessons Learned](./lessons-learned.md)

![Recipe Cloud Architecture](./recipe-cloud-architecture.png)

Technologies Used

    Python / FastAPI
    SQLite
    Google OAuth / Firebase
    Red Hat Linux VM
    OCR tools: Tesseract and EasyOCR
    Browser developer tools for debugging
    Local networking and VM-based hosting

What I Built

I created an MVP backend for a recipe application with:

    Google OAuth login
    user-based recipe storage
    SQLite database support
    image upload capability
    session-based authentication
    local testing and hosting from a Linux VM

Part of the work included connecting the application to a local virtual machine environment, configuring authentication, and validating access from another device on the same network.
OCR Experimentation

One of the project goals was to add OCR support for recipe extraction.

I tested:

    Tesseract
    EasyOCR

This worked as an initial proof of concept, especially for English text, but the OCR quality was not strong enough for the broader use case I wanted. After testing, I concluded that a more advanced AI-based OCR approach would likely be needed for better results.
Infrastructure and Security-Related Work

During the project, I worked on:

    setting up and running the app on a Red Hat VM
    allocating local compute resources for the VM and OCR processing
    configuring local connectivity for testing from a phone
    troubleshooting CORS configuration for HTTP-based local development
    testing user authentication and registration behavior
    reviewing cookies, requests, and authentication issues in browser developer tools
    reducing unnecessary exposure by reviewing open protocols and closing services that were not needed during testing

Key Challenges

    Getting local authentication flows to work correctly across devices
    Configuring CORS for early local HTTP testing
    Balancing VM resource allocation with OCR processing needs
    Understanding the limitations of local infrastructure for HTTPS-based deployment
    Evaluating OCR quality and deciding whether the approach was good enough to continue

What I Learned

    How local application hosting, networking, and authentication flows behave in practice
    The importance of protecting secrets, client IDs, and configuration values
    How browser developer tools can help troubleshoot authentication, cookies, and user registration issues
    How infrastructure choices affect application performance and usability
    How to think about reducing exposure by limiting unnecessary protocols and services
    The difference between a proof of concept and a more production-ready design

Project Status

This project is currently paused. The main reason is that the OCR results were not accurate enough for the intended use case, and improving the solution would require moving toward a stronger AI-based OCR approach and a more mature HTTPS-ready setup.
Why This Project Matters

This project helped me practice:

    Linux-based application hosting
    authentication setup and troubleshooting
    local infrastructure management
    OCR evaluation
    debugging web application behavior
    security-aware configuration decisions during development
