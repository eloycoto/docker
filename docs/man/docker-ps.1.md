% DOCKER(1) Docker User Manuals
% Docker Community
% JUNE 2014
# NAME
docker-ps - List containers

# SYNOPSIS
**docker ps**
[**-a**|**--all**[=*false*]]
[**--before**[=*BEFORE*]]
[**-f**|**--filter**[=*[]*]]
[**-l**|**--latest**[=*false*]]
[**-n**[=*-1*]]
[**--no-trunc**[=*false*]]
[**-q**|**--quiet**[=*false*]]
[**-s**|**--size**[=*false*]]
[**-x**|**--expanded**[=*false*]]
[**--since**[=*SINCE*]]


# DESCRIPTION

List the containers in the local repository. By default this show only
the running containers.

# OPTIONS
**-a**, **--all**=*true*|*false*
   Show all containers. Only running containers are shown by default. The default is *false*.

**--before**=""
   Show only container created before Id or Name, include non-running ones.

**-f**, **--filter**=[]
   Provide filter values. Valid filters:
                          exited=<int> - containers with exit code of <int>

**-l**, **--latest**=*true*|*false*
   Show only the latest created container, include non-running ones. The default is *false*.

**-n**=-1
   Show n last created containers, include non-running ones.

**--no-trunc**=*true*|*false*
   Don't truncate output. The default is *false*.

**-q**, **--quiet**=*true*|*false*
   Only display numeric IDs. The default is *false*.

**-s**, **--size**=*true*|*false*
   Display total file sizes. The default is *false*.

**--since**=""
   Show only containers created since Id or Name, include non-running ones.

**-x**=""
    Turn on the expanded formatting mode.

# EXAMPLES
# Display all containers, including non-running

    # docker ps -a
    CONTAINER ID        IMAGE                 COMMAND                CREATED             STATUS      PORTS    NAMES
    a87ecb4f327c        fedora:20             /bin/sh -c #(nop) MA   20 minutes ago      Exit 0               desperate_brattain
    01946d9d34d8        vpavlin/rhel7:latest  /bin/sh -c #(nop) MA   33 minutes ago      Exit 0               thirsty_bell
    c1d3b0166030        acffc0358b9e          /bin/sh -c yum -y up   2 weeks ago         Exit 1               determined_torvalds
    41d50ecd2f57        fedora:20             /bin/sh -c #(nop) MA   2 weeks ago         Exit 0               drunk_pike

# Display only IDs of all containers, including non-running

    # docker ps -a -q
    a87ecb4f327c
    01946d9d34d8
    c1d3b0166030
    41d50ecd2f57

# HISTORY
April 2014, Originally compiled by William Henry (whenry at redhat dot com)
based on docker.com source material and internal work.
June 2014, updated by Sven Dowideit <SvenDowideit@home.org.au>
August 2014, updated by Sven Dowideit <SvenDowideit@home.org.au>
