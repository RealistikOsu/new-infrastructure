# Table of contents

- [Table of contents](#table-of-contents)
- [What are the motives behind the new infrastructure?](#what-are-the-motives-behind-the-new-infrastructure)
- [What does this new infrastructure entail?](#what-does-this-new-infrastructure-entail)
- [What can we expect from the new infrastructure?](#what-can-we-expect-from-the-new-infrastructure)
  - [A more stable experience](#a-more-stable-experience)
  - [A faster, more efficient experience](#a-faster-more-efficient-experience)
  - [More features, aswell as a higher likelihood for more features in the future](#more-features-aswell-as-a-higher-likelihood-for-more-features-in-the-future)
  - [A future.](#a-future)
- [What does this mean for servers which utilise RealistikOsu's current infrastructure?](#what-does-this-mean-for-servers-which-utilise-realistikosus-current-infrastructure)
- [I want it! How long will it take?](#i-want-it-how-long-will-it-take)
- [How will this new infrastructure work?](#how-will-this-new-infrastructure-work)
- [The end](#the-end)

# What are the motives behind the new infrastructure?

Since the beginning of RealistikOsu, many things have been changed, modified and rewritten to satisfy the server's needs as we get better as developers aswell as the player base grows. However, there is one thing that has never changed - the reliance on Ripple in some form. We currently rely on the Ripple ecosystem in a few ways - our website, API, bancho server and the worst of all: **database structure**. Ripple has served us well, however the code is outdated and inefficient and in need of new life. Furthermore, we would like to be able to containerize the entire server which will play a large part into how the new announced infrastructure will be designed.

# What does this new infrastructure entail?

The new infrastructure aims to rewrite all backend parts of the server, the frontend will not change. This new infrastructure will see not only a complete code rewrite but the introduction of new services and processes, aswell as an entirely new database structure. The new infrastructure will run on PostgreSQL instead of MySQL/MariaDB, with a key requirement of being entirely stateless so it can be ran in containers. Furthermore, all services must have stellar migrations to aid the process of containerization and continuous integration; we must be able to setup an instance at any time with no more than 2 commands (build and run).

# What can we expect from the new infrastructure?

This is probably the part people care about most, nobody wants to sit here and read pages and pages of writing without knowing the benefit to them. Since the new infrastructure is on the backend, noticable differences are not so simple to point out as most people will only see or care about the frontend (website) but there are very much a long list of benefits to the average user.

## A more stable experience

With a new infrastructure written entirely by ourselves, we will be much more familar with the code we are running and therefore will have an easier time fixing any potential bugs which may arise. Furthermore, with the extremely high standards we will withhold throughout this journey it will be incredibly difficult for bugs to pass through.

## A faster, more efficient experience

Aswell as things being more stable, the new infrastructure will run much more efficiently as it allows for load balancing aswell as optimisations as much as possible; we will use all the latest, efficient technologies such as asynchronous design in order to deliver the fastest experience to end users. This is something our current stack lacks in 90% of it's services, and it's something we take extreme pride in.

## More features, aswell as a higher likelihood for more features in the future

One of the key principles of the new infrastructure is to be easily extendible and as simple as possible, combining these factors will mean that implementing new features should be much easier than before. This means you should expect a very high standard from us when it comes to implementing suggestions or other cool ideas that anyone may have!

## A future.

This one sounds kinda stupid, and may be confused by the stability pointer. However, this is more talking about the future **past osu!**. Everyone knows that osu!lazer is just around the corner, and it's something we must openly consider when creating the new infrastructure. When osu!stable becomes obsolete, we do not want RealistikOsu to simply die and so there are compatibilities we must keep in mind. The new infrastructure will aim to make this migration process as painless as possible for when that time comes, so RealistikOsu can remain.

# What does this mean for servers which utilise RealistikOsu's current infrastructure?

Well, as any other server, we will have to undergo migrations in order to use the new infrastructure once it's ready. The entire new infrastructure will be open source, alongside anything required/used in order to move to the new infrastructure. This means that you too can be using our new infrastructure once it's ready!

# I want it! How long will it take?

Well, this is the **hardest** question of them all. It's hard to put an estimate on a project when it has so many things to consider as this new infrastructure digs deeper than just a code rewrite. Furthermore, you have to factor in our personal lives and not burning out. This new infrastructure will certainly be a large project, and for that reason it is important to not allow creating it to take over our lives too much or it will simply never happen.

The new infrastructure is a long term investment to give us something great which can essentially exist for aslong as osu! does - we really wish to pioneer the private server ecosystem.

This means the infrastructure could take months, or even longer, but time is not our biggest priority! We understand many people may be eager to have the new infrastructure as soon as possible, because it sounds great. However, I will assure you, if the correct time is not spent to perfect it - you will not receive the amazing results we promise.

A good example of this is osu!lazer. It started back in 2016, a long time ago, and it has always been a running meme that it will never release. It will release, and it is very close, much closer than people anticipate. The reason it took so long for it to get where it is, is nothing other than the same strive for perfection that we also share.

And so, please bare with the time it takes, it will be worth it!

# How will this new infrastructure work?

I'd like to also document how the entire new infrastructure is planned to work, what services it will have etc.

If you are not interested in the nerdy implementation side of things, then I suggest you don't read this section.

The new infrastructure is planned to be split into more services than before. This is to allow for better distribution, but also for specific features to be more efficient as they serve a single purpose.

There is a document similar to this one for each service (and their relevant processors) in the new infrastructure:

- [Bancho service](services/bancho.md)
- [Leaderboard service](services/leaderboards.md)
- [Score service](services/scores.md)
- [API service](services/api.md)

# The end

With everything explained, I would like to end off this document by thanking everyone on the RealistikOsu team aswell as the community for keeping the server active for as long as it has, and providing the motivation for the future. I hope we have a long time ahead of us with many great times :D

~ tsunyoku, and the RealistikOsu team