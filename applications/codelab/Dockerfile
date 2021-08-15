# See the associated GitHub workflow, that builds and publishes
# this docker image to Docker Hub:
# .github/workflows/publish-builder-img.yml
# It can be triggered manually from the GitHub project page. 

FROM sh 
RUN yarn \
    yarn electron package
    yarn theia start /my-container --hostname 0.0.0.0 --port 8080
