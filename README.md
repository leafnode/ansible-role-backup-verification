# backup-verification

[![Build Status](https://travis-ci.com/iroquoisorg/ansible-role-backup-verification.svg?branch=master)](https://travis-ci.com/iroquoisorg/ansible-role-memcached)

Ansible role for backup-verification

This role was prepared and tested for Ubuntu 16.04.

# Installation

`$ ansible-galaxy install iroquoisorg.backup-verification`

# Default settings

```
# Each command needs to be passed in following format:
# - { command: "pwgen 20 1", dir: "/var/www/log" }
backup_pre_commands: []
backup_post_commands: []

backup_postgresql: false
backup_postgresql_dbs: []
backup_postgresql_user: ""
backup_postgresql_pass: ""
backup_postgresql_host: 'localhost'
backup_postgres_size_threshold: 1000000
backup_postgresql_backup_file_name: "backup.sql.gz"

backup_mysql: false
backup_mysql_db: ""
backup_mysql_user: ""
backup_mysql_pass: ""
backup_mysql_backup_file_name: "backup.sql"

backup_redis: false
backup_redis_save_path: "/var/lib/redis"

backup_elasticsearch: false

backup_mongodb: false
backup_mongodb_backup_file_name: "mongodb_backup"
backup_mongodb_admin_db: admin
backup_mongodb_backup_user: backup
backup_mongodb_backup_pass: ""
backup_mongodb_db: database
backup_mongodb_user: username
backup_mongodb_pass: secret

backup_files: false
backup_files_paths: []

backup_tmp_path: "{{ ansible_env.HOME}}/backup"
backup_folder_prefix: ""

backup_gpg_passphrase: "CHANGE_ME_AND_ADD_TO_VAULT"

backup_to_s3: false
backup_s3_bucket: "BACKUP_BUCKET_NAME"
backup_s3_aws_access_key: "CHANGE_ME"
backup_s3_aws_secret_key: "CHANGE_ME"
backup_s3_target_dir: "/change-me"

backup_to_directory: false
backup_directory: "/var/backup"
backup_max_keep_files: false    # number of last files to keep or false to disable

backup_to_azure: false
backup_azure_container: "change-me"
backup_azure_storage_account: "change-me"
backup_azure_access_key: "change-me"
backup_azure_target_dir: "/change-me"

```
