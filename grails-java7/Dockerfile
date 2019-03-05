FROM openjdk:7-jdk
MAINTAINER Canadensys IT <canadensys.network@gmail.com>

RUN apt-get --quiet update \
 && apt-get -qqy install \
    groovy \
 && apt-get clean \
 && apt-get purge \
 && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

# Set customizable env vars defaults.
#ENV GRAILS_VERSION 2.3.11
ENV GRAILS_VERSION ${grails_version}

# Install Grails
WORKDIR /usr/lib/jvm
ADD https://github.com/grails/grails-core/releases/download/v${GRAILS_VERSION}/grails-${GRAILS_VERSION}.zip /usr/lib/jvm
RUN unzip grails-${GRAILS_VERSION}.zip && \
    rm -rf grails-${GRAILS_VERSION}.zip && \
    ln -s grails-${GRAILS_VERSION} grails

# Setup Grails path.
ENV GRAILS_HOME /usr/lib/jvm/grails
ENV PATH $GRAILS_HOME/bin:$PATH

# Create App Directory
RUN mkdir /app
WORKDIR /app

# Set Default Behavior
ENTRYPOINT ["grails"]
