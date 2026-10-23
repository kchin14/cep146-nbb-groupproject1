# How AI Coding Assistants Are Changing Software Development

**CEP146 group presentation — research notes**  
**Researched:** October 23, 2026  
**Topic:** GitHub Copilot and other AI coding assistants

## Short summary

AI coding assistants are changing software development from *writing all code manually* to *working with AI-generated suggestions and delegating some tasks to AI agents*. Modern tools can suggest code, explain unfamiliar files, write tests, troubleshoot errors, and sometimes edit a repository and open pull requests. They can save time on well-defined work, but their code still needs testing, security checks, and human review. Evidence on productivity is mixed: the result depends on the developer, task, and codebase.

## 1. Main tools

| Tool | What it does | Key distinction |
| --- | --- | --- |
| **GitHub Copilot** | Code completions and chat in development environments; coding agents can take assigned issues, make changes, run checks, and submit pull requests. | Deep GitHub/issue/pull-request integration. |
| **Cursor** | AI-first editor with an agent that searches a codebase, modifies multiple files, and runs commands. | AI assistance integrated into an editor. |
| **Claude Code** | Terminal-based agent that explores repositories, edits files, runs tests/commands, and helps with Git workflows. | Strong emphasis on command-line, repository-wide tasks. |
| **Gemini Code Assist** | IDE chat, code completions, generation, and codebase-aware assistance for supported Google Cloud editions. | Integration with Google development tools and enterprise environments. Note: Google migrated some individual plans to Antigravity in June 2026. |
| **Amazon Q Developer** | Code assistance, explanations, unit tests, and AWS development guidance in supported IDEs. | Particularly useful for AWS-oriented development. |

