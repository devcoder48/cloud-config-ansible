# cloud-config-ansible
Contains Ansible playbooks which are fed to Cloud Init scripts on boot.

## Playbooks

### `common-dev-tools`

Installs a baseline set of development tooling (compilers, build helpers, git, curl, etc.)
and automatically handles both Debian-based and RHEL/Rocky-based systems. The playbook
leverages Ansible facts to detect the OS family at runtime and executes the appropriate
package manager commands, including the `@Development Tools` group on Red Hat derivatives.

Run a syntax check locally with:

```bash
ansible-playbook --syntax-check playbooks/common-dev-tools.yml
```
