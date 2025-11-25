# Profile Website

This repository contains the source code for Matthijs Liethof's personal profile website, built with [Hugo](https://gohugo.io/) and the [Congo theme](https://jpanther.github.io/congo/).

## About

This site serves as a digital profile and blog for Matthijs Liethof, a self-taught programmer focused on .NET development, devops, and elastic leadership. Matthijs is an organizer at [Nimma.codes](https://nimma.codes) and is passionate about leveraging software to create meaningful impact, building exceptional teams, and sharing insights with the developer community.

## Features
- Personal profile and about page
- Blog posts and articles
- Modern, responsive design using the Congo Hugo theme
- Configurable site parameters and theme options

## Getting Started

### Prerequisites
- [Hugo](https://gohugo.io/getting-started/installing/) (version 0.87.0 or later recommended)
- Go (for theme/module management)

### Installation
1. Clone this repository:
   ```sh
   git clone https://github.com/devmatthijstech/profile.git
   cd profile
   ```
2. Install Hugo and Go if you haven't already.
3. Run the site locally:
   ```sh
   hugo server
   ```
4. Visit `http://localhost:1313` in your browser to view the site.

## Updating
To update the Hugo theme and modules, run:
```sh
hugo mod get -u
```

## Configuration
- Site configuration is in `config/_default/config.toml`.
- Theme and appearance options are in `config/_default/params.toml`.
- Content is organized in the `content/` directory.

## Contributing
This repository is primarily for personal use, but suggestions and improvements are welcome. Feel free to open an issue or submit a pull request.

## License
This project is open source and available under the MIT License.

---

For more information, visit [matthijs.tech](https://www.matthijs.tech/) or connect via [Nimma.codes](https://nimma.codes).
