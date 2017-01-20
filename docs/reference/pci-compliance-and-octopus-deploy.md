---
title: PCI Compliance and Octopus Deploy
position: 5
---


We have a lot of customers running Octopus Deploy in their PCI compliant environments. We don't claim to be experts in PCI compliance, especially since every situation is slightly different. What we can do is offer some recommendations primarily focused on your use of Octopus Deploy and different models you can achieve with it.

:::success
This free e-book is a good starting place when considering how deployment automation can work well in a highly regulated environment: [DevOps for Finance - How DevOps will help you surpass the common challenges of financial services software development.](http://radar.oreilly.com/2015/09/devops-for-finance.html)
:::


On this page:


- How Octopus Deploy can help with PCI Compliance
- Security considerations

:::success
**Try not to give up too much automation wherever possible**
Pessimistic approaches to PCI compliance controls will, at first glance, make it more difficult to automate certain activities. One of the main benefits to using Octopus Deploy is end-to-end automation and we recommend not giving that up without spending time to understand why the automation is considered "harmful". Quite often our customers find that leveraging end-to-end automation in Octopus Deploy makes implementing compliance controls and auditing easier. It's often a case of working with your auditor and their concerns on a case-by-case basis.
:::

## How Octopus Deploy can help with PCI Compliance


PCI Compliance is primarily concerned with implementing "controls" or "practices" which help ensure the safety and security of sensitive information, and the ability to audit that those practices are being enforced and followed. In many ways, full end-to-end automation helps with that since the interaction with your secure systems is tightly controlled: everything is scripted!

- In Octopus Deploy, everything is scripted which leaves less room for human error or uncontrolled activities.
- Octopus Deploy supports authentication with Active Directory and other external identity providers which can be used to enforce multi-factor authentication. Learn about�[authentication providers](/docs/home/administration/authentication-providers.md).
- You can implement strict, fine-grained, environment-aware security permissions. Learn about�[managing users and teams](/docs/home/administration/managing-users-and-teams.md).
- Every activity is carefully audited. Learn more about�[auditing](/docs/home/administration/auditing.md).
- You can control how long you retain data and packages. Learn about�[Retention Policies](/docs/home/administration/retention-policies.md).
- You can insert an HTTP proxy server between Octopus Server and any Tentacles or SSH endpoints. This is helpful when you want to have DMZs in your network with controlled entry/exit points. Learn about�[proxy support](/docs/home/installation/installing-tentacles/proxy-support.md).
- If you really cannot use Tentacle or SSH, you can use Offline Package Drops for fully disconnected deployment automation.�Learn about the�[Offline Package Drop](/docs/home/deployment-targets/offline-package-drop.md) deployment target.
- If you require isolated instance of Octopus Server our licensing model is quite flexible. Each licence of Octopus Deploy grants you the right to install and configure up to three (3) separate instances of Octopus Server. Learn about managing�[Isolated Octopus Deploy servers](/docs/home/patterns/isolated-octopus-deploy-servers.md).


## Security considerations

- Learn about�[Octopus - Tentacle communication](/docs/home/reference/octopus---tentacle-communication.md) to understand how automation instructions are transmitted securely to maintain trust.
 - Full support for TLS 1.2 was introduced in Octopus Deploy 3.1. We recommend using the latest version of Octopus Deploy whenever possible.
- Learn about�[security and encryption](/docs/home/reference/security-and-encryption.md) of sensitive information in Octopus Deploy.
- Learn about how Octopus Deploy handles�[sensitive variables](/docs/home/deploying-applications/variables/sensitive-variables.md).


:::success
We conduct independent security analysis and penetration testing for Octopus Deploy. Contact our support team for a copy of the most recent report.
:::