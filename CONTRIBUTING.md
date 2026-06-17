# Contributing to Cyber Assassins

Thank you for your interest in contributing! Here's everything you need to know.

## How to Add a Command

1. Open `index.html`
2. Find the `COMMANDS` object in the `<script>` tag
3. Add your command as a method:

```javascript
mycommand(args) {
  if (!args.length) return [cl('mycommand: missing operand', 'out-error')];
  // your logic here
  return [cl('Output', 'out-normal')];
},
```

4. Add a tip in the `TIPS` object:
```javascript
mycommand: 'Explanation of what this command does.',
```

5. Add it to the cheatsheet in the `CHEATSHEET` array:
```javascript
{ cat: 'Category Name', cmds: [
  ['mycommand -flag', 'Short description'],
]}
```

## Color Helper Classes

| Class | Use for |
|---|---|
| `out-normal` | Regular output |
| `out-success` | Successful operations |
| `out-error` | Error messages |
| `out-warn` | Warnings |
| `out-info` | Informational |
| `out-accent` | Highlights |
| `out-dim` | Secondary/muted text |
| `out-dir` | Directory names |
| `out-exec` | Executable file names |

## Pull Request Checklist

- [ ] Command works without errors in Chrome and Firefox
- [ ] Realistic output matching real Linux behavior
- [ ] Edge cases handled (missing args, invalid paths, etc.)
- [ ] Tip added to TIPS object
- [ ] Entry added to CHEATSHEET
- [ ] No external dependencies added

## Ideas for Contributions

- New commands (especially ones cybersecurity students use)
- New themes
- Better error messages
- CTF challenge mode
- Mobile keyboard improvements
- More realistic man pages

---

Made with ❤️ by Shivam
