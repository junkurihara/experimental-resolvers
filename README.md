# Experimental resolvers of DNSCrypt v2 and relays of PoC &mu;ODNS

This repo provides lists of experimental resolvers and relays for our experimental project called **&mu;ODNS** that is a **multiple-relay-based anonymization protocol for DNS queries**. Servers listed in this repo have been deployed with our PoC implementation given [here](https://github.com/junkurihara/dnscrypt-proxy-modns).

Our &mu;ODNS has been designed to protect user privacy in DNS even if a relay(s) colludes with a resolver(s), which cannot be solved in existing DNS anonymization protocols. For the detailed information of &mu;ODNS, please refer to our concept paper below:

> Jun Kurihara and Takeshi Kubo, ''Mutualized oblivious DNS (&mu;ODNS): Hiding a tree in the wild forest,'' Apr. 2021. [https://arxiv.org/abs/2104.13785](https://arxiv.org/abs/2104.13785)

**Relays and resolvers listed in this repo may stop sometimes for maintenance.** Source codes for PoC implementations of &mu;ODNS are now publicly available.

- relay: https://github.com/junkurihara/encrypted-dns-server-modns

- client: https://github.com/junkurihara/dnscrypt-proxy-modns

## Contributing (Make your own relay public for user anonymity)

If you deploy your own relay on the Internet and want to public for the concept of &mu;ODNS, please make a PR to `relays.md`. We shall check, sign and publish it!

## DoH-&mu;ODNS translator just for testing

> **THIS TRANSLATOR IS NOT AVAILABLE NOW.**
> Please use our PoC implementation of &mu;ODNS for your own relay and resolver.

~~If you want to just check if it works, you can try our DoH-&mu;ODNS translator from Chrome and Firefox browsers without using the above client. The translator converts DoH queries to PoC &mu;ODNS queries. It first works as the 'first-hop' relay of &mu;ODNS, and randomly choose subsequent (up to 2) relays from listed relays for user anonymity in DNS queries. The DoH address is:~~

~~> https://dns.secarchlab.net/dns-query~~

~~Target full-service resolvers are ones listed in this repo and Quad9 servers of no-filters.~~

~~**NOTE**: Although our experimental resolvers and relays are ones with no log and no filter, **the DoH-&mu;ODNS filters some content by using public ad lists and logs blocking histories.** Please use this translator only for testing at your own risk, and do not use this translator for your private activity. From the concept of &mu;ODNS, you should build your dedicated relay. Also note that **it is not guaranteed that our translator works 24/365.**~~
