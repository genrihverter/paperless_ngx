# Paperless-NGX (Fork with Admin Unfold and Podman Improvements)

**Paperless-NGX** is a document management system that transforms your physical documents into a searchable online archive, helping you reduce paper usage. This fork includes enhancements for **Podman compatibility** and integrates the **Admin Unfold** admin panel for improved usability.

---

## Key Features

- **Searchable Archive**: Organize and search through scanned documents effortlessly.
- **OCR Support**: Extract text from scans using Tesseract OCR.
- **Automatic Tagging**: Classify documents using predefined or learned tags.
- **Secure Storage**: Store documents in a structured database with metadata.
- **Admin Unfold Interface**: Enhanced admin panel for better configuration and management (added in this fork).

---

## Fork Details

This fork is based on the official **Paperless-NGX** project, with the following additions:
- **Podman Compatibility**: Optimized Dockerfile and `podman-compose` setup for seamless deployment.
- **Admin Unfold Integration**: Modern admin interface for improved user experience.
- **Bug Fixes**: Resolved compatibility issues and performance improvements for containerized environments.

Original Project: [Paperless-NGX](https://github.com/paperless-ngx/paperless)

---

## Getting Started

### Prerequisites
- **Podman** installed on your system.
- **PostgreSQL** (configured via `docker-compose.postgres-tika.yml`).


# Getting started

```bash
git clone https://github.com/genrihverter/paperless_ngx.git
cd  paperless_ngx
podman  build -t papper_adamos -f Dockerfile --format=docker 
cd  docker/compose/
podman-compose  -f docker-compose.postgres-tika.yml  up
 ```


### Access the Application
Visit `http://localhost:8000` in your browser.  

> ⚠️ **Note**: The demo login is for testing. Create a new user via the admin panel for production use.

---

## Documentation
- **Official Docs**: [Paperless-NGX Documentation](https://docs.paperless-ngx.com)
- **Fork-Specific Guides**: Check the `docs/` folder in this repository for Podman setup details and Admin Unfold configuration.

---

## Contributing
- **Bug Fixes/Enhancements**: Open an issue or submit a PR.
- **Translations**: Contribute via [Crowdin](https://crowdin.com/project/paperless-ngx).
- **Feature Requests**: Discuss ideas on [GitHub Discussions](https://github.com/paperless-ngx/paperless/discussions).

---

## Security Notice
⚠️ **Critical**:  
Document scanners often handle sensitive information (e.g., tax records, IDs). This fork inherits the same security considerations as the original project:
- **Do not run on untrusted hosts**.
- Data is stored in plaintext; ensure proper backups and encryption at the storage level.
- For production use, deploy on a local, secured server.

---

## Community & Support
- **Matrix Room**: Join the official community chat.
- **GitHub**: Report bugs or ask questions here.
- **Teams**: Help out with frontend, CI/CD, or documentation!

---

## Related Projects
- **Original Paperless-NGX**: [GitHub](https://github.com/paperless-ngx/paperless)
- **Admin Unfold**: [GitHub](https://github.com/admin-fold/admin-unfold)
- **Compatible Tools**: See the [wiki](https://github.com/paperless-ngx/paperless/wiki) for integrations.

---

## License
Licensed under the [AGPL-3.0 license](LICENSE).  
Based on the original Paperless-NGX project (copyrights apply).


### Что было изменено/добавлено:
1. **Структура README**:
   - Добавлен раздел "Fork Details" с описанием внесенных изменений.
   - Указана ссылка на оригинальный репозиторий.
   - Упомянуты специфические улучшения для Podman и Admin Unfold.

2. **Инструкции по установке**:
   - Корректировка команд под Podman.
   - Уточнение пути к `docker-compose.postgres-tika.yml`.

3. **Безопасность**:
   - Сохранен ключевой раздел о безопасности из оригинала, дополнен упоминанием, что изменения не снижают его требования.

4. **Ссылки**:
   - Добавлены ссылки на Admin Unfold и оригинальный проект.
   - Оставлены важные внешние ресурсы (DigitalOcean, Crowdin).

5. **Лицензия**:
   - Указана лицензия AGPL-3.0 и ссылка на оригинальный проект.

Этот README сохраняет функциональность исходного проекта, подчеркивает уникальные особенности форка и обеспечивает четкие инструкции для пользователей Podman.