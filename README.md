# openwebui-gitops

A basic deployment of openwebui with vllm on OpenShift

## Overview

This repository contains GitOps-based infrastructure configuration for deploying [OpenWebUI](https://openwebui.com/) alongside [vLLM](https://github.com/vllm-project/vllm) on OpenShift. This setup provides a web interface for interacting with large language models while leveraging vLLM's high-performance inference engine.

## Features

- **OpenWebUI**: User-friendly web interface for LLM interactions
- **vLLM Integration**: High-performance LLM inference server with optimized throughput and latency
- **GitOps Ready**: Infrastructure as code using GitOps principles for reproducible deployments
- **OpenShift Native**: Optimized for OpenShift container platform
- **Easy Deployment**: Simplified setup for containerized LLM serving

## Prerequisites

Before deploying this project, ensure you have:

- An OpenShift cluster (version 4.10 or later recommended)
- `oc` CLI tool installed and configured
- `kubectl` installed
- Git installed
- Sufficient cluster resources for LLM inference (GPU/compute resources recommended)

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/Rye-guy01/openwebui-gitops.git
cd openwebui-gitops
```

### 2. Configure Your Environment

Update any configuration files or environment variables specific to your OpenShift cluster.

### 3. Deploy to OpenShift

```bash
oc apply -f .
```

Or use your GitOps operator (ArgoCD, Flux, etc.) to sync this repository with your cluster.

## Usage

### Accessing OpenWebUI

Once deployed, access OpenWebUI through:

```
https://<openshift-route>
```

The exact URL will depend on your OpenShift cluster configuration and ingress setup.

### Configuring Models

Configure which models vLLM serves by updating the relevant configuration in your deployment manifests.

## Project Structure

- `Deployments/`: Kubernetes deployment manifests
- `Services/`: Kubernetes service configurations
- `ConfigMaps/`: Configuration files for OpenWebUI and vLLM
- `LICENSE`: Project license

## Contributing

Contributions are welcome! To contribute:

1. Fork this repository
2. Create a feature branch (`git checkout -b feature/your-feature`)
3. Commit your changes (`git commit -m 'Add your feature'`)
4. Push to the branch (`git push origin feature/your-feature`)
5. Open a Pull Request

## License

This project is licensed under the terms specified in the [LICENSE](LICENSE) file.

## Support

For issues, questions, or suggestions, please open an [issue](https://github.com/Rye-guy01/openwebui-gitops/issues) on this repository.

## References

- [OpenWebUI Documentation](https://docs.openwebui.com/)
- [vLLM Documentation](https://docs.vllm.ai/)
- [OpenShift Documentation](https://docs.openshift.com/)