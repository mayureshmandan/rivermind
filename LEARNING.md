# Learning log

One entry per merged PR: the concept behind the change, in plain words.

## 2026-10-05: scaffold the maven project

The Maven wrapper (`mvnw` plus `.mvn/wrapper/maven-wrapper.properties`) pins
the exact Maven version in the repo. Anyone, or any CI runner, gets the same
build tool without installing it, so "works on my machine" problems from
version drift go away. The JUnit BOM (bill of materials) sets one version for
every JUnit module, so they can't drift apart either. CI runs the same
`./mvnw verify` on every pull request, which is what lets main stay green
without anyone pushing to it directly.
