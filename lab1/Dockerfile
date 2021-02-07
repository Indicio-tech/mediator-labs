FROM bcgovimages/von-image:py36-1.15-0

RUN pip3 install git+https://github.com/hyperledger/aries-cloudagent-python.git@81b41b6a0a8953720dface27ac33e22d1217a53f
RUN pip3 install git+https://github.com/hyperledger/aries-acapy-plugin-toolbox.git@6b594fd328874643ac04567819c9fa1f0239ad8e
ADD configs/ configs/

ENTRYPOINT ["/bin/bash", "-c", "aca-py \"$@\"", "--"]
