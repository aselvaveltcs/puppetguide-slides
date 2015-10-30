# Essential Puppet concepts

When approaching Puppet it's important to understand it's basic concepts and terminology.

A complete official [glossary](http://docs.puppetlabs.com/references/glossary.html) is online, use it.

Here we outline a few essential Puppet concepts, be sure to understand them all:

- A typical Puppet setup is based on a client-server architecture: the client is also called **agent** (or **agent node** or simply **node**), the server is called **master**
- When the puppet client connects to the server, it sends it's own ssl **certname** and a list of **facts** (units of information about the client's system generated by the command **facter**)
- Based on the client **certname** and its facts, the master replies with a **catalog** that describes what has to be configured on the client
- The catalog is based on Puppet code, which is written in **manifests** (files with **.pp** extension)
- In the Puppet code we declare **resources** that affect elements of the system (files, packages, services ...)
- Resources are grouped in **classes** which may expose **parameters** that affect their behavior.
- The values of the class parameters can be defined in different ways, one of them is **Hiera**
- **Hiera** is a very common and versatile tool to store the values of parameters

- Classes and the configuration files that are shipped to nodes are organized in **modules**.