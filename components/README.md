# Components Directory

This directory contains React components for the Top Finanzas website. The components are organized by function and purpose.

## Directory Structure

- `/forms` - Form components
- `/layout` - Layout components (header, footer, etc.)
- `/mdx` - MDX-related components for blog rendering
- `/ui` - Reusable UI components

## Layout Components

### Blog Layout (`/layout/blog-layout.tsx`)

Main layout component for blog pages. It includes:

- Header and footer
- Blog post metadata display (title, author, date, etc.)
- Social sharing buttons
- Sidebar with recent articles, categories, and newsletter signup
- Advertisement placeholders

Usage:

```tsx
<BlogLayout metadata={postMetadata}>
  {/* Blog content */}
</BlogLayout>
```

## MDX Components

### Blog Post (`/mdx/blog-post.tsx`)

Component for rendering individual blog posts. It takes post metadata and content as props and renders them using the BlogLayout component.

Usage:

```tsx
<BlogPost metadata={postMetadata}>
  {compiledMdxContent}
</BlogPost>
```

### Blog Layout (MDX Version) (`/mdx/blog-layout.tsx`)

A simplified version of the blog layout used for rendering MDX content in the blog section. It includes:

- Header and footer
- Content area
- Sidebar with recent articles, categories, and newsletter signup

## UI Components

The `/ui` directory contains reusable UI components for the site. These follow a consistent pattern and are generally based on the shadcn/ui component library.

### Key UI Components

- **AdPlaceholder** (`/ui/ad-placeholder.tsx`) - Component for displaying advertisement placeholders
- **Button** (`/ui/button.tsx`) - Reusable button component
- **Card** (`/ui/card.tsx`) - Card component for displaying content in a container
- **Image-related components** - Components for displaying images with rounded corners and animations

## Modifying Components

When modifying components, consider the following guidelines:

1. **Maintain consistency**: Keep styles consistent with the rest of the site.
2. **Preserve functionality**: Ensure that components continue to work as expected.
3. **Use Tailwind classes**: The project uses Tailwind CSS for styling.
4. **Responsive design**: Ensure components work well on all screen sizes.

### Image Components

All image components should include the `rounded-xl` class for consistent styling. When creating or modifying image containers, ensure they also have this class.

## Adding New Components

When adding new components:

1. Create a new file in the appropriate subdirectory
2. Use the existing component pattern as a guide
3. Export the component so it can be imported elsewhere
4. Add appropriate JSDoc comments for better developer experience
