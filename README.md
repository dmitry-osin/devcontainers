# Development Containers

A collection of pre-configured VS Code Dev Containers for various programming languages and technologies, all based on minimal Debian images.

## Author

**Dmitry Osin** <d@osin.pro>

## Available Containers

### Programming Languages

#### Clojure
- **Location**: `clojure/`
- **Configuration**: 
  ```
  https://github.com/dmitry-osin/devcontainers/blob/main/clojure/.devcontainer/devcontainer.json
  ```
- **Relative Configuration**: 
  ```
  /clojure/.devcontainer/devcontainer.json
  ```
- **Features**: Clojure CLI tools, OpenJDK 17, oh-my-zsh
- **Extensions**: Calva, Clojure
- **Settings**: Format on save enabled
- **Tools**: Clojure CLI, rlwrap for better REPL experience

#### Deno
- **Location**: `deno/`
- **Configuration**: 
  ```
  https://github.com/dmitry-osin/devcontainers/blob/main/deno/.devcontainer/devcontainer.json
  ```
- **Relative Configuration**: 
  ```
  /deno/.devcontainer/devcontainer.json
  ```
- **Features**: Latest Deno, oh-my-zsh
- **Extensions**: Deno extension
- **Settings**: Deno enabled with linting

#### .NET Core
- **Location**: `dotnet/`
- **Configuration**: 
  ```
  https://github.com/dmitry-osin/devcontainers/blob/main/dotnet/.devcontainer/devcontainer.json
  ```
- **Relative Configuration**: 
  ```
  /dotnet/.devcontainer/devcontainer.json
  ```
- **Features**: Latest .NET SDK, oh-my-zsh
- **Extensions**: C# Dev Kit, C# extension, .NET Runtime, Blazor WASM Companion
- **Settings**: Roslyn analyzers enabled, EditorConfig support, format on save, organize imports
- **Tools**: .NET CLI, C# compiler, NuGet package manager

#### Elixir
- **Location**: `elixir/`
- **Configuration**: 
  ```
  https://github.com/dmitry-osin/devcontainers/blob/main/elixir/.devcontainer/devcontainer.json
  ```
- **Relative Configuration**: 
  ```
  /elixir/.devcontainer/devcontainer.json
  ```
- **Features**: Latest Elixir, Erlang/OTP, Mix package manager, Hex, Rebar, oh-my-zsh
- **Extensions**: ElixirLS, Elixir extension, Elixir formatter
- **Settings**: Auto-formatting on save, ElixirLS language server enabled
- **Tools**: Elixir compiler, Mix build tool, Hex package manager, Rebar build tool

#### FASM (Assembly)
- **Location**: `assembly/fasm/`
- **Configuration**: 
  ```
  https://github.com/dmitry-osin/devcontainers/blob/main/assembly/fasm/.devcontainer/devcontainer.json
  ```
- **Relative Configuration**: 
  ```
  /assembly/fasm/.devcontainer/devcontainer.json
  ```
- **Features**: FASM (Flat Assembler), GDB debugger, GCC compiler, build tools, oh-my-zsh
- **Extensions**: x86-64 Assembly language support, ASM code lens, Assembly extension, C++ tools
- **Settings**: FASM file associations (.asm, .inc, .fasm), tab size configuration
- **Tools**: FASM assembler, GDB debugger, GCC/G++ compiler, GNU binutils, Make, linker

#### Go
- **Location**: `go/`
- **Configuration**: 
  ```
  https://github.com/dmitry-osin/devcontainers/blob/main/go/.devcontainer/devcontainer.json
  ```
- **Relative Configuration**: 
  ```
  /go/.devcontainer/devcontainer.json
  ```
- **Features**: Latest Go, oh-my-zsh
- **Extensions**: Go extension, Go nightly
- **Settings**: Go modules enabled, goimports formatter, golangci-lint, format on save
- **Tools**: goimports, golangci-lint

