# Example/Test case for combined DocC archive rendering with GitHub Pages

To replicate this:

- clone the Swift Package Manager repo locally 

In my example, it's sourced from `/Users/joeheck/src/swift-project/swiftpm`

- configure the repo to display GitHub pages
  - deployed from the `main` branch in the `docs` subdirectory

```bash
cd /Users/joeheck/src/swift-project/swiftpm

export DOCC_JSON_PRETTYPRINT=YES
swift package --disable-sandbox generate-documentation \
  --enable-experimental-combined-documentation \
  --enable-mentioned-in \
  --enable-experimental-external-link-support \
  --target PackageManagerDocs \
  --target PackageDescription \
  --target PackagePlugin \
  --hosting-base-path swiftpm-docc-repo-example \
  --transform-for-static-hosting \
  -o /Users/joeheck/src/swiftpm-docc-repo-example/docs
```

Using GitHub pages, the combined Content is available from:

- https://heckj.github.io/swiftpm-docc-repo-example/documentation

Specific archives combined:
  - https://heckj.github.io/swiftpm-docc-repo-example/documentation/packagemanagerdocs
  - https://heckj.github.io/swiftpm-docc-repo-example/documentation/packageplugin
  - https://heckj.github.io/swiftpm-docc-repo-example/documentation/packagedescription



