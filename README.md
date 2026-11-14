# CampusNotes

A small browser-based notes app for the VCS CSE25303 Assignment 2. It lets a student create, search and delete notes. Notes are stored in the current browser using `localStorage`.

## Run the project

No package installation is needed.

1. Open `index.html` in a modern browser.
2. Add a title and note, then select **Save note**.
3. Use the search field to filter notes.
4. Select **Delete** to remove a note.

## Git hooks

The team hooks are stored in the tracked `.githooks/` folder.

On Git Bash, from the repository root, run:

```bash
chmod +x .githooks/pre-commit .githooks/commit-msg
git config core.hooksPath .githooks
```

This configures the local clone to use the tracked hooks. Each collaborator must run the configuration command in their own clone.

### Hook checks

- `pre-commit` checks staged file contents for `TODO` or `FIXME`.
- `commit-msg` requires at least 10 characters and one of `feat:`, `fix:`, `docs:`, `refactor:` or `chore:` followed by a description.

To verify the hooks, use the demonstration steps in `docs/assignment2-guide.md`. Do not use `--no-verify` to bypass the checks.

## Assignment integrity

This is a starter project prepared for your own Git workflow. Create your own commits, screenshots, GitHub repository, pull requests and review evidence. Do not present sample output as if it came from a real GitHub action.

## Clone and Push Test
This update was made from the second cloned repository.

## Project Structure

Main entry point: `index.html` (open it in a browser; it loads `app.js` and `styles.css`).

- `index.html` - page layout and form for notes (application entry point)
- `app.js` - note logic: create, search, delete and localStorage handling
- `styles.css` - styling for the app
- `docs/` - assignment guide and demonstration steps (`assignment2-guide.md`)
- `.githooks/` - tracked pre-commit and commit-msg hooks (activate using `git config core.hooksPath .githooks`)
- `.gitignore` - files excluded from version control
