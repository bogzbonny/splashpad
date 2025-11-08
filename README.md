# Splashpad

TUI rust playground using your `$EDITOR` of choice.

 - actually change the working directory when working on a project https://doc.rust-lang.org/std/env/fn.set_current_dir.html
    - then change back after close https://doc.rust-lang.org/std/process/struct.Command.html#method.get_current_dir
 - righthand, commandline terminal
 - lefthand: Editor with upper buttons zone:
    - upper: 
       - the name in cool text "splashpad"
       - textbox: a name for the test 
       - a toggle between main.rs and cargo.toml 
         - these two should actually be seperate neovim instances probably. 
       - button: a RED run button 
         - dropdown to change between: Run, Build, Test, Check
           - ideally this would be a new type of dropdown which is just a
             button with a popup selector like in the actual playground
           - could just be a button which opens up a right-click-menu
       - button: a cargo add button with two text fields for name and @ version
       - dropdown "mode" either: debug, or release
       - dropdown "rust-version" either: stable, or nightly (don't bother with
         beta chanel for now)
         - cargo +nightly run
    - When there isn't an editor there should be the project selector in the
      lefthand side. 
       - project list starts at the top
       - a list of names, when highlighting over each name, the main code
         should preview on the righthand side in a bat pane. 
       - when creating a new project use no git so that the whole splashpad dir 
         does not have git submodules. 
           cargo init --vcs=none my_project

### Setup 

```
cargo install splashpad
```
 - recommended to set up the ~/.config/splashpad/projects dir as a git repo
 - projects dir: ~/.config/splashpad/projects/
 - config dir: ~/.config/splashpad/config.toml

### Usage

```
// open the tui to select/create a project
splash

// creates a new empty test project 
splash my-test-proj

// creates a new empty test project with some cargo imports
splash my-test-proj tokio crossterm 

// push all the splash projects to the git remote (if remote is setup)
splash push
```

### Others Similar Projects
 - https://sr.ht/~k1nkreet/rsplay/ 
 - https://github.com/Frank-III/ra-monaco-astro
