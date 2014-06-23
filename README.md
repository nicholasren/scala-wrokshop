### Prepare

##### install sbt
Run `brew install sbt` to install the latest version sbt.
Run `sbt sbtVersion` to verify sbt installed successfully.

##### add sbt idea plugin
Run the following commands to add `sbt-idea` plugin:

```
mkdir -p ~/.sbt/0.13/plugins/
cd ~/.sbt/0.13/plugins/
touch build.sbt
echo "addSbtPlugin(\"com.github.mpeltonen\" % \"sbt-idea\" % \"1.5.2\")" > build.sbt
```

##### generate IDEA project file
run `sbt gen-idea` to generate IDEA project file, then open this project from generated project files.

##### add extra repos
create a file named `repositories` under `~/.sbt`

```
cd ~/.sbt/
touch repositories
```
put the following content to the new file
```
[repositories]
local
osc: http://maven.oschina.net/content/groups/public/
typesafe-release: http://repo.typesafe.com/typesafe/releases/
sonatype-oss-releases
maven-central
sonatype-oss-snapshots
```

