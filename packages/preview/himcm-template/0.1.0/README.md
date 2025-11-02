# HiMCM Template for Typst

A professional template for the High School Mathematical Contest in Modeling (HiMCM) that creates properly formatted papers with summary sheets and team information.

## Preview

See `main.pdf` for a complete example of the formatted output.

## Features

- **HiMCM Summary Sheet**: Automatically generates the required title page with team control number, problem choice, and year
- **Professional Formatting**: Clean, academic styling based on rubber-article template
- **Page Headers**: Automatic team number and page numbering on all pages
- **Table of Contents**: Auto-generated outline for easy navigation
- **Mathematical Support**: Full Typst math support for equations and formulas
- **Responsive Layout**: Proper margins and spacing for contest requirements

## Installation

### Using Typst Universe (recommended)

```bash
typst init @preview/himcm-template:0.1.0
```

### Manual Installation

1. Download the template files
2. Import the template in your document:
```typst
#import "template.typ": *
```

## Usage

Create a new Typst document and use the template:

```typst
#import "template.typ": *

#show: project.with(
  title: "Your Paper Title",
  abstract: [
    Your abstract text goes here. This should be a concise summary of your solution approach, results, and conclusions.
  ],
  team-number: "12345",
  problem-chosen: "A",
  year: "2025"
)

= Introduction
Your introduction content...

= Problem Analysis
Your analysis content...

= Solution
Your solution content...

= Conclusion
Your conclusion content...
```

## Parameters

The `project` function accepts the following parameters:

- `title`: String - Your paper title
- `abstract`: Content - Abstract text (can be multiple paragraphs)
- `team-number`: String - Your team control number
- `problem-chosen`: String - Problem letter (A, B, C, etc.)
- `year`: String - Contest year
- `body`: Content - Main document content

## Example Output

The template generates:
1. **Summary Sheet**: Title page with team information in red text
2. **Table of Contents**: Auto-generated outline
3. **Main Content**: Professional academic formatting with headers
4. **Page Numbers**: "Page X of Y" format with team number

## Dependencies

- `@preview/rubber-article:0.5.0` - Base article template
- `Libertinus Serif` font (should come preinstalled with typst, falls back to default if unavailable)

## License

MIT License - feel free to use and modify for your HiMCM submissions.

## Contributing

This template is designed specifically for HiMCM contests. If you find issues or have suggestions for improvements, please open an issue or submit a pull request.

## Support

For questions about using this template:
- Check the example in `main.typ`
- Refer to the [Typst documentation](https://typst.app/docs/)
- Join the [Typst Discord](https://discord.gg/2uDybryKPe) for community support
