FROM ubuntu:20.04

RUN apt update && \
    apt install wget gnupg2 -y && \
    # Register the packagecloud key
    wget -O - https://packagecloud.io/gpg.key | apt-key add - && \
    # Add deb http://packages.blackfire.io/debian any main to /etc/apt/sources.list.d/blackfire.list
    echo "deb http://packages.blackfire.io/debian any main" | tee /etc/apt/sources.list.d/blackfire.list && \
    # Update the repositories
    apt-key adv --keyserver keyserver.ubuntu.com --recv-keys 696DBE66A72D76DA && \
    apt update && \
    # Install the blackfire-agent package
    apt install blackfire-agent -y && \
    # Remove unnecessary packages and clean apt cache
    apt purge gnupg2 wget -y && \
    apt autopurge -y && \
    apt clean

ENTRYPOINT ["blackfire-agent"]