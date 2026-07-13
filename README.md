<div align="center">

<!-- Header Banner with Capsule Render -->
![Header](https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=200&section=header&text=dronreef2&fontSize=80&fontAlignY=35&animation=twinkling&fontColor=fff)

<!-- Typing Animation -->
[![Typing SVG](https://readme-typing-svg.herokuapp.com?font=Fira+Code&pause=1000&color=58A6FF&center=true&vCenter=true&width=435&lines=%F0%9F%91%8B+Welcome+to+my+GitHub+Profile!;%F0%9F%9A%80+Full+Stack+Developer;%E2%98%81%EF%B8%8F+Cloud+%26+DevOps+Enthusiast;%F0%9F%92%BB+Always+Learning+New+Things)](https://git.io/typing-svg)

</div>

---

## 👨‍💻 About Me

- 🔭 Currently working on **Advanced GNSS Gateway Systems & Geospatial Engineering**
- 🌱 Learning **Apache SIS, Geospatial Data Processing, Resilience Patterns**
- 👯 Looking to collaborate on **Microservices Architecture, Cloud-Native Applications, GIS Systems**
- 💬 Ask me about **Spring Boot, Docker/Kubernetes, GNSS/GPS Systems, Coordinate Transformations**
- 📫 How to reach me: **[dronreef@gmail.com**

---

## 🛠️ Tech Stack

<div align="center">

![Skills](https://skillicons.dev/icons?i=java,spring,docker,kubernetes,redis,postgres,prometheus,grafana,git,maven&perline=5)

</div>

---

## 🌟 Featured Projects

### 🛰️ [GeoSat Gateway - Advanced GNSS Data Processing System](https://github.com/dronreef2/SistemasGNSS)

[![Deploy Status](https://img.shields.io/badge/deploy-success-brightgreen)](https://sistemasgnss.sliplane.app) [![Production](https://img.shields.io/badge/production-online-blue)](https://sistemasgnss.sliplane.app) [![Java](https://img.shields.io/badge/Java-17-orange)](https://github.com/dronreef2/SistemasGNSS) [![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.2.5-green)](https://github.com/dronreef2/SistemasGNSS)

> **Production URL:** [sistemasgnss.sliplane.app](https://sistemasgnss.sliplane.app) | [API Docs](https://sistemasgnss.sliplane.app/swagger-ui/index.html)

Gateway unificado para dados GNSS da RBMC (IBGE): relatórios técnicos, arquivos RINEX2/3 e órbitas – com resiliência, métricas e base para visualizações geoespaciais.

#### 🎯 Pontos Mais Interessantes (Technically Challenging Features)

1. **🌐 Geospatial Engineering com Apache SIS 1.4**
   - Transformações geodésicas avançadas: WGS84 ↔ UTM com detecção automática de zona
   - Processamento de coordenadas GNSS com precisão sub-métrica
   - Integração ISO 19115 para metadata geoespacial
   - Conversões de unidades JSR-385 compliant (meters, degrees, radians)
   - **52 testes unitários** com 100% de cobertura nos módulos SIS

2. **🛡️ Resiliência e Alta Disponibilidade**
   - **Circuit Breaker Pattern** com Resilience4j (proteção contra falhas em cascata)
   - **Retry com Exponential Backoff** para recuperação automática
   - **Fallback inteligente** com cache Redis (TTL 6h/12h)
   - Sistema funciona com ou sem Redis (`@ConditionalOnProperty`)
   - Responde com HTTP 503 estruturado durante degradação

3. **📊 Observabilidade Completa (Production-Ready)**
   - Métricas Prometheus customizadas: `rbmc.requests.total`, `rbmc.circuitbreaker.state`
   - Health probes (liveness/readiness) para Kubernetes
   - Dashboards Grafana pré-configurados
   - Logs estruturados por perfil (dev/docker/prod)
   - Tracing distribuído preparado para OpenTelemetry

4. **🚀 DevOps & Cloud-Native**
   - Docker multi-stage build otimizado (~180MB final)
   - Deploy em produção com Sliplane PaaS (24/7 uptime)
   - CI/CD completo com GitHub Actions
   - JVM otimizado para containers (G1GC, MaxRAMPercentage)
   - Startup time: ~15 segundos

5. **🔬 Processamento de Dados GNSS/RINEX**
   - Parser de arquivos RINEX2/RINEX3 (1s e 15s epochs)
   - Integração com API IBGE para órbitas multiconstelação
   - Séries temporais SNR e posições com decimação adaptativa
   - Validação e conversão de observações GNSS

#### 💻 Habilidades Técnicas Mais Difíceis Demonstradas

**1. Engenharia Geoespacial Avançada**
- Implementação de transformações geodésicas complexas usando Apache SIS
- Manipulação de sistemas de coordenadas (EPSG, WGS84, UTM)
- Cálculos de precisão numérica para aplicações GNSS profissionais

**2. Arquitetura de Software Resiliente**
- Implementação de patterns de resiliência (Circuit Breaker, Retry, Bulkhead)
- Gerenciamento de estado distribuído com cache
- Tratamento de falhas em cascata e degradação graceful

**3. Performance & Otimização**
- Docker multi-stage builds com otimização de layers
- JVM tuning para ambientes containerizados
- Decimação de séries temporais com algoritmos adaptativos

**4. Integração com APIs Externas**
- Cliente HTTP/2 com Apache HttpComponents 5
- Streaming de dados binários (RINEX files)
- Rate limiting e throttling inteligente

**5. Observabilidade em Produção**
- Design de métricas customizadas para negócio
- Instrumentação de código com Micrometer
- Correlação de logs e traces distribuídos

#### 🛠️ Stack Tecnológica

- **Backend:** Java 17, Spring Boot 3.2.5, Apache SIS 1.4
- **Resiliência:** Resilience4j (Circuit Breaker, Retry, Rate Limiter)
- **HTTP Client:** Apache HttpComponents 5 (HTTP/2 ready)
- **Cache:** Redis 7 com Testcontainers para testes
- **Observabilidade:** Micrometer, Prometheus, Grafana
- **Geospatial:** Apache SIS 1.4 (coordinate transforms, metadata, units)
- **Docs:** SpringDoc OpenAPI 3.0
- **Testes:** JUnit 5, Mockito, Testcontainers
- **DevOps:** Docker, GitHub Actions, Sliplane PaaS

#### 🏆 Desafios Técnicos Resolvidos

1. **Maven Build Configuration** - JAR executável com spring-boot-maven-plugin
2. **Docker ENTRYPOINT Optimization** - Variáveis de ambiente + JVM flags
3. **Optional Redis Dependency** - Graceful degradation sem Redis
4. **Health Check Configuration** - Deploy bem-sucedido com probes K8s

📖 **Documentação Técnica Completa:** [DEPLOY.md](https://github.com/dronreef2/SistemasGNSS/blob/main/DEPLOY.md) | [SIS_INTEGRATION.md](https://github.com/dronreef2/SistemasGNSS/blob/main/docs/SIS_INTEGRATION.md)

---

## 📊 GitHub Metrics

<div align="center">

<!-- GitHub Stats with tokyonight theme -->
![GitHub Stats](https://github-readme-stats.vercel.app/api?username=dronreef2&show_icons=true&theme=tokyonight&include_all_commits=true&count_private=true&hide_border=true)

<!-- Top Languages -->
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=dronreef2&layout=compact&langs_count=8&theme=tokyonight&hide_border=true)

</div>

---

## 🔥 GitHub Streak

<div align="center">

![GitHub Streak](https://github-readme-streak-stats.herokuapp.com/?user=dronreef2&theme=tokyonight&hide_border=true)

</div>

---

## 🏆 GitHub Trophies

<div align="center">

![Trophies](https://github-profile-trophy.vercel.app/?username=dronreef2&theme=tokyonight&no-frame=true&row=1&column=7&margin-w=15&margin-h=15)

</div>

---

## ⏱️ WakaTime Stats

<!-- WakaTime stats will be automatically updated here if you configure WAKATIME_API_KEY -->
<!--START_SECTION:waka-->
<!--END_SECTION:waka-->

> **Note:** To enable WakaTime stats, add your `WAKATIME_API_KEY` as a repository secret.

---

## 🐍 Contribution Snake

<div align="center">

<!-- Snake animation - light mode -->
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/dronreef2/dronreef2/output/github-contribution-grid-snake-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/dronreef2/dronreef2/output/github-contribution-grid-snake.svg">
  <img alt="github contribution grid snake animation" src="https://raw.githubusercontent.com/dronreef2/dronreef2/output/github-contribution-grid-snake.svg">
</picture>

</div>

---

## 📝 Latest Blog Posts

<!-- Blog posts will be automatically updated here if you configure BLOG_RSS -->
<!-- BLOG-POST-LIST:START -->
<!-- BLOG-POST-LIST:END -->

> **Note:** To enable blog posts, add your blog's RSS feed URL as a repository variable named `BLOG_RSS`.

---

## 🎵 Spotify Playing

<!-- Spotify status will be automatically updated if you configure Spotify secrets -->
<div align="center">

[![Spotify](https://spotify-github-profile.vercel.app/api/view?uid=YOUR_SPOTIFY_USER_ID&cover_image=true&theme=novatorem&show_offline=false&background_color=121212&interchange=false&bar_color=53b14f&bar_color_cover=false)](https://spotify-github-profile.vercel.app/api/view?uid=YOUR_SPOTIFY_USER_ID&redirect=true)

</div>

> **Note:** To enable Spotify integration, replace `YOUR_SPOTIFY_USER_ID` and configure the Spotify workflow secrets.

---

## 📫 Connect with Me

<div align="center">

<!-- REPLACE THE LINKS BELOW WITH YOUR ACTUAL SOCIAL PROFILES -->
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/YOUR_LINKEDIN)
[![Twitter](https://img.shields.io/badge/Twitter-1DA1F2?style=for-the-badge&logo=twitter&logoColor=white)](https://twitter.com/YOUR_TWITTER)
[![Portfolio](https://img.shields.io/badge/Portfolio-255E63?style=for-the-badge&logo=About.me&logoColor=white)](https://YOUR_PORTFOLIO_URL)
[![Email](https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white)](mailto:YOUR_EMAIL@example.com)
[![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/dronreef2)

</div>

---

## ☕ Support Me

<!-- OPTIONAL: Replace with your Buy Me a Coffee link or remove this section -->
<div align="center">

[![Buy Me A Coffee](https://img.shields.io/badge/Buy%20Me%20A%20Coffee-FFDD00?style=for-the-badge&logo=buy-me-a-coffee&logoColor=black)](https://www.buymeacoffee.com/YOUR_USERNAME)

</div>

> **Note:** Replace `YOUR_USERNAME` with your Buy Me a Coffee username or remove this section.

---

## 👀 Profile Views

<div align="center">

![Profile Views](https://komarev.com/ghpvc/?username=dronreef2&color=blueviolet&style=for-the-badge&label=PROFILE+VIEWS)

</div>

---

<!-- Footer Banner -->
<div align="center">

![Footer](https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=6,11,20&height=100&section=footer)

</div>

---

<div align="center">
  
### 💫 Made with ❤️ by dronreef2

</div>
