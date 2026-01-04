# Code Challenge 18: React Uses Section

## Getting Started

Install dependencies:

```bash
npm install
```

Start the server on http://localhost:3000:

```bash
npm run dev
```

Run unit tests:

```bash
npm test
```

## Linting & Formatting the Code

```bash
npm run lint
npm run format
```

## Your task

1. Complete the **UsesSection** component: `src/components/UsesSection/UsesSection.jsx`.
2. Style the **UsesSection** component using CSS: `src/components/UsesSection/UsesSection.css`.

### **Component Properties**

Implement the component to accept the props below:

```js
UsesSection.propTypes = {
  items: PropTypes.arrayOf(
    PropTypes.shape({
      groupName: PropTypes.string,
      items: PropTypes.arrayOf(
        PropTypes.shape({
          title: PropTypes.string,
          description: PropTypes.string,
        })
      ),
    })
  ),
};
```

Set default values for the props using `defaultProps`:

```js
UsesSection.defaultProps = {
  items: [],
};
```

### **Component Structure**

The component should render the following structure:

```html

<section class="uses-section">
  <div class="uses-section__content">
    <!-- for each group -->
    <div class="uses-section__group">
      <h2>Workstation</h2>
      <div class="uses-section__group-content">
        <!-- for each item inside the group -->
        <UseCard title="Item title" description="Item description" />
        <!-- ... -->
      </div>
    </div>
    <!-- ... -->
  </div>
</section>

```

### **Component Behavior**

The `UsesSection` component organizes and displays various groups of items with titles and descriptions.

- Iterates through the array of `items` provided as a prop.
- Renders a container for each item group, displaying the group's title and item content.
- Within each group container, iterates through the array of items.
- Renders a `UseCard` component for each item, passing the `title` and `description` as props.
- Supports multiple item groups with unique titles and lists of items.
- Facilitates structured and organized content display.
- Utilizes the `UseCard` component for rendering individual items.
- Promotes code reusability and modularity by separating group rendering logic from item rendering logic.

### Component Styling

Apply CSS styling to the component to ensure it has the appearance described below:

**Uses Section Styles (`uses-section`):**

- `display`: `flex` - Utilized for flexible layout.
- `flex-direction`: `column` - Arranges content vertically within the section.
- `padding`: `32px` - Adds 32 pixels of padding around the section content.

**Uses Section Content Styles (`uses-section__content`):**

- `display`: `flex` - Utilized for flexible layout.
- `flex-direction`: `column` - Arranges content vertically within the section content.
- `row-gap`: `64px` - Adds 64 pixels of vertical gap between rows in the section content.

**Uses Section Group Styles (`uses-section__group`):**

- `display`: `flex` - Utilized for flexible layout.
- `flex-direction`: `row` - Arranges content horizontally within the group.
- `justify-content`: `start` - Aligns content to the start of the horizontal axis.
- `column-gap`: `32px` - Adds 32 pixels of horizontal gap between columns in the group.
- `padding-left`: `16px` - Adds 16 pixels of padding to the left side of the group.
- `border-left`: `2px solid #e0e0e0` - Applies a 2 pixel solid border to the left side of the group with a light gray
  color.

**Uses Section Group Heading Styles (`uses-section__group h2`):**

- `margin`: `0` - Removes margin from the group heading.
- `font-size`: `18px` - Sets the font size of the group heading to 18 pixels.
- `font-weight`: `bold` - Applies bold font weight to the group heading.
- `min-width`: `128px` - Sets the minimum width of the group heading to 128 pixels.

**Uses Section Group Content Styles (`uses-section__group-content`):**

- `display`: `flex` - Utilized for flexible layout.
- `flex-direction`: `column` - Arranges content vertically within the group content.
- `row-gap`: `32px` - Adds 32 pixels of vertical gap between rows in the group content.

---

## Preview

![Preview](https://github.com/Ensign-College/CS220-CC-18/assets/4071288/58c21508-bc9e-4b9c-88a6-375953efbfc7)

