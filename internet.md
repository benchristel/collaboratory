# Internet: The Bad Parts

- security
  - people don't understand security / crypto
  - engineers don't even understand crypto
  - even the people who dedicate their lives to crypto make mistakes
  - no matter how good the technical solution is, humans will still choose "password" as their password.
- time is local
  - my system clock time is not the same as yours
  - it never will be
  - time zones are evil
  - UTC is just a band-aid. Once we start networking between computers that are moving at relativistic speeds, our whole concept of time will have to be thrown out, so we'd better get used to doing without it.
- networks can fail
  - handling failures gracefully in end-user UIs takes extra effort
  - handling failures in distributed systems is a subject for many, many PhD theses
- networks are slow
- networks are low-bandwidth
  - contributes to the difficulty of API design; you can't just send your whole database over the wire, so you compromise.
- public APIs are rigid
- the whole concept of dev/acceptance/test/staging/prod environments. The whole concept of dev/prod parity being a thing that has to be designed, managed, monitored
- devs having to schedule time on remote machines in order to verify that their code works, because their workstations aren't  sufficiently similar to a "real" environment.
- getting paged in the middle of the night because a disk filled up with logs

People may read the above litany of grievances and think "so what? That's just the way computers are, so we'll just have to deal." But no, it's not just the way computers are. All of those problems are specific to the Internet, and even more specifically, to the way the Internet is used to support modern web and mobile applications. It doesn't have to be this way.

In much the same way that the automobile transformed our cities and suburbs, the Internet has transformed software development. It's permeated our development processes, our favored architectures, and our understanding of the systems we build to such an extent that now we can't imagine that it could be any other way.

But the fact is, computers are not built to be internet portals. Computers _compute_. And we can keep on _computing_, without HTTPS or JodaTime or ReactiveX or REST or any of it.

The rest of this post is a modest proposal to re-somethingorother The Good Parts of the Internet.

# The web is a content distribution platform

It is good at
  - letting you download files and software from servers far away

It is bad at
  - letting the state for your application live thousands of miles away from the CPU executing the code
  - knowing who is requesting a resource and whether they have permission to do so
  - synchronizing running programs that are all supposed to reflect the same underlying facts about the universe

Why is it so popular?

- communication
- collaboration
- "better than nothing"

Can we get rid of it?

I work for a company (a _software company_) that avoids email and prefers face-to-face communication whenever possible.

You can totally collaborate without the internet.