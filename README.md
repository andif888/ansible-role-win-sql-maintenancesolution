# ansible-role-win-sql-maintenancesolution

Role to install SQL Maintenance Solution https://github.com/olahallengren/sql-server-maintenance-solution

## Table of content

- [Default Variables](#default-variables)
  - [sql_maintenance_disable_jobs](#sql_maintenance_disable_jobs)
  - [sql_maintenance_download_url_maintenancesolution_sql](#sql_maintenance_download_url_maintenancesolution_sql)
  - [sql_maintenance_download_url_uninstall_sql](#sql_maintenance_download_url_uninstall_sql)
  - [sql_maintenance_download_url_versioncheck_sql](#sql_maintenance_download_url_versioncheck_sql)
  - [sql_maintenance_file_path_maintenancesolution_sql](#sql_maintenance_file_path_maintenancesolution_sql)
  - [sql_maintenance_file_path_uninstall_sql](#sql_maintenance_file_path_uninstall_sql)
  - [sql_maintenance_file_path_versioncheck_sql](#sql_maintenance_file_path_versioncheck_sql)
  - [sql_maintenance_install_path](#sql_maintenance_install_path)
  - [sql_maintenance_script_prefix](#sql_maintenance_script_prefix)
- [Dependencies](#dependencies)
- [License](#license)
- [Author](#author)

---

## Default Variables

### sql_maintenance_disable_jobs

do not create automatically jobs in sql agent

#### Default value

```YAML
sql_maintenance_disable_jobs: false
```

### sql_maintenance_download_url_maintenancesolution_sql

download url of MaintenanceSolution.sql

#### Default value

```YAML
sql_maintenance_download_url_maintenancesolution_sql: https://raw.githubusercontent.com/olahallengren/sql-server-maintenance-solution/master/MaintenanceSolution.sql
```

### sql_maintenance_download_url_uninstall_sql

download url for Uninstall.sql

#### Default value

```YAML
sql_maintenance_download_url_uninstall_sql: https://ola.hallengren.com/scripts/misc/Uninstall.sql
```

### sql_maintenance_download_url_versioncheck_sql

download url for VersionCheck.sql

#### Default value

```YAML
sql_maintenance_download_url_versioncheck_sql: https://ola.hallengren.com/scripts/misc/VersionCheck.sql
```

### sql_maintenance_file_path_maintenancesolution_sql

local path to aintenanceSolution.sql

#### Default value

```YAML
sql_maintenance_file_path_maintenancesolution_sql: '{{ sql_maintenance_install_path
  }}\{{ sql_maintenance_download_url_maintenancesolution_sql | basename }}'
```

### sql_maintenance_file_path_uninstall_sql

local path to Uninstall.sql

#### Default value

```YAML
sql_maintenance_file_path_uninstall_sql: '{{ sql_maintenance_install_path }}\{{ sql_maintenance_download_url_uninstall_sql
  | basename }}'
```

### sql_maintenance_file_path_versioncheck_sql

local path to VersionCheck.sql

#### Default value

```YAML
sql_maintenance_file_path_versioncheck_sql: '{{ sql_maintenance_install_path }}\{{
  sql_maintenance_download_url_versioncheck_sql | basename }}'
```

### sql_maintenance_install_path

Path to install sql scripts into

#### Default value

```YAML
sql_maintenance_install_path: '{{ ansible_env.ProgramFiles }}\{{ sql_maintenance_script_prefix
  }}'
```

### sql_maintenance_script_prefix

download files gets prefixed with this value

#### Default value

```YAML
sql_maintenance_script_prefix: hallengreen_sql
```



## Dependencies

None.

## License

license (GPL-2.0-or-later, MIT, etc)

## Author

andif888
