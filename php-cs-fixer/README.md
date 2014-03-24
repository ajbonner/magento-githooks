# PHP Code Style Fixer Pre-Commit

To use this pre-commit hook, you will need to have [php-cs-fixer.phar](http://get.sensiolabs.org/php-cs-fixer.phar) somewhere in your path.

This pre-commit hook will use php-cs-fixer to inspect each file being commited if it:

    - has a .php extension
    - is inside the local code pool, i.e. app/code/local
    - is not a controller (which do not obey PSR-0 class name -> path conventions)

Qualifying files will be run through php-cs-fixer.phar to check for code style issues. If an issue is found, a diff of suggested changes will be displayed and the fixers that failed listed. The commit will then be aborted.

To force a commit to bypass these checks run git commit with the --no-verify argument.
