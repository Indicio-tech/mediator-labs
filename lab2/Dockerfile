FROM bcgovimages/von-image:py36-1.15-0

RUN pip3 install git+https://github.com/hyperledger/aries-cloudagent-python.git@81b41b6a0a8953720dface27ac33e22d1217a53f
RUN pip3 install git+https://github.com/hyperledger/aries-acapy-plugin-toolbox.git@6b594fd328874643ac04567819c9fa1f0239ad8e
ADD configs/ configs/
USER root
ADD https://github.com/stedolan/jq/releases/download/jq-1.6/jq-linux64 ./jq
RUN chmod +x ./jq
COPY ngrok-wait.sh wait.sh
RUN chmod +x ./wait.sh
USER $user

ENTRYPOINT ["/bin/bash", "-c", "./wait.sh aca-py \"$@\"", "--"]
