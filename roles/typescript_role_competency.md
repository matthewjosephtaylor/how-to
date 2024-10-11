# TypeScript Role-Competency

### TypeScript Core Competencies

#### Typing
- **Purpose**: Typing is essential as a form of linting and rapid-feedback testing, providing both quality assurance and clearer communication within the codebase.
- **Efficiency**: Avoid writing extra code. If TypeScript can infer types, prefer that. Minimizing code complexity is key—every line removed reduces potential bugs.
  
#### Generics
- **Appropriate Use**: Generics should be used when necessary, but should often include defaults to avoid requiring explicit specification. Aim for simplicity.
- **Defaults**: Prefer `unknown` over `any` where applicable, as it offers safer handling without sacrificing flexibility.
  
#### Linting & Configuration
- **Continuous Adjustment**: Linting and `tsconfig.json` settings should strike a balance between flexibility and rigidity and be continually adjusted to reflect the evolving needs of the project.

### Platform-Neutral Code
- **Multi-Platform Focus**: Developers should aim to write TypeScript code that is platform-neutral, capable of running across diverse environments, including browsers, Node.js, Cloudflare Workers, Bun, and future platforms.
- **Reusability**: Prioritize writing code that can be reused in different environments. Avoid platform-specific assumptions unless absolutely necessary, and keep code adaptable for various runtimes.
- **Adaptability to Change**: Given the rapid evolution of the JavaScript/TypeScript ecosystem, developers should maintain flexibility, ensuring code remains compatible with new and emerging platforms.

### Error Handling & Reliability

#### Error Handling
- **Situational Handling**: Use the error-handling approach that best fits the situation. Exceptions are effective in most cases, while validation errors may be handled in a functional style, returning either a value or an error.
- **Proactive Testing**: Types, linters, and unit tests should catch bugs early, but runtime errors will still occur and must be handled gracefully within the application.

#### Reliability
- **Balancing Speed & Quality**: Developers should prioritize types and linters for fast, effective feedback during development. Unit and integration tests should be used strategically—target areas where problems are common or expected.
- **Effective Resource Management**: The goal is to balance quality with feature development. Developers must track known bugs and make use of automated auditing tools to monitor problem areas, understanding that not all areas require the same level of attention.
- **Measuring Reliability**: Each project, and even different parts of a project, will have varying quality measures. Developers need to balance resources wisely, knowing when to invest in thorough testing and when to focus on forward momentum.
