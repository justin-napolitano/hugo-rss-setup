# hugo-rss-setup

A configuration setup for customizing Hugo's XML output to enhance RSS feeds. This repository provides a tailored RSS template and instructions to extend Hugo's default RSS feed with additional metadata useful for downstream processing.

## Features

- Custom RSS XML template for Hugo posts
- Adds unique post identifiers via Hugo's `.File.UniqueID`
- Includes author metadata (name, email, hashed email) when defined in site parameters
- Provides guidance for integrating the custom RSS template into a Hugo project

## Tech Stack

- Hugo (Static Site Generator)
- XML (RSS feed format)
- Bash (for setup commands)

## Getting Started

### Prerequisites

- Hugo installed on your system
- A Hugo site with a theme that includes an RSS template

### Installation

1. From your Hugo root directory, create necessary directories and copy the RSS template from your theme:

```bash
mkdir -p layouts/posts
cp themes/[theme]/layouts/posts/index.xml layouts/posts/rss.xml
```

2. Replace the copied `rss.xml` with the customized version from this repository or modify it according to the instructions.

3. Customize the RSS template to include additional metadata such as post IDs and author information.

### Running

Build your Hugo site as usual:

```bash
hugo
```

The generated RSS feed will include the custom fields.

## Project Structure

- `index.md` - Documentation and explanation of the RSS customization process.
- `rss.xml` - The customized RSS template for Hugo posts.

## Future Work / Roadmap

- Automate integration of the customized RSS template into Hugo projects.
- Extend support for additional metadata fields as needed.
- Provide examples of consuming the enhanced RSS feed with external tools or databases.
- Add validation and testing for the RSS output to ensure compliance with RSS standards.
