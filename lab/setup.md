# Workshop Setup

To complete this workshop you will need Visual Studio 2026, the .NET 10 SDK, and a GitHub account with access to GitHub Copilot.

## Prerequisites

Before starting, ensure you have:

- **Visual Studio 2026** with the GitHub Copilot extension installed
- **.NET 10 SDK** installed
- **GitHub account** with one of the following:
  - [GitHub Copilot Free](https://github.com/features/copilot) - Free tier with limited usage
  - [GitHub Copilot Pro](https://github.com/features/copilot) - Full access (30-day free trial available)
  - GitHub Copilot through your organization

> [!TIP]
> If you don't have GitHub Copilot yet, you can [sign up for Copilot Free](https://github.com/features/copilot) or start a [free trial of Copilot Pro](https://github.com/github-copilot/signup).

## Install .github + MCP Extension

Before we begin, let's install the .github + MCP extension for Visual Studio. This extension provides access to GitHub MCP servers which we will use later in the lab.

1. [] Open Visual Studio 2026
1. [] Go to **Extensions -> Manage Extensions**
1. [] Search for **.github + MCP** in the search box
1. [] Click **Install** on the **.github + MCP** extension by Mads Kristensen
1. [] Restart Visual Studio if prompted

> [!TIP]
> You can also install this extension from the [Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=MadsKristensen.GitHubNode). The .github + MCP extension is important because it provides the Node.js runtime required by some MCP servers, which you'll use in Part 9 of this lab.

## Sign in to GitHub Copilot

1. [] Open your browser and go to `https://github.com`.
1. [] Sign in with your GitHub account or create a new account if you don't have one.
1. [] Open Visual Studio 2026.
1. [] Select **Continue without code**. If prompted to sign-in, you can click Close.
1. [] Click the Copilot icon on the top bar (left side next to the search input box).
1. [] Click **Sign in to use Copilot**.
1. [] A browser window will open prompting you to sign in to GitHub and authorize Visual Studio and Copilot. Complete the sign-in and click **Authorize** when prompted.
1. [] When the browser shows the confirmation, click **Open** to return to Visual Studio.
1. [] After setup you should see the **GitHub Copilot Walkthrough** tab and the Copilot button should be green.

> [!NOTE]
> For the hands-on lab exercises that create or modify repository data via cloud agents (Part 12), you'll need to fork the lab repo into your own account. This gives the cloud agent permissions to operate on your fork.

## Turn on Copilot Settings

1. [] Ensure Code Completions and Next Edit Suggestions are enabled:
   - Go to the Code Completions settings in Visual Studio by heading to **Tools -> Options -> Text Editor -> Inline Suggestions -> General** under Suggestion Providers
   - Ensure **Copilot Completions** is checked.
   - Ensure **Copilot Next Edit Suggestions** is checked.

   ![](./images/0-enable-nes.png)

1. [] Head to **Tools -> Options -> GitHub -> Copilot -> Copilot Chat** and ensure the following settings are enabled:
   - **Enable Agent mode in chat pane**
   - **Enable MCP server integration in agent mdoe**
   - **Enable Planning**
   - **Enable Ask Question**
   - **Enable View Plan Execution**
   - **Enable Cloud agent (Preview)**
   - **Enable custom instructions**

1. [] Head to **Tools -> Options -> GitHub -> Editor** and ensure the following settings are enabled:
   - **Enable AI generated description for auto-inserted documentation comments in support languages**

## Clone Lab Repository

For the full experience—especially if you plan to delegate tasks to cloud agents or allow Copilot to create issues and push changes—fork the repository to your own GitHub account and clone your fork.

1. [] In your browser, go to `https://github.com/dotnet-presentations/visual-studio-github-copilot-lab` and click **Fork** to create a fork under your GitHub account.
1. [] In Visual Studio, click **File -> Clone Repository**.
1. [] Enter the URL of your fork (for example `https://github.com/<your-username>/visual-studio-github-copilot-lab`) and press **Clone**.

If you prefer not to fork, you can still clone the upstream repository directly:

1. [] In Visual Studio, click **File -> Clone Repository**.
1. [] Enter `https://github.com/dotnet-presentations/visual-studio-github-copilot-lab` and press **Clone**.

The code is now opened in Visual Studio. Feel free to take a look at it or skip to the next section to start the app.

## Start the App

1. [] Open the **Solution Explorer** from the **View -> Solution Explorer** menu.
1. [] Set the **TinyShop.AppHost** as the startup project if it isn't already by right-clicking on **TinyShop.AppHost** and selecting **Set as Startup Project**. Start the project with F5 or **Debug -> Start Debugging** from the menu.

    The [Aspire](https://aspire.dev) AppHost will start two applications and the  Aspire Dashboard:

    - The backend .NET app on **https://localhost:7130/api/Product**
    - The frontend Blazor app on **https://localhost:7085** - You can see the app by opening that URL from the dashboard

1. [] Stop debugging and close the application.

## Summary and Next Steps

You've now set up your environment and cloned the repository you'll use for the rest of the workshop. Let's start exploring GitHub Copilot!

---

[Next: Part 00 - Exploring the Codebase](./part00-exploring-codebase.md)
