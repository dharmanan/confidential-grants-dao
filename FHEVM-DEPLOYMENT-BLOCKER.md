# FHEVM Node Deployment Blocker

As of October 2025, deploying a local Zama FHEVM node using the official `ethermint-dev-node` Docker image (v0.5.1-2 and later) is not possible without providing FHE key files. The container expects key files to be mounted at `/network-fhe-keys` and will immediately exit if they are missing.

- There is currently **no public script or example** for generating these FHE key files in the official Zama documentation or Docker image.
- Previous deployments may have worked if the image auto-generated keys, included example keys, or if the node was started before this requirement was enforced.
- As a result, all local development and confidential contract testing is blocked until Zama provides a key generation script or example key set.

**Next steps:**
- Request example FHE key files or a key generation script from the Zama team (Discord, GitHub Issues, or support channels).
- Once keys are available, mount them into the container and restart the node as described in the Zama documentation.

---

If you have a working node from a previous session, you may be able to copy its key files and reuse them for new containers.
