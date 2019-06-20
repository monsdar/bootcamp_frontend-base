# bootcamp_frontend-base
Docker image used to build the frontend. Use this as a base for your CI jobs to build your frontend.

Sample `.gitlab-ci.yml`:

```
image: node:0.12.4

pages:
  script:
  - mv * /public && cd /public
  - npm run build && npm run fixcolor && npm run render
  - rm -rf node_modules
  
  artifacts:
    paths:
    - /public

```
