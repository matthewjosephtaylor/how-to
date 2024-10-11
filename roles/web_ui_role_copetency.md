# Web UI Developer Competency

### React-Specific Competencies

- **Functional Components**: Developers should use functional components with the `const export` style for consistency. Typically, one component function per file is preferred, but exceptions can be made if it aids clarity.
- **Component Size**: Aim for component functions that fit on a single page of text in the editor. If a function grows beyond that, consider splitting it into sub-components for better readability.
- **State Management**: Use Zustand for shared state across React and non-React parts of the application, keeping state as simple as possible. React state hooks should be used as needed, with a preference for immutable state, though not strictly enforced.
- **Immer for Complex State**: Prefer using Immer when managing complex state objects for easier state manipulation.
- **Performance Awareness**: Performance is important but should not be the primary focus. Use memos and performance optimizations where applicable, especially since React performance can be a pain-point. Apply known patterns like memoization thoughtfully.

### General UI Design Competencies

- **Responsiveness**: Assume that users will have varying screen sizes and aspect ratios. Designs should adapt fluidly to different devices, with the flexibility to target desktop or mobile where appropriate, but never lock the user into a specific size or shape.
- **Accessibility**: Follow accessibility practices (e.g., WCAG standards) thoughtfully, incorporating them when they make sense. Accessibility isn’t just about meeting the needs of disabled users—it’s about making the application more usable for everyone.
- **Design Patterns & Aesthetics**: A consistent UI design improves both usability and aesthetics. Developers should focus on clean, intuitive interfaces and address any areas that feel cluttered or hard to navigate. The UI should bring joy to users and make the application feel natural to use.
- **Critical Role of UI**: The UI is often how users perceive the entire application, making its role vital. Developers should treat it as the front line of user interaction and give it the high priority it deserves.

### Styling & Theming

- **Theming System**: A robust theming system is required, with a preference for styled components over static CSS. The styling should integrate tightly with the theme system in use.
- **Preferred Frameworks**: MUI is currently the primary focus, with Radix Themes also being used. Developers should work within these frameworks, using their built-in systems for theming and customization rather than overriding them unnecessarily.
- **Consistency Through Themes**: Use the theme system to control the overall look and feel. Custom styles are allowed when necessary but must adhere to consistency and good design principles.
- **Custom Component Wrapping**: If customization is needed, developers should start with the stock components and create a custom wrapper that extends them. These custom components should use the `...rest` pattern to pass down properties, and align closely with the API of the original component, only adding specific functionality where needed.

### Component Architecture & Optimization

- **Composability**: Small, reusable components are preferred. If a component can fit on one page of text, it’s acceptable, but once it grows beyond that, consider refactoring it into sub-components. Only make sub-components reusable once they are needed by at least two components and have proven their value.
- **Refactoring for Clarity**: Be open to refactoring components to improve clarity and reduce complexity. Refactoring should focus on simplifying the codebase without introducing unnecessary overhead.
- **Performance Optimization**: Use tools like `React.memo` and `useMemo` where they make sense, balancing performance gains against added complexity. Performance should be considered from the start, but avoid over-optimizing simple components unnecessarily. Keep in mind that React is known for rendering performance issues, so be proactive but practical.
