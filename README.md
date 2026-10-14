# Satrap Releases

Public distribution of satrap artifacts. The source repositories are
private; everything here can be downloaded without a GitHub login.

| What | Where | Published by |
|---|---|---|
| satrap instance agent (`linux/amd64`, `linux/arm64`, with `.sha256`) | [Releases](https://github.com/basalt79/satrap-releases/releases), tags `agent/v*` | `satrap` CI on an `agent/v*` tag |
| satrap-java-lib (Maven, `0.1.0-SNAPSHOT`) | branch [`maven`](https://github.com/basalt79/satrap-releases/tree/maven) | `satrap-java-lib` CI on every push to `main` |
| Container images | not here – GitHub Container Registry, e.g. `ghcr.io/basalt79/satrap-hello` | the app's CI |

## Agent binary

```
https://github.com/basalt79/satrap-releases/releases/download/agent%2Fv<version>/satrap-agent-linux-<arch>
```

## Maven repository

```xml
<repository>
  <id>satrap-releases</id>
  <url>https://raw.githubusercontent.com/basalt79/satrap-releases/maven</url>
  <snapshots><enabled>true</enabled></snapshots>
</repository>
```

The `maven` branch is rewritten on every publish and keeps only the newest
build of each SNAPSHOT – do not commit to it.
