Build Image

```
docker build -t my-website:0.0.1 .
docker run --rm --name my-website -d -p 80:80 my-website:0.0.1

docker stop my-website

docker save -o /home/neossoftware/my-website_0.0.1.tar
```