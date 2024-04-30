# local readme
```bash
# run vinca:
vinca --multiple --platform linux-64 -n

# run boa:
boa build additional_recipes/ros-distro-mutex -m ./conda_build_config.yaml
boa build additional_recipes/ros-noetic-eigenpy -m ./conda_build_config.yaml
boa build recipes -m ./conda_build_config.yaml --skip-existing --no-test --continue-on-failure

# run upload:
anaconda login
# input user name and password
anaconda upload *.tar.bz2 --skip-existing -u ros-noetic-py10
```
## make patch
```bash
cd build dir
change files
git diff > xxx.patch
put it in patchs folder
```
