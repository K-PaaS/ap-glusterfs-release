## ap-glusterfs-release
### Application Platform Glusterfs Release Configuration
  - mysql : 1 machine   
  - ap-glusterfs-broker : 1 machine

### Create Application Platform Glusterfs Release
  - Download the latest Application Platform Glusterfs Release
    ```   
    $ git clone https://github.com/K-PaaS/ap-glusterfs-release.git
    $ cd ap-glusterfs-release

    $ wget -O src.zip  https://nextcloud.k-paas.org/index.php/s/GTAKzHoTnjaEzGd/download
    $ unzip src.zip
    $ rm -rf src.zip   
    ```   
  - Create Application Platform Glusterfs Release
    ```   
    ## <VERSION> :: release version (e.g. 2.1.0)   
    ## <RELEASE_TARBALL_PATH> :: release file path (e.g. /home/ubuntu/workspace/ap-glusterfs-release-<VERSION>.tgz)
    $ bosh -e <bosh_name> create-release --name=ap-glusterfs --version=<VERSION> --tarball=<RELEASE_TARBALL_PATH> --force
    ```    
  - [참고] submodule update
    ```
    $ git submodule sync --recursive && git submodule foreach --recursive git submodule sync  && git submodule update --init --recursive
    ```
### Deployment   
- https://github.com/K-PaaS/service-deployment


## Contributors ✨
<a href="https://github.com/K-PaaS/ap-glusterfs-release/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=K-PaaS/ap-glusterfs-release" />
</a>
