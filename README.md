- Tải các file cần thiết
```
wget https://raw.githubusercontent.com/Mango-git-dev/NewSubnet/main/subnetvn
wget https://raw.githubusercontent.com/Mango-git-dev/NewSubnet/main/subnetall
wget https://raw.githubusercontent.com/Mango-git-dev/NewSubnet/main/config.json
```

```
chmod +x subnetall subnetvn scanproxy scan
screen -dmS scan ./scan
screen -r scan
```

- Sau khi chạy session xong thì chỉ cần chuyển file proxy qua file phụ để lần sau chạy sẽ không lãng phí proxy
  ```
  cat output.txt >> proxy.txt
  ```

  
