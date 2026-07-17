# OCaml Security Team 2026 First-Half Report

Throughout the first half of 2026, the security team has worked on security advisories: the publishing pipeline (from report over communication and fixes, to the security vulnerability database - these days osv.dev and CVE).

The team consists of:

- Hannes Mehnert - @hannesm - individual, robur.coop
- Mindy Preston - @yomimono - individual
- Joe - @cfcs - individual
- Edwin Török - @edwintorok - individual, Tarides
- Nicolás Ojeda Bär - @nojb - LexiFi
- Louis Roché - @Khady - ahrefs
- Boning Dong - @bn-d - Bloomberg

# Vulnerability Database

The public vulnerability database (https://github.com/ocaml/security-advisories) is established, and filled as well with old security advisories (from the MirageOS project, etc.). There is tooling via CI which generates a branch "generated-osv", which is a source for the Open Source Vulnerability database (https://osv.dev), run by Google. The direct link for all security advisories of the OCaml Security team is [here](https://osv.dev/list?ecosystem=opam).

The tooling is available from https://github.com/hannesm/advisories.

# Audit Tooling

Another utility to check your "opam switch" for installed vulnerable packages (using the above mentioned vulnerability database), has been developed - available at https://github.com/hannesm/opam-audit.

# Public Meetings

On March 19th a public OCaml security meeting took place with 10 attendees. The meeting notes are available at https://pad.data.coop/7-Ic5rG6ToynsW02hJsndg

# Modification Policy of the opam-repository

The Security Team proposed to make the immutability policy stricter (see https://github.com/ocaml/opam-repository/pull/29072) - which has been merged. So, any published opam package must not modify its sources (change tarball, add patches, modify build instructions, ...). Instead, a new version must be published. This makes the package URL (https://github.com/package-url/purl-spec) sensible and point to a precise source.

# Grant Proposals

A call for contributions was opened until end of March 2026. The Security Team is impressed by the amount and quality of the proposals. Evaluation and finding funding for proposals is still ongoing. We have some preliminary decisions and will reach out to the applicants by the end of July 2026.

# Advisories

So far, there have been 10 advisories (OSEC-2026-01 until OSEC-2026-10) published, and some more are worked on. Our primary communication channel is email, and we reach out to reports that we received GitHub by email. A [public mailing list](https://sympa.inria.fr/sympa/info/ocsf-ocaml-security-announcements) is available where security advisories are announced.

They range from issues in the OCaml runtime (Marshal buffer over-read OSEC-2026-01 CVE-2026-28364, Bigarray.reshape interger overflow OSEC-2026-04 CVE-2026-34353, command injection on Windows via filename OSEC-2026-05 CVE-2026-41083), opam sandbox escape (OSEC-2026-03 CVE-2026-41082, OSEC-2026-10 CVE-2026-57825), insufficient certificate property checks (in tls, OSEC-2026-06 CVE-2026-45388, OSEC-2026-07 CVE-2026-45389), path traversal (in tar, OSEC-2026-08 CVE-2026-45390), memory exhaustion (unbounded memory usage in arp, OSEC-2026-02, infinite loop in albatross-console, OSEC-2026-09).

The variety of reporters - 8 different people in 10 reports - is amazing. Thanks to all reporters, as well as the upstream developers. It has been a pleasure to coordinate the vulnerabilities.

# Future Plans

The Security Team also hopes to publish security guides for OCaml programmers and project maintainers.

# Acknowledgements

The Security Team is an initiative of the OCaml Software Foundation and is grateful to the OCSF and its sponsors for their support.
