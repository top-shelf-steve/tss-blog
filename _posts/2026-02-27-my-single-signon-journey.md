---
layout: post
title: "My Single Sign-On Journey"
date: 2026-02-27 14:59:18 -0400
---

I was pretty deep into my IT career before I really understood single sign-on (SSO). Sure, I understood *generally* what SSO was: "use your corporate credentials to sign into \<x\> application".

In all fairness... that's exactly what it is BUT the importance of SSO goes much deeper than that, and it was something I didn't quite realize until I was put on a project where I had to configure literally hundreds of SSO applications during an identity provider migration.

If you were to ask me today how I felt about configuring SSO for applications I would say honestly, that I really enjoy it. I'm not sure if that is because it was brutally beat into me or if deep down there was already some connection I wasn't aware of.

Boiled down to its simplest form SSO configuration is quite easy. For the most part (though some protocols make this easier than others) it's essentially the classic, "have your people call my people, and I'll have my people call your people".

One gets a "metadata" file from a 3rd party application (SalesForce, Zoom, Asana, etc.) and import it into identity provider of choice (Microsoft Entra in my case), send my metadata file over to the application and that's *usually* all it takes (some applications are much better than others in this regard).

Once that connection is made though the benefits immediately reveal themselves. The management headache turns down dramatically. Users no longer have to keep track of separate logins for the application. Even better, when someone leaves the company, there's no longer the worry that they will still have access to the application when someone forgets to deactivate them. When the account is disabled in Entra, they'll lose access to the application as well. Bring SCIM (automated user provisioning, stay tuned for posts on this specifically) into the mix of all this and it becomes a thing of beauty.

Mid and large sized companies can have hundreds of SaaS applications. Even smaller companies will often have dozens of SaaS applications. The headache of having to create and manage accounts within those applications goes away, the security concerns reduce, and users no longer have to have separate logins for every single 3rd party application (and let's be real, password reuse is most likely happening here).

Dynamic groups, SSO, automated user provisioning can be a real dream. A new hire in \<x\> department gets put into a group automatically based on their job title (or anything), which then enables sign in access for the application(s), along with automatic user provisioning which then automatically creates the account(s) for them. Cleanup also becomes nonexistent because when the user leaves, they're removed from the target application and access is revoked.

Much of my focus these days is in the identity space. I'm looking forward to putting out some guides, useful information, tips I have picked up along the way for configuring single sign-on applications. The identity space is constantly evolving and I'm excited to share what I have learned (and continue to learn). Single sign-on always felt like the *boring* side of identity (and IT in general) to me, but after years of configuring these applications the immense value quickly revealed itself. It can honestly be a fun exercise working through the setup of these applications, almost like a puzzle, as every application is different.

It can also be really scary, configure SSO wrong, and you have just locked out yourself and everyone else who needs access to the application (more on that in future posts).
