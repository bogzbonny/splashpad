
# splashpad

TUI rust playground using your $EDITOR of choice

  - store everything in a ~/.splashpad folder ?
  - store everything in ~/config/splashpad/   ?
  - could check a ~/.config/splashpad.toml config file for possible
    alternative locations to the splashpad folder.
  - command: splash or spl ?
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

### Others

  - https://sr.ht/~k1nkreet/rsplay/ 
  - https://github.com/Frank-III/ra-monaco-astro
