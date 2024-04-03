# SvelteKit & Capacitor Mobile App Starter Kit

Welcome to the SvelteKit & Capacitor Mobile App Starter Kit! This kit provides a streamlined setup for building native mobile applications using the power of Svelte for the frontend and Capacitor for the bridge between web technologies and native code.

## Technologies Used

- **Node.js**: JavaScript runtime used for building and running the project.
- **SvelteKit**: SvelteKit is a framework for building fast, highly optimized web applications with Svelte. It offers server-side rendering, routing, and more out of the box.
- **Capacitor**: Capacitor is a cross-platform runtime that allows you to build web applications that run natively on iOS, Android, Electron, and the web.
- **Konsta UI**: The Lib for componets based on IOS and Material Styles.
- **pnpm**: Package managers for installing dependencies and running scripts.
- **TypeScript**: Optional but recommended for statically typed JavaScript.

## Installation

Follow these steps to get started with the project:

1. **Clone the Repository**: 

    ```bash
    git clone https://github.com/anvimaa/capacitor-sveltekit-app.git
    ```

2. **Navigate to the Project Directory**:

    ```bash
    cd app-to-directory
    ```

3. **Install Dependencies**:

    ```bash
    pnpm install
    ```

4. **Add Platforms**:

    ```bash
    npx cap add android
    npx cap add ios
    ```

5. **Sync and Build Capacitor**:

    ```bash
    pnpm build
    npx cap sync
    ```

## Configuration

### SvelteKit Configuration

- **Routes**: Define your routes in the `src/routes` directory. SvelteKit automatically handles routing based on file structure.
- **Layouts**: Layouts are reusable components for wrapping your pages. They are stored in the `src/routes` directory.
- **Stores**: Manage application state using Svelte stores, located in the `src/stores` directory.
- **Components**: Build reusable UI components in the `src/components` directory.

### Capacitor Configuration

- **Platform Configuration**: Each platform (iOS, Android) has its own configuration files located in the respective platform directories (`android`, `ios`).
- **Plugins**: Extend the functionality of your app by adding Capacitor plugins. Install plugins using pnpm and follow the plugin's documentation for usage.
- **Icons and Splash Screens**: Customize the icons and splash screens for your app by replacing the default images located in the `resources` directory.

## Usage

- **Development Mode**: Run the app in development mode with live reloading:

    ```bash
    pnpm run dev
    ```

- **Building for Production**: Build the app for production:

    ```bash
    pnpm run build
    ```

- **Running on iOS/Android**: Run the app on a specific platform:

    ```bash
    npx cap run ios
    npx cap run android
    ```

## Contributing

Contributions are welcome! If you find any bugs or have suggestions for improvement, please open an issue or submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE). Feel free to use and modify it for your own purposes.

---

Happy coding! If you have any questions, feel free to reach out.
