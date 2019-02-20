# linux_update

This role updates a Linux Host. It is known to work on Ubuntu 16.04, Ubuntu 18.04, and Centos 7. This role may work on other distributions using apt or yum package managers.

<b>Caution:
* Host will be rebooted if required by package manager
* All packages will be updated
* Autoremove will be run to remove unneeded packages
* It is often difficult to revert these changes</b>

## Requirements

* Role uses sudo to update and reboot system; <code>ansible_user</code> must be able to sudo to root without a password.
* Role uses the respective package manager to install packages, and must be configured.
* The role defaults use Ansible magic variables; facts must be available.

## Role Variables

There are no variables for this role.

## Dependencies

Check out the following roles to satisfy this role's requirements

|Role|Description|Source|
|---|---|---|
|ar_linux_package_sources|Sets package sources on a Linux host|https://github.com/dinohead/ar_linux_package_sources|


## Example Playbook

```yaml
    - hosts: servers
      roles:
         - ar_linux_update
```

## Author Information

|Author              |E-mail                   |
|:-------------------|:------------------------|
|Derek 'dRock' Halsey|derek.halsey@dinohead.com|

## License

MIT License

Copyright (c) 2019 Dinohead LLC

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

## Role Development Information

### Testing

### Contributing

### Git SCM
Please refer to the .gitignore file and update accordingly depending on your
development environment, etc.  The particular file was generated at 
[gitignore.io](https://www.gitignore.io/) and contains settings for the following:
  - Ansible
  - Python
  - Vim
  - Eclipse
  - IntelliJ IDEA
  - Linux
  - Windows
  
### Versioning
Please update [VERSION.md](./VERSION.md) as you release new versions of your role and try to
abide by [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

### Self-contained
Please try to keep this role as self-contained as possible such that it may be
simply installed (e.g. `ansible-galaxy install`) and applied as part of a 
playbook.
