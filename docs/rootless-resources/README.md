# Rootless Resources

## Slides

### 1. `Rootless Containers & Unresolved Issues` (by akihiro suda)

* https://events19.linuxfoundation.org/wp-content/uploads/2017/11/The-State-of-Rootless-Containers-Aleksa-Sarai-SUSE-LLC-Akihiro-Suda-NTT.pdf

#### Summary

1. Map UIDs/GIDs in the guest to **different** UIDs/GIDs on the HOST.

2. Docker does not support `overlayfs` because of "security concerns"
    * using `fuse-overlayfs` to achieve this problem.
    * refer [this](https://docs.docker.com/engine/security/rootless/#known-limitations)

3. Lack of Network Support
    * Using `slirp4netns`
