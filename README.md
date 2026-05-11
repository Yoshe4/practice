# Secure Build Pipeline

Проект демонстрирует CI/CD пайплайн безопасности для Spring Boot приложения.

## Джобы пайплайна

| Джоба | Инструмент | Назначение |
|---|---|---|
| secrets-scan | Gitleaks | Поиск секретов в коде |
| build | Maven | Сборка jar |
| sast | SpotBugs | Статический анализ кода |
| dependency-scan | OWASP Dependency-Check | Анализ зависимостей |
| container-security | Trivy | Сканирование Docker-образа |
| dast | OWASP ZAP | Динамический анализ |
| web-fuzzing | feroxbuster | Поиск скрытых URL |
| security-check | Bash | Финальная проверка |

## Статус

Все джобы успешно проходят. DAST и web-fuzzing запускаются в тестовом режиме (приложение требует БД в CI-окружении).
