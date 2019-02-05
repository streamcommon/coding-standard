# StreamCommon Team Coding Standard

## Installation
1. Install the module via composer:
    * Console run:
    ```console
        composer require --dev streamcommon/coding-standard
    ```
    * Or add into your `composer.json`:
    ```json
        "require-dev": {
            "streamcommon/coding-standard": "*"
        }
    ```
2. Add composer scripts into your `composer.json`:
   ```json
        "scripts": {
        "cs-check": "phpcs",
        "cs-fix": "phpcbf"
        }
    ```
3. Create file `phpcs.xml`:
    ```xml
        <?xml version="1.0"?>
            <ruleset name="StreamCommon Team Coding Standard">
            <rule ref="./vendor/streamcommon/coding-standard/ruleset.xml"/>
            <file>bin</file>
            <file>config</file>
            <file>lib</file>
            <file>src</file>
            <file>test</file>
        </ruleset>
    ```
## Usage
Run: `composer cs-check` OR `composer cs-fix`

## Customize
See https://github.com/squizlabs/PHP_CodeSniffer/wiki/Annotated-ruleset.xml