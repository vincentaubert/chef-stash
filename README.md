= DESCRIPTION:

Installs Atlassian Stash.

= REQUIREMENTS:

== Cookbooks:

Opscode Cookbooks (http://github.com/opscode-cookbooks/)

* git (once CHEF-1537 is incorporated, otherwise use git cookbook fork below)
* java
* postgresql

Third-Party Cookbooks

* git::source from https://github.com/bflad/git

= USAGE:

For a localhost Postgres database, create a stash/stash encrypted data bag
with the following information (repeat for other environments as necessary):

    {
      "id": "stash"
      "ENVIRONMENT1": {
        "database": "ENVIRONMENT1_DATABASE_NAME",
        "database_user": "ENVIRONMENT1_DATABASE_USER",
        "database_password": "ENVIRONMENT1_DATABASE_PASSWORD",
      }
    }

Add recipe[stash] and get on your merry way.

= LICENSE and AUTHOR:
      
Author:: Brian Flad (<bflad417@gmail.com>)

Copyright:: 2012

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.