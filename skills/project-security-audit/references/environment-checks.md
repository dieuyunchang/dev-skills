# Supply-Chain & Environment Security

Auditing the ecosystem around the code.

## 1. Package Manager Malware
Audit `package.json`, `requirements.txt`, `Gemfile`, `Cargo.toml`, etc.
- **Install Hooks**: `preinstall`, `postinstall`, `lifecycle` scripts.
- **Dependency Confusion**: Checking for internal package names that might be hijacked on public registries.
- **Typosquatting**: Looking for packages with names very similar to popular ones.
- **Obfuscated Installers**: Shell scripts downloaded and run during package installation.

## 2. Docker & Container Security
Check `Dockerfile` and `docker-compose.yml`:
- **Privileged Mode**: `--privileged` or `privileged: true`.
- **Host Mounts**: Mounting `/`, `/var/run/docker.sock`, or sensitive home directories.
- **Hidden Listeners**: Ports exposed that are not documented.
- **Secret Copying**: `COPY .env` or similar commands that bake secrets into images.

## 3. Git & CI/CD Security
Audit `.github/workflows`, `.gitlab-ci.yml`:
- **Secret Exfiltration**: Workflows that send `secrets.*` to external URLs.
- **Malicious Runners**: Use of untrusted third-party actions or runners.
- **Artifact Poisoning**: Logic that modifies build artifacts before they are deployed.
