# Technical Charter (the "Charter") for Aether Project

*Apply since October 18, 2026*

This Charter sets forth the responsibilities and procedures for
technical contribution to, and oversight of, the Aether open source
project. All contributors (including committers, maintainers, and other
technical positions) and other participants in the Project (collectively,
"Collaborators") must comply with the terms of this Charter.

## 1.  Mission and Scope of the Project

a. The mission of the Project is to provide an independent, modular, embeddable web engine, which allows developers to deliver content and applications using web standards.

b. The scope of the Project includes collaborative development under the Project License (as defined herein) supporting the mission, including documentation, testing, integration and the creation of other artifacts that aid the development, deployment, operation or adoption of the open source project.

---

## 2. Project Governance & Maintainers

a. The technical oversight, roadmap, and administrative decisions of the Project will be led by the **Project Maintainers**.

b. The list of current Maintainers and active Collaborators is maintained within the [`AetherBrowser/project`](https://github.com/AetherBrowser/project) repository.

c. Participation in the Project through becoming a Collaborator, Contributor, or Maintainer is open to anyone so long as they abide by the terms of this Charter and the Project's Code of Conduct.

d. The Maintainers may establish workflow procedures for the submission, approval, and archiving of contributions or sub-projects, and set requirements for appointing new Maintainers.

e. Responsibilities: The Maintainers will be responsible for all aspects of technical and community oversight relating to the Project, which may include:

> i. coordinating the technical direction and architectural decisions of the Project;
> ii. approving project proposals, deprecations, and major structural changes;
> iii. organizing sub-projects or repositories under the `AetherBrowser` organization;
> iv. establishing community norms, contribution workflows, releases, and security reporting policies;
> v. maintaining and enforcing the Code of Conduct and contribution guidelines published in the [`AetherBrowser/project`](https://github.com/AetherBrowser/project) repository;
> vi. coordinating any marketing, documentation, or public communications regarding the Project.

---

## 3. Decision Making

a. The Project aims to operate as a consensus-based community. Maintainers, Contributors, and Collaborators will strive to reach agreement through open discussion.

b. In the event that consensus cannot be reached on a technical or administrative decision, the active **Maintainers** will make the final decision by a simple majority vote among the Maintainers.

---

## 4. Community Standards & Code of Conduct

a. All Collaborators must abide by the **Project Code of Conduct** published in the [`AetherBrowser/project`](https://github.com/AetherBrowser/project) repository.

b. All Collaborators must allow open participation from any individual or organization meeting the requirements for contributing under this Charter, regardless of competitive interests. The Project community must not seek to exclude any participant based on any criteria or reason other than those that are reasonable and applied on a non-discriminatory basis.

c. The Project will operate in a transparent, open, collaborative, and ethical manner at all times. The output of all Project discussions, proposals, issues, pull requests, decisions, and status should be made open and easily visible to the public.

---

## 5. Project Assets and Accounts

a. All Project assets, including GitHub repositories under the `AetherBrowser` organization, social media accounts, domain name registrations, and project branding created by the community, are managed collectively by the Project Maintainers for the benefit of the Aether open source community.

b. Any use of the Project name, logo, or trademarks must align with the open source mission of the Project and respect the guidelines set forth in the project repository.

---

## 6. Intellectual Property Policy

a. Collaborators acknowledge that the copyright in all new contributions will be retained by the copyright holder as independent works of authorship, and that no contributor or copyright holder will be required to assign copyrights to the Project.

b. Except as described in Section 6.c, all contributions to the Project are subject to the following:

> i. All new inbound code contributions to the Project must be made as follows:
> > 1. contributions to the main Aether code base will be made under the **Mozilla Public License, Version 2.0** (MPL-2.0), available in the "LICENSE" file within the Project's code repository (the "Project License"); and
> > 2. contributions to subproject code bases that are not part of the main Aether code base will be made under an open source license (approved by the Open Source Initiative) that has been approved by the Maintainers.
> > 
> > 
> 
> 
> ii. All new inbound code contributions must be accompanied by a **Developer Certificate of Origin** ([DCO](https://developercertificate.org/)) sign-off in the source code system (e.g., `Signed-off-by: Name <email>`) submitted through the contribution process;
> iii. All outbound code will be made available under the Project License;
> iv. Documentation will be received and made available by the Project under the **Creative Commons Attribution 4.0 International License** ([CC-BY-4.0](http://creativecommons.org/licenses/by/4.0/));
> v. The Project may seek to integrate and contribute back to other open source projects ("Upstream Projects"). In such cases, the Project will conform to all license requirements of the Upstream Projects.

c. The Maintainers may approve the use of an alternative license or licenses for inbound or outbound contributions on an exception basis, provided the alternative license is an OSI-approved open source license.

d. Contributed files should contain license information, such as SPDX short-form identifiers (`SPDX-License-Identifier: MPL-2.0`), indicating the open source license pertaining to the file.

---

## 7. Code Security & Cryptographic Verification

a. To ensure the integrity of the Project's code base and protect against unauthorized modifications or identity spoofing, the Project strongly encourages—and may require for certain maintainer roles—cryptographic verification of commits.

b. Contributors and Maintainers are encouraged to sign their commits and tags using GPG (GNU Privacy Guard) or SSH keys supported by GitHub, ensuring that the "Verified" badge is displayed on contributions.

c. The Maintainers may establish automated security policies, vulnerability reporting workflows, and branch protection rules (such as requiring signed commits on main release branches) within the AetherBrowser repositories to maintain a high level of code trust and security.

---

## 8. Amendments

a. This Charter may be amended by a agreement or majority vote of the Project Maintainers and will be published transparently in the [`AetherBrowser/project`](https://github.com/AetherBrowser/project) repository.
