
# Table of Contents

1.  [SqueakHOWTO [SqueakHOWTOHelp]](#org9c57090)
    1.  [Introduction](#orgbafb293)
    2.  [Howto Fix RTPRIO stuff](#orge47880c)
    3.  [Howto Fix Expired SSL Cert Issue In Monticello](#org970eb48)


<a id="org9c57090"></a>

# SqueakHOWTO [SqueakHOWTOHelp]


<a id="orgbafb293"></a>

## Introduction

    This is catch-all help for odd-ball squeak HOWTO issues.


<a id="orge47880c"></a>

## Howto Fix RTPRIO stuff

    have at it folks!


<a id="org970eb48"></a>

## Howto Fix Expired SSL Cert Issue In Monticello

    
    Context: On October 1 2021 Monticello would not let me open the squeaksource.com  repository.
    
    After much emailing at the board, it was determined that ...
    1. squeaksource.com uses a funky certificate provider or something.
    2. the problem was on my (a typical user) side of things.
    3. this website gives us hoops to jump through:  https://www.openssl.org/blog/blog/2021/09/13/LetsEncryptRootCertExpire/
    
    
    
    This fix worked for me:
    
    su root
    cd /etc/ssl/certs.
    update-ca-certificate
    mv DST_Root_CA_X3.pem  ~/   (or delete it)

