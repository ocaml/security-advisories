# OCaml Security Team 2025 End-Of-Year Report

In May of 2025, the OCaml Software Foundation encouraged the formation of an OCaml Security Team, which would handle issues and provide guidance for improving software security in the OCaml ecosystem. Throughout 2025, the team has been building structure and procedures to accomplish these goals. A regular public update on the team's activity is among many good ideas taken from the Haskell Security Response Team, and we hope the community will find this first public update useful.

The team consists of:

- Hannes Mehnert - @hannesm - individual, robur.coop
- Mindy Preston - @yomimono - individual
- Joe - @cfcs - individual
- Edwin Török - @edwintorok - individual
- Nicolás Ojeda Bär - @nojb - LexiFi
- Louis Roché - @Khady - ahrefs
- Boning Dong - Bloomberg

Until December 2025:
- Maxim Grankin - @maxim092001 - Bloomberg

The newly created website [ocaml.org/security](https://ocaml.org/security) gives some guidelines for people finding security issues.

# Contact and Disclosure Process

The team established a procedure for reporting security issues as one of its first activities. The security disclosure process is available at https://github.com/ocaml/security-advisories?tab=readme-ov-file#reporting-vulnerabilities . The OCaml Security Team can also be contacted at security@ocaml.org for matters besides vulnerability disclosure. Mails to security@ocaml.org are not public.

The public, announce-only mailing list https://sympa.inria.fr/sympa/info/ocsf-ocaml-security-announcements will broadcast information on security advisories.

These procedures were [announced in July 2025](https://discuss.ocaml.org/t/ann-ocaml-security-team).

# Vulnerability Database

A public vulnerability database for OCaml software is another of the Security Team's goals. We indend to accomplish this by publishing information from the existing, but empty https://github.com/ocaml/security-advisories to the public [osv.dev](https://osv.dev) database (again borrowing a good idea from the Haskell SRT). Some work on a pipeline for publishing advisories there and backporting existing advisories is ongoing.

# Tool development

An OCaml library that supports the [package URL](https://github.com/package-url/purl-spec) "purl" was developed and released to the opam-repository (https://github.com/hannesm/purl, https://ocaml.org/p/purl/latest). In the process, we propose to make the policy for opam-repository more strict to have immutable packages (where the source is not modified): https://github.com/ocaml/opam-repository/pull/29072. We also propose to integrate opam into the package URL specification https://github.com/package-url/purl-spec/pull/763.

The vulnerability database mentioned above hosts advisories in markdown (with some opam-file-format metadata header). We developed [tooling](https://github.com/hannesm/advisories) to convert these into json (following the json schema from osv.dev). We also made OCaml/opam known for the schema https://github.com/ossf/osv-schema/pull/473.

# Public Meetings and Presentations

On September 15, Hannes Mehnert gave an introduction to the OCaml Security Team at [FUN OCaml](https://fun-ocaml.com/) in Warsaw.

Maxim Grankin gave a talk ["Towards a More Secure OCaml Ecosystem"](https://conf.researchr.org/details/icfp-splash-2025/ocaml-2025-papers/9/Toward-a-More-Secure-OCaml-Ecosystem) at the OCaml Users and Developers Workshop in October of 2025, which is available at https://www.youtube.com/watch?v=PekeGxGlc3Q .

On October 22 2025, the Security Team held a public meeting, for which the notes are available at https://pad.data.coop/7-Ic5rG6ToynsW02hJsndg?both .

# Advisories

A potential clickjacking issue with ocurrent's web interface was reported to the Security Team by Kunal Mhaske was fixed by Mark Elvers in https://github.com/ocurrent/ocurrent/pull/465 .

No other communications with the security team have resulted in publicly available remediation information or advisories.

# Future Plans

The Security Team has received a lot of interest in the advisory database mentioned above, and this work is a high priority for the team.

The Security Team also hopes to publish security guides for OCaml programmers and project maintainers.

The OCaml Software Foundation has indicated that some funding may be available for projects that make OCaml more secure. The Security Team is actively developing a process for soliciting and evaluating proposals, as discussed in the October public meeting.

# Acknowledgements

The Security Team is an initiative of the OCaml Software Foundation and is grateful to the OCSF and its sponsors for their support.