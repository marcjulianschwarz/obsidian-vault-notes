```
git clone --filter=blob:none--no-checkout https://github.com/raycast/extensions
cd extensions
git sparse-checkout set --cone extensions/gif-search
git checkout main
```
