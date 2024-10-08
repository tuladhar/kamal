# Kamal: Deploy web apps anywhere

### Fork of Kamal with enhanced Dockerfile to add CLI binaries for supported password managers.

| Name  |  Binary Path |   Version | 
|---|---|---|
| 1Password  | `/usr/local/bin/op`  |  `2.30.0`
| Bitwarden  | `/usr/local/bin/bw`  | `2024.9.0`
| LastPass  | `/usr/bin/lpass`  | `1.3.3`

> [!NOTE]
> While [enchancement PR](https://github.com/basecamp/kamal/pull/1075) is pending review, feel free to use the below unofficial Docker image from my repository.
```sh
docker pull ptuladhar/kamal:latest
```

```sh
$ docker run -it --entrypoint sh ptuladhar/kamal:latest
/workdir # lpass --version
LastPass CLI v1.3.3.GIT
$ /workdir # op --version
2.30.0
$ /workdir # bw --version
Could not find dir, "/root/.config/Bitwarden CLI"; creating it instead.
Could not find data file, "/root/.config/Bitwarden CLI/data.json"; creating it instead.
2024.9.0
```

## License

Kamal is released under the [MIT License](https://opensource.org/licenses/MIT).
