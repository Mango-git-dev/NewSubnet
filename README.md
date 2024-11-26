- Cách để quét 2000-5000 proxy http,https,socks4,socks5 đang hoạt động

- Config
```
 {
  "check-site": "https://google.com",
  "proxy-type": "http",

  "http_threads": 2000,
  "headers": {
    "user-agent": "Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/102.0.5005.115 Safari/537.36",
    "accept": "text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8"
  },
  "print_ips": {
    "enabled": true,
    "display-ip-info": true
  },
  "timeout": {
    "http_timeout": 5,
    "socks4_timeout": 5,
    "socks5_timeout": 5
  }
}
```

- Flag Args
```
-p <port> - Port you want to scan.
-o <proxies.txt> - Writes proxy hits to file.
-input <proxies.txt> - Loads the proxy list and checks it.
-url https://api.com/proxies - Loads the proxies from an api and checks it.
```

- Tải các file cần thiết
```
wget https://raw.githubusercontent.com/Mango-git-dev/NewSubnet/main/scan
wget https://raw.githubusercontent.com/Mango-git-dev/NewSubnet/main/subnetvn
wget https://raw.githubusercontent.com/Mango-git-dev/NewSubnet/main/config.json
```

- Yêu cầu:
```
Screen
Golang
Zmap
```

```
chmod +x subnetvn scan
screen -dmS scan ./scan
screen -r scan
```

- Sau khi chạy session xong thì chỉ cần chuyển file proxy qua file phụ để lần sau chạy sẽ không lãng phí proxy
  ```
  cat output.txt >> proxy.txt
  ```

  
