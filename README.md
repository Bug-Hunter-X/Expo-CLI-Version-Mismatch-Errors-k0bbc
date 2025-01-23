# Expo CLI Version Mismatch Errors

This repository demonstrates a common error encountered when using the Expo CLI: version mismatches between the CLI and project dependencies.  Specifically, it highlights issues that can arise when the Expo CLI version is upgraded without updating the associated project packages (e.g., `expo`, `react-native`, etc.).

## How to Reproduce the Bug

1.  Clone this repository.
2.  Install the initial project dependencies (see `package.json`).
3.  Run `expo start` to start the development server.  This should work without issues (at least initially).
4.  Update the Expo CLI to a newer version.  For example, you can run `npm install -g expo-cli@latest`.
5.  Try to run `expo start` again.  You'll likely encounter various build errors or unexpected behavior because of the dependency mismatch.

## How to Fix the Bug

The solution is to update your project dependencies to be compatible with the newer Expo CLI. This is typically done by checking the Expo documentation to find out the compatible versions, and then updating the versions in the project's `package.json` and running `expo install` to fetch the new versions. 

## Additional Notes

* This issue often arises after significant Expo CLI updates.
* Carefully review the release notes for any changes to dependency compatibility.
* Using EAS Build may also trigger these issues if the dependencies are incompatible with the build system.