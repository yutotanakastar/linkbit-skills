# Publish `yutotanakastar/linkbit-skills`

SSH as `yutotanakastar` works locally; the empty GitHub repo must exist first (API create needs a token / browser).

1. Open https://github.com/new  
2. Owner: **yutotanakastar** · Name: **linkbit-skills** · Public · **no** README/gitignore  
3. Create repository  
4. Then push the prepared tree:

```bash
cd /tmp/linkbit-skills-repo   # or: copy from ShortLinks/publish/claude-skill
GIT_SSH_COMMAND='ssh -i ~/.ssh/id_ed25519_yuto -o IdentitiesOnly=yes' \
  git push -u origin main
```

5. Install:

```bash
claude plugin marketplace add yutotanakastar/linkbit-skills
```
