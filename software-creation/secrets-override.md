# Override secrets locally

When you need to override secrets locally in a yaml file, use:
```
 foo_secret: <%= env['FOO'] || 'value' %>
```
to pull in an environment var with the overriding value. The secret that you set
in the environment will be cleared when you close that terminal. This will keep
you from leaving non development values in your secrets file.
