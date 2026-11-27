# OWASP Juice Shop Docker Lab

## Описание
Это мой первый шаг в DevSecOps. Я развернула уязвимое веб-приложение OWASP Juice Shop в Docker-контейнере для дальнейшего тестирования безопасности.
<3
## Стек
- Docker
- Docker Compose
- OWASP Juice Shop

## Как запустить
```bash
docker-compose up -d


## CI/CD Безопасность 
В проекте настроен автоматизированный пайплайн безопасности, который запускается при каждом пуше и Pull Request.

### Текущий этап (CI - Continuous Integration):
- [x] SCA & Container Scanning (Trivy): Поиск уязвимостей в Docker-образе и зависимостях.
- [x] SAST (Semgrep): Статический анализ кода на уязвимости OWASP Top 10.
- [x] Secret Scanning (Gitleaks): Поиск закоммиченных секретов (паролей, токенов, ключей).
- [ ] IaC Scanning (Checkov): Проверка конфигураций инфраструктуры (Docker, Terraform) на ошибки.

### Следующие этапы (CD - Continuous Delivery):
- [ ] DAST (OWASP ZAP): Динамическое сканирование запущенного приложения.
- [ ] Signing (Cosign): Криптографическая подпись Docker-образов.
- [ ] Policy as Code (OPA): Проверка соответствия образов политикам безопасности.

### Runtime Security (Мониторинг):
- [ ] Falco: Обнаружение аномалий в контейнерах в реальном времени.
- [ ] Wazuh / ELK: Сбор логов и SIEM-мониторинг.
