# SocialStar Technical Assessment

Welcome to the SocialStar technical assessment! This is a basic tech check to ensure you can work with our EmberJS-based technology stack. Please follow the steps below carefully.

## Prerequisites

- Node.js installed on your system
- Basic familiarity with command line/terminal
- Text editor of your choice

## Instructions

### Step 1: Install EmberJS (Skip if already installed)

If you already have EmberJS installed, you can skip to Step 2.

```bash
npm install -g ember-cli
```

### Step 2: Create Project Directory

Create a new empty directory for this project:

```bash
mkdir socialstar-assessment
cd socialstar-assessment
```

### Step 3: Initialize Ember Application

Initialize a new Ember application in your directory:

```bash
ember init
```

### Step 4: Install ember-tribe Package

Install our custom ember-tribe package which includes our complete tech stack (including Bootstrap):

```bash
yes | ember install ember-tribe
```

**Note:** This command will install all repositories from our technology stack, including Bootstrap which you'll use in the following steps.

### Step 5: Update Styles

Replace the content of `app/styles/app.scss` with the provided style code:

1. Navigate to `app/styles/app.scss`
2. Remove all existing code from the file
3. Copy and paste the complete SCSS code provided below

<details>
<summary>Click to expand SCSS code</summary>

```scss
@import url("https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap");
@import url("https://fonts.googleapis.com/css?family=Permanent+Marker");

$font-family-sans-serif: "Poppins", sans-serif !default;
$display-font-family: "Poppins", sans-serif !default;
$enable-rounded: true !default;
$enable-negative-margins: true !default;

// scss-docs-start gray-color-variables
$white: #fff !default;
$gray-100: #f9f6f4 !default;
$gray-200: #e9e7e2 !default;
$gray-300: #d9d7d5 !default;
//$gray-400: #ced4da !default;
$gray-500: #adaaa2 !default;
$gray-600: #9ea3b1 !default;
$gray-700: #5b6073 !default;
$gray-800: #393938 !default;
//$gray-900: #212529 !default;
$black: #000 !default;
// scss-docs-end gray-color-variables

$blue: #58a7f8 !default;
$indigo: #6610f2 !default;
$purple: #a273c6 !default;
$pink: #d63384 !default;
$red: #ff7550 !default;
$orange: #ffab3e !default;
$yellow: #ffce00 !default;
$green: #45b99f !default;
$teal: #20c997 !default;
$cyan: #0dcaf0 !default;
$purple-100: #dac7e8 !default;
$purple-300: #f8f1ff !default;
$orange-100: #fff0df !default;
$orange-300: #ffdbb3 !default;

// scss-docs-start theme-color-variables
$primary: $green !default;
$secondary: $orange !default;
$success: $green !default;
$info: $blue !default;
$warning: $orange !default;
$danger: $red !default;
$light: $gray-100 !default;
$dark: $gray-800 !default;
// scss-docs-end theme-color-variables

// scss-docs-start theme-colors-map
$theme-colors: (
  "primary": $primary,
  "secondary": $secondary,
  "success": $success,
  "info": $info,
  "warning": $warning,
  "danger": $danger,
  "light": $light,
  "dark": $dark,
  "primary-lighter": $purple-300,
  "primary-light": $purple-100,
  "secondary-lighter": $orange-300,
  "secondary-light": $orange-100,
) !default;
// scss-docs-end theme-colors-map

$aspect-ratios: (
  "1x1": 100%,
  "4x3": calc(3 / 4 * 100%),
  "3x5": calc(5 / 3 * 100%),
  "1x2": calc(2 / 1 * 100%),
  "2x3": calc(3 / 2 * 100%),
  "16x9": calc(9 / 16 * 100%),
  "9x16": calc(16 / 9 * 100%),
  "10x16": calc(16 / 10 * 100%),
  "21x9": calc(9 / 21 * 100%),
);

$spacer: 1rem !default;
$spacers: (
  0: 0,
  1: $spacer * 0.25,
  2: $spacer * 0.5,
  3: $spacer,
  4: $spacer * 1.5,
  5: $spacer * 3,
  6: $spacer * 4.5,
  7: $spacer * 6,
  8: $spacer * 7.5,
  9: $spacer * 9,
  10: $spacer * 12,
) !default;

$border-radius: 0.5rem !default;
$border-radius-sm: 0.25rem !default;
$border-radius-lg: 0.75rem !default;
$border-radius-xl: 1rem !default;
$border-radius-2xl: 1.25rem !default;
$border-radius-pill: 50rem !default;
$small-font-size: 0.78em !default;
$sub-sup-font-size: 0.6em !default;
$input-btn-padding-y: 0.5rem !default;
$input-btn-padding-x: 1rem !default;
$input-btn-padding-y-sm: 0.37rem !default;
$input-btn-padding-x-sm: 0.75rem !default;
$input-btn-padding-y-lg: 0.64rem !default;
$input-btn-padding-x-lg: 1.2rem !default;
$btn-border-radius: $border-radius-lg !default;
$btn-border-radius-sm: $border-radius-sm !default;
$btn-border-radius-lg: $border-radius-lg !default;
$body-bg: $white !default;
$body-color: $gray-800 !default;
$dropdown-link-color: $gray-800 !default;
$list-group-color: $gray-800 !default;
$input-border-color: $gray-300 !default;
$min-contrast-ratio: 3 !default;
// $modal-fade-transform: scale(.9);
$modal-fade-transform: translateY(50%);
$themeColor: var(--bs-primary) !default;

@import "node_modules/bootstrap/scss/bootstrap";
@import "node_modules/animate.css/animate";
@import "ember-power-select/themes/bootstrap";
@import "ember-power-select";

html {
  background-color: var(--bs-gray-200);
  overscroll-behavior-y: none;
}

html,
body {
  -webkit-user-select: none; /* Chrome all / Safari all */
  -moz-user-select: none; /* Firefox all */
  -ms-user-select: none; /* IE 10+ */
  user-select: none; /* Likely future */
  -webkit-touch-callout: none;
}

body {
  overscroll-behavior-y: auto;
}

.header a {
  color: var(--bs-dark);
}

.header a.active {
  color: var(--bs-success);
}

a:focus {
  outline: none !important;
}

img {
  pointer-events: none;
}

button:focus,
a:focus {
  outline: none;
  box-shadow: none;
}
```

