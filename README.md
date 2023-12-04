![Anurag's GitHub stats](https://github-readme-stats.vercel.app/api?username=jeonghoonchoi74&show_icons=true&theme=cobalt) ![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=jeonghoonchoi74&layout=compact)


name: Update gist
on:
  push:
    branches:
      - master
  schedule:
    - cron: "0 0 * * *"
jobs:
  update-gist:
    runs-on: ubuntu-latest
    steps:
      - name: Update gist
        uses: maxam2017/productive-box@master
        env:
          GH_TOKEN: ${{ secrets.GH_TOKEN }}
          GIST_ID: ${{ secrets.GIST_ID }}
          TIMEZONE: Asia/Seoul
