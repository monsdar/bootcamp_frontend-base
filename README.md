# bootcamp_frontend-base
Docker image used to build the frontend. Use this as a base for your CI jobs to build your frontend.

Sample `.gitlab-ci.yml` from [here](https://gitlab.com/monsdar/bootcamp_test):

```
image: monsdar/bootcamp-frontend-base

pages:
  script:
  - mv * /public && cd /public
  - npm run build && npm run fixcolor && npm run render
  - rm -rf node_modules
  
  artifacts:
    paths:
    - /public

```
