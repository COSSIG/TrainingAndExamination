[#]: subject: "CPE Quarterly Update Q4 2021"
[#]: via: "https://blog.centos.org/2022/03/cpe-quarterly-update-q4-2021/"
[#]: author: "CentOS Blog https://blog.centos.org"
[#]: collector: "lkxed"
[#]: translator: " "
[#]: reviewer: " "
[#]: publisher: " "
[#]: url: " "

CPE Quarterly Update Q4 2021
======

This is a summary of the work done on initiatives by the [CPE][1] Team. Each quarter CPE Team together with CentOS and Fedora community representatives choose initiatives that will be being worked on in this quarter. The CPE Team is then split into multiple smaller sub-teams that will work on chosen initiatives + day to day work that needs to be done.

Following is the list of sub-teams in this quarter:

- Infra & Releng
- CentOS Stream
- OSCI – Distrobaker monitoring
- EPEL
- CentOS Duffy CI

## About

Purpose of this sub-team is to take care of day to day business regarding CentOS and Fedora Infrastructure and Fedora release engineering work. It’s responsible for services running in Fedora and CentOS infrastructure and preparing things for the new Fedora release (mirrors, mass branching, new namespaces etc.). This sub-team is also investigating possible initiatives. This is done by ARC (The Advance Reconnaissance Crew), which is formed from the Infra & Releng sub-team members based on the initiative that is being investigated.

**Issue trackers**

- [Fedora Infrastructure][2]
- [CentOS Infrastructure][3]
- [Fedora Release Engineering][4]

**Documentation**

- [Fedora Infrastructure][5]
- [CentOS Infrastructure][6]
- [Fedora Release Engineering][7]

## Members of sub-team for Q4 2021

- Mark O’Brien (Team Lead) (Fedora Operations, CentOS Operations) (mobrien)
- Kevin Fenzi (Team Lead) (Fedora Operations) (kevin)
- Michal Konecny (Agile Practitioner) (Developer) (mkonecny)
- Patrik Polakovic (Agile Practitioner) (Developer) (ppolakov)
- Fabian Arrotin (CentOS Operations) (arrfab)
- Tomas Hrcka (Release Engineering) (humaton)
- Adam Saleh (Developer) (asaleh)
- Aurelien Bompard (Developer) (abompard)
- Emma Kidney (Developer) (ekidney)
- Pedro Moura (Developer) (pmoura)
- Ryan Lerch (Developer) (rlerch)

## What the sub-team did in Q4 2021

### Fedora Infrastructure

- Fedora Infra moved their documentation to [docs.fedoraproject.org][5].
- [Migrated discourse2fedmsg from fedmsg to fedora messaging][8] and deployed the app in production.
- Migrated most koji builders to Fedora 35 (finished in Q1 2022)
- Got CentOS stream 9 using mirrormanager ([mirrors.centos.org][9])
- Helped release Fedora 35 Beta and then Final
- Kinoite website published.
- Fedoraproject dnssec keys moved to sha384 from sha1
- All wiki talk pages have been disabled. We don’t use them or read them.
- S390x builders moved to the new z15 mainframe. Additional resources allowed us to increase kvm builders from 10 to 20.

### CentOS Infrastructure

- Upgraded openshift for CI tenants
- Migrated the cico-workspace to CentOS 8-stream instead of CentOS 7
- Onboarding new SIGs and adapted workflow
- Migrated sig guide to [https://sigs.centos.org/guide][10] and hosting [sigs.centos.org][11] SIGs docs (opt-in)
- Prepared the CentOS Linux 8 EOL/decommissioning steps
- Migrated several services in infrastructure due to some sponsors leaving the project (willing to sponsor other rebuilds now instead)
- Rolled out (with Artwork SIG) new visual theme across all centos infra for stream 9 visual style (website, mirrors, mailing-list, etc)
- Implemented the new mirror.stream.centos.org mirror pool for Stream 9 (that is also used with mirrormanager)

### Fedora Release Engineering

- On 2nd November Fedora Linux 35 was released
- [Updated list of critpath packages][12]

### ARC

The ARC Team was looking at Bodhi and Image Builder in Q4.

- Investigated doing an initiative on Bodhi
- Looked at splitting Bodhi up into separate packages
- Investigated decoupling Bodhi from PDC
- Looked at dependency management
- Concluded PDC functionality should move to dist-git instead
- Not suitable for an initiative
- Package separation & dependency management work to go ahead outside of initiative work

- Possible replacement for OZ and Image factory
- Could be used as a service from Red Hat internal team
- Would likely need to use our own builders for Fedora
- Fedora IOT moving to image builder could use builders provided by Image builder as it does not support ppc or s390x
- Initiative going ahead in Q1 2022 to use image builder for Fedora IOT
- Potentially used for Fedora/CentOS Stream in the future

- Bodhi:
- Image Factory

## About

This initiative is working on CentOS Stream/Emerging RHEL to make this new distribution a reality. The goal of this initiative is to prepare the ecosystem for the new CentOS Stream.

**Issue trackers**

- [Bugzilla][13]

**Documentation**

- [CentOS documentation][14]

**Application URLs**

- [https://centos.org/centos-stream/][15]

## Members of sub-team for Q4 2021

- Brian Stinson (Team Lead) (bstinson)
- Adam Samalik (Agile Practitioner) (asamalik)
- James Antill (jantill)
- Johnny Hughes
- Merlin Mathesius
- Mohan Boddu (mboddu)
- Petr Bokoc (pbokoc)
- Stephen Gallagher (sgallagher)
- Troy Dawson (tdawson)

## What the sub-team did in Q4 2021

- 1/3 of all srpms built in Stream were modules in Nov (fun/interesting fact!)
- Automated compose checks for c9s and added repoclosure check for baseOS and app stream
- We now report on differences between RHEL 9 and CentOS Stream 9 composes
- Added c9s links on mirror network for downloading!
- CI testing for SIGs enabled for c9s
- Started work on bringing c8s and c9s closer
- Updated the ELN Extras docs
- Got ELN side tag builds working
- Started work on Content Resolver buildroot integration

## About

In Q4 some of the CPE team were able to assist the OSCI team with some open issues they had that they were finding hard to get to before the end of the year. Our team worked on a way to improve the Distrobaker monitoring to monitor side-tags and have the code update prometheus for metrics on the side-tags. Distrobaker itself is a service which rebuilds the CentOS 9 Stream Koji builds for RHEL 9 in Brew and having good metrics on the application provides useful insights as to how the service is operating.

**Issue trackers**

- [Gitlab][16]

**Documentation**

- [README][17]

## Members of sub-team for Q4 2021

- David Kirwan
- Lenka Segura
- Leonardo Rossetti

## What the sub-team did in Q4 2021

This team managed to do everything that is described in the ‘about’ section.

## About

Extra Packages for Enterprise Linux (or EPEL) is a Fedora Special Interest Group that creates, maintains, and manages a high quality set of additional packages for Enterprise Linux, including, but not limited to, Red Hat Enterprise Linux (RHEL), CentOS and Scientific Linux (SL), Oracle Linux (OL).

EPEL packages are usually based on their Fedora counterparts and will never conflict with or replace packages in the base Enterprise Linux distributions. EPEL uses much of the same infrastructure as Fedora, including buildsystem, bugzilla instance, updates manager, mirror manager and more.

**Issue trackers**

- [Pagure][18]

**Documentation**

- [EPEL documentation][19]

## Members of sub-team for Q4 2021

- Carl George (Team Lead) (carlwgeorge)

## What the sub-team did in Q4 2021

- [Launch of EPEL9][20]

## About

Duffy is a system within CentOS CI Infra which allows tenants to provision and access bare metal resources of multiple architectures for the purposes of CI testing.

We need to add the ability to checkout VMs in CentOS CI in Duffy. We have OpenNebula hypervisor available, and have started developing playbooks which can be used to create VMs using the OpenNebula API, but due to the current state of how Duffy is deployed, we are blocked with new dev work to add the VM checkout functionality.

**Issue trackers**

- [Github][21]

**Documentation**

- Not available yet

**Application URLs**

- Not available yet

## Members of sub-team for Q4 2021

- Nils Philippsen (Team Lead) (nphilipp)
- Akashdeep Dhar (t0xic0der)
- Ben Capper
- Vipul Siddharth (vipul)

## What the sub-team did in Q4 2021

Reimplement Duffy from the ground up (which is ongoing). It features a new, much cleaner API than the currently deployed version which allows users to allocate differently featured nodes for their CI workflows. It comes with a metaclient app which translates between users of the legacy API and the new one. The Duffy core is agnostic of the features of managed nodes (e.g. bare metal vs. VM, architecture, OS type & version) and shifts that knowledge into configurable node pools with corresponding Ansible playbooks used for provisioning and deprovisioning.

## About

The datanommer and datagrepper stacks are currently relying on fedmsg which we want to deprecate. These two applications need to be ported off fedmsg to fedora-messaging. As these applications are 'old-timers' in the fedora infrastructure, we would also like to look at optimizing the database or potentially redesigning it to better suit the current infrastructure needs.

For phase two, we would like to focus on a DB overhaul.

**Issue trackers**

- [Github project][22]

**Documentation**

- [Datagrepper][23]

**Application URLs**

- [Datagrepper][23]

## Members of sub-team for Q4 2021

- Aurelien Bompard (Team Lead) (abompard)
- Ryan Lerch
- Lenka Segura

## What the sub-team did in Q4 2021

The team migrated the datanommer and datagrepper tools to use TimescaleDB as a backend, instead of plain PostgreSQL. This will greatly improve the scalability of the apps. As a reminder, datanommer stores all messages ever sent to our message bus (and that’s a lot of messages), and datagreppers is a web UI and API to query this database.

## About

Enable the Fedora CoreOS to move their pipeline from the CentOS CI OCP4 cluster to the newly deployed Fedora infra OCP4 cluster.

**Issue trackers**

- [Fedora Infra tracker][2]

**Documentation**

- [Ansible playbook][24]

**Application URLs**

- [Openshift project (restricted access)][25]

## Members of sub-team for Q4 2021

- David Kirwan (Team Lead) (Saffronique)
- James Richardson (jrichardson)
- Lenka Segura (lenkaseg)
- Stephen Coady (scoady)

## What the sub-team did in Q4 2021

Fedora CoreOS were making use of the CentOS CI OCP4 cluster to run some of their pipelines. We reused the playbooks and roles already developed in CentOS CI Infra, to recreate the project, service account and permissions required in order to deploy their pipeline on the new Fedora infra OCP4 cluster.

If you get here, thank you for reading this. If you want to contact us, feel free to do it in #redhat-cpe channel on [libera.chat][26].

--------------------------------------------------------------------------------

via: https://blog.centos.org/2022/03/cpe-quarterly-update-q4-2021/

作者：[CentOS Blog][a]
选题：[lkxed][b]
译者：[译者ID](https://github.com/译者ID)
校对：[校对者ID](https://github.com/校对者ID)

[a]: https://blog.centos.org
[b]: https://github.com/lkxed
[1]: https://docs.fedoraproject.org/en-US/cpe/
[2]: https://pagure.io/fedora-infrastructure/issues
[3]: https://pagure.io/centos-infra/issues
[4]: https://pagure.io/releng/issues/
[5]: https://docs.fedoraproject.org/en-US/infra/
[6]: https://docs.infra.centos.org/
[7]: https://docs.pagure.org/releng/
[8]: https://pagure.io/fedora-infrastructure/issue/9576
[9]: https://mirrors.centos.org
[10]: https://sigs.centos.org/guide
[11]: https://sigs.centos.org
[12]: https://pagure.io/releng/issue/8948
[13]: https://bugzilla.redhat.com/buglist.cgi?version=CentOS%20Stream
[14]: https://docs.centos.org/en-US/docs/
[15]: https://centos.org/centos-stream/
[16]: https://gitlab.cee.redhat.com/lsegura/distrobaker_monitoring
[17]: https://gitlab.cee.redhat.com/lsegura/distrobaker_monitoring/-/blob/master/README.md
[18]: https://pagure.io/epel/issues
[19]: https://docs.fedoraproject.org/en-US/epel/
[20]: https://communityblog.fedoraproject.org/epel-9-is-now-available/
[21]: https://github.com/CentOS/duffy/issues
[22]: https://github.com/orgs/fedora-infra/projects/10
[23]: https://apps.fedoraproject.org/datagrepper/
[24]: https://pagure.io/fedora-infra/ansible/blob/main/f/playbooks/openshift-apps/fedora-coreos-pipeline.yml
[25]: https://console-openshift-console.apps.ocp.fedoraproject.org/k8s/cluster/projects/fedora-coreos-pipeline
[26]: https://libera.chat/
