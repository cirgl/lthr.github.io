---
layout: post
title: Run a PHP server with Docker
tags:
- php
- apache
- docker
---

1. Install Docker
2. From terminal, run the following (fix the path to your PHP project dir):
```bash
docker run -tid -p 80:80 --name apache -v ~/your-php-project/:/var/www/html nimmis/apache-php5
```

3. Enjoy on `localhost`
