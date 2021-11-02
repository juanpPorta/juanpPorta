### Hi there 👋

<p>#- 🔭 I’m currently working in you hearth</p>
#- 🌱 I’m currently learning 42 madrid 
#- 🤔 I’m looking for help with Proyects
#- 💬 Ask me about anything
name: Generate Datas
<p>[![jaeskim's 42 stats](https://badge42.herokuapp.com/api/stats/jporta)](https://github.com/JaeSeoKim/badge42)</p>
on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"
  workflow_dispatch:

jobs:
  build:
    name: Jobs to update datas
    runs-on: ubuntu-latest
    steps:
      # Snake Animation
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: rafaballerini
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
  
