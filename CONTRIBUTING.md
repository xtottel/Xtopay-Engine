
````md
# Contributing to Xtopay Engine

First off, thank you for taking the time to contribute to **Xtopay Engine** — a project proudly built and maintained by [Xtottel Technologies Ltd](https://xtottel.com).

We welcome meaningful contributions, especially from developers interested in improving Ghana's payment infrastructure. Please take a moment to review this guide before submitting issues or pull requests.

---

## 🧠 Ground Rules

- ❗ **Do not remove or modify license or attribution headers.**
- All contributions must comply with our [MIT License](./LICENSE), **with attribution to Xtottel Technologies Ltd**.
- By submitting a contribution, you certify that your work is original and does not violate the rights of any third party.

---

## 🛠️ How to Contribute

### 1. Fork the Repository

```bash
git clone https://github.com/xtottel/xtopay-engine.git
cd xtopay-engine
````

### 2. Create a Branch

Use a feature- or fix-specific name:

```bash
git checkout -b feat/add-new-momo-connector
```

### 3. Make Your Changes

Please follow the coding structure and file placement guidelines in the `/packages` and `/services` directories.

### 4. Run Tests & Lint

```bash
pnpm test
pnpm lint
```

### 5. Commit Your Changes

Use clear, conventional commit messages:

```bash
git commit -m "feat: added support for G-Money connector"
```

### 6. Push & Open a Pull Request

```bash
git push origin feat/add-new-momo-connector
```

Then open a PR against the `main` branch.

---

## 📁 Repo Structure Summary

* `/packages` – Core engine logic, connectors, shared types
* `/services` – Microservices for transactions, notifications, etc.
* `/infrastructure` – Monitoring, deployment, configs

Please respect this modular structure when submitting code.

---

## ✅ Contribution Checklist

* [ ] Code follows project style and naming conventions
* [ ] Unit or integration tests included (if applicable)
* [ ] README or docs updated for changes
* [ ] No license or attribution headers modified

---

## 💬 Questions or Feedback?

If you're unsure about your contribution or need guidance, contact us:

**Email:** [collins@xtottel.com](mailto:collins@xtottel.com)
**Website:** [https://xtopay.co](https://xtopay.co)

---

Thank you for helping improve financial infrastructure for Ghana and beyond 🇬🇭
— Xtottel Technologies Ltd

```
