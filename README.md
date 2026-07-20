# Coding Projects Hub

A single static page that acts as the home base for all my coding projects — live apps link out, local-only builds just show what they are and where they live. No build step, no dependencies: everything is in `index.html`.

## Editing the project list

Open `index.html`, find the `PROJECTS` array at the top of the `<script>` block, and add/remove/edit entries. Each entry:

```js
{
  name: 'Project Name',
  type: 'live' | 'local' | 'research',
  category: 'PWA',                       // small pill next to the badge
  description: 'One or two sentences.',
  tags: ['nodejs', 'react'],
  url: 'https://...',                    // live only — leave '' for "link coming soon"
  locked: true,                          // live only — shows 🔒 password-protected
  localPath: 'D:\\...',                  // local/research only
  runCmd: 'npm run dev',                 // local only
}
```

Then commit and push — GitHub Pages redeploys automatically:

```powershell
git add index.html
git commit -m "Update projects"
git push
```

## Rules

- This repo contains **only this page** — never any source code from the projects it lists.
- No dependencies, no npm, no global installs. If tooling is ever needed, keep it inside this folder.
