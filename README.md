# mackerel-plugin-thermal
Add metrics of temperature obtained from thermal sensors to mackerel.

## Installation
#### Please install smartctl in advance.
for Ubuntu/Debian
```
sudo apt-get -y install lm-sensors
```
for CentOS
```
sudo yum -y install lm_sensors
```

#### Place mackerel-plugin-smart-temp and make it executable.
```
curl -o /usr/local/bin/mackerel-plugin-thermal https://raw.githubusercontent.com/masato-hi/mackerel-plugin-thermal/master/mackerel-plugin-thermal
chmod +x /usr/local/bin/mackerel-plugin-thermal
```

#### Please add the following contents to /etc/mackerel-agent/mackerel-agent.conf
```
[plugin.metrics.thermal]
command = "mackerel-plugin-thermal"
```

#### Please restart mackerel-agent.
```
service mackerel-agent restart
```


## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/masato-hi/mackerel-plugin-thermal.


## License

The script is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).

