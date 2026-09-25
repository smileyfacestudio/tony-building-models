# Sava — English setup

[Русская версия](START-HERE.ru.md) · [Project home](../README.md)

## 1. Get the project

Open [the public repository](https://github.com/smileyfacestudio/tony-building-models). No SFS organization membership is needed to read it.

For a quick start without Git, choose **Code → Download ZIP**, extract the archive, and keep the extracted folder on your computer. This gives you a working copy but not Git history or a direct update/push workflow.

For ongoing collaboration, use GitHub Desktop to clone the repository by its URL, or, if Git is already installed, run:

```sh
git clone https://github.com/smileyfacestudio/tony-building-models.git
cd tony-building-models
```

GitHub's [cloning guide](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository) covers both desktop and command-line options.

## 2. Open your copy in Codex

Use your own existing Codex setup and sign in with your own account. In the desktop app, add/open the extracted or cloned `tony-building-models` folder as a local project and start a task there. If your app has a ChatGPT/Codex selector, choose Codex for repository work. If you use the Codex CLI or IDE extension, open the same local folder there instead.

If you need installation or sign-in help, follow the [official OpenAI quickstart](https://learn.chatgpt.com/docs/quickstart). Interface labels can differ by version. No SFS vault access, shared account, API key, Node.js install, or app build is needed for this document/template phase. Do not share your login with anyone.

## 3. Give your agent this first task

Copy this prompt into your Codex task:

```text
I am Sava, the hardware consultant on this SFS project. Speak Russian with me
unless I ask for English. Read AGENTS.md, README.md, docs/project-brief.md,
docs/capture-guide.md and docs/data-dictionary.md.

First summarize what exists, what is missing, and what is not yet verified.
Ask me up to five practical questions about the work areas and electrical /
networking scope for CV255 and NC3007. Help me prepare a site-survey checklist
and the structure of a preliminary estimate. Do not invent dimensions,
concealed wiring, quantities, prices, or compliance conclusions.

This is a PUBLIC repository. Do not request sensitive photos or site details
in a public issue. Before saving actual site data, ask me to confirm an approved
private working location. Keep public templates empty; do not commit or publish
site evidence, client pricing, private links, or secrets. Do not push, invite
anyone, contact third parties, or change repository visibility without my request.
```

## 4. Your first deliverable

Start with one property and identify:

1. Which floors, suites, and areas are actually in scope.
2. What is existing versus requested: outlets, circuits, data drops, Wi-Fi, racks, pathways, or other systems.
3. Which plans, photos, videos, and measurements are still needed.
4. What you can price from evidence versus what needs a survey, test, allowance, or exclusion.
5. Your proposed first-pass estimate structure, without invented prices or quantities.

Read the [capture guide](capture-guide.md) before any site visit. The blank CSV files in `templates/` can be copied into approved private working storage and opened in Excel, a spreadsheet editor, or Codex. Keep their column names and IDs unchanged. Do not fill the public copies with real site data.

## 5. Share work safely

- To read/download, just use the link. No invitation is needed.
- To contribute public-safe changes directly, send Boris your GitHub username privately. He can invite you to this repository with Write access; an invitation has not been sent as part of this starter.
- Once access is active, make a branch such as `sava/intake-checklist`, review the exact changes, and open a pull request for SFS review. Do not push directly to `main`.
- Keep actual site media, layouts, pricing, and client details in the agreed private workspace. A private folder on your computer is not automatically synchronized with Boris. Agree on how to transfer it before sending it.
- Access to this project does not grant SFS vault access. Vault onboarding comes later.

**Done for day one:** the project opens in your Codex, your agent understands both property IDs and the public boundary, you have identified the first missing inputs, and Boris knows your GitHub username if you need Write access.