Tool documentation: [GitHub](https://github.blog/news-insights/product-news/github-copilot-meet-the-new-coding-agent/), [Cursor](https://cursor.com/docs/agent/overview), [Anthropic](https://support.claude.com/en/articles/14553517-claude-code-common-developer-use-cases), [Google](https://docs.cloud.google.com/gemini/docs/codeassist/overview), [AWS](https://docs.aws.amazon.com/amazonq/latest/qdeveloper-ug/q-in-IDE-chat.html).

## 2. Advantages

- **Speed on routine work:** AI can generate boilerplate, small features, repetitive changes, and tests.
- **Learning and onboarding:** Explains unfamiliar syntax, errors, and existing code.
- **Debugging and documentation:** Suggests fixes, unit tests, refactoring, and explanatory comments.
- **Delegation:** Coding agents can handle scoped tasks and propose changes as pull requests while a developer tackles other work.
- **Accessibility:** Natural-language instructions can help less-experienced developers prototype and explore ideas.

## 3. Disadvantages and risks

- **Incorrect output:** Code may compile yet implement the wrong behavior, invent APIs, or fail edge cases.
- **Security:** Generated code can contain vulnerabilities or expose credentials if not checked.
- **Review overhead:** Debugging, integrating, and verifying AI changes can erase the time saved generating them.
- **Privacy, copyright, and licensing:** Uploading confidential source code to a tool may raise governance concerns; code resembling public repositories may raise license questions.
- **Skill erosion and maintenance:** Overreliance may impair learning, and teams must maintain code that nobody fully understands.
- **Variable productivity:** Better results on a short, clear task do not imply better results on every large or mature project.

## 4. Research evidence — use these exact qualifications

1. **Adoption and trust (Stack Overflow 2025):** 84% of survey respondents *used or planned to use* AI tools in their development workflow. This is **not** the same as 84% using them. More respondents distrusted output accuracy (46%) than trusted it (33%); 66% cited solutions that were 'almost right' as a frustration. [Source: 2025 Developer Survey](https://survey.stackoverflow.co/2025/ai)

2. **Faster on one controlled task (Peng et al., 2023):** In a controlled experiment, developers with GitHub Copilot finished a JavaScript HTTP-server implementation **55.8% faster** than the comparison group. This was a specific task, not an all-project speed guarantee. [Study](https://arxiv.org/abs/2302.06590)

3. **Slower for some experienced developers (METR, 2025):** A randomized study of **16 experienced open-source developers working on 246 tasks** found AI availability increased task completion time by **19%** in mature repositories they knew well. Researchers caution against generalizing this result to all developers and settings. [Study](https://arxiv.org/abs/2507.09089)

4. **AI amplifies team practices (Google DORA 2025):** DORA studied nearly 5,000 technology professionals. It described AI as an *amplifier* of existing organizational strengths and weaknesses. Higher AI adoption was associated with greater software delivery throughput and product performance, but also lower delivery stability. These are observed associations, not proof of causation. [Report](https://cloud.google.com/blog/products/ai-machine-learning/announcing-the-2025-dora-report)

5. **Security requires independent checking (SecureVibeBench, ACL 2026):** A peer-reviewed benchmark involving **105 C/C++ tasks** found that even the best agent/model combination produced only **23.8%** solutions that were *both correct and secure* under that benchmark's criteria. This is a benchmark-specific result, not a failure rate for all AI-generated code. [Paper](https://aclanthology.org/2026.acl-long.1107/)

## 5. Recent developments (2025–2026)

- **May 2025 — GitHub Copilot coding agent:** GitHub introduced an agent that accepts issues, works inside GitHub Actions environments, commits code, and opens a pull request for review. [GitHub announcement](https://github.blog/news-insights/product-news/github-copilot-meet-the-new-coding-agent/)
- **February 2026 — Multi-agent workflows on GitHub:** GitHub began supporting Claude and OpenAI Codex alongside Copilot in Agent HQ. [GitHub announcement](https://github.blog/news-insights/company-news/pick-your-agent-use-claude-and-codex-on-agent-hq/)
- **June 2026 — Automatic security validation expanded:** GitHub announced security checks for code produced by third-party coding agents, including CodeQL, dependency checks, and secret scanning. [GitHub changelog](https://github.blog/changelog/2026-06-09-security-validation-for-third-party-coding-agents/)
- **September 2026 — Further workflow integration:** GitHub announced Jira integration for Copilot and experimental multi-model orchestration in its CLI. These are vendor-announced capabilities, not independent effectiveness measurements. [GitHub changelog](https://github.blog/changelog/2026-09-10-github-copilot-weekly-releases-september-7/)

## 6. Suggested speaking segment (approximately 40–50 seconds)

> AI coding assistants such as GitHub Copilot, Cursor, and Claude Code are changing how programmers work. Instead of writing every line themselves, developers can ask AI to suggest code, debug errors, generate tests, and even prepare pull requests. These tools can help, but they are not always faster. One Copilot experiment found a 55.8 percent speed improvement on a specific programming task, while a 2025 study found some experienced developers were 19 percent slower with AI in familiar projects. Security and accuracy also remain concerns. Our conclusion is that AI works best as a tool for developers, with human testing and review before code is accepted.

## 7. Takeaway for the team

**AI coding assistants are shifting developers' jobs toward specifying tasks, evaluating changes, and reviewing automated work — not eliminating the need to understand programming.** Show both the benefits and the limits. Clearly identify whether any statistic comes from a survey, a controlled experiment, or a vendor announcement.

## References

1. Stack Overflow. (2025). *2025 Developer Survey — AI.* https://survey.stackoverflow.co/2025/ai
2. Peng, S., Kalliamvakou, E., Cihon, P., & Demirer, M. (2023). *The Impact of AI on Developer Productivity: Evidence from GitHub Copilot.* https://arxiv.org/abs/2302.06590
3. Becker, J., Rush, N., Barnes, E., & Rein, D. (2025). *Measuring the Impact of Early-2025 AI on Experienced Open-Source Developer Productivity.* https://arxiv.org/abs/2507.09089
4. Google Cloud / DORA. (2025, September 23). *Announcing the 2025 DORA Report.* https://cloud.google.com/blog/products/ai-machine-learning/announcing-the-2025-dora-report
5. Chen, J., et al. (2026). *SecureVibeBench: Benchmarking Secure Vibe Coding of AI Agents via Reconstructing Vulnerability-Introducing Scenarios.* ACL 2026. https://aclanthology.org/2026.acl-long.1107/
6. GitHub. (2025, May 19). *GitHub Copilot: Meet the new coding agent.* https://github.blog/news-insights/product-news/github-copilot-meet-the-new-coding-agent/
7. GitHub. (2026, February 4). *Pick your agent: Use Claude and Codex on Agent HQ.* https://github.blog/news-insights/company-news/pick-your-agent-use-claude-and-codex-on-agent-hq/
8. GitHub. (2026, June 9). *Security validation for third-party coding agents.* https://github.blog/changelog/2026-06-09-security-validation-for-third-party-coding-agents/
9. GitHub. (2026, September 10). *GitHub Copilot weekly releases — September 7.* https://github.blog/changelog/2026-09-10-github-copilot-weekly-releases-september-7/
