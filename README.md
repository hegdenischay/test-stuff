# click_me on Apple Silicon macOS

This repository runs `click_me` on a GitHub-hosted Apple Silicon macOS 14 runner.

Push to `main`, or open **Actions → Run click_me → Run workflow** to start it manually. Manual runs have an `interactive` option. Turn it on to open an SSH session to the runner. Install the Upterm client on your Mac with `brew install --cask owenthereal/upterm/upterm`, copy the SSH command from the workflow log, and run it in Terminal. In the session, run `cd "$GITHUB_WORKSPACE" && ./click_me`. Exit the shell when you're done.

Interactive access uses your SSH public key registered with GitHub. The runner is temporary and the job has read-only repository permissions. Keep secrets out of this workflow while remote shell access is enabled.

With `interactive` off, the job prints the runner architecture and the binary's Mach-O architectures, runs the binary, and reports its exit status.
