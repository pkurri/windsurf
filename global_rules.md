# Global Rules for Windsurf Cascade

## code-quality

- Enforce linting with ESLint using project-specific configurations.
- Achieve at least 80% test coverage for all codebases.
- Optimize code for performance, avoiding unnecessary computations.

## security

- Prohibit hard-coded credentials in source code.
- Use environment variables for sensitive information.
- Implement input validation and sanitization for all user inputs.

## documentation

- Require JSDoc comments for all public functions and classes.
- Maintain an up-to-date `README.md` with project setup instructions.
- Document architectural decisions in a dedicated memory file.

## version-control

- Use Conventional Commits standard for commit messages.
- Prohibit direct commits to the main branch; use pull requests.
- Avoid committing `.env` files or sensitive configuration data.

## performance

- Optimize for minimal resource usage and fast execution.
- Use lazy loading for assets where applicable.
- Monitor and address performance bottlenecks proactively.
