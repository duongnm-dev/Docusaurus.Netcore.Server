# Contributing to Docusaurus + ASP.NET Core Server

First off, thank you for considering contributing to this project! Your help is greatly appreciated.

## How Can I Contribute?

### Reporting Bugs
If you find a bug, please make sure the bug has not already been reported by searching on GitHub under [Issues](https://github.com/yourname/DocusaurusServer/issues). If you're unable to find an open issue addressing the problem, open a [new one](https://github.com/yourname/DocusaurusServer/issues/new). Be sure to include a clear title, a description of the issue, and steps to reproduce it.

### Suggesting Enhancements
If you have an idea for an enhancement, please open an [issue](https://github.com/yourname/DocusaurusServer/issues/new) to discuss the feature. This allows us to coordinate and ensure it aligns with the project's goals.

### Pull Requests
We welcome pull requests! Please follow these steps to make your contribution:

1.  **Fork the repository** and create your branch from `main`.
2.  **Set up your development environment.** You will need [.NET SDK](https://dotnet.microsoft.com/download) and [Node.js](https://nodejs.org/) installed.
3.  **Make your changes.**
    * For changes to the Docusaurus site, work within the `DocusaurusApp/` directory.
    * For changes to the ASP.NET Core server, work within the `DocusaurusServer.Web/` directory.
4.  **Test your changes.** Run the project locally to ensure everything works as expected:
    ```bash
    dotnet run --project DocusaurusServer.Web
    ```
    The build process will automatically build the Docusaurus app and serve it.
5.  **Commit your changes** with a clear and descriptive commit message.
6.  **Push to your fork** and submit a pull request to the `main` branch of the original repository.
7.  **Describe your changes** in the pull request, referencing any related issues.

## Development Workflow
* Remember that the .NET build process (`dotnet build` or `dotnet run`) is configured to automatically run `npm install` and `npm run build` for the Docusaurus project.
* The output of the Docusaurus build is copied to the `wwwroot` folder in the `DocusaurusServer.Web` project. You should not modify the contents of `wwwroot` directly.

## Code of Conduct
This project and everyone participating in it is governed by the [Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code.

Thank you for your contribution!
