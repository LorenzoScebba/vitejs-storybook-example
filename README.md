# ViteJS Storybook example

- Create project with `yarn create vite <name> --template react-ts`
- Run `npx sb init --builder @storybook/builder-vite`
- Delete all extra files created under `src/`
- Run `npm run storybook` or `yarn storybook`

If you need any providers to wrap all stories add the following in `.storybook/preview.jsx`

```jsx
export const decorators = [
    (Story) => (
        <ThemeProvider theme={theme}>
          <Story />
        </ThemeProvider>
    ),
];
```