FROM biocontainers/biocontainers:vdebian-buster-backports_cv1
MAINTAINER biocontainers <biodocker@gmail.com>
LABEL    software="wise" \ 
    base_image="biocontainers/biocontainers:vdebian-buster-backports_cv1" \ 
    container="wise" \ 
    about.summary="comparison of biopolymers, like DNA and protein sequences" \ 
    about.home="http://www.ebi.ac.uk/~birney/wise2/" \ 
    software.version="2.4.1-21-deb" \ 
    upstream.version="2.4.1" \ 
    version="1" \ 
    extra.identifiers.biotools="wise" \ 
    about.copyright=" 1996-2001 Genome Research Limited (GRL) and" \ 
    about.license="GRL" \ 
    about.license_file="/usr/share/doc/wise/copyright" \ 
    extra.binaries="/usr/bin/dba,/usr/bin/dnal,/usr/bin/estwise,/usr/bin/estwisedb,/usr/bin/genewise,/usr/bin/genewisedb,/usr/bin/genomewise,/usr/bin/promoterwise,/usr/bin/psw,/usr/bin/pswdb,/usr/bin/scanwise,/usr/bin/scanwise_server" \ 
    about.tags="field::biology, field::biology:bioinformatics, implemented-in::c,:commandline, role::program, scope::utility, use::comparing,:TODO" 

USER root
ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update && (apt-get install -t buster-backports -y wise || apt-get install -y wise) && apt-get clean && apt-get purge && rm -rf /var/lib/apt/lists/* /tmp/*
USER biodocker
