# Ansible Role: User Management

## Описание

Эта роль управляет пользователями и группами на Ubuntu Server 22 LTS.

Доступные теги:
1. groups
2. users
3. sudoers
4. disable
5. expiration

## Установка

1. Клонируйте репозиторий:
   ```bash
   git clone <url>
   ```

2. Для запуска:
   ```bash 
   mv ./opercoder.agrotest /etc/ansible/roles
   mv /etc/ansible/roles/opercoder.agrotest/to_run /etc/ansible/
   ```

3. Запустите плейбук (Пароль для passwords.yml: opercoder):
   ```bash
   ansible-playbook playbook.yml -i inventory/hosts.yaml --ask-vault-pass  --tag XXX 
   ansible-playbook /etc/ansible/test.yml --tags users --extra-vars "users_file=/etc/ansible/developers.yml" --ask-vault-pass
   ```
   Хосты (all, group, host) назначаются в test.yml.  
   Пользователи прописываются в файлах developers.yml, admins.yml, с которыми можно соверщать операции на выбранных хостах.  

## Тестирование

Запустите тесты:
```bash
ansible-playbook tests/test_playbook.yml -i tests/test_inventory.yaml
```