</details>

### Step 6: Edit the Index Template

Navigate to `app/templates/index.hbs` and remove the `<WelcomeFlame />` component.

### Step 7: Add SocialStar Logo

Add the SocialStar logo at the top of your page, center-aligned:

```html
<div class="text-center">
  <img src="https://mvp.socialstar.co/favicon.png" alt="SocialStar Logo" class="mb-4">
</div>
```

### Step 8: Implement Bootstrap Accordion

Below the logo, add a Bootstrap accordion component. Use the sample code from the [Bootstrap 5.3 Accordion documentation](https://getbootstrap.com/docs/5.3/components/accordion/).

**Example accordion structure:**

```html
<div class="accordion" id="accordionExample">
  <div class="accordion-item">
    <h2 class="accordion-header">
      <button class="accordion-button" type="button" data-bs-toggle="collapse" data-bs-target="#collapseOne">
        Accordion Item #1
      </button>
    </h2>
    <div id="collapseOne" class="accordion-collapse collapse show">
      <div class="accordion-body">
        Your content here...
      </div>
    </div>
  </div>
  <!-- Add more accordion items as needed -->
</div>
```

### Step 9: Build and Submit

Build your project using one of the following commands:

```bash
ember build --dev
```

or the npm equivalent:

```bash
npm run build
```

**Submission:** Once the build is complete, locate the generated `dist` folder in your project directory and send it to us for review.

## Expected Deliverable

- A working Ember application with:
  - SocialStar logo displayed at the top (center-aligned)
  - Bootstrap accordion component implemented below the logo
  - Custom styling applied from the provided SCSS
  - Clean, professional layout

## Questions or Issues?

If you encounter any problems during this assessment, please document them and include your troubleshooting steps in your submission.

Good luck! 🚀
