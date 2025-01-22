# thanks
 - https://github.com/dongchengjie/subscription-fetcher
# subscription-fetcher

```yml
jobs:
  dev:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v4

      - name: Fetch subscription files
        uses: dongchengjie/subscription-fetcher@main
        with:
          config: https://example.com/config.json # or yaml
          token: ${{ secrets.GITHUB_TOKEN }}
        #   whitelist: foo,bar
        #   blacklist: foo,bar
```
下面是自用
```
jobs:
  dev:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v4
# 执行任务        
    - name: 执行任务 - Fetch subscription files
      uses: rxsweet/subs-fetcher@main
      with:
        config: /home/runner/work/collectProxy/collectProxy/utils/staticSub/static_config.yaml
        token: ${{ secrets.GITHUB_TOKEN }}
```
