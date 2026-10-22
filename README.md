<a id="readme-top"></a>

[![Contributors][contributors-shield]][contributors-url]
[![Stars][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]

<div align="center">
  <h1>BrigadeCraft</h1>
  <p>An educational, from-scratch Java simulation of Minecraft-inspired commands and concepts from Mojang's Brigadier.</p>
  <p><a href="https://github.com/riniwtz/MCCJava">Explore the Source</a> · <a href="https://github.com/riniwtz/MCCJava/issues">Report a Bug</a> · <a href="https://github.com/riniwtz/MCCJava/issues">Request a Feature</a></p>
</div>

> **Status:** This repository currently implements a **console application**. A **JavaFX GUI** is planned, but no JavaFX UI is present in the checked-in code. BrigadeCraft is not an official Mojang/Minecraft product or a drop-in Brigadier replacement.

<details><summary>Table of Contents</summary>

- [About the Project](#about-the-project)
- [Built With](#built-with)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [Roadmap](#roadmap)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)
- [Acknowledgments](#acknowledgments)
</details>

## About the Project

**BrigadeCraft** (formerly **MCCJava**) is an educational recreation of Minecraft-like commands in Java. It models player and world state, command dispatch, arguments and output. The current implementation uses a straightforward command switch rather than Brigadier's full command-tree architecture.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

### Built With

- [Java](https://www.java.com/) — the committed IntelliJ module targets **JavaSE-16**.
- [IntelliJ IDEA](https://www.jetbrains.com/idea/) — IDE configuration is included.
- [JavaFX](https://openjfx.io/) — **intended GUI framework, not yet implemented**.

## Getting Started

### Prerequisites

- JDK 16 or newer (Java 16 is the configured version; newer JDK compatibility has not been verified).
- Git and a terminal, or an IDE such as IntelliJ IDEA.

No Maven or Gradle build configuration exists in the checked-in files. The current console version does not require JavaFX.

### Installation

1. Clone the project:
   ```sh
   git clone https://github.com/riniwtz/MCCJava.git
   cd MCCJava
   ```
2. Compile the sources (macOS/Linux):
   ```sh
   mkdir -p out
   javac -d out $(find MCCJava/src -name '*.java')
   ```
3. Launch the console entry point:
   ```sh
   java -cp out io.github.riniwtz.main.Main
   ```

Alternatively, open the project in IntelliJ IDEA, configure the JDK, and run `io.github.riniwtz.main.Main`.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Usage

Enter a player name of **3–16 characters** that does not begin with `-`. Then enter regular messages or Minecraft-style slash commands.

```text
/help
/gamemode creative
/give
/time
/kill
/quit
```

The dispatcher recognizes these commands, but argument support and behavior differ from Minecraft. Use `/help` to explore the project's supported forms and `/quit` to exit.

## Roadmap

- [x] Create an interactive console-based command simulator
- [x] Add an initial collection of Minecraft-inspired commands
- [ ] Add a JavaFX command-input/output GUI
- [ ] Implement a Brigadier-inspired command tree and argument parsing
- [ ] Improve validation, suggestions, and user-facing errors
- [ ] Add automated tests and a reproducible build system

See [open issues](https://github.com/riniwtz/MCCJava/issues) for ideas and known issues. Unchecked entries are planned directions, not shipped features.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Contributing

Contributions and educational improvements are welcome.

1. Fork the repository.
2. Create a focused branch: `git switch -c feat/command-suggestions`.
3. Implement and test your change.
4. Use [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/), such as `git commit -m "feat(commands): add command suggestions"`.
5. Push the branch and open a pull request.

## License

**No license file is currently present.** No open-source license is implied. Contact the maintainer for reuse or redistribution permissions.

## Contact

**[@riniwtz](https://github.com/riniwtz)** · [Project Repository](https://github.com/riniwtz/MCCJava)

## Acknowledgments

- [Mojang's Brigadier](https://github.com/Mojang/brigadier) — inspiration for command-processing concepts.
- [Minecraft](https://www.minecraft.net/) — inspiration for game commands and world concepts.
- [Best README Template](https://github.com/othneildrew/Best-README-Template) — README structure.

Minecraft and Mojang are trademarks of their respective owners. This is an independent learning project.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

[contributors-shield]: https://img.shields.io/github/contributors/riniwtz/MCCJava.svg?style=for-the-badge
[contributors-url]: https://github.com/riniwtz/MCCJava/graphs/contributors
[stars-shield]: https://img.shields.io/github/stars/riniwtz/MCCJava.svg?style=for-the-badge
[stars-url]: https://github.com/riniwtz/MCCJava/stargazers
[issues-shield]: https://img.shields.io/github/issues/riniwtz/MCCJava.svg?style=for-the-badge
[issues-url]: https://github.com/riniwtz/MCCJava/issues
