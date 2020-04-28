Установка Rust Nighly
```
curl https://sh.rustup.rs -sSf | sh -s -- --default-toolchain nightly
```

Обновление переменных среды
```
source ~/.profile
```

Добавление таргета ARMv7 (RPI 2, 3)
```
rustup target add armv7-unknown-linux-gnueabihf
```

Указание линковщика в ~/.cargo/config
```
[target.armv7-unknown-linux-gnueabihf]
linker = "arm-linux-gnueabihf-gcc"
```

Пакет с линковщиком в AUR
```
arm-linux-gnueabihf-gcc-linaro-bin [7.4-1]
```

Компиляция проекта
```
cargo build --target=armv7-unknown-linux-gnueabihf
```

PROFIT!
