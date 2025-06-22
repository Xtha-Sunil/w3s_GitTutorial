
## 🔖 Git Tagging

A **tag** in Git is like a label or bookmark pointing to a specific commit. Tags are often used to mark important points in a project's history, such as a release (`v1.0`, `v2.0`, etc.).

---

### 🎯 Use Cases
- **Release:** Mark when your project is ready for release so you can easily find that version later.
- **Milestone:** Highlight major milestones like feature completion or bug fixes.
- **Deployment:** Many deployment tools use tags to identify which version of code to deploy.
- **Hotfixes:** Tag specific versions that need fixes or patches.

---

### 🏷️ Types of Tags
- **Annotated Tag:**  
  Stores metadata like the tagger's name, email, date, and a message.  
  ➤ Recommended for public releases.

- **Lightweight Tag:**  
  A simple name pointer to a commit (no metadata).  
  ➤ Acts like a bookmark.

---

### 🧰 Git Tagging Commands

1. **Create a lightweight tag**
   ```bash
   git tag v1.0
   ```

2. **Create an annotated tag**
   ```bash
   git tag -a v1.0 -m "Version 1.0 release"
   ```

3. **Tag an older commit**
   ```bash
   git tag v1.0 <commit-hash>
   ```

4. **List all tags**
   ```bash
   git tag
   ```

5. **Push tags to remote**  
   (Note: `git push` does **not** push tags by default.)
   ```bash
   git push --tags
   ```

6. **Delete tags**
   - **Locally:**
     ```bash
     git tag -d <tag_name>
     ```
   - **From remote:**
     ```bash
     git push --delete origin <tag_name>
     ```

7. **Update a tag to a new commit**
   ```bash
   git tag -f v1.0 <new-commit-hash>
   git push --force origin v1.0
   ```
