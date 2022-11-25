# Gimana cara jalanin sonar di local?

## Siapin toolsnya dulu
1. Download sonar scanner [disini](https://docs.sonarcloud.io/advanced-setup/ci-based-analysis/sonarscanner-cli/)
2. Extract, dan tambahkan $install_directory/bin ke path config. Karena saya pakai linux, dan zshrc, saya tambahkan di `~/.zshrc`
    ```bash
    # APPEND PATH
    path+=('/home/ninoloid/populix/sonar-scanner-4.7.0.2747-linux/bin')
    export PATH
    ```
3. Pastikan di projectnya udah ada `sonar-project.properties`

## Gimana cara jalaninnya?
1. Clone repo ini
2. Jalanin `docker-compose up`
3. Buka [localhost:9000](http://localhost:9000)
4. Buka directory project yg mau di scan
5. Ketik `sonar-scanner` di terminal, lalu enter
6. Tunggu hasilnya. Balik lagi ke browser tab yg tadi sonarqube, cek hasilnya di tab Projects
