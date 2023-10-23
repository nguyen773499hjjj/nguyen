Log:
  Level: none # Log level: none, error, warning, info, debug
  AccessPath: # /etc/XrayR/access.Log
  ErrorPath: # /etc/XrayR/error.log
DnsConfigPath: # /etc/XrayR/dns.json # Path to dns config, check https://xtls.github.io/config/dns.html for help
RouteConfigPath: # /etc/XrayR/route.json # Path to route config, check https://xtls.github.io/config/routing.html for help
InboundConfigPath: # /etc/XrayR/custom_inbound.json # Path to custom inbound config, check https://xtls.github.io/config/inbound.html for help
OutboundConfigPath: # /etc/XrayR/custom_outbound.json # Path to custom outbound config, check https://xtls.github.io/config/outbound.html for help
ConnetionConfig:
  Handshake: 4 # Handshake time limit, Second
  ConnIdle: 30 # Connection idle time limit, Second
  UplinkOnly: 2 # Time limit when the connection downstream is closed, Second
  DownlinkOnly: 4 # Time limit when the connection is closed after the uplink is closed, Second
  BufferSize: 64 # The internal cache size of each connection, kB
Nodes: #Default XrayR config
   -
     PanelType: V2board
     ApiConfig:
       ApiHost: https://4gsieuviet.com
       ApiKey: nguyendznhatthegioi
       NodeID: 
       NodeType: V2ray
       Timeout: 30
       EnableVless: false
       EnableXTLS: false
       SpeedLimit: 0
       DeviceLimit: 2
       RuleListPath:
     ControllerConfig:
       ListenIP: 0.0.0.0
       SendIP: 0.0.0.0
       UpdatePeriodic: 60
       EnableDNS: false
       DNSType: AsIs
       EnableProxyProtocol: false
       AutoSpeedLimitConfig:
         Limit: 0
         WarnTimes: 0
         LimitSpeed: 0
         LimitDuration: 0
       RedisConfig:
         RedisEnable: false
         RedisAddr: 127.0.0.1:6379
         RedisPassword: PASSWORD
         RedisDB: 0
         Timeout: 5
         Expiry: 60
       CertConfig:
         CertMode: none
         CertDomain: none
         CertFile: /etc/XrayR/cert/server.pem
         KeyFile: /etc/XrayR/cert/privkey.key
         Provider: cloudflare
         Email: herotbty@gmail.com
         DNSEnv:
           CLOUDFLARE_EMAIL: aaa
           CLOUDFLARE_API_KEY: bbb
   -
     PanelType: V2board
     ApiConfig:
       ApiHost: https://4gsieuviet.com
       ApiKey: nguyendznhatthegioi
       NodeID: 
       NodeType: Trojan
       Timeout: 30
       EnableVless: false
       EnableXTLS: false
       SpeedLimit: 0
       DeviceLimit: 2
       RuleListPath:
     ControllerConfig:
       ListenIP: 0.0.0.0
       SendIP: 0.0.0.0
       UpdatePeriodic: 60
       EnableDNS: false
       DNSType: AsIs
       EnableProxyProtocol: false
       AutoSpeedLimitConfig:
         Limit: 0
         WarnTimes: 0
         LimitSpeed: 0
         LimitDuration: 0
       RedisConfig:
         RedisEnable: false
         RedisAddr: 127.0.0.1:6379
         RedisPassword: PASSWORD
         RedisDB: 0
         Timeout: 5
         Expiry: 60
       CertConfig:
         CertMode: file
         CertDomain: sg04.nhkvpn.com
         CertFile: /etc/XrayR/cert/server.pem
         KeyFile: /etc/XrayR/cert/privkey.key
         Provider: cloudflare
         Email: herotbty@gmail.com
         DNSEnv:
           CLOUDFLARE_EMAIL: aaa
           CLOUDFLARE_API_KEY: bbb
