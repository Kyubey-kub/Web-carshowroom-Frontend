🎨 Car Showroom Frontend
Welcome to the Frontend of the Car Showroom project! This submodule powers the user interface, built with React, TypeScript, and Vite. 🚀

🌟 Features

📱 Responsive Design: Works seamlessly on all devices using TailwindCSS.
🖼️ 3D Visualization: Powered by @react-three/fiber and @react-three/drei for stunning car model rendering.
📊 Data Visualization: Interactive charts with chart.js and react-chartjs-2.
⚡ Fast Development: Hot Module Replacement (HMR) with Vite for a smooth dev experience.


📦 Installed Packages
Here are the packages powering the Frontend (car-showroom-frontend@0.0.0):



Category
Packages



Core Frameworks
react@19.0.0, react-dom@19.0.0, react-router-dom@7.4.1


3D Rendering
@react-three/fiber@9.1.0, @react-three/drei@10.0.4, three@0.174.0


Styling
tailwindcss@3.4.17, autoprefixer@10.4.21, postcss@8.5.3


Data & API
axios@1.8.4, chart.js@4.4.8, react-chartjs-2@5.3.0


Animations
framer-motion@12.6.2


Linting & Types
eslint@9.22.0, @eslint/js@9.22.0, typescript@5.7.3, typescript-eslint@8.26.0, eslint-plugin-react-hooks@5.2.0, eslint-plugin-react-refresh@0.4.19, @types/react@19.0.10, @types/react-dom@19.0.4, globals@15.15.0


Build Tools
vite@6.2.1, @vitejs/plugin-react@4.3.4


Validation
validator@13.15.0



🛠️ Setup Details
This project uses Vite for a fast build process and React with TypeScript for type safety. Key features include:

Hot Module Replacement (HMR): Instant updates during development.
ESLint Rules: Ensures code quality with TypeScript-aware linting.

Available Plugins

@vitejs/plugin-react: Uses Babel for Fast Refresh.
@vitejs/plugin-react-swc: Uses SWC for Fast Refresh.

Expanding the ESLint Configuration
For production, enable type-aware lint rules by updating your ESLint configuration:
export default tseslint.config({
  extends: [
    // Remove ...tseslint.configs.recommended and replace with this
    ...tseslint.configs.recommendedTypeChecked,
    // Alternatively, use this for stricter rules
    ...tseslint.configs.strictTypeChecked,
    // Optionally, add this for stylistic rules
    ...tseslint.configs.stylisticTypeChecked,
  ],
  languageOptions: {
    parserOptions: {
      project: ['./tsconfig.node.json', './tsconfig.app.json'],
      tsconfigRootDir: import.meta.dirname,
    },
  },
})

Adding React-Specific Lint Rules
You can enhance linting with React-specific rules by installing eslint-plugin-react-x and eslint-plugin-react-dom:

Install the Packages:
npm install eslint-plugin-react-x eslint-plugin-react-dom --save-dev


Update ESLint Configuration:Add the following to your eslint.config.js:
// eslint.config.js
import reactX from 'eslint-plugin-react-x'
import reactDom from 'eslint-plugin-react-dom'

export default tseslint.config({
  plugins: {
    'react-x': reactX,
    'react-dom': reactDom,
  },
  rules: {
    ...reactX.configs['recommended-typescript'].rules,
    ...reactDom.configs.recommended.rules,
  },
})




🚀 Getting Started

Clone the Repository:
git clone https://github.com/Kyubey-kub/web-carshowroom-Frontend.git
cd web-carshowroom-Frontend


Install Dependencies:
npm install


Run the Project:
npm run dev




🤝 Contributing
We welcome contributions! Please fork the repository, create a new branch, and submit a pull request. For major changes, open an issue first to discuss.

📜 License
This project is licensed under the MIT License - see the LICENSE file for details.

🌟 Happy coding! If you have any questions, feel free to reach out via GitHub Issues.
