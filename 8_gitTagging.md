# Git Tagging
---
## Key Commands for Tagging

- `git tag <tagname>` - Create a lightweight tag
- `git tag -a <tagname> -m "message"` - Create an annotated tag
- `git tag <tagname> <commit-hash>` - Tag a specific commit
- `git tag` - List tags
- `git show <tagname>` - Show tag details

---

## What is a Tag?

A **tag in Git is like a label or bookmark for a specific commit.

Tags are most often used to mark important points in your project history, like release (`v1.0` or `v2.0`).

Tags are a simple and reliable way to keep track of versions and share them with your team or users.

Some common tag types include:

- **Releases**: Tags let you mark when your project is ready for release, so you (and others) can always find that exact version later.
- **Milestones**: Use tags to highlight major milestones, like when a big feature is finished or a bug is fixed.
- **Deployment**: Many deployment tools use tags to know which version of your code to deploy.
- **Hotfixes**: If you need to fix an old version, tags make it easy to check out and patch the right code.

---

## Create a Lightweight Tag

A lightweibht tag is just a name for a commit.

It's quick and simple, but does not store extra information.

### Annotated vs Lightweight tags

- **Annotated Tag**: Stores author, dat, and message.<br>
Recommended for releases and sharing with others.
- **Lightweight Tag**: Just a simple name for a commit (no extra info, like a bookmark)

```sh
Example:

git tag v1.0
```

---

## Create an Annotated Tag (`-a -m`)

An annotated tag stores your name, the date, and a message.

This is recommended for most uses.

```sh
Example:

git tag -a v1.0 -m "Version 1.0 release"
```

---

## Tag a Specific Commit

You can tag an older commit by specifying its hash:

```sh
Example:

git tag v1.1 1a2b3c4d
```

---

## List tags

See all tags in your repo:

```sh
git tag
```

---

## Show Tag Details (`git show`)

See details about a tag and the commit it points to:

```sh
Example:

git show v1.0
```

---

## Push Tags to Remote

By default, tags exist only on your local computer.

If you want others to see your tags, you need to push them to your remote repo.

If you don't push your tags, only you will see them, and only locally.

To push a single tag to your remote repo (for example, after creating a release tag):

```sh
Example: Push a Single Tag

git push origin v1.0
```

> **Did you know?** Pushing commits with `git push` does <u>not</u> push your tags!
>
> YOu must push tags explicitly as shown above.

To push **all** your local tags to the remote at once (useful if you've created several tags):

```sh
Example: Push All Tags

git push --tags
```

---

## Delete Tags

Delete a tag locally:

```sh
Example:

git tag -d v1.0
```

Delete a tag from the remote repo:

```sh
Example:

git push origin --delete tag v1.0
```
---

## Update or Replace a Tag (Force Push)

If you need to move a tag to a different commit and update the remote, use `--force`:

```sh
Example:

git tag -f v1.0 <new-commit-has>

git push --force origin v1.0
```

---

## Tagging Best Practices

- Use tags to mark releases, major milestones, or stable points in your project.
- Always use **annotated tags** (with `-a` `-m`) for anything public or shared.
- Create tags after passing all tests or before deploying/releasing code.

---

## Troubleshooting

- **Tag already exists?** Use `git tag -d <tagname>` to delete it, then re-create.
- **Pushed the wrong tag?** Delete it locally and remotely, then push the correct tag.
- **Tag not showing on remote?** Remember to push tags with `git push origin <tagname>` or `git push --tags`.
- **Need to overwrite a tag on the remote?** You can force-push a tag with `git push --force origin <tagname>`, but be careful! This will overwrite the tag for everyone using the remote.