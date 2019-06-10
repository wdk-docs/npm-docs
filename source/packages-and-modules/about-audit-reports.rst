About audit reports
===========================================================================================

About audit reports
Audit reports contain tables of information about security vulnerabilities in your project’s dependencies to help you fix the vulnerability or troubleshoot further.

.. figure:: https://docs.npmjs.com/assets/images/packages-and-modules/audit-report-vuln-table.png
   :alt: command line audit report vulnerability table

Vulnerability table fields
--------------------------------------------------------------------------

- Severity
- Description
- Package
- Patched in
- Dependency of
- Path
- More info

Severity
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The severity of the vulnerability, determined by the impact and exploitability of the vulnerability in its most common use case.

+----------+--------------------------------+
| Severity |       Recommended action       |
+==========+================================+
| Critical | Address immediately            |
+----------+--------------------------------+
| High     | Address as quickly as possible |
+----------+--------------------------------+
| Moderate | Address as time allows         |
+----------+--------------------------------+
| Low      | Address at your discretion     |
+----------+--------------------------------+

Description
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The description of the vulnerability. For example, “Denial of service”.

Package
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The name of the package that contains the vulnerability.

Patched in
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The semantic version range that describes which versions contain a fix for the vulnerability.

Dependency of
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The module that the package with the vulnerability depends on.

Path
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The path to the code that contains the vulnerability.

More info
--------------------------------------------------------------------------

A link to the security report.
