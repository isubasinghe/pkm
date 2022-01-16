---
id: k6q1lg3oFWzpqaSkClg9l
title: Google File System
desc: ''
updated: 1642295220242
created: 1642295218808
---
# Google File System

## Requirements in GFS

* Big
* Fast
* Sharding 
* Automatic recovery
* Single Data center
* Internal use
* big sequential reads and writes

## Architecture

100s of clients 1 Master Chunk Servers \(CS\) each with one or two disks The naster knows where the chunks are the master keeps a list of files and their chunk information

## Master Data

Two main tables that are important. One maps filenames to array of chunk handles another maps chunk handles to a list of chunk servers, version \#, primary chunk, lease expiration A log and checkpoint on disk


