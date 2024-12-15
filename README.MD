# SSH Config

- B1: Cấu hình SSH Server
  - Cài SSH Server bằng lệnh:

    ```batch
    apt install openssh-server
    ```

  - Tìm dòng trong `PermitRootLogin` file `/etc/ssh/sshd_config`
  - Sửa giá trị thành `yes` *nếu có comment, thì bỏ dấu* `#` *ở đầu*
  - Khởi động `service` bằng lệnh

    ```batch
    systemctl restart sshd
    ```

  - Lấy IP server bằng lệnh

    ```batch
    ip addr show | grep inet | grep brd | awk '{print $2}' | cut -d'/' -f1
    ```

- B2: Cài SSH Client
  - Connect tới server bằng lệnh
        `IP` là IP server (trong LAN hoặc ngoài LAN)

    ```batch
    ssh root@<IP>
    ```

<!-- mint, kde -->