# Chromia Todo App

A decentralized Todo application built on Chromia blockchain with Nuxt.js and MetaMask integration.

## Author
- Name: Tsion Tesfaye
- Email: tsitesfaye87466@gmail.com
- GitHub: https://github.com/TsionTesfaye

## Demo

🎥 [Watch the demo video](https://www.loom.com/share/942c7dc100fa42df8baa9da36d6c35a7?sid=a789e8e0-43d0-47ac-846d-aca9eee6bdb9) to see the application in action!

## Overview

This Todo App showcases the capabilities of Chromia's blockchain platform in building decentralized applications. By utilizing the Rell programming language for backend logic and integrating MetaMask for authentication, the app ensures secure, blockchain-based data storage and seamless user interactions. With a modern, responsive design built using Nuxt.js and Tailwind CSS, users can easily manage their tasks while enjoying the benefits of decentralized technology, including real-time updates and data integrity.

## Features

- 🔐 MetaMask Authentication
- ✏️ Create, Read, Update, and Delete Todos and update Username
- 🔄 Search for Todos and sort them along with task overview
- 📱 Responsive Design
- 🎨 Modern UI with Tailwind CSS
- ⛓️ Blockchain-based Data Storage

## Prerequisites

Before you begin, ensure you have installed:

- [Node.js](https://nodejs.org/en) (v16 or higher)
- [PostgreSQL](https://docs.chromia.com/intro/installation/) (Reccomended within docker)
- [Chromia CLI](https://docs.chromia.com/intro/installation/)
- [MetaMask Browser Extension](https://chromewebstore.google.com/detail/metamask/nkbihfbeogaeaoehlefnkodbefgpgknn?hl=en)
- [Nuxt.js](https://nuxt.com/docs/getting-started/installation)


## Installation

### 1. Blockchain Setup

First, set up the Chromia blockchain:

In a new terminal

```bash
# Navigate to the blockchain directory
cd backend

# Install Chromia files
chr install

# Start your postgres database (instruction uses inside docker)

dockerd
docker start postgres

# Start the chain
chr node start

```

### 2. Frontend Setup

In a new terminal:

```bash
# Navigate to the frontend directory
cd frontend

# Install dependencies
pnpm install

# install font

pnpm install @vercel/fonts


# Start the development server
pnpm run dev
```

## Usage

1. Open your browser and navigate to `http://localhost:3000`
2. Click "Connect with wallet" to connect with MetaMask or Connect with MetaMask button
3. Sign the authentication transaction when prompted
4. After successful authentication, you'll be redirected to the todo page
5. Start creating and managing your todos!

## Project Structure

```
.
├── frontend/         # Frontend application
│   ├── components/   # Vue components
│   │── pages/        # Vue Pages
│   │── app.vue       # Vue single page application 
│   |__ composables   #  Reusable logic hooks
│   │__ utils         # helper functions
│   └── types         # type definitions 
│       
|__ backend/
|  |__src/ Rell source code
| 
└── README.md
```

## Technology Stack

- **Frontend**
  - Nuxt.js
  - Vue
  - TypeScript
  - Tailwind CSS
  - shadcn/ui

- **Blockchain**
  - Chromia
  - Rell Programming Language
  - PostgreSQL

- **Authentication**
  - MetaMask

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

MIT License

Copyright (c) 2025 Celse13

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

## How It Works

The application works through the following flow:
1. Users connect their MetaMask wallet for authentication
2. Todo data is stored on the Chromia blockchain, ensuring decentralization and data integrity
3. The frontend communicates with the blockchain through the REST API port it will be running on the port number 7740
5. All transactions are signed using MetaMask and recorded on the blockchain

## Additional Information

No Session Storage: Due to time constraints, the app does not store session data, as I was unable to find a solution for persistent sessions. As a result, every time the page is refreshed, users are redirected to the home page. However, the app uses the key stored in local storage to avoid prompting users to reconnect their wallet via the MetaMask extension after a refresh.

Learning and Building in One Week: I joined the program late, leaving me with only one week to learn the Rell language. Despite this, I successfully learned Rell and used it to build this app. In addition to completing the core functionality, I also added extra features beyond the original requirements, showcasing my ability to quickly learn and implement new technologies.


