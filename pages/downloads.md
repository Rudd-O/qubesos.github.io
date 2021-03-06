---
layout: default
title: Downloads
permalink: /downloads/
redirect_from:
- /doc/releases/
- /en/doc/releases/
- /doc/QubesDownloads/
- /wiki/QubesDownloads/
---

Before You Download...
----------------------

-   [System Requirements](/doc/system-requirements/)
-   [Hardware Compatibility List](/hcl/)
-   [Supported Versions](/doc/supported-versions/)
-   [Version Scheme](/doc/version-scheme/)
-   [How to Verify Signatures](/doc/verifying-signatures/)
-   [Installation Security Considerations](/doc/install-security/)
-   [Qubes OS License](/doc/license/)
-   [Qubes OS Source Code](/doc/source-code/)

{% for release in site.data.downloads.releases %}

{{ release.name }}
-------------------------------------

<table class="table">
  <thead>
    <tr>
      <th>Source</th>
      <th>Download</th>
      <th><a href="/doc/verifying-signatures/"
             title="How to verify the authenticity of your download">Verifiers</a> ⚠</th>
    </tr>
  </thead>
  <tbody>
    {% for sourcedata in release.sources %}
    {% assign source_name = sourcedata[0] %}
    {% assign source = sourcedata[1] %}
    <tr>
      <td><em><a href="https://{{ source_name }}/">{{ source_name }}</a></em> ({{ source.method }})</td>
      <td><a href="{{ source.url }}">{{ source.filename }}</a> ({{ source.type }})</td>
      <td>
        {% for verifier in source.verifiers %}
          ◇ <a href="{{ verifier[1] }}">{{ verifier[0] }}</a>
        {% endfor %}
      </td>
    </tr>
    {% endfor %}
  </tbody>
</table>

<ul>
  {% for docdata in release.docs %}
  {% assign doc_name = docdata[0] %}
  {% assign doc = docdata[1] %}
  {% assign featured = doc.featured | default: "no" %}
  <li>
    <a href="{{ doc.url }}">{{ doc_name }}</a>
    {% if featured != "no" %} ☚{% endif %}
  </li>
  {% endfor %}
</ul>

{% endfor %}

Qubes Live USB (alpha)
----------------------

**Warning: Live USB edition is older than recent 3.1 release and lack some of
its features (and bug fixes). If you want newest available image, download 3.1
installation image. You can install it on a second USB stick**

-   [**Qubes-R3.1-alpha1.1-x86_64-LIVE.iso**](https://mirrors.kernel.org/qubes/iso/Qubes-R3.1-alpha1.1-x86_64-LIVE.iso)
      [[sig](https://mirrors.kernel.org/qubes/iso/Qubes-R3.1-alpha1.1-x86_64-LIVE.iso.asc)]
      [[key](https://keys.qubes-os.org/keys/qubes-release-3-signing-key.asc)]
      [[?](/doc/verifying-signatures/)]
      (mirrors.kernel.org)
-   [**Qubes-R3.1-alpha1.1-x86_64-LIVE.iso**](https://ftp.qubes-os.org/iso/Qubes-R3.1-alpha1.1-x86_64-LIVE.iso)
      [[sig](https://ftp.qubes-os.org/iso/Qubes-R3.1-alpha1.1-x86_64-LIVE.iso.asc)]
      [[key](https://keys.qubes-os.org/keys/qubes-release-3-signing-key.asc)]
      [[?](/doc/verifying-signatures/)]
      (ftp.qubes-os.org)

-   [**Usage Guide**](/doc/live-usb/)

Qubes Release 2
---------------------------------------

(This is an old release. We strongly recommend using Qubes 3.0 or higher.)

-   [**Qubes-R2-x86_64-DVD.iso**](https://mirrors.kernel.org/qubes/iso/Qubes-R2-x86_64-DVD.iso)
      [[hash](https://mirrors.kernel.org/qubes/iso/Qubes-R2-x86_64-DVD.iso.DIGESTS)]
      [[sig](https://mirrors.kernel.org/qubes/iso/Qubes-R2-x86_64-DVD.iso.asc)]
      [[key](https://keys.qubes-os.org/keys/qubes-release-2-signing-key.asc)]
      [[?](/doc/verifying-signatures/)]
      (mirrors.kernel.org)
-   [**Qubes-R2-x86_64-DVD.iso**](https://ftp.qubes-os.org/iso/Qubes-R2-x86_64-DVD.iso)
      [[hash](https://ftp.qubes-os.org/iso/Qubes-R2-x86_64-DVD.iso.DIGESTS)]
      [[sig](https://ftp.qubes-os.org/iso/Qubes-R2-x86_64-DVD.iso.asc)]
      [[key](https://keys.qubes-os.org/keys/qubes-release-2-signing-key.asc)]
      [[?](/doc/verifying-signatures/)]
      (ftp.qubes-os.org)

-   [**Installation Guide**](/doc/installation-guide/)
-   [Release Notes](/doc/releases/2.0/release-notes/)
-   [Upgrading to Qubes R2](/doc/releases/2.0/release-notes/#upgrading)

Qubes Release 1
---------------

(This is an old release. We strongly recommend using Qubes 3.0 or higher.)

-   [**Qubes-R1-x86_64-DVD.iso**](https://mirrors.kernel.org/qubes/iso/Qubes-R1-x86_64-DVD.iso)
      [[hash](https://mirrors.kernel.org/qubes/iso/Qubes-R1-x86_64-DVD.iso.DIGESTS)]
      [[sig](https://mirrors.kernel.org/qubes/iso/Qubes-R1-x86_64-DVD.iso.asc)]
      [[key](https://keys.qubes-os.org/keys/qubes-release-1-signing-key.asc)]
      [[?](/doc/verifying-signatures/)]
      (mirrors.kernel.org)
-   [**Qubes-R1-x86_64-DVD.iso**](https://ftp.qubes-os.org/iso/Qubes-R1-x86_64-DVD.iso)
      [[hash](https://ftp.qubes-os.org/iso/Qubes-R1-x86_64-DVD.iso.DIGESTS)]
      [[sig](https://ftp.qubes-os.org/iso/Qubes-R1-x86_64-DVD.iso.asc)]
      [[key](https://keys.qubes-os.org/keys/qubes-release-1-signing-key.asc)]
      [[?](/doc/verifying-signatures/)]
      (ftp.qubes-os.org)

-   [**Installation Guide**](/doc/installation-guide/)
-   [Release Notes](/doc/releases/1.0/release-notes/)

Mirrors
-------

Qubes ISOs are available from the following mirrors:

-   [Burnbit torrent](http://burnbit.com/search?q=qubes)
-   [mirrors.kernel.org](https://mirrors.kernel.org/qubes/iso/)
