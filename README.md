# Vulnerable Docker Compose Environments

This repository contains a collection of precompiled, ready-to-go vulnerable apps. All you need is to run `docker compose up` and you have a vulnerable environment ready to be exploited.

# Usage

Just specify the file under `apps/` you want to run and execute the following command:

```bash
# Syntax:
docker compose -f <docker-compose-file> up -d
```

Examples:

```bash
docker compose -f apps/docker-compose-crapi.yml up
docker compose -f apps/docker-compose-crawlmaze.yml up
docker compose -f apps/docker-compose-dvcsharp-api.yml up
docker compose -f apps/docker-compose-dvna.yml up
docker compose -f apps/docker-compose-dvpwa.yml up
docker compose -f apps/docker-compose-dvwa.yml up
docker compose -f apps/docker-compose-dvws-node.yml up
docker compose -f apps/docker-compose-govwa.yml up
docker compose -f apps/docker-compose-javaspringvulny.yml up
docker compose -f apps/docker-compose-juice-shop.yml up
docker compose -f apps/docker-compose-log4shell.yml up
docker compose -f apps/docker-compose-nodejs-goof.yml up
docker compose -f apps/docker-compose-railsgoat.yml up
docker compose -f apps/docker-compose-ssti.yml up
docker compose -f apps/docker-compose-tiredful-api.yml up
docker compose -f apps/docker-compose-vampi.yml up
docker compose -f apps/docker-compose-vuln-django-play.yml up
docker compose -f apps/docker-compose-vuln-node-express.yml up
docker compose -f apps/docker-compose-vulnerable-flask-app.yml up
docker compose -f apps/docker-compose-vulnerableapp.yml up
docker compose -f apps/docker-compose-vulnlab.yml up
docker compose -f apps/docker-compose-webgoat.yml up
docker compose -f apps/docker-compose-xxelab.yml up
```

# Vulnerable Apps

## No Authentication Required

