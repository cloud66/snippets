snippets
========

Deploy Hook Snippets

Below is a bare-bone example of using a snippet with the required fields - it will execute the Cloud 66 Node snippet as the first thing on all production servers.

```
production: # Environment
  first_thing: # Hook point
    - snippet: cloud66/node # Hook type
      target: any # Hook fields
      sudo: true # Needed to install a package
      execute: true # Must be set to true for all snippets
```