#### Java
Multiple JDK versions available:
- **JDK 8**: `java/jdk8/`
  - **Configuration**: 
    ```
    https://github.com/dmitry-osin/devcontainers/blob/main/java/jdk8/.devcontainer/devcontainer.json
    ```
  - **Relative Configuration**: 
    ```
    /java/jdk8/.devcontainer/devcontainer.json
    ```
- **JDK 11**: `java/jdk11/`
  - **Configuration**: 
    ```
    https://github.com/dmitry-osin/devcontainers/blob/main/java/jdk11/.devcontainer/devcontainer.json
    ```
  - **Relative Configuration**: 
    ```
    /java/jdk11/.devcontainer/devcontainer.json
    ```
- **JDK 17**: `java/jdk17/`
  - **Configuration**: 
    ```
    https://github.com/dmitry-osin/devcontainers/blob/main/java/jdk17/.devcontainer/devcontainer.json
    ```
  - **Relative Configuration**: 
    ```
    /java/jdk17/.devcontainer/devcontainer.json
    ```
- **JDK 21**: `java/jdk21/`
  - **Configuration**: 
    ```
    https://github.com/dmitry-osin/devcontainers/blob/main/java/jdk21/.devcontainer/devcontainer.json
    ```
  - **Relative Configuration**: 
    ```
    /java/jdk21/.devcontainer/devcontainer.json
    ```

Each includes:
- Microsoft OpenJDK
- Java extension pack
- Gradle and Maven support
- Spring Boot tools
- oh-my-zsh

#### MASM (Assembly)
- **Location**: `assembly/masm/`
- **Configuration**: 
  ```
  https://github.com/dmitry-osin/devcontainers/blob/main/assembly/masm/.devcontainer/devcontainer.json
  ```
- **Relative Configuration**: 
  ```
  /assembly/masm/.devcontainer/devcontainer.json
  ```
- **Features**: NASM assembler (Linux alternative to MASM), GDB debugger, build tools, oh-my-zsh
- **Extensions**: x86-64 Assembly language support, ASM code lens, C++ tools
- **Settings**: Assembly file associations, tab size configuration
- **Tools**: NASM assembler, GDB debugger, GNU binutils, Make
- **Note**: MASM (Microsoft Macro Assembler) is Windows-specific. This container uses NASM (Netwide Assembler) as a Linux-compatible alternative with similar syntax.

#### NASM (Assembly)
- **Location**: `assembly/nasm/`
- **Configuration**: 
  ```
  https://github.com/dmitry-osin/devcontainers/blob/main/assembly/nasm/.devcontainer/devcontainer.json
  ```
- **Relative Configuration**: 
  ```
  /assembly/nasm/.devcontainer/devcontainer.json
  ```
- **Features**: NASM assembler, GDB debugger, GCC compiler, build tools, oh-my-zsh
- **Extensions**: x86-64 Assembly language support, ASM code lens, Assembly extension, C++ tools
- **Settings**: NASM file associations (.asm, .s, .S, .inc), tab size configuration
- **Tools**: NASM assembler, GDB debugger, GCC/G++ compiler, GNU binutils, Make, linker

#### Node.js
- **Location**: `nodejs/`
- **Configuration**: 
  ```
  https://github.com/dmitry-osin/devcontainers/blob/main/nodejs/.devcontainer/devcontainer.json
  ```
- **Relative Configuration**: 
  ```
  /nodejs/.devcontainer/devcontainer.json
  ```
- **Features**: Node.js LTS, npm, oh-my-zsh
- **Extensions**: ESLint, Prettier, Tailwind CSS, TypeScript
- **Settings**: Auto-formatting on save, ESLint auto-fix

#### Python
- **Location**: `python/`
- **Configuration**: 
  ```
  https://github.com/dmitry-osin/devcontainers/blob/main/python/.devcontainer/devcontainer.json
  ```
