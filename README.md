# Notes in VSCode

This is an example of my note taking strategy in VSCode.

I keep all of my notes as files that are version-controlled and written in Markdown. This allows me to pass the notes to an LLM and have it retrieve things that I ask for.

## Benefits for Application Development and Testing

This note-taking strategy is especially useful for capturing application development and testing commands. By documenting commands such as `curl` and `grpcurl` in Markdown files, you can easily reference and reuse them during development and testing. This ensures that you have a reliable record of the exact commands used, which can be crucial for troubleshooting.

## GitHub Copilot Chat Usage

I use GitHub Copilot as a tool to retrieve information from my notes. By leveraging the capabilities of GitHub Copilot, I can quickly search and extract relevant information from my version-controlled Markdown files. This enhances my productivity and ensures that I can easily access the knowledge I have documented over time.

## Using GitHub Copilot to Update Commands with New Data

One of the powerful features of GitHub Copilot is its ability to assist in updating existing commands with new data. If you have a command documented in your notes and you need to replace old data with new data, GitHub Copilot can help streamline this process.

### Example Scenario

Suppose you have an older `curl` command in your notes:

```bash
curl -X POST https://api.example.com/data -H "Content-Type: application/json" -d '{"key1":"oldValue1","key2":"oldValue2"}'
```

Now, you have new data that you want to use:

```json
{
    "key1": "newValue1",
    "key2": "newValue2"
}
```

Simply by asking Github Copilot Chat for an updated command, it will return the updated command.

With the new data, the updated `curl` command would look like this:

```bash
curl -X POST https://api.example.com/data -H "Content-Type: application/json" -d '{"key1":"newValue1","key2":"newValue2"}'
```

By leveraging GitHub Copilot, you can quickly and accurately regenerate these commands using new data, ensuring that your notes remain useful for your development and testing needs.

## GitHub Copilot Chat Installation

1. **Open VSCode**: Launch Visual Studio Code on your computer.

2. **Access Extensions**: Click on the Extensions view icon on the Sidebar or press `Ctrl+Shift+X` to open the Extensions view.

3. **Search for GitHub Copilot**: In the Extensions view search bar, type `GitHub Copilot`.

4. **Install the Extension**: Find the GitHub Copilot extension in the search results and click the `Install` button.

5. **Sign In to GitHub**: After installation, you will be prompted to sign in to your GitHub account. Follow the on-screen instructions to complete the sign-in process.

6. **Enable GitHub Copilot Chat**: Once signed in, you may need to enable GitHub Copilot Chat specifically. Check the extension settings or documentation for any additional steps required.

7. **Start Using GitHub Copilot Chat**: You can now start using GitHub Copilot Chat by opening a new file or an existing project and interacting with the Copilot Chat features.

For more detailed instructions, refer to the [official GitHub Copilot documentation](https://docs.github.com/en/copilot).

# New Note (VSCode Task)

## Overview
The "New Note" task in Visual Studio Code allows you to quickly create and manage notes directly within the IDE. This task is set up to streamline the process of note-taking, making it efficient and integrated with your development workflow.

## Setup
1. **Configure Tasks**: Add the following configuration to your `tasks.json` file in the `.vscode` directory:
    ```json
    {
        "version": "2.0.0",
        "tasks": [
            {
                "label": "New Note",
                "type": "shell",
                "command": "${workspaceFolder}/new-note.sh",
                "runOptions": {
                    "runOn": "default"
                }
            }
        ]
    }
    ```
2. **Install Optional Extensions**: Optionally, you can install useful extensions such as Markdown All in One. Really, you could do this without any extensions, but I find them useful.

## Usage
1. **Run the Task**: Open the Command Palette (`Ctrl+Shift+P`), type `Run Task`, and select `New Note`.
2. **Edit the Note**: A new file will be created in your workspace. The script will open the file for you within VSCode.

## Script Explanation
- **Command**: The task runs a shell script `new-note.sh` which creates a new directory structure based on the current date and a new Markdown file with a timestamped filename.
- **Label**: The task is labeled as "New Note" for easy identification.
- **Type**: The task type is set to `shell`, indicating it runs a shell command.
- **File Creation**: The script creates a new Markdown file in a directory structure organized by year, month, and day, and opens it in VSCode for editing.

By following these steps, you can efficiently create and manage notes within Visual Studio Code, enhancing your productivity and organization.

# How to create a GitHub Repository from your notes

## Overview

This process outlines the steps to create a new GitHub repository from your local notes. This can be useful to keep your notes in sync with your GitHub repository, or to share your notes with others.

## Steps

1. Create a new repository on GitHub.
2. Clone the repository to your local machine.
3. Copy your notes into the repository.
4. Add and commit your changes.
5. Push your changes to the repository.

## Example

```bash
# Create a new repository
git init

# Add your notes
git add .

# Commit your changes
git commit -m "Initial commit of notes"

# Push your changes to the repository
git push -u origin master
```

## Tips

- Use a consistent naming convention for your repositories to make it easier to find them later.
- Consider adding a README file to your repository to provide an overview of the repository and its contents.

By following these steps, you can easily create a GitHub repository from your local notes and keep them in sync with your development workflow.
