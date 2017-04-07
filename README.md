# api documentation for  [network (v0.3.2)](https://github.com/tomas/network#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-network.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-network) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-network.svg)](https://travis-ci.org/npmdoc/node-npmdoc-network)
#### Cross platform network utilities for Node.js (gateway_ip, MAC address, etc)

[![NPM](https://nodei.co/npm/network.png?downloads=true)](https://www.npmjs.com/package/network)

[![apidoc](https://npmdoc.github.io/node-npmdoc-network/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-network_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-network/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-network/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-network/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Tomas Pollak",
        "email": "tomas@forkhq.com"
    },
    "bin": {
        "network": "./bin/network"
    },
    "bugs": {
        "url": "https://github.com/tomas/network/issues"
    },
    "dependencies": {
        "async": "^1.5.2",
        "needle": "1.1.2",
        "wmic": "^0.1.0"
    },
    "description": "Cross platform network utilities for Node.js (gateway_ip, MAC address, etc)",
    "devDependencies": {},
    "directories": {},
    "dist": {
        "shasum": "7d985b32acf09f8e44140a7d54fcc1b7e138b053",
        "tarball": "https://registry.npmjs.org/network/-/network-0.3.2.tgz"
    },
    "gitHead": "527756878093880eee649b387ad6d4f1555c750c",
    "homepage": "https://github.com/tomas/network#readme",
    "license": "MIT",
    "main": "./lib/index.js",
    "maintainers": [
        {
            "name": "tomas",
            "email": "tomas@forkhq.com"
        }
    ],
    "name": "network",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/tomas/network.git"
    },
    "scripts": {
        "test": "echo \"Error: no test specified\" && exit 1"
    },
    "version": "0.3.2"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module network](#apidoc.module.network)
1.  [function <span class="apidocSignatureSpan">network.</span>get_active_interface (cb)](#apidoc.element.network.get_active_interface)
1.  [function <span class="apidocSignatureSpan">network.</span>get_gateway_ip (cb)](#apidoc.element.network.get_gateway_ip)
1.  [function <span class="apidocSignatureSpan">network.</span>get_interfaces_list (cb)](#apidoc.element.network.get_interfaces_list)
1.  [function <span class="apidocSignatureSpan">network.</span>get_private_ip (cb)](#apidoc.element.network.get_private_ip)
1.  [function <span class="apidocSignatureSpan">network.</span>get_public_ip (options, cb)](#apidoc.element.network.get_public_ip)
1.  [function <span class="apidocSignatureSpan">network.</span>mac_address_for (nic_name, cb)](#apidoc.element.network.mac_address_for)
1.  object <span class="apidocSignatureSpan">network.</span>darwin
1.  object <span class="apidocSignatureSpan">network.</span>linux
1.  object <span class="apidocSignatureSpan">network.</span>win32

#### [module network.darwin](#apidoc.module.network.darwin)
1.  [function <span class="apidocSignatureSpan">network.darwin.</span>gateway_ip_for (nic_name, cb)](#apidoc.element.network.darwin.gateway_ip_for)
1.  [function <span class="apidocSignatureSpan">network.darwin.</span>get_active_network_interface_name (cb)](#apidoc.element.network.darwin.get_active_network_interface_name)
1.  [function <span class="apidocSignatureSpan">network.darwin.</span>get_network_interfaces_list (cb)](#apidoc.element.network.darwin.get_network_interfaces_list)
1.  [function <span class="apidocSignatureSpan">network.darwin.</span>mac_address_for (nic_name, cb)](#apidoc.element.network.darwin.mac_address_for)
1.  [function <span class="apidocSignatureSpan">network.darwin.</span>netmask_for (nic_name, cb)](#apidoc.element.network.darwin.netmask_for)

#### [module network.linux](#apidoc.module.network.linux)
1.  [function <span class="apidocSignatureSpan">network.linux.</span>gateway_ip_for (nic_name, cb)](#apidoc.element.network.linux.gateway_ip_for)
1.  [function <span class="apidocSignatureSpan">network.linux.</span>get_active_network_interface_name (cb)](#apidoc.element.network.linux.get_active_network_interface_name)
1.  [function <span class="apidocSignatureSpan">network.linux.</span>get_network_interfaces_list (cb)](#apidoc.element.network.linux.get_network_interfaces_list)
1.  [function <span class="apidocSignatureSpan">network.linux.</span>interface_type_for (nic_name, cb)](#apidoc.element.network.linux.interface_type_for)
1.  [function <span class="apidocSignatureSpan">network.linux.</span>mac_address_for (nic_name, cb)](#apidoc.element.network.linux.mac_address_for)
1.  [function <span class="apidocSignatureSpan">network.linux.</span>netmask_for (nic_name, cb)](#apidoc.element.network.linux.netmask_for)

#### [module network.win32](#apidoc.module.network.win32)
1.  [function <span class="apidocSignatureSpan">network.win32.</span>gateway_ip_for (nic_name, cb)](#apidoc.element.network.win32.gateway_ip_for)
1.  [function <span class="apidocSignatureSpan">network.win32.</span>get_active_network_interface_name (cb)](#apidoc.element.network.win32.get_active_network_interface_name)
1.  [function <span class="apidocSignatureSpan">network.win32.</span>get_network_interfaces_list (callback)](#apidoc.element.network.win32.get_network_interfaces_list)
1.  [function <span class="apidocSignatureSpan">network.win32.</span>mac_address_for (nic_name, cb)](#apidoc.element.network.win32.mac_address_for)
1.  [function <span class="apidocSignatureSpan">network.win32.</span>netmask_for (nic_name, cb)](#apidoc.element.network.win32.netmask_for)



# <a name="apidoc.module.network"></a>[module network](#apidoc.module.network)

#### <a name="apidoc.element.network.get_active_interface"></a>[function <span class="apidocSignatureSpan">network.</span>get_active_interface (cb)](#apidoc.element.network.get_active_interface)
- description and source-code
```javascript
get_active_interface = function (cb) {

  os_functions.get_active_network_interface_name(function(err, nic_name) {
    if (err || !nic_name) return cb(err || new Error("No active interfaces detected."));

    nic_by_name(nic_name, function(err, nic) {
      if (err) return cb(err);

      os_functions.netmask_for(nic_name, function(err, netmask) {
        if (!err && netmask)
          nic.netmask = netmask.trim();

        os_functions.gateway_ip_for(nic_name, function(err, ip) {
          if (!err && ip)
            nic.gateway_ip = ip.toString().trim();

          cb(null, nic);
        })
      });
    });
  });

}
```
- example usage
```shell
...

## Get active interface

Returns the IP, MAC address and interface type for the active network
interface. On OS X and Linux you also get the IP of its assigned gateway.

''' js
network.get_active_interface(function(err, obj) {

/* obj should be:

{ name: 'eth0',
  ip_address: '10.0.1.3',
  mac_address: '56:e5:f9:e4:38:1d',
  type: 'Wired',
...
```

#### <a name="apidoc.element.network.get_gateway_ip"></a>[function <span class="apidocSignatureSpan">network.</span>get_gateway_ip (cb)](#apidoc.element.network.get_gateway_ip)
- description and source-code
```javascript
get_gateway_ip = function (cb) {

  os_functions.get_active_network_interface_name(function(err, nic_name) {
    if (err || nic_name.trim() == '')
      return cb(err || new Error('No active network interface found.'));

    os_functions.gateway_ip_for(nic_name, function(err, out) {
      if (err || !out || out.toString() == '')
        return cb(err || new Error('No gateway IP assigned to ' + nic_name));

      cb(null, out.toString().trim())
    })
  });

}
```
- example usage
```shell
...
$ network private_ip

## Get gateway IP

Returns the IP of the gateway that your active network interface is linked to.

''' js
network.get_gateway_ip(function(err, ip) {
  console.log(err || ip); // err may be 'No active network interface found.'
})
'''

##### CLI

$ network gateway_ip
...
```

#### <a name="apidoc.element.network.get_interfaces_list"></a>[function <span class="apidocSignatureSpan">network.</span>get_interfaces_list (cb)](#apidoc.element.network.get_interfaces_list)
- description and source-code
```javascript
get_interfaces_list = function (cb) {

  var count = 0,
      list = [],
      nics = os.networkInterfaces();

  function append_data(obj) {
    async.parallel([
      function(cb) {
        exports.mac_address_for(obj.name, cb)
      },
      function(cb) {
        exports.gateway_ip_for(obj.name, cb)
      },
      function(cb) {
        exports.netmask_for(obj.name, cb)
      },
      function(cb) {
        exports.interface_type_for(obj.name, cb)
      }
    ], function(err, results) {
      if (results[0]) obj.mac_address = results[0];
      if (results[1]) obj.gateway_ip  = results[1];
      if (results[2]) obj.netmask     = results[2];
      if (results[3]) obj.type        = results[3];

      list.push(obj);
      --count || cb(null, list);
    })
  }

  for (var key in nics) {
    if (key != 'lo0' && key != 'lo' && !key.match(/^tun/)) {

      count++;
      var obj = { name: key };

      nics[key].forEach(function(type) {
        if (type.family == 'IPv4') {
          obj.ip_address = type.address;
        }
      });

      append_data(obj);
    }
  }

  if (count == 0)
    cb(new Error('No interfaces found.'))
}
```
- example usage
```shell
...

## Get interfaces list

Returns list of network interfaces, including MAC addresses and the such, just
as in the example above.

''' js
network.get_interfaces_list(function(err, list) {

/* list should be:

[{
  name: 'eth0',
  ip_address: '10.0.1.3',
  mac_address: '56:e5:f9:e4:38:1d',
...
```

#### <a name="apidoc.element.network.get_private_ip"></a>[function <span class="apidocSignatureSpan">network.</span>get_private_ip (cb)](#apidoc.element.network.get_private_ip)
- description and source-code
```javascript
get_private_ip = function (cb) {

  os_functions.get_network_interfaces_list(function(err, list) {
    if (err || !list)
      return cb(err || new Error('No network interfaces found.'));

    os_functions.get_active_network_interface_name(function(err, active_nic) {
      if (err) return cb(err);

      var ips = list.filter(function(nic) {
        if (is_ip_address(nic.ip_address))
          return active_nic ? active_nic == nic.name : true;
      });

      if (ips.length > 0)
        cb(null, ips[0].ip_address);
      else
        cb(new Error('No private IPs found (' + list.length + ' interfaces)'));
    });
  });

}
```
- example usage
```shell
...
$ network public_ip

## Get private IP

Returns the IP address assigned to your first active network inteface.

''' js
network.get_private_ip(function(err, ip) {
  console.log(err || ip); // err may be 'No active network interface found'.
})
'''

##### CLI

$ network private_ip
...
```

#### <a name="apidoc.element.network.get_public_ip"></a>[function <span class="apidocSignatureSpan">network.</span>get_public_ip (options, cb)](#apidoc.element.network.get_public_ip)
- description and source-code
```javascript
get_public_ip = function (options, cb) {

  var default_urls = [
    'checkip.dyndns.org',
    'http://wtfismyip.com/text',
    'http://ipecho.net/plain',
    'http://ifconfig.me/ip'
  ];

  if (typeof options == 'function') { // no options passed
    cb = options;
    options = {};
  }

  var urls = options.urls || default_urls;

  function get(i) {
    var url = urls[i];
    if (!url) return cb(new Error('Unable to fetch IP address.'));

    needle.get(url, function(err, resp) {
      var body = resp && resp.body.toString();
      if (body && body.match(ip_regex)) {
        return cb(null, body.match(ip_regex)[1]);
      }

      get(i+1);
    })
  };

  get(0);
}
```
- example usage
```shell
...
## Get public IP

Returns your public IP address, as reported by DynDNS.org or other services.

''' js
var network = require('network');

network.get_public_ip(function(err, ip) {
  console.log(err || ip); // should return your public IP address
})
'''

##### CLI

$ network public_ip
...
```

#### <a name="apidoc.element.network.mac_address_for"></a>[function <span class="apidocSignatureSpan">network.</span>mac_address_for (nic_name, cb)](#apidoc.element.network.mac_address_for)
- description and source-code
```javascript
mac_address_for = function (nic_name, cb) {
  var cmd = 'cat /sys/class/net/' + nic_name + '/address';
  trim_exec(cmd, cb);
}
```
- example usage
```shell
...
var count = 0,
    list = [],
    nics = os.networkInterfaces();

function append_data(obj) {
  async.parallel([
    function(cb) {
      exports.mac_address_for(obj.name, cb)
    },
    function(cb) {
      exports.gateway_ip_for(obj.name, cb)
    },
    function(cb) {
      exports.netmask_for(obj.name, cb)
    },
...
```



# <a name="apidoc.module.network.darwin"></a>[module network.darwin](#apidoc.module.network.darwin)

#### <a name="apidoc.element.network.darwin.gateway_ip_for"></a>[function <span class="apidocSignatureSpan">network.darwin.</span>gateway_ip_for (nic_name, cb)](#apidoc.element.network.darwin.gateway_ip_for)
- description and source-code
```javascript
gateway_ip_for = function (nic_name, cb) {
  var cmd = "ipconfig getoption " + nic_name + " router";
  trim_exec(cmd, cb);
}
```
- example usage
```shell
...
var count = 0,
    list  = [],
    nics  = os.networkInterfaces();

function append_data(obj) {
  async.parallel([
    function(cb) {
      exports.gateway_ip_for(obj.name, cb)
    },
    function(cb) {
      exports.netmask_for(obj.name, cb)
    }
  ], function(err, results) {
    if (results[0]) obj.gateway_ip = results[0];
    if (results[1]) obj.netmask    = results[1];
...
```

#### <a name="apidoc.element.network.darwin.get_active_network_interface_name"></a>[function <span class="apidocSignatureSpan">network.darwin.</span>get_active_network_interface_name (cb)](#apidoc.element.network.darwin.get_active_network_interface_name)
- description and source-code
```javascript
get_active_network_interface_name = function (cb) {
  var cmd = "netstat -rn | grep UG | awk '{print $6}'";
  exec(cmd, function(err, stdout) {
    if (err) return cb(err);

    var raw = stdout.toString().trim().split('\n');
    if (raw.length === 0 || raw === [''])
      return cb(new Error('No active network interface found.'));

    cb(null, raw[0]);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.network.darwin.get_network_interfaces_list"></a>[function <span class="apidocSignatureSpan">network.darwin.</span>get_network_interfaces_list (cb)](#apidoc.element.network.darwin.get_network_interfaces_list)
- description and source-code
```javascript
get_network_interfaces_list = function (cb) {

  var count = 0,
      list  = [],
      nics  = os.networkInterfaces();

  function append_data(obj) {
    async.parallel([
      function(cb) {
        exports.gateway_ip_for(obj.name, cb)
      },
      function(cb) {
        exports.netmask_for(obj.name, cb)
      }
    ], function(err, results) {
      if (results[0]) obj.gateway_ip = results[0];
      if (results[1]) obj.netmask    = results[1];

      list.push(obj);
      --count || cb(null, list);
    })
  }

  exec('networksetup -listallhardwareports', function(err, out) {
    if (err) return cb(err);

    var blocks = out.toString().split(/Hardware/).slice(1);
    count = blocks.length;

    blocks.forEach(function(block) {
      var parts = block.match(/Port: (.+)/),
          mac   = block.match(/Address: ([A-Fa-f0-9:-]+)/),
          name  = block.match(/Device: (\w+)/);

      if (!parts || !mac || !name)
        return --count;

      var obj   = {},
          port  = parts[1];

      obj.name  = name[1];
      // obj.desc  = port;
      obj.type  = determine_nic_type(port);
      obj.ip_address  = null;
      obj.mac_address = mac[1];

      (nics[obj.name] || []).forEach(function(type) {
        if (type.family == 'IPv4') {
          obj.ip_address = type.address;
        }
      });

      append_data(obj);
    })

    if (count == 0)
      cb(new Error('No interfaces found.'))
  })

}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.network.darwin.mac_address_for"></a>[function <span class="apidocSignatureSpan">network.darwin.</span>mac_address_for (nic_name, cb)](#apidoc.element.network.darwin.mac_address_for)
- description and source-code
```javascript
mac_address_for = function (nic_name, cb) {
  var cmd = "networksetup -getmacaddress " + nic_name + " | awk '{print $3}'";
  trim_exec(cmd, cb);
}
```
- example usage
```shell
...
var count = 0,
    list = [],
    nics = os.networkInterfaces();

function append_data(obj) {
  async.parallel([
    function(cb) {
      exports.mac_address_for(obj.name, cb)
    },
    function(cb) {
      exports.gateway_ip_for(obj.name, cb)
    },
    function(cb) {
      exports.netmask_for(obj.name, cb)
    },
...
```

#### <a name="apidoc.element.network.darwin.netmask_for"></a>[function <span class="apidocSignatureSpan">network.darwin.</span>netmask_for (nic_name, cb)](#apidoc.element.network.darwin.netmask_for)
- description and source-code
```javascript
netmask_for = function (nic_name, cb) {
  var cmd = "ipconfig getoption " + nic_name + " subnet_mask";
  trim_exec(cmd, cb);
}
```
- example usage
```shell
...

  function append_data(obj) {
async.parallel([
  function(cb) {
    exports.gateway_ip_for(obj.name, cb)
  },
  function(cb) {
    exports.netmask_for(obj.name, cb)
  }
], function(err, results) {
  if (results[0]) obj.gateway_ip = results[0];
  if (results[1]) obj.netmask    = results[1];

  list.push(obj);
  --count || cb(null, list);
...
```



# <a name="apidoc.module.network.linux"></a>[module network.linux](#apidoc.module.network.linux)

#### <a name="apidoc.element.network.linux.gateway_ip_for"></a>[function <span class="apidocSignatureSpan">network.linux.</span>gateway_ip_for (nic_name, cb)](#apidoc.element.network.linux.gateway_ip_for)
- description and source-code
```javascript
gateway_ip_for = function (nic_name, cb) {
  trim_exec("ip r | grep " + nic_name + " | grep default | cut -d ' ' -f 3", cb);
}
```
- example usage
```shell
...
var count = 0,
    list  = [],
    nics  = os.networkInterfaces();

function append_data(obj) {
  async.parallel([
    function(cb) {
      exports.gateway_ip_for(obj.name, cb)
    },
    function(cb) {
      exports.netmask_for(obj.name, cb)
    }
  ], function(err, results) {
    if (results[0]) obj.gateway_ip = results[0];
    if (results[1]) obj.netmask    = results[1];
...
```

#### <a name="apidoc.element.network.linux.get_active_network_interface_name"></a>[function <span class="apidocSignatureSpan">network.linux.</span>get_active_network_interface_name (cb)](#apidoc.element.network.linux.get_active_network_interface_name)
- description and source-code
```javascript
get_active_network_interface_name = function (cb) {
  var cmd = "netstat -rn | grep UG | awk '{print $NF}'";
  exec(cmd, function(err, stdout) {
    if (err) return cb(err);

    var raw = stdout.toString().trim().split('\n');
    if (raw.length === 0 || raw === [''])
      return cb(new Error('No active network interface found.'));

    cb(null, raw[0]);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.network.linux.get_network_interfaces_list"></a>[function <span class="apidocSignatureSpan">network.linux.</span>get_network_interfaces_list (cb)](#apidoc.element.network.linux.get_network_interfaces_list)
- description and source-code
```javascript
get_network_interfaces_list = function (cb) {

  var count = 0,
      list = [],
      nics = os.networkInterfaces();

  function append_data(obj) {
    async.parallel([
      function(cb) {
        exports.mac_address_for(obj.name, cb)
      },
      function(cb) {
        exports.gateway_ip_for(obj.name, cb)
      },
      function(cb) {
        exports.netmask_for(obj.name, cb)
      },
      function(cb) {
        exports.interface_type_for(obj.name, cb)
      }
    ], function(err, results) {
      if (results[0]) obj.mac_address = results[0];
      if (results[1]) obj.gateway_ip  = results[1];
      if (results[2]) obj.netmask     = results[2];
      if (results[3]) obj.type        = results[3];

      list.push(obj);
      --count || cb(null, list);
    })
  }

  for (var key in nics) {
    if (key != 'lo0' && key != 'lo' && !key.match(/^tun/)) {

      count++;
      var obj = { name: key };

      nics[key].forEach(function(type) {
        if (type.family == 'IPv4') {
          obj.ip_address = type.address;
        }
      });

      append_data(obj);
    }
  }

  if (count == 0)
    cb(new Error('No interfaces found.'))
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.network.linux.interface_type_for"></a>[function <span class="apidocSignatureSpan">network.linux.</span>interface_type_for (nic_name, cb)](#apidoc.element.network.linux.interface_type_for)
- description and source-code
```javascript
interface_type_for = function (nic_name, cb) {
  exec('cat /proc/net/wireless | grep ' + nic_name, function(err, out) {
    return cb(null, err ? 'Wired' : 'Wireless')
  })
}
```
- example usage
```shell
...
  function(cb) {
    exports.gateway_ip_for(obj.name, cb)
  },
  function(cb) {
    exports.netmask_for(obj.name, cb)
  },
  function(cb) {
    exports.interface_type_for(obj.name, cb)
  }
], function(err, results) {
  if (results[0]) obj.mac_address = results[0];
  if (results[1]) obj.gateway_ip  = results[1];
  if (results[2]) obj.netmask     = results[2];
  if (results[3]) obj.type        = results[3];
...
```

#### <a name="apidoc.element.network.linux.mac_address_for"></a>[function <span class="apidocSignatureSpan">network.linux.</span>mac_address_for (nic_name, cb)](#apidoc.element.network.linux.mac_address_for)
- description and source-code
```javascript
mac_address_for = function (nic_name, cb) {
  var cmd = 'cat /sys/class/net/' + nic_name + '/address';
  trim_exec(cmd, cb);
}
```
- example usage
```shell
...
var count = 0,
    list = [],
    nics = os.networkInterfaces();

function append_data(obj) {
  async.parallel([
    function(cb) {
      exports.mac_address_for(obj.name, cb)
    },
    function(cb) {
      exports.gateway_ip_for(obj.name, cb)
    },
    function(cb) {
      exports.netmask_for(obj.name, cb)
    },
...
```

#### <a name="apidoc.element.network.linux.netmask_for"></a>[function <span class="apidocSignatureSpan">network.linux.</span>netmask_for (nic_name, cb)](#apidoc.element.network.linux.netmask_for)
- description and source-code
```javascript
netmask_for = function (nic_name, cb) {
  var cmd = "ifconfig " + nic_name + " 2> /dev/null | egrep 'netmask|Mask:' | awk '{print $4}' | sed 's/Mask://'";
  trim_exec(cmd, cb);
}
```
- example usage
```shell
...

  function append_data(obj) {
async.parallel([
  function(cb) {
    exports.gateway_ip_for(obj.name, cb)
  },
  function(cb) {
    exports.netmask_for(obj.name, cb)
  }
], function(err, results) {
  if (results[0]) obj.gateway_ip = results[0];
  if (results[1]) obj.netmask    = results[1];

  list.push(obj);
  --count || cb(null, list);
...
```



# <a name="apidoc.module.network.win32"></a>[module network.win32](#apidoc.module.network.win32)

#### <a name="apidoc.element.network.win32.gateway_ip_for"></a>[function <span class="apidocSignatureSpan">network.win32.</span>gateway_ip_for (nic_name, cb)](#apidoc.element.network.win32.gateway_ip_for)
- description and source-code
```javascript
gateway_ip_for = function (nic_name, cb) {
  get_wmic_ip_value('DefaultIPGateway', nic_name, cb);
}
```
- example usage
```shell
...
var count = 0,
    list  = [],
    nics  = os.networkInterfaces();

function append_data(obj) {
  async.parallel([
    function(cb) {
      exports.gateway_ip_for(obj.name, cb)
    },
    function(cb) {
      exports.netmask_for(obj.name, cb)
    }
  ], function(err, results) {
    if (results[0]) obj.gateway_ip = results[0];
    if (results[1]) obj.netmask    = results[1];
...
```

#### <a name="apidoc.element.network.win32.get_active_network_interface_name"></a>[function <span class="apidocSignatureSpan">network.win32.</span>get_active_network_interface_name (cb)](#apidoc.element.network.win32.get_active_network_interface_name)
- description and source-code
```javascript
get_active_network_interface_name = function (cb) {
  wmic.get_value('nic', 'NetConnectionID', 'NetConnectionStatus = 2', cb);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.network.win32.get_network_interfaces_list"></a>[function <span class="apidocSignatureSpan">network.win32.</span>get_network_interfaces_list (callback)](#apidoc.element.network.win32.get_network_interfaces_list)
- description and source-code
```javascript
get_network_interfaces_list = function (callback) {

  var list = [],
      node_nics = os.networkInterfaces();

  wmic.get_list('nic', function(err, nics) {
    if (err) return callback(err);

    nics.forEach(function(nic){
      if (nic.Name && nic.NetConnectionID != '' && nic.MACAddress != '') {

        var obj = {
          name: nic.NetConnectionID,
          // description: nic.Name,
          mac_address: nic.MACAddress,
          ip_address: nic.IPAddress,
          vendor: nic.Manufacturer,
          model: nic.Description,
          type: nic.Name.match(/wi-?fi|wireless/i) ? 'Wireless' : 'Wired'
        }

        var node_nic = node_nics[obj.name] || [];

        node_nic.forEach(function(type){
          if (type.family == 'IPv4') {
            obj.ip_address = type.address;
          }
        });

        list.push(obj);
      }
    })

    callback(null, list);
  });

}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.network.win32.mac_address_for"></a>[function <span class="apidocSignatureSpan">network.win32.</span>mac_address_for (nic_name, cb)](#apidoc.element.network.win32.mac_address_for)
- description and source-code
```javascript
mac_address_for = function (nic_name, cb) {
  var cond = 'NetConnectionID = \'' + nic_name + '\'';
  wmic.get_value('nic', 'MACAddress', cond, cb);
}
```
- example usage
```shell
...
var count = 0,
    list = [],
    nics = os.networkInterfaces();

function append_data(obj) {
  async.parallel([
    function(cb) {
      exports.mac_address_for(obj.name, cb)
    },
    function(cb) {
      exports.gateway_ip_for(obj.name, cb)
    },
    function(cb) {
      exports.netmask_for(obj.name, cb)
    },
...
```

#### <a name="apidoc.element.network.win32.netmask_for"></a>[function <span class="apidocSignatureSpan">network.win32.</span>netmask_for (nic_name, cb)](#apidoc.element.network.win32.netmask_for)
- description and source-code
```javascript
netmask_for = function (nic_name, cb) {
  get_wmic_ip_value('IPSubnet', nic_name, cb);
}
```
- example usage
```shell
...

  function append_data(obj) {
async.parallel([
  function(cb) {
    exports.gateway_ip_for(obj.name, cb)
  },
  function(cb) {
    exports.netmask_for(obj.name, cb)
  }
], function(err, results) {
  if (results[0]) obj.gateway_ip = results[0];
  if (results[1]) obj.netmask    = results[1];

  list.push(obj);
  --count || cb(null, list);
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
