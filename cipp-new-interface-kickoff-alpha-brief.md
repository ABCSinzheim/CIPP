---
hidden: true
---

# CIPP New Interface Kickoff: Alpha Brief

Thank you for testing our new front end! Since most of you already have a working development environment for the current setup, transitioning to the new interface should be relatively seamless with some adjustments. Let’s dive into what you need to know.&#x20;

***

## Overview&#x20;

The new front-end rewrite, built with [Material UI](https://mui.com/material-ui/getting-started/) and React, introduces significant enhancements in design, performance, and usability. This alpha testing phase focuses on:

* Familiarizing yourself with the new UI navigation.
* Exploring changes and identifying standout issues or features.
* Deferring detailed bug reporting to later phases.

***

## What’s New?&#x20;

1. **Modernized Framework:** Uses Material UI for a cleaner, more consistent design.&#x20;
2. **Performance Improvements:** Faster load times locally and online.&#x20;
3. **Updated Development Workflow:** Minor changes to setup and dependencies.&#x20;

***

## Key Changes&#x20;

#### 1. Framework and Tooling&#x20;

* **Old Frontend:** Built with Vite and CoreUI.&#x20;
* **New Frontend**: Migrates to Next.js and Material-UI.&#x20;
* **State Management**: Introduces React Query for server-side state.&#x20;

#### 2. Package Manager&#x20;

* Switch from `npm` to `Yarn` for dependency management. Yarn ensures consistent installs and faster builds.&#x20;
* Use `yarn install --network-timeout 500000` to avoid timeout errors when downloading dependencies.

#### 3. Routing&#x20;

* **Old**: Used `react-router-dom` for client-side routing.&#x20;
* **New**: Uses `Next.js` file-based routing, simplifying the creation of pages.&#x20;

***

## Known Issues&#x20;

1. **Tooltips and Sorting:** UI quirks like misplaced tooltips or inconsistent sorting behavior.&#x20;
2. **Customizable Filters:** Planned for future iterations.&#x20;
3. **AAD Login Redirect:** Temporarily disabled for easier debugging during development.&#x20;
4. **Navigation Highlighting**: On some pages (e.g., License Report), the menu may highlight the wrong section. This is due to an ongoing update in the navigation paths.

***

## **Next Steps**

1. **Set Up Your Environment**:
   * Follow the instructions in the section below.
2. **Explore the Interface**:
   * Note differences from the current setup.
   * Focus on navigation, new features, and overall usability.
3. **Engage in Discussions**:
   * Use the **New Interface Alpha Testers Unite!!** thread in the `#cipp-dev` channel to share observations or ask questions.
   * Avoid focusing on detailed bug fixes for now.

***

## **Transition from Current Development Environment**

### **Step 1: Switch Branches**

Change both your frontend and backend repositories to the `interface-rewrite` branch:

```bash
git checkout interface-rewrite
git pull
```

### **Step 2: Reinstall Dependencies**

For the new interface:

```bash
yarn install --network-timeout 500000
```

If switching back to the old frontend:

```bash
npm install
```

### **Step 3: Launch the Environment**

To start the new CIPP frontend and API, use the **Launch in Windows Terminal** shortcut from the VSCode debug menu. This task runs both the frontend and API in a separate Windows Terminal instance, avoiding the potential performance issues caused by running both within VSCode itself.

1. Open the CIPP project in **Visual Studio Code**.
2. Go to the **Run and Debug** tab (`Ctrl+Shift+D` or the play icon in the sidebar).
3. Select the task **Launch in Windows Terminal** from the dropdown menu.
4. Click the green **Start Debugging** button or press `F5`.

**Tip for Linux Users**: If "Launch in Windows Terminal" is unavailable, use your terminal or VSCode's integrated terminal to run the frontend and API.

***

## **New Setup for Local Development**

### **Prerequisites**

Install the following tools:

*   **VSCode**:

    ```bash
    winget install --exact vscode
    ```
* **VSCode Extensions**: ESLint, Prettier, Stylelint, Azure Functions, npm Intellisense.
*   **Node.js v18.x LTS**:

    ```bash
    winget install --exact OpenJS.NodeJS.LTS --version 18.20.4
    ```
*   **Yarn**:

    ```bash
    npm install -g yarn
    ```
*   **Azure Static Web Apps CLI**:

    ```bash
    npm install --global @azure/static-web-apps-cli
    ```
*   **Azurite**:

    ```bash
    npm install --global azurite
    ```
*   **Azure Functions Core Tools**:

    ```bash
    npm install --global azure-functions-core-tools@4 --unsafe-perms true
    ```

## **Tips for Development**

*   **Timeouts**: Material UI dependencies can cause timeouts. Use:

    ```bash
    yarn install --network-timeout 500000
    ```
* **GitHub Fork Issues**:
  * If you don’t see the `interface-rewrite` branch, ensure your fork includes it.
  * Alternatively, create a new branch from Kelvin’s repository and set it as your `interface-rewrite` branch.
* If you prefer GUI tools, you can use **GitHub Desktop** to manage branches and fetch remotes. Ensure you fetch all remotes to see the latest branches.

We appreciate your collaboration and look forward to your feedback. Happy testing! 😊&#x20;
