# Upgrade project React Quick Poll to v1.21.1

Date: 07/07/2025

## Findings

Following is the list of steps required to upgrade your project to SharePoint Framework version 1.21.1. [Summary](#Summary) of the modifications is included at the end of the report.

### FN001001 @microsoft/sp-core-library | Required

Upgrade SharePoint Framework dependency package @microsoft/sp-core-library

Execute the following command:

```sh
npm i -SE @microsoft/sp-core-library@1.21.1
```

File: [./package.json:12:5](./package.json)

### FN001002 @microsoft/sp-lodash-subset | Required

Upgrade SharePoint Framework dependency package @microsoft/sp-lodash-subset

Execute the following command:

```sh
npm i -SE @microsoft/sp-lodash-subset@1.21.1
```

File: [./package.json:13:5](./package.json)

### FN001003 @microsoft/sp-office-ui-fabric-core | Required

Upgrade SharePoint Framework dependency package @microsoft/sp-office-ui-fabric-core

Execute the following command:

```sh
npm i -SE @microsoft/sp-office-ui-fabric-core@1.21.1
```

File: [./package.json:14:5](./package.json)

### FN001004 @microsoft/sp-webpart-base | Required

Upgrade SharePoint Framework dependency package @microsoft/sp-webpart-base

Execute the following command:

```sh
npm i -SE @microsoft/sp-webpart-base@1.21.1
```

File: [./package.json:16:5](./package.json)

### FN001021 @microsoft/sp-property-pane | Required

Upgrade SharePoint Framework dependency package @microsoft/sp-property-pane

Execute the following command:

```sh
npm i -SE @microsoft/sp-property-pane@1.21.1
```

File: [./package.json:15:5](./package.json)

### FN001034 @microsoft/sp-adaptive-card-extension-base | Optional

Install SharePoint Framework dependency package @microsoft/sp-adaptive-card-extension-base

Execute the following command:

```sh
npm i -SE @microsoft/sp-adaptive-card-extension-base@1.21.1
```

File: [./package.json:11:3](./package.json)

### FN002001 @microsoft/sp-build-web | Required

Upgrade SharePoint Framework dev dependency package @microsoft/sp-build-web

Execute the following command:

```sh
npm i -DE @microsoft/sp-build-web@1.21.1
```

File: [./package.json:31:5](./package.json)

### FN002002 @microsoft/sp-module-interfaces | Required

Upgrade SharePoint Framework dev dependency package @microsoft/sp-module-interfaces

Execute the following command:

```sh
npm i -DE @microsoft/sp-module-interfaces@1.21.1
```

File: [./package.json:32:5](./package.json)

### FN002022 @microsoft/eslint-plugin-spfx | Required

Install SharePoint Framework dev dependency package @microsoft/eslint-plugin-spfx

Execute the following command:

```sh
npm i -DE @microsoft/eslint-plugin-spfx@1.21.1
```

File: [./package.json:29:3](./package.json)

### FN002023 @microsoft/eslint-config-spfx | Required

Install SharePoint Framework dev dependency package @microsoft/eslint-config-spfx

Execute the following command:

```sh
npm i -DE @microsoft/eslint-config-spfx@1.21.1
```

File: [./package.json:29:3](./package.json)

### FN010001 .yo-rc.json version | Recommended

Update version in .yo-rc.json

```json
{
  "@microsoft/generator-sharepoint": {
    "version": "1.21.1"
  }
}
```

File: [./.yo-rc.json:5:5](./.yo-rc.json)

### FN002024 eslint | Required

Install SharePoint Framework dev dependency package eslint

Execute the following command:

```sh
npm i -DE eslint@8.57.1
```

File: [./package.json:29:3](./package.json)

### FN002026 typescript | Required

Install SharePoint Framework dev dependency package typescript

Execute the following command:

```sh
npm i -DE typescript@5.3.3
```

File: [./package.json:29:3](./package.json)

### FN002029 @microsoft/rush-stack-compiler-5.3 | Required

Install SharePoint Framework dev dependency package @microsoft/rush-stack-compiler-5.3

Execute the following command:

```sh
npm i -DE @microsoft/rush-stack-compiler-5.3@0.1.0
```

File: [./package.json:29:3](./package.json)

### FN012017 tsconfig.json extends property | Required

Update tsconfig.json extends property

```json
{
  "extends": "./node_modules/@microsoft/rush-stack-compiler-5.3/includes/tsconfig-webon"
}
```

File: [./tsconfig.json:2:3](./tsconfig.json)

### FN021003 package.json engines.node | Required

Update package.json engines.node property

```json
{
  "engines": {
    "node": ">=22.14.0 < 23.0.0"
  }
}
```

File: [./package.json:1:1](./package.json)

### FN002021 @rushstack/eslint-config | Required

Install SharePoint Framework dev dependency package @rushstack/eslint-config

Execute the following command:

```sh
npm i -DE @rushstack/eslint-config@4.0.1
```

File: [./package.json:29:3](./package.json)

### FN010010 .yo-rc.json @microsoft/teams-js SDK version | Recommended

Update @microsoft/teams-js SDK version in .yo-rc.json

```json
{
  "@microsoft/generator-sharepoint": {
    "sdkVersions": {
      "@microsoft/teams-js": "2.24.0"
    }
  }
}
```

File: [./.yo-rc.json:2:3](./.yo-rc.json)

### FN001022 office-ui-fabric-react | Required

Remove SharePoint Framework dependency package office-ui-fabric-react

Execute the following command:

```sh
npm un -S office-ui-fabric-react
```

File: [./package.json:22:5](./package.json)

### FN001035 @fluentui/react | Required

Install SharePoint Framework dependency package @fluentui/react

Execute the following command:

```sh
npm i -SE @fluentui/react@8.106.4
```

File: [./package.json:11:3](./package.json)

### FN007002 serve.json initialPage | Required

Update serve.json initialPage URL

```json
{
  "initialPage": "https://{tenantDomain}/_layouts/workbench.aspx"
}
```

File: [./config/serve.json:5:3](./config/serve.json)

### FN015009 config/sass.json | Required

Add file config/sass.json

Execute the following command:

```sh
cat > "config/sass.json" << EOF 
{
  "$schema": "https://developer.microsoft.com/json-schemas/core-build/sass.schema.json"
}
EOF
```

File: [config/sass.json](config/sass.json)

### FN001008 react | Required

Upgrade SharePoint Framework dependency package react

Execute the following command:

```sh
npm i -SE react@17.0.1
```

File: [./package.json:23:5](./package.json)

### FN001009 react-dom | Required

Upgrade SharePoint Framework dependency package react-dom

Execute the following command:

```sh
npm i -SE react-dom@17.0.1
```

File: [./package.json:24:5](./package.json)

### FN002015 @types/react | Required

Upgrade SharePoint Framework dev dependency package @types/react

Execute the following command:

```sh
npm i -DE @types/react@17.0.45
```

File: [./package.json:34:5](./package.json)

### FN002016 @types/react-dom | Required

Upgrade SharePoint Framework dev dependency package @types/react-dom

Execute the following command:

```sh
npm i -DE @types/react-dom@17.0.17
```

File: [./package.json:35:5](./package.json)

### FN010008 .yo-rc.json nodeVersion | Recommended

Update nodeVersion in .yo-rc.json

```json
{
  "@microsoft/generator-sharepoint": {
    "nodeVersion": "22.15.1"
  }
}
```

File: [./.yo-rc.json:2:38](./.yo-rc.json)

### FN010009 .yo-rc.json @microsoft/microsoft-graph-client SDK version | Recommended

Update @microsoft/microsoft-graph-client SDK version in .yo-rc.json

```json
{
  "@microsoft/generator-sharepoint": {
    "sdkVersions": {
      "@microsoft/microsoft-graph-client": "3.0.2"
    }
  }
}
```

File: [./.yo-rc.json:2:3](./.yo-rc.json)

### FN022001 Scss file import | Required

Remove scss file import

```scss
@import '~office-ui-fabric-react/dist/sass/References.scss'
```

File: [src/webparts/simplePoll/components/SimplePoll.module.scss](src/webparts/simplePoll/components/SimplePoll.module.scss)

### FN022002 Scss file import | Optional

Add scss file import

```scss
@import '~@fluentui/react/dist/sass/References.scss'
```

File: [src/webparts/simplePoll/components/MessageContainer/MessageContainer.module.scss](src/webparts/simplePoll/components/MessageContainer/MessageContainer.module.scss)

### FN022002 Scss file import | Optional

Add scss file import

```scss
@import '~@fluentui/react/dist/sass/References.scss'
```

File: [src/webparts/simplePoll/components/SimplePoll.module.scss](src/webparts/simplePoll/components/SimplePoll.module.scss)

### FN012020 tsconfig.json noImplicitAny | Required

Add noImplicitAny in tsconfig.json

```json
{
  "compilerOptions": {
    "noImplicitAny": true
  }
}
```

File: [./tsconfig.json:3:22](./tsconfig.json)

### FN007001 serve.json schema | Required

Update serve.json schema URL

```json
{
  "$schema": "https://developer.microsoft.com/json-schemas/spfx-build/spfx-serve.schema.json"
}
```

File: [./config/serve.json:2:3](./config/serve.json)

### FN001033 tslib | Required

Install SharePoint Framework dependency package tslib

Execute the following command:

```sh
npm i -SE tslib@2.3.1
```

File: [./package.json:11:3](./package.json)

### FN002007 ajv | Required

Upgrade SharePoint Framework dev dependency package ajv

Execute the following command:

```sh
npm i -DE ajv@6.12.5
```

File: [./package.json:36:5](./package.json)

### FN002009 @microsoft/sp-tslint-rules | Required

Remove SharePoint Framework dev dependency package @microsoft/sp-tslint-rules

Execute the following command:

```sh
npm un -D @microsoft/sp-tslint-rules
```

File: [./package.json:33:5](./package.json)

### FN002013 @types/webpack-env | Required

Upgrade SharePoint Framework dev dependency package @types/webpack-env

Execute the following command:

```sh
npm i -DE @types/webpack-env@1.15.2
```

File: [./package.json:38:5](./package.json)

### FN002025 eslint-plugin-react-hooks | Required

Install SharePoint Framework dev dependency package eslint-plugin-react-hooks

Execute the following command:

```sh
npm i -DE eslint-plugin-react-hooks@4.3.0
```

File: [./package.json:29:3](./package.json)

### FN015003 tslint.json | Required

Remove file tslint.json

Execute the following command:

```sh
rm "tslint.json"
```

File: [tslint.json](tslint.json)

### FN015008 .eslintrc.js | Required

Add file .eslintrc.js

Execute the following command:

```sh
cat > ".eslintrc.js" << EOF 
require('@rushstack/eslint-config/patch/modern-module-resolution');
module.exports = {
  extends: ['@microsoft/eslint-config-spfx/lib/profiles/react'],
  parserOptions: { tsconfigRootDir: __dirname }
};
EOF
```

File: [.eslintrc.js](.eslintrc.js)

### FN023002 .gitignore '.heft' folder | Required

To .gitignore add the '.heft' folder


File: [./.gitignore](./.gitignore)

### FN006005 package-solution.json metadata | Required

In package-solution.json add metadata section

```json
{
  "solution": {
    "metadata": {
      "shortDescription": {
        "default": "react-simple-poll description"
      },
      "longDescription": {
        "default": "react-simple-poll description"
      },
      "screenshotPaths": [],
      "videoUrl": "",
      "categories": []
    }
  }
}
```

File: [./config/package-solution.json:3:3](./config/package-solution.json)

### FN006006 package-solution.json features | Required

In package-solution.json add features for components

```json
{
  "solution": {
    "features": [
      {
        "title": "react-simple-poll SimplePollWebPart Feature",
        "description": "The feature that activates SimplePollWebPart from the react-simple-poll solution.",
        "id": "346292ca-514f-49ce-91aa-f1bf3b30088b",
        "version": "2.1.0.0",
        "componentIds": [
          "346292ca-514f-49ce-91aa-f1bf3b30088b"
        ]
      }
    ]
  }
}
```

File: [./config/package-solution.json:3:3](./config/package-solution.json)

### FN017001 Run npm dedupe | Optional

If, after upgrading npm packages, when building the project you have errors similar to: "error TS2345: Argument of type 'SPHttpClientConfiguration' is not assignable to parameter of type 'SPHttpClientConfiguration'", try running 'npm dedupe' to cleanup npm packages.

Execute the following command:

```sh
npm dedupe
```

File: [./package.json](./package.json)

## Summary

### Execute script

```sh
npm un -S office-ui-fabric-react
npm un -D @microsoft/sp-tslint-rules
npm i -SE @microsoft/sp-core-library@1.21.1 @microsoft/sp-lodash-subset@1.21.1 @microsoft/sp-office-ui-fabric-core@1.21.1 @microsoft/sp-webpart-base@1.21.1 @microsoft/sp-property-pane@1.21.1 @microsoft/sp-adaptive-card-extension-base@1.21.1 @fluentui/react@8.106.4 react@17.0.1 react-dom@17.0.1 tslib@2.3.1
npm i -DE @microsoft/sp-build-web@1.21.1 @microsoft/sp-module-interfaces@1.21.1 @microsoft/eslint-plugin-spfx@1.21.1 @microsoft/eslint-config-spfx@1.21.1 eslint@8.57.1 typescript@5.3.3 @microsoft/rush-stack-compiler-5.3@0.1.0 @rushstack/eslint-config@4.0.1 @types/react@17.0.45 @types/react-dom@17.0.17 ajv@6.12.5 @types/webpack-env@1.15.2 eslint-plugin-react-hooks@4.3.0
npm dedupe
cat > "config/sass.json" << EOF 
{
  "$schema": "https://developer.microsoft.com/json-schemas/core-build/sass.schema.json"
}
EOF
rm "tslint.json"
cat > ".eslintrc.js" << EOF 
require('@rushstack/eslint-config/patch/modern-module-resolution');
module.exports = {
  extends: ['@microsoft/eslint-config-spfx/lib/profiles/react'],
  parserOptions: { tsconfigRootDir: __dirname }
};
EOF
```

### Modify files

#### [./.yo-rc.json](./.yo-rc.json)

Update version in .yo-rc.json:

```json
{
  "@microsoft/generator-sharepoint": {
    "version": "1.21.1"
  }
}
```

Update @microsoft/teams-js SDK version in .yo-rc.json:

```json
{
  "@microsoft/generator-sharepoint": {
    "sdkVersions": {
      "@microsoft/teams-js": "2.24.0"
    }
  }
}
```

Update nodeVersion in .yo-rc.json:

```json
{
  "@microsoft/generator-sharepoint": {
    "nodeVersion": "22.15.1"
  }
}
```

Update @microsoft/microsoft-graph-client SDK version in .yo-rc.json:

```json
{
  "@microsoft/generator-sharepoint": {
    "sdkVersions": {
      "@microsoft/microsoft-graph-client": "3.0.2"
    }
  }
}
```

#### [./tsconfig.json](./tsconfig.json)

Update tsconfig.json extends property:

```json
{
  "extends": "./node_modules/@microsoft/rush-stack-compiler-5.3/includes/tsconfig-webon"
}
```

Add noImplicitAny in tsconfig.json:

```json
{
  "compilerOptions": {
    "noImplicitAny": true
  }
}
```

#### [./package.json](./package.json)

Update package.json engines.node property:

```json
{
  "engines": {
    "node": ">=22.14.0 < 23.0.0"
  }
}
```

#### [./config/serve.json](./config/serve.json)

Update serve.json initialPage URL:

```json
{
  "initialPage": "https://{tenantDomain}/_layouts/workbench.aspx"
}
```

Update serve.json schema URL:

```json
{
  "$schema": "https://developer.microsoft.com/json-schemas/spfx-build/spfx-serve.schema.json"
}
```

#### [src/webparts/simplePoll/components/SimplePoll.module.scss](src/webparts/simplePoll/components/SimplePoll.module.scss)

Remove scss file import:

```scss
@import '~office-ui-fabric-react/dist/sass/References.scss'
```

Add scss file import:

```scss
@import '~@fluentui/react/dist/sass/References.scss'
```

#### [src/webparts/simplePoll/components/MessageContainer/MessageContainer.module.scss](src/webparts/simplePoll/components/MessageContainer/MessageContainer.module.scss)

Add scss file import:

```scss
@import '~@fluentui/react/dist/sass/References.scss'
```

#### [./.gitignore](./.gitignore)

To .gitignore add the '.heft' folder:

```text
.heft
```

#### [./config/package-solution.json](./config/package-solution.json)

In package-solution.json add metadata section:

```json
{
  "solution": {
    "metadata": {
      "shortDescription": {
        "default": "react-simple-poll description"
      },
      "longDescription": {
        "default": "react-simple-poll description"
      },
      "screenshotPaths": [],
      "videoUrl": "",
      "categories": []
    }
  }
}
```

In package-solution.json add features for components:

```json
{
  "solution": {
    "features": [
      {
        "title": "react-simple-poll SimplePollWebPart Feature",
        "description": "The feature that activates SimplePollWebPart from the react-simple-poll solution.",
        "id": "346292ca-514f-49ce-91aa-f1bf3b30088b",
        "version": "2.1.0.0",
        "componentIds": [
          "346292ca-514f-49ce-91aa-f1bf3b30088b"
        ]
      }
    ]
  }
}
```