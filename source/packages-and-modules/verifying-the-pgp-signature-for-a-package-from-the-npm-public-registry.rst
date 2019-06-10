Verifying the PGP signature of a package from the npm public registry
===========================================================================================

To ensure the integrity of a package version you download from the npm public registry, you can manually verify the PGP signature of the package.

.. note:: Since fully verifying signatures on Keybase requires rechecking proofs (which requires network activity) and is therefore expensive, we recommend only verifying signatures if it is absolutely necessary -- for example, when verifying a deploy artifact, or when initially storing a package in your cache.

Prerequisites
-------------------------------------------------------

Install Keybase from https://keybase.io/download
Create a Keybase account on https://keybase.io
Follow “npmregistry” on Keybase.
Download a local copy of the npm public registry’s public PGP key.

Verifying npm signatures for the public registry
-------------------------------------------------------

.. note:: The following steps use version 1.4.3 of the light-cycle package as an example.
On the command line, fetch the signature for the package version you want and save it in a file:
  $ http GET https://registry.npmjs.org/light-cycle | json "versions['1.4.3'].dist.npm-signature" > sig-to-check
Get the integrity field for that version (example below includes response):
  $ http GET https://registry.npmjs.org/light-cycle | json "versions['1.4.3'].dist.integrity"
Example response:

  sha512-sFcuivsDZ99fY0TbvuRC6CDXB8r/ylafjJAMnbSF0y4EMM1/1DtQo40G2WKz1rBbyiz4SLAc3Wa6yZyC4XSGOQ==
Construct the string that ties the unique package name and version to the integrity string (example below includes response):
  $ keybase pgp verify --signed-by npmregistry -d sig-to-check -m 'light-cycle@1.4.3:sha512-sFcuivsDZ99fY0TbvuRC6CDXB8r/ylafjJAMnbSF0y4EMM1/1DtQo40G2WKz1rBbyiz4SLAc3Wa6yZyC4XSGOQ=='
Example response:

  ▶ INFO Identifying npmregistry
  ✔ <tracked> public key fingerprint: 0963 1802 8A2B 58C8 4929 D8E1 3D4D 5B12 0276 566A
  You last followed npmregistry on 2018-04-10 21:21:57 PDT
  ✔ <tracked> admin of DNS zone npmjs.com: found TXT entry keybase-site-verification=iK3pjpRBkv-CIJ4PHtWL4TTcFXMpPiwPynatKl3oWO4
  ✔ <tracked> "npmjs" on twitter: https://twitter.com/npmjs/status/981288548845240320 [cached 2018-04-12 13:18:31 PDT; but got a retryable error (API network error: Get https://twitter.com/npmjs/status/981288548845240320: net/http: request canceled (Client.Timeout exceeded while awaiting headers) (code=170)) this time around]
  ✔ <tracked> admin of DNS zone npmjs.org: found TXT entry keybase-site-verification=Ls8jN55i6KesjiX91Ck79bUZ17eA-iohmw2jJFM16xc
  Signature verified. Signed by npmregistry 7 minutes ago (2018-04-13 15:00:37 -0700 PDT).
  PGP Fingerprint: 096318028a2b58c84929d8e13d4d5b120276566a.
