# Tmpreaper module for puppet

**Manage tmpreaper/tmpwatch on Debian and RHEL families**

## Usage
This module aims to provide a simple way to clean directories.

## Simple
```Puppet
include ::tmpreaper
::tmpreaper::directory {'my tmpreaper on tmp':
	ensure    => present,
	age       => '2d',
	directory => '/tmp',
}
```

### Advanced
```Puppet
class {'tmpreaper':
	enabled => false,
	package => 'tmpreaper',
}
::tmpreaper::directory {'my tmpreaper on foo home':
	ensure    => present,
	age       => '2d',
	directory => '/home/foo',
	user 	  => 'foo',
}
```

## Contributing

Please report bugs and feature request using [GitHub issue
tracker](https://github.com/camptocamp/puppet-tmpreaper/issues).

For pull requests, it is very much appreciated to check your Puppet manifest
with [puppet-lint](https://github.com/camptocamp/puppet-tmpreaper/issues) to follow the recommended Puppet style guidelines from the
[Puppet Labs style guide](http://docs.puppetlabs.com/guides/style_guide.html).

## License

Copyright (c) 2013 <mailto:puppet@camptocamp.com> All rights reserved.

    This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with this program.  If not, see <http://www.gnu.org/licenses/>.
