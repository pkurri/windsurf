# Windsurf Project Setup

## Project Overview

This repository provides a comprehensive setup for Windsurf Cascade, an AI-powered coding assistant integrated into the Windsurf IDE. It includes configuration files for global rules, project-specific rules, workflows, and memories to enhance development efficiency, prevent AI hallucinations, and maintain project context. The setup is tailored to a project using the following tech stack:

- **Backend**: Node.js v20, Express.js v4.18
- **Frontend**: React v18 with TypeScript, Vite
- **Database**: PostgreSQL v15 with Prisma ORM
- **Testing**: Jest, Cypress

The files are designed to ensure consistent coding standards, automate repetitive tasks, and preserve project knowledge, drawing on best practices from community resources as of 09:30 AM EDT on Thursday, July 24, 2025.

## Setup Instructions

To integrate this setup into your Windsurf environment, follow these steps:

1. **Global Rules**:
   - Copy `global_rules.md` to `~/.codeium/windsurf/memories/global_rules.md` on your system.
   - This file enforces organization-wide standards for code quality, security, documentation, version control, and performance across all projects.

2. **Project Rules**:
   - Place `.windsurfrules` in the root directory of your project.
   - Customize the file to reflect your project’s specific directory structure, technology stack, or coding preferences (e.g., adjust file paths or add new rules).

3. **Workflows**:
   - Create a `windsurf_workflows/` directory in your project root and add `test_and_lint.yaml`.
   - Configure your CI/CD system (e.g., GitHub Actions) to use this workflow, or trigger it manually within Windsurf.
   - Update the script paths in `test_and_lint.yaml` to match your project’s `package.json` commands.

4. **Memories**:
   - Create a `memories/` directory in your project root and add `user_stories.md` and `architectural_decisions.md`.
   - Update these files with project-specific details, such as user requirements or design decisions, and add new memory files as needed (e.g., error logs).

5. **Test and Refine**:
   - Open your project in the Windsurf IDE and use Cascade to verify that it adheres to the rules and executes workflows correctly.
   - Refine the files based on Cascade’s responses and project evolution, ensuring ongoing alignment.

## Usage Tips

- **IDE Integration**:
  - Use Windsurf’s IDE to integrate these configurations, allowing Cascade to provide context-aware code suggestions based on `global_rules.md` and `.windsurfrules`.

- **Workflows**:
  - Trigger the `test_and_lint.yaml` workflow manually or via CI/CD events (e.g., push to `main` branch) to automate testing and linting.
  - Expand workflows to include deployment or code review tasks by creating additional YAML files in `windsurf_workflows/`.

- **Memories**:
  - Regularly update `memories/` files to capture new user stories, architectural decisions, or lessons learned.
  - Use these files to aid onboarding and maintain context across sessions, leveraging the Adaptive Project State (APS) concept from RuleSurf.

- **Adaptive Project State (APS)**:
  - Initialize APS by typing `init` in Cascade’s chat interface to start or resume project work.
  - Save progress with the `save` command to enable auto-reload of context in future sessions.

- **Customization**:
  - Adapt rules, workflows, and memories to your project’s specific needs, addressing potential AI behavior issues (e.g., over-eagerness noted in community feedback) by refining instructions.

## Files Included

| **File/Directory**                | **Location**                          | **Purpose**                                                                 |
|-----------------------------------|---------------------------------------|-----------------------------------------------------------------------------|
| `global_rules.md`                 | `~/.codeium/windsurf/memories/`       | Enforces universal standards for code quality, security, and documentation. |
| `.windsurfrules`                  | Project root                          | Defines project-specific rules for tech stack, structure, and coding standards. |
| `windsurf_workflows/test_and_lint.yaml` | `windsurf_workflows/`            | Automates testing and linting to ensure code quality.                       |
| `memories/user_stories.md`        | `memories/`                           | Documents user stories with acceptance criteria and linked files.            |
| `memories/architectural_decisions.md` | `memories/`                       | Records architectural decisions for context and onboarding.                  |

## Rules and Best Practices

This setup incorporates best practices from community resources:

- **From kinopeee/windsurfrules**: Customize `.windsurfrules` as projects evolve, prioritizing key directories and tech compatibility.
- **From mberman84’s Gist**: Check PRDs, limit files to 300 lines (adjusted to 250 in `.windsurfrules`), write thorough tests, and address Cascade’s eagerness with clear instructions.
- **From shimayuz’s Gist**: Implement strict TypeScript, enforce ESLint, and maintain consistent patterns, adapted for React/Vite.
- **From Engineered Meta-Cognitive Workflow Architecture**: Use a three-layer memory system (Working, Short-Term, Long-Term) and detailed error-handling protocols.
- **From RuleSurf**: Leverage APS for persistent context, keeping project guidance front-and-center.

These rules ensure Cascade provides accurate suggestions, preventing hallucinations by verifying against the codebase and documentation.

## Workflows

- **test_and_lint.yaml**:
  - **Trigger**: Push or pull request to `main` branch.
  - **Steps**: Sets up Node.js v20, installs dependencies, runs ESLint, executes Jest/Cypress tests, and checks coverage.
  - **Customization**: Update script paths or add steps for additional checks (e.g., security scans).

## Memories

- **user_stories.md**: Example entries include user authentication and payment processing, linked to code and tests for traceability.
- **architectural_decisions.md**: Documents choices like using Prisma ORM and Vite, aiding onboarding and design consistency.
- **Maintenance**: Add new files (e.g., `error_logs.md`) and update existing ones regularly to reflect project progress.

## Contributing

- Fork this repository and adapt the files to your project’s requirements.
- Submit pull requests with improvements or additional configurations (e.g., new workflows).
- Share feedback to enhance the Windsurf community’s resources, addressing any observed AI behavior issues.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Resources

- [Windsurf Rules by kinopeee](https://github.com/kinopeee/windsurfrules)
- [Windsurf Rules by mberman84](https://gist.github.com/mberman84/19e184e3a3a4c3a20f32a18af51ce3bc)
- [Windsurf Cascade Rules by shimayuz](https://gist.github.com/shimayuz/ac53a6a84f452c068973092c061889af)
- [Using Windsurf Rules, Workflows, and Memories](https://www.paulmduvall.com/using-windsurf-rules-workflows-and-memories/)
- [Engineered Meta-Cognitive Workflow Architecture](https://github.com/entrepeneur4lyf/engineered-meta-cognitive-workflow-architecture)
- [RuleSurf Framework](https://github.com/akapug/RuleSurf)