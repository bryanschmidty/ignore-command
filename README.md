# ignore

`ignore` is a small Bash command for managing patterns in a Git repository's local exclude file (`.git/info/exclude`) and for managing files marked with Git's `assume-unchanged` or `skip-worktree` flags.

You can copy the script directly into a single project directory and run it there if you only want it for that repository. If you want to use `ignore` across all of your Git projects, it is recommended to move it into `~/.local/bin` so it is available globally in your shell.

## Install on macOS to `~/.local/bin`

1. Create the local bin directory:

```bash
mkdir -p ~/.local/bin
```

2. Copy this script into your local bin as `ignore`:

```bash
cp ignore ~/.local/bin/ignore
```

3. Make it executable:

```bash
chmod +x ~/.local/bin/ignore
```

4. Ensure `~/.local/bin` is on your `PATH` (zsh):

```bash
echo 'export PATH="$HOME/.local/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc
```

## Verify installation

Run:

```bash
which ignore
```

It should print:

```text
/Users/<your-user>/.local/bin/ignore
```

## Usage

From inside any Git repository:

```bash
ignore
```

If you run it outside a Git repository, it will exit with:

```text
Not inside a git repository.
```

## Contributing

I would love help testing this command on operating systems and platforms other than macOS. If you try it on Linux, Windows (including WSL), or other environments, please share how it worked for you.

If you find bugs or compatibility issues, pull requests with fixes are very welcome.
