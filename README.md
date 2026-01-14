# Animated Card Component with Motion & Tailwind CSS

This project is a React-based demonstration of a dynamic card component. The card uses `motion/react` (a library with a Framer Motion-like API) for animations and is styled with [Tailwind CSS](https://tailwindcss.com/).

## Features

-   **Enter/Exit Animation**: The card gracefully fades and blurs into view when the component mounts, and animates out when closed. This is managed by the `<AnimatePresence>` component.
-   **Content Hover Effect**: The list of items inside the card is initially blurred and becomes clear when the user hovers over the content area, creating a neat focus effect.
-   **Icon Libraries**: Uses icons from both [Lucide React](https://lucide.dev/guide/packages/lucide-react) and [Tabler Icons](https://tabler-icons.io/) to enhance the UI.

## Technologies Used

-   **[React](https://react.dev/)**: For building the user interface.
-   **[Vite](https://vitejs.dev/)**: (Assumed) As the frontend build tool.
-   **[motion/react](https://motion.dev/)**: For the animations.
-   **[Tailwind CSS](https://tailwindcss.com/)**: For all styling.
-   **[Lucide React](https://lucide.dev/)** & **[Tabler Icons](https://tabler-icons.io/)**: For icons.


## Live Demo

[CHECK IT HERE](https://aman-shahi-dev.github.io/card-component-using-framer-motion/)

## How It Works

1.  **State Management**: A React state variable (`open`) is used to control the visibility of the card. Clicking the "Close the Card" button sets this state to `false`.
2.  **`<AnimatePresence>`**: This component from `motion/react` wraps the card. It allows the card to perform an exit animation before it is removed from the DOM.
3.  **Card Animation**: The main `<motion.div>` for the card has `initial`, `animate`, and `exit` props that define the fade-and-blur effect.
4.  **Hover Animation**: A nested `<motion.div>` inside the card contains the feature list. It uses a `whileHover` prop to animate the `opacity` and `filter` from blurred to clear when the mouse is over it.

## Getting Started Locally

To run this project, you'll need a setup with React and Tailwind CSS, likely through Vite.

### Installation

*Note: The following commands are based on a typical Vite project setup, as `package.json` was not provided. You may need to adjust them.*

1.  **Clone the repository** (if you have one).

2.  **Install dependencies**. Your `package.json` should include the following. If not, you can install them manually:
    ```bash
    # For React and Motion
    npm install react react-dom motion

    # For icons
    npm install lucide-react @tabler/icons-react

    # Development dependencies for a Vite + Tailwind project
    npm install -D vite @vitejs/plugin-react tailwindcss postcss autoprefixer
    ```

3.  **Start the development server**:
    ```bash
    npm run dev
    ```

This should start the development server, allowing you to see the component in your browser.
