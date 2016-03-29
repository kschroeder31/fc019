fc019 Cookbook
=======================
This simply demonstrates FC019 issue. Here is my command-line output for 6.0.1:
```
$ ./foodcritic -V
foodcritic 6.0.1
$ ./foodcritic ~/chef/chef-repo/cookbooks/fc019/
FC019: Access node attributes in a consistent manner: ~/chef/chef-repo/cookbooks/fc019/recipes/default.rb:2
FC064: Ensure issues_url is set in metadata: ~/chef/chef-repo/cookbooks/fc019/metadata.rb:1
FC065: Ensure source_url is set in metadata: ~/chef/chef-repo/cookbooks/fc019/metadata.rb:1
```

Here is the output for 5.0.0:
```
$ foodcritic -V
foodcritic 5.0.0
$ foodcritic .
FC019: Access node attributes in a consistent manner: ./recipes/default.rb:2
```

Requirements
------------
None

Attributes
----------

See the relevant cookbooks for documentation on their attributes.

Usage
-----
#### starter::default

e.g.
Just include `starter` in your node's `run_list`:

```json
{
  "name":"my_node",
  "run_list": [
    "recipe[starter]"
  ]
}
```

License and Authors
-------------------
Owned by: Target Corporation
Authors: Kevin Schroeder
