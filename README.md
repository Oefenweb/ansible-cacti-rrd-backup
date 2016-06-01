## cacti-rrd-backup

[![Build Status](https://travis-ci.org/Oefenweb/ansible-cacti-rrd-backup.svg?branch=master)](https://travis-ci.org/Oefenweb/ansible-cacti-rrd-backup) [![Ansible Galaxy](http://img.shields.io/badge/ansible--galaxy-cacti--rrd--backup-blue.svg)](https://galaxy.ansible.com/Oefenweb/ansible-cacti-rrd-backup)

Perform Cacti RRD backups using [rrdtool](http://oss.oetiker.ch/rrdtool/).

#### Requirements

* `rrdtool` (will be installed)

#### Variables

* `cacti_rrd_backup_install_path`: [default: `/usr/local/bin`]: Install directory

* `cacti_rrd_backup_rra_path`: [default: `/var/lib/cacti/rra`]: The source path (cacti `rra` path)
* `cacti_rrd_backup_backup_path`: [default: `/tmp/cacti-rrd-backup`]: The destination path

* `cacti_rrd_backup_rrd_file_mode`: [default: `0664`]: The mode of rrd files (after restore)
* `cacti_rrd_backup_rrd_file_owner`: [default: `www-data`]: The owner of rrd files (after restore)
* `cacti_rrd_backup_rrd_file_group`: [default: `cacti_rrd_backup_rrd_file_owner`]: The group of rrd files (after restore)

#### Dependencies

None

#### Example

```yaml
---
- hosts: all
  roles:
   - cacti-rrd-backup
```

#### License

MIT

#### Author Information

Mischa ter Smitten

#### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/Oefenweb/ansible-cacti-rrd-backup/issues)!
