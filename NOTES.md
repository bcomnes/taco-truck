


```
13:46 <bret> have you cats done anything wrt remote execution and https://github.com/maxogden/taco ?
13:47 <@ogd> bret: just ssh stuff
13:47 <@ogd> bret: is that waht you mean?
13:47 <bret> eg agent less remote execution
13:48 <bret> the examples need the taco programs to be installed remotely right?
13:49 <bret> i was looking at ways for boostrapping new servers and all the tools are either ruby or python and totally ugly
13:50 <@ogd> bret: oh yea i used to have a bootstrap script that installed node and taco over ssh but its no longer maintained
13:51 <bret> whats it called, mind if I take a look?
13:52 <@ogd> bret: https://github.com/maxogden/taco/blob/6dd068373eefae97bc5596b83827610116713a88/bootstrap.sh
13:52 <@ogd> bret: i the two install- things are on npm
13:52 <bret> cool ty
13:53 <@ogd> bret: and the last one is https://github.com/maxogden/taco/blob/6dd068373eefae97bc5596b83827610116713a88/package.json#L10
13:53 <@ogd> bret: also theres instructions in that old readme
13:53 <@ogd> bret: if you get something good working again feel free to PR it to the readme. i just felt my bootstrap was a little too opinionated (ubuntu only etc) and i also havent even used it in a while, so i removed it
```

https://github.com/maxogden/install-nginx-on-ubuntu
https://github.com/maxogden/install-node-on-ubuntu
http://docs.ansible.com/ansible/index.html
https://github.com/maxogden/taco
https://github.com/maxogden/taco-mon
https://github.com/mafintosh/taco-pack
https://github.com/mafintosh/taco-build
https://github.com/mafintosh/taco-nginx


## Minimal Viable OS Support

- OS X
- Archlinux

## Nice to have

- Windows
- Ubuntu/Debian
- Centos

## To the moon

- CoreOS
