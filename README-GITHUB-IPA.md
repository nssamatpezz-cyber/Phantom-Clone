# Youtube Phantom Clone — build IPA with GitHub Actions

## Upload to GitHub
1. Create a new empty repository on GitHub.
2. Extract this ZIP and upload/commit the **contents** of this folder to the repository root (the `.github` folder must be included).
3. Open the repository's **Actions** tab. If prompted, enable workflows.
4. Run **Build iOS IPA** using **Run workflow**, or push a commit to `main`.
5. When the run finishes successfully, open the run and download the artifact named `Youtube_Phantom_clone-unsigned-ipa`.

## Important
This workflow creates an **unsigned IPA**. It is useful as a build artifact, but normally cannot be installed directly on a physical iPhone without signing/provisioning. For installation on a real iPhone, configure Apple signing (Apple Developer account, certificate and provisioning profile) or use an appropriate sideloading workflow. Do not upload signing certificates or private keys into the repository; use GitHub Actions Secrets.

The project uses SwiftUI, Xcode, and the Kingfisher Swift Package. The workflow resolves dependencies and builds on a macOS GitHub-hosted runner.
