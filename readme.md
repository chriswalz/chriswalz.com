## Installation

### One time
brew upgrade hugo
git init

git submodule add https://github.com/budparr/gohugo-theme-ananke.git themes/ananke

add theme ananke to config.toml

### Testing

hugo server -D

// for pickles theme\
hugo server -t hugo_theme_pickles -w -D

### Deploy

hugo; firebase deploy
