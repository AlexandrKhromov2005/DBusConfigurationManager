### Установка `sdbus-c++` 

```bash
sudo apt update
sudo apt install -y git cmake g++ pkg-config libsystemd-dev ninja-build

# Клонируем репозиторий
git clone https://github.com/Kistler-Group/sdbus-cpp.git
cd sdbus-cpp

# Сборка и установка
mkdir build && cd build
cmake .. -G Ninja -DCMAKE_BUILD_TYPE=Release -DCMAKE_INSTALL_PREFIX=/usr
ninja
sudo ninja install
````

---

### Установка `clang-format`

```bash
sudo apt install -y clang-format
```

Проверка версии:

```bash
clang-format --version
```