# AdoptOpenJDK JRE Build

This is a minimal JRE build based on Ubuntu and AdoptOpenJDK JRE 11, with an addon for ssl and running as a non root user.

### Create Master country signing cert

You can validate and convert the German CSCA by downloading the following files to a subdirectory called 'german' then running:

docker run -it -v $PWD/german/:/tmp/ -v $PWD/output/:/certs/ digitapatterns/jre:latest /app/csca_to_ks.sh /tmp/20200709_DEMasterList.ml /tmp/csca-germany_05-2019_self_signed.cer

--note
The German master list can be obtained here [https://www.bsi.bund.de/EN/Topics/ElectrIDDocuments/securPKI/securCSCA/Root_Certificate/cscaGermany_node.html](German master list)


![Publish Docker](https://github.com/DigitalPatterns/jre/workflows/Publish%20Docker/badge.svg)
