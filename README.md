# docker-hugo

Docker image for hugo static page generator (https://gohugo.io)

## Usage

Create a new repo with the following Dockerfile

```
FROM docker-hugo:latest
```

Put your hugo site in the root of the repo, you should see the following output
when you build your docker image.

```
Sending build context to Docker daemon 8.041 MB
Step 1 : FROM docker-hugo:latest
# Executing 2 build triggers...
Step 1 : ADD /site /site
Step 1 : RUN hugo -s /site -d /usr/share/nginx/html
 ---> Running in 920cc48105cb
0 of 2 drafts rendered
0 future content
0 pages created
0 paginator pages created
0 tags created
0 categories created
in 9 ms
 ---> 1ae60eb2bdac
Removing intermediate container da605817e1fd
Removing intermediate container 920cc48105cb
Successfully built 1ae60eb2bdac
```
