---
title: Server.Import.RegistryHunter
hidden: true
tags: [Server Artifact]
---

This artifact will import the latest Registry Hunter artifact.

To read more about the Registry Hunter, see
https://registry-hunter.velocidex.com/


<pre><code class="language-yaml">
name: Server.Import.RegistryHunter
description: |
  This artifact will import the latest Registry Hunter artifact.

  To read more about the Registry Hunter, see
  https://registry-hunter.velocidex.com/

type: SERVER

required_permissions:
- SERVER_ADMIN

sources:
  - query: |
      SELECT * FROM Artifact.Server.Import.ArtifactExchange(
         ExchangeURL="https://registry-hunter.velocidex.com/Windows.Registry.Hunter.zip",
         Prefix="")

</code></pre>

