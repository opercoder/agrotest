# Ansible Role: User Management

## Описание

Эта роль управляет пользователями и группами на Ubuntu Server 22 LTS.

## Установка

1. Клонируйте репозиторий:
   ```bash
   git clone <url>
   cd ansible-role-user-management
   ```

2. Установите зависимости:
   ```bash
   ansible-galaxy install -r requirements.yml
   ```

3. Запустите плейбук:
   ```bash
   ansible-playbook playbook.yml -i inventory/hosts.yaml
   ```

## Тестирование

Запустите тесты:
```bash
ansible-playbook tests/test_playbook.yml -i tests/test_inventory.yaml
```
