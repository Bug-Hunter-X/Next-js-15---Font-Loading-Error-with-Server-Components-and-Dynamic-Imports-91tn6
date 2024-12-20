# Next.js 15 Font Loading Issue with Server Components and Dynamic Imports

This repository demonstrates a subtle bug in Next.js 15 related to font loading when using the `next/font` API with server components and dynamic imports.  The issue arises when a font, dynamically imported within a server component, isn't properly loaded within a client component due to timing issues.

## Problem

The `bug.js` file shows a scenario where a server component dynamically imports a Google font using `next/font`. When this server component is rendered within a client component, the font may not load correctly, resulting in missing styles.

## Solution

The `bugSolution.js` demonstrates a solution that utilizes `async/await` within the client component to explicitly await the font loading before rendering the server component. This ensures the font is ready before it is used, preventing the styling issue.

## How to Reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run `npm run dev`.
4. Observe the potential font loading issue on the page.