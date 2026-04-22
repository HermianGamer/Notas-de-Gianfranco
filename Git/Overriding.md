If you set a configuration in a more specific [[Locations]], it will override the same configuration in a more general location. For example, if you set `user.name` in the local configuration, it will override the `user.name` set in the global configuration.

![](https://storage.googleapis.com/qvault-webapp-dynamic-assets/course_assets/e4S7M9u-1055x600.png)

Suppose you set user.name='Prime' at the system level, user.name='Lane' at the global level, and user.name='TJ' at the local level. When running Git in that repository, which value will Git actually use? --> TJ