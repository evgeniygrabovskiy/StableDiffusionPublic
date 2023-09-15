Want to share stable diffusion to internet?
Try this:

1. Generate .htpasswd file at https://hostingcanada.org/htpasswd-generator/
  - and copy generated data to  .htpasswd file
2. Open 7860 port on NAT (in the router settings page)
3. docker run -d -p 7860:80 -v %cd%/nginx.conf:/etc/nginx/nginx.conf:ro -v %cd%/.htpasswd:/etc/nginx/.htpasswd:ro nginx