- **Relative Configuration**: 
  ```
  /python/.devcontainer/devcontainer.json
  ```
- **Features**: Latest Python, pip, oh-my-zsh
- **Extensions**: Python, Pylance, Black formatter, isort, Flake8, mypy
- **Tools**: Black, isort, Flake8, mypy for code quality

#### Ruby
- **Location**: `ruby/`
- **Configuration**: 
  ```
  https://github.com/dmitry-osin/devcontainers/blob/main/ruby/.devcontainer/devcontainer.json
  ```
- **Relative Configuration**: 
  ```
  /ruby/.devcontainer/devcontainer.json
  ```
- **Features**: Latest Ruby, Bundler, Gem package manager, oh-my-zsh
- **Extensions**: Ruby extension, Solargraph language server, RuboCop linter, rdbg debugger
- **Settings**: Auto-formatting on save, RuboCop formatter, Solargraph language server enabled
- **Tools**: Ruby interpreter, Bundler dependency manager, Gem package manager

#### Rust
- **Location**: `rust/`
- **Configuration**: 
  ```
  https://github.com/dmitry-osin/devcontainers/blob/main/rust/.devcontainer/devcontainer.json
  ```
- **Relative Configuration**: 
  ```
  /rust/.devcontainer/devcontainer.json
  ```
- **Features**: Latest Rust toolchain, rust-analyzer, LLDB debugger, oh-my-zsh
- **Extensions**: rust-analyzer, vscode-lldb, crates

#### Scala
- **Location**: `scala/`
- **Configuration**: 
  ```
  https://github.com/dmitry-osin/devcontainers/blob/main/scala/.devcontainer/devcontainer.json
  ```
- **Relative Configuration**: 
  ```
  /scala/.devcontainer/devcontainer.json
  ```
- **Features**: Scala 3.3.1, sbt 1.9.7, Java 17, Coursier, oh-my-zsh
- **Extensions**: Scala extension, Scala debug adapter
- **Settings**: Scala language server enabled
- **Tools**: Scala compiler, sbt build tool, Coursier package manager

#### Solidity
- **Location**: `solidity/`
- **Configuration**: 
  ```
  https://github.com/dmitry-osin/devcontainers/blob/main/solidity/.devcontainer/devcontainer.json
  ```
- **Relative Configuration**: 
  ```
  /solidity/.devcontainer/devcontainer.json
  ```
- **Features**: Node.js LTS, Solidity compiler (solc), Hardhat framework, oh-my-zsh
- **Extensions**: Hardhat Solidity, Solidity extension, ESLint, Prettier
- **Settings**: Auto-formatting on save, Prettier formatter for Solidity
- **Tools**: solc compiler, Hardhat development framework, npm package manager

#### Zig
- **Location**: `zig/`
- **Configuration**: 
  ```
  https://github.com/dmitry-osin/devcontainers/blob/main/zig/.devcontainer/devcontainer.json
  ```
- **Relative Configuration**: 
  ```
  /zig/.devcontainer/devcontainer.json
  ```
- **Features**: Latest Zig, oh-my-zsh
- **Extensions**: Zig language support
- **Settings**: Zig path configured, ZLS (Zig Language Server) support

## Common Features

All containers include:
- **Base Image**: Minimal Debian-based image
- **Shell**: zsh with oh-my-zsh
- **User**: vscode (non-root)
- **Workspace**: Mounted at `/workspace`

## Usage

1. Open the desired container folder in VS Code
2. Press `F1` or `Ctrl+Shift+P` (Windows/Linux) / `Cmd+Shift+P` (Mac)
3. Select **"Dev Containers: Reopen in Container"**
4. VS Code will build and start the container
5. Wait for the container to be ready and extensions to install

## Requirements

- [Docker](https://www.docker.com/) installed and running
- [VS Code](https://code.visualstudio.com/) with the [Dev Containers extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributing

Feel free to submit issues, fork the repository, and create pull requests for any improvements.
