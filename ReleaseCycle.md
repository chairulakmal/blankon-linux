# Release Cycle

This page is for maintainers and contributors. It explains how package updates move from Debian Sid to BlankOn users. The most important point: BlankOn Sinambung is a guarded rolling release, so there are no versioned releases. Updates go to a staging repository first, and reach users only after manual testing. The page has three parts: the update cycle, security updates, and ISO images. If you only use BlankOn, see [Managing Repository](https://github.com/BlankOn/blankon-linux/blob/main/UserGuides/ManagingRepository.md) instead.

## Update Cycle

BlankOn has two package repositories, both with the suite name `sinambung`:

- **Arsip-dev** (`arsip-dev.blankonlinux.id`) is the staging repository. New packages from Sid arrive here first.
- **Arsip** (`arsip.blankonlinux.id`) is the production repository. User systems get their updates from here.

A team member runs each update by hand, after the team agrees to start it:

1. **Snapshot.** Take a Btrfs snapshot of the Arsip-dev repository, so a bad update can be rolled back. See [Btrfs Snapshot](https://github.com/BlankOn/blankon-linux/blob/main/Infrastructure/BtrfsSnapshots.md).
2. **Pull.** Pull new packages from Sid into Arsip-dev.
3. **QA (quality assurance).** Contributors install and test Arsip-dev by hand.
4. **Decide.** The contributors who ran QA choose one of three results:
   - **All clear:** promote the update (step 5).
   - **Some packages are broken:** patch and rebuild those packages with [IRGSH](https://github.com/BlankOn/irgsh-go), put them back into Arsip-dev, and run QA again.
   - **Too much is broken:** roll Arsip-dev back to the snapshot from step 1, and wait for Sid to become stable before the next pull.
5. **Promote.** Copy Arsip-dev to Arsip with `reprepro`. Packages are copied, not rebuilt. See [Reprepro](https://github.com/BlankOn/blankon-linux/blob/main/Infrastructure/Reprepro.md).
6. **Announce.** Tell users that an update is available.

Two tools help with the decision. [untung](https://github.com/BlankOn/untung) compares the repositories with upstream. [tambal](https://github.com/BlankOn/tambal), at https://security.blankonlinux.id/, tracks security advisories.

## Security Updates

The normal update cycle also brings security fixes from Sid. A time-critical fix does not wait for the next pull: the team imports the fixed package with IRGSH. See [Package Vulnerability Monitoring](https://github.com/BlankOn/blankon-linux/blob/main/Security/PackageVulnerabilityMonitoring.md).

## ISO Images

A release ISO image has a name of the form `blankon-sinambung-YY.MM-verbeek-amd64.iso`, where `YY.MM` is the year and month, for example `26.09` for September 2026. Release images are published at https://jahitan.blankonlinux.id/releases/current/.
