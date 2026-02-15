# Copilot Instructions for `cluster-template`

- This repository is a Kubernetes cluster template used by TrueForge ForgeTool.
- Keep changes minimal and focused; avoid broad refactors.
- Prefer editing manifests under `kubernetes/`, `base/`, and `patches/` without changing unrelated resources.
- Preserve GitOps conventions and existing Flux/Kustomize structure.
- For validation, use the existing kubeconform workflow/script (`.github/scripts/kubeconform.sh`).
