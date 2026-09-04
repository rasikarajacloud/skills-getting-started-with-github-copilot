# Getting Started with GitHub Copilot

<img src="https://octodex.github.com/images/Professortocat_v2.png" align="right" height="200px" />

Hey rasikarajacloud!

Mona here. I'm done preparing your exercise. Hope you enjoy! 💚

Remember, it's self-paced so feel free to take a break! ☕️

[![](https://img.shields.io/badge/Go%20to%20Exercise-%E2%86%92-1f883d?style=for-the-badge&logo=github&labelColor=197935)](https://github.com/rasikarajacloud/skills-getting-started-with-github-copilot/issues/1)

## Switch to a branch

```bash
git switch accelerate-with-copilot
```

You are currently on the `main` branch.

To create and publish the branch from `main`, run:

```bash
git switch -c accelerate-with-copilot
git push --set-upstream origin accelerate-with-copilot
```

---

&copy; 2025 GitHub &bull; [Code of Conduct](https://www.contributor-covenant.org/version/2/1/code_of_conduct/code_of_conduct.md) &bull; [MIT License](https://gh.io/mit)

## Bug investigation

If students can register twice for the same activity, check the registration flow for a missing duplicate check and the database for a missing unique constraint on the student/activity pair. Also verify that repeated or concurrent requests are handled idempotently.

Likely source: the registration handler/service function that creates a student activity record, such as `registerForActivity`, `createRegistration`, or `submitRegistration`. The common bug is that it inserts a row without checking whether a matching `(student_id, activity_id)` record already exists, and without enforcing a unique database constraint. For repeated or concurrent requests, also inspect the same function for missing idempotency checks or transaction protection before the insert.

