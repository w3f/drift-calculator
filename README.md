Role Name
=========

Store NTP drift for all W3F validators

Must set a cronjob to run: `ansible-playbook log_drift.yml` every hour (`1 * * * *`).
Must set a cronjob to run: `./ntp-drift/files/parse.sh` at the end of the day before midnight (`40 23 * * *`).


Requirements
------------

1. to have PACKET_API_TOKEN set in environment
2. to have requirements.txt installed.
3. private key with proper permissions at `~/.ssh/id_rsa_sv_validator`


Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: "{{ target | default('ubuntu_18_04') }}"
      gather_facts: true
      roles:
         - ntp-drift

License
-------

BSD-3-Clause
