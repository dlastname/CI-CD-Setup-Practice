# GitHub Actions CI/CD Pipeline

## Description

I needed some practice with seting up a CI/CD pipeline using GitHub Actions to automate testing and deployment for a full-stack application, so I made this repo. The pipeline runs Cypress component tests whenever a pull request is made to the `develop` branch and automatically deploys the application to Render when code is merged from `develop` to `main`.

The application is based on a [tech quiz project that I previously developed](https://github.com/dlastname/Tech-Quiz-Testing-Pratice), which is available in my GitHub repository. This project ensures the quiz application remains reliable by implementing automated testing and seamless deployment.

The application is [deployed on Render](https://ci-cd-setup-practice.onrender.com) and can be accessed at the provided deployment URL.

---

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [CI/CD Workflow](#ci-cd-workflow)
- [Technologies Used](#technologies-used)
- [License](#license)
- [Contributing](#contributing)
- [Questions](#questions)

---

## Features

- CI/CD pipeline with GitHub Actions
  - Runs Cypress component tests on every pull request to develop.
  - Automatically deploys to Render when `develop` is merged into `main`.
  
- Full-stack application deployment
  - Uses MongoDB Atlas for database storage.
  - Hosted on Render.

---

## Installation

To install the necessary dependencies, run:

```bash
npm install
```

Ensure you have created a GitHub repository and pushed the starter code before proceeding with CI/CD setup.

---

## Usage

1. Start the application locally:
   ```bash
   npm run start
   ```
   The application will be available at `http://localhost:3000`.

2. Run Cypress tests locally:
   ```bash
   npm run test
   ```

3. Deploy the application manually to Render (only for initial setup). After deployment, disable auto-deploy and copy the deploy hook URL from Render settings.

### Deployment

The application is deployed on Render and can be accessed at:

[Live Application](YOUR_RENDER_DEPLOYMENT_URL)

---

## CI/CD Workflow

This project includes two GitHub Actions workflows:

1. Cypress testing workflow (`.github/workflows/test.yml`)
   - Runs Cypress component tests when a pull request is made to develop.
   - Ensures all tests pass before merging.

2. Render deployment workflow (`.github/workflows/deploy.yml`)
   - Triggers when develop is merged into main.
   - Deploys the latest code to Render using the deploy hook URL.

### Setting Up GitHub Secrets

Add the following secrets to your GitHub repository under `Settings > Secrets and variables > Actions`:

- `RENDER_DEPLOY_HOOK` → Your Render deploy hook URL
- `MONGO_URI` → Your MongoDB Atlas connection string

---

## Technologies Used

- GitHub Actions: Automates CI/CD workflows.
- Cypress: Runs component and end-to-end tests.
- Render: Hosting platform for deployment.
- MongoDB Atlas: NoSQL database.
- Node.js & Express.js: Backend framework.
- React: Frontend framework.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

---

## Contributing

Contributions are welcome! Follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Commit your changes.
4. Push your branch and submit a pull request.

For major changes, please open an issue first to discuss proposed updates.

---

## Questions

If you have any questions, feel free to reach out:

- Email: [dllorens28@gmail.com](mailto:dllorens28@gmail.com)
- GitHub: [dlastname](https://github.com/dlastname)

---

