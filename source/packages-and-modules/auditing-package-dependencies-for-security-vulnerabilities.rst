Auditing package dependencies for security vulnerabilities
================================================================

About security audits
---------------------------------------------------------

A security audit is an assessment of package dependencies for security vulnerabilities.
Security audits help you protect your package’s users by enabling you to find and fix known vulnerabilities in dependencies that could cause data loss, service outages, unauthorized access to sensitive information, or other issues.

Running a security audit with npm audit
---------------------------------------------------------

.. note:: The npm audit command is available in npm@6. To upgrade, run npm install npm@latest -g.

The :option:`npm audit` command submits a description of the dependencies configured in your package to your default registry and asks for a report of known vulnerabilities.
:option:`npm audit` checks direct dependencies, devDependencies, bundledDependencies, and optionalDependencies, but does not check peerDependencies.

:option:`npm audit` automatically runs when you install a package with npm install.
You can also run :option:`npm audit` manually on your locally installed packages to conduct a security audit of the package and produce a report of dependency vulnerabilities and, if available, suggested patches.

1. On the command line, navigate to your package directory by typing cd path/to/your-package-name and pressing Enter.
2. Ensure your package contains package.json and package-lock.json files.
3. Type :option:`npm audit` and press Enter.
4. Review the audit report and run recommended commands or investigate further if needed.

Resolving EAUDITNOPJSON and EAUDITNOLOCK errors
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. code-block::

   npm audit requires packages to have package.json and package-lock.json files.

- If you get an EAUDITNOPJSON error, create a package.json file by following the steps in “Creating a package.json file”.
- If you get an EAUDITNOLOCK error, make sure your package has a package.json file, then create the package lock file by running npm i --package-lock-only.

Reviewing and acting on the security audit report
---------------------------------------------------------

Running :option:`npm audit` will produce a report of security vulnerabilities with the affected package name, vulnerability severity and description, path, and other information, and, if available, commands to apply patches to resolve vulnerabilities.
For more information on the fields in the audit report, see “About audit reports”

Security vulnerabilities found with suggested updates
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If security vulnerabilities are found and updates are available, you can either:

- Run the :option:`npm audit` fix subcommand to automatically install compatible updates to vulnerable dependencies.
- Run the recommended commands individually to install updates to vulnerable dependencies.
  (Some updates may be semver-breaking changes; for more information, see “SEMVER warnings”.)

.. figure:: https://docs.npmjs.com/assets/images/packages-and-modules/audit-report-vulns-found-patches.png
   :alt: command line vulnerability table with suggested fix

SEMVER warnings
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If the recommended action is a potential breaking change (semantic version major change), it will be followed by a SEMVER WARNING that says “SEMVER WARNING: Recommended action is a potentially breaking change”.
If the package with the vulnerability has changed its API, you may need to make additional changes to your package’s code.

Security vulnerabilities found requiring manual review
---------------------------------------------------------

If security vulnerabilities are found, but no patches are available, the audit report will provide information about the vulnerability so you can investigate further.

.. figure:: https://docs.npmjs.com/assets/images/packages-and-modules/audit-report-vulns-found-manual-review.png
   :alt: command line audit report requiring manual review

To address the vulnerability, you can

- Check for mitigating factors
- Update dependent packages if a fix exists
- Fix the vulnerability
- Open an issue in the package or dependent package issue tracker

Check for mitigating factors
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Review the security advisory in the “More info” field for mitigating factors that may allow you to continue using the package with the vulnerability in limited cases.
For example, the vulnerability may only exist when the code is used on specific operating systems, or when a specific function is called.

Update dependent packages if a fix exists
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If a fix exists but packages that depend on the package with the vulnerability have not been updated to include the fixed version, you may want to open a pull or merge request on the dependent package repository to use the fixed version.

1. To find the package that must be updated, check the “Path” field for the location of the package with the vulnerability, then check for the package that depends on it.
   For example, if the path to the vulnerability is @package-name > dependent-package > package-with-vulnerability, you will need to update dependent-package.
2. On the npm public registry, find the dependent package and navigate to its repository.
   For more information on finding packages, see “Searching for and choosing packages to download”.
3. In the dependent package repository, open a pull or merge request to update the version of the vulnerable package to a version with a fix.
4. Once the pull or merge request is merged and the package has been updated in the npm public registry, update your copy of the package with npm update.

Fix the vulnerability
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If a fix does not exist, you may want to suggest changes that address the vulnerability to the package maintainer in a pull or merge request on the package repository.

1. Check the “Path” field for the location of the vulnerability.
2. On the npm public registry, find the package with the vulnerability.
   For more information on finding packages, see “Searching for and choosing packages to download”.
3. In the package repository, open a pull or merge request to make the fix on the package repository.
4. Once the fix is merged and the package has been updated in the npm public registry, update your copy of the package that depends on the package with the fix.

Open an issue in the package or dependent package issue tracker
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If you do not want to fix the vulnerability or update the dependent package yourself, open an issue in the package or dependent package issue tracker.

1. On the npm public registry, find the package with the vulnerability or the dependent package that needs an update.
   For more information on finding packages, see “Searching for and choosing packages to download”.
2. In the package or dependent package issue tracker, open an issue and include information from the audit report, including the vulnerability report from the “More info” field.

No security vulnerabilities found
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


If no security vulnerabilities are found, this means that packages with known vulnerabilities were not found in your package dependency tree.
Since the advisory database can be updated at any time, we recommend regularly running :option:`npm audit` manually, or adding npm audit to your continuous integration process.

.. figure:: https://docs.npmjs.com/assets/images/packages-and-modules/audit-report-no-vulns-found.png
   :alt: command line audit report no vulnerabilities found

Turning off npm audit on package installation
---------------------------------------------------------

Installing a single package
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

To turn off :option:`npm audit` when installing a single package, use the --no-audit flag::

   npm install example-package-name --no-audit

For more information, see the npm-install command.

Installing all packages
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

To turn off :option:`npm audit` when installing all packages,
set the audit setting to false in your user and global npmrc config files::

   npm set audit false

For more information, see the npm-config management command and the npm-config audit setting.
