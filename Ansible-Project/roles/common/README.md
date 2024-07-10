# Common Role

This role contains tasks and configurations that are common across different types of servers.

### Structure

- `tasks/`: Tasks directory containing main tasks for common configurations.
- `handlers/`: Handlers directory for managing service restarts or actions.
- `templates/`: Templates directory for Jinja2 templates.
- `files/`: Files directory for any static files needed by tasks.
- `vars/`: Variables directory for role-specific variables.
- `defaults/`: Default variables for the role.
- `meta/`: Meta information about the role.

### Usage

Include this role in your playbooks to apply common configurations across your infrastructure.
