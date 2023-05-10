Validate and visualise dependencies: https://www.npmjs.com/package/dependency-cruiser

```bash
cd awx/ui

npm install --save-dev dependency-cruiser
# To access the dot command for visualization
brew install graphviz

npx depcruise --init
✔ Where do your source files live? … src
✔ Do your test files live in a separate folder? … no
✔ Looks like you're using a 'jsconfig.json'. Use that? … yes
✔ Full path to your 'jsconfig.json › jsconfig.json

  ✔ Successfully created '.dependency-cruiser.js'

# Validate

npx depcruise --config .dependency-cruiser.js src


# Visualize

npx depcruise src --include-only "^src" --config --output-type dot | dot -T svg > dependency-graph.svg

```