| Application                                                                          | Languages/Frameworks                                                                           | Command                                                            | URL                   | Credentials |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|-----------------------|-------------|
| [Crawl Maze](https://github.com/google/security-crawl-maze) by Google Security       | Python (Flask)                                                                                 | `docker compose -f apps/docker-compose-crawl-maze.yml up`          | http://localhost:80   | None        |
| [log4shell-vulnerable-app](https://github.com/christophetd/log4shell-vulnerable-app) | Java (Spring)                                                                                  | `docker compose -f apps/docker-compose-log4shell.yml up`           | http://localhost:8080 | None        |
| [nodejs-goof](https://github.com/vulnerable-apps/nodejs-goof)                        | JavaScript (Express)                                                                           | `docker compose -f apps/docker-compose-nodejs-goof.yml`            | http://localhost:3001 | None        |
| [SSTI websites](https://github.com/DiogoMRSilva/websitesVulnerableToSSTI)            | Go (net/http); Java (Spring); JavaScript (Express. Vue); PHP;  Python (Flask, Tornado, Django) | `docker compose -f apps/docker-compose-ssti.yml up`                | http://localhost:4000 | None        |
| [Tiredful-API](https://github.com/vulnerable-apps/Tiredful-API)                      | Python (Django REST Framework)                                                                 | `docker compose -f apps/docker-compose-tiredful-api.yml up`        | http://localhost:8000 | None        |
| [Vulnerable Polls App](https://github.com/vulnerable-apps/vuln_django_play)          | Python (Django)                                                                                | `docker compose -f apps/docker-compose-vuln-django-play.yml up`    | http://localhost:8020 | None        |
| [vuln_node_express](https://github.com/vulnerable-apps/vuln_node_express/)           | JavaScript (Express)                                                                           | `docker compose -f apps/docker-compose-vuln-node-express.yml up`   | http://localhost:3000 | None        |
| [VulnerableCoreApp](https://github.com/vulnerable-apps/VulnerableCoreApp)            | C# (.NET)                                                                                      | `docker compose -f apps/docker-compose-vulnerable-core-app.yml up` | http://localhost:5000 | None        |
| [VulnerableApp](https://github.com/vulnerable-apps/VulnerableApp)                    | Java (Spring)                                                                                  | `docker compose -f apps/docker-compose-vulnerableapp.yml up`       | http://localhost:80   | None        |
| [VulnLab](https://github.com/Yavuzlar/VulnLab)                                       | PHP                                                                                            | `docker compose -f apps/docker-compose-vulnlab.yml up`             | http://localhost:1337 | None        |


## Authentication Required


| Application                                                                        | Languages/Frameworks                                                             | Command                                                         | URL                                                      | Credentials                   |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------------------------------|----------------------------------------------------------|-------------------------------|
| [crAPI](https://github.com/OWASP/crAPI)                                            | Go (net/http); Java (Spring); JavaScript (React); Python (Django REST Framework) | `docker compose -f apps/docker-compose-crapi.yml up`            | http://localhost:8888                                    | admin@mail.com: adminA1!      |
| [DVWA](https://github.com/vulnerable-apps/DVWA) - Damn Vulnerable Web App          | PHP                                                                              | `docker compose -f apps/docker-compose-dvwa.yml up`             | http://localhost:4280                                    | superadmin: superadmin        |
| [DVPWA](https://github.com/vulnerable-apps/dvpwa) - Damn Vulnerable Python Web App | Python (aiohttp)                                                                 | `docker compose -f apps/docker-compose-dvpwa.yml up`            | http://localhost:8080                                    | admin: letmein                |
| [Javaspringvulny](https://github.com/vulnerable-apps/javaspringvulny)              | Java (Spring)                                                                    | `docker compose -f apps/docker-compose-javaspringvulny.yml up ` | https://localhost:9000                                   | username: password            |
| [juice-shop](https://github.com/juice-shop/juice-shop) by OWASP                    | JavaScript (Express, Angular)                                                    | `docker compose -f apps/docker-compose-juice-shop.yml up`       | http://localhost:3000                                    | admin@juice-sh.op: admin123   |
| [Pixi](https://github.com/vulnerable-apps/Pixi/) by OWASP DevSlop                  | JavaScript (Express)                                                             | `docker compose -f apps/docker-compose-pixi.yml up`             | http://localhost:8000 (web); http://localhost:8888 (API) | pixiadmin: adminpixi          |
| [railsgoat](https://github.com/OWASP/railsgoat/)                                   | Ruby (Rails)                                                                     | `docker compose -f apps/docker-compose-railsgoat.yml up`        | http://localhost:3000                                    | admin@metacorp.com: admin1234 |


## Registration or Pre-Scan Script Required

| Application                                                                     | Languages/Frameworks          | Command                                                             | URL                                                        | Credentials                                                      |
|---------------------------------------------------------------------------------|-------------------------------|---------------------------------------------------------------------|------------------------------------------------------------|------------------------------------------------------------------|
| [dvcsharp-api](https://github.com/vulnerable-apps/dvcsharp-api)                 | C# (ASP.NET Core)             | `docker compose -f apps/docker-compose-dvcsharp-api.yml up`         | http://localhost:5000                                      | Requires API registration                                        |
| [DVNA](https://github.com/appsecco/dvna) - Damn Vulnerable NodeJS               | JavaScript (Express)          | `docker compose -f apps/docker-compose-dvna.yml up`                 | http://localhost:9090                                      | Requires registration                                            |
| [DVWS Node](https://github.com/vulnerable-apps/dvws-node)                       | JavaScript (Express, GraphQL) | `docker compose -f apps/docker-compose-dvws-node.yml up`            | http://localhost:80 (web); http://localhost:4000 (GraphQL) | Requires registration                                            |
| [GoVWA](https://github.com/0c34/govwa) - Go Vulnerable Web App                  | Go (gin)                      | `docker compose -f apps/docker-compose-govwa.yml up`                | http://localhost:8888                                      | admin: govwaadmin; user1: govwauser1. Requires DB initialization |
| [VAmPI](https://github.com/erev0s/VAmPI) - Vulnerable REST API                  | Python (Flask)                | `docker compose -f apps/docker-compose-vampi.yml up`                | http://localhost:5002                                      | Requires API registration                                        |
| [Vulnerable-Flask-App](https://github.com/vulnerable-apps/Vulnerable-Flask-App) | Python (Flask)                | `docker compose -f apps/docker-compose-vulnerable-flask-app.yml up` | http://localhost:5050                                      | Requires API registration                                        |
| [xxelab](https://github.com/jbarone/xxelab)                                     | PHP                           | `docker compose -f apps/docker-compose-xxelab.yml up`               | http://localhost:5000                                      | Requires registration                                            |
| [WebGoat](http://localhost:8080/WebGoat/login)                                  | Java (Spring)                 | `docker compose -f apps/docker-compose-webgoat.yml up`              | http://localhost:8888/WebGoat                              | Requires registration                                            |


# References

* **Markdown table generated with**: https://www.tablesgenerator.com/markdown_tables#

* [Google Sheet of the above table](https://docs.google.com/spreadsheets/d/1zn5IlzW5eWCgecJWi7Zfr0ZHu9FSJ9un9QKpEUeB8U8/edit?gid=0#gid=0)

