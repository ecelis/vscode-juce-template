# JUCE VS Code Template

This folder contains a template for developing JUCE projects in Visual Studio Code on Linux.

## Configuration

Before you can build and debug the project, you need to configure two settings in the `.vscode/settings.json` file:

1.  `juce.juce_path`: This should be the absolute path to your JUCE folder.

    - **Example**: `"/home/<user>/JUCE"`

2.  `juce.project_name`: This should be the name of your project's executable file, as defined in the Projucer.
    - **Example**: `"MyAwesomePlugin"`

### Example `settings.json`:

```json
{
  // ... other settings
  "juce.juce_path": "/home/<user>/UCE",
  "juce.project_name": "juce1"
  // ... other settings
}
```

## How to Use

### Building the Project

You can build the project using the following VS Code tasks:

- **Build**: Compiles the project. (Ctrl+Shift+B by default)
- **Clean**: Cleans the build files.
- **Make (Debug)**: Compiles the project in debug mode.
- **Clean and Build**: Cleans and then builds the project.

You can run these tasks from the VS Code command palette (Ctrl+Shift+P) by selecting "Tasks: Run Task".

You can also build the project from CLI

```sh
make -C Builds/LinuxMakefile
```

### Debugging

To debug your project, you can use the launch configurations:

- **Make and debug in plugin host**: This will first build the project in debug mode and then launch the debugger. You will need to attach it to a plugin host.
- **Launch Binary**: This will clean and build the project, then launch the debugger on the standalone application.

You can start debugging from the "Run and Debug" panel in VS Code (Ctrl+Shift+D).

### Run

After a successful build your executable will be

```sh
./Builds/LinuxMakefile/build/ninju
```
