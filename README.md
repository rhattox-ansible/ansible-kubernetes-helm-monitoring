# ansible-kubernetes-helm-monitoring

Installs kube-prometheus-stack, including Prometheus, Grafana, and Alertmanager.

## Layout

```text
main.yaml
defaults/main.yaml
meta/main.yml
tasks/main.yaml
tasks/0-install-monitoring.yaml
```

The root playbook loads defaults and includes the task dispatcher. The dispatcher
reports progress and includes the installation tasks. Galaxy role metadata is in
`meta/main.yml`.

## Usage

Requires Ansible, the `kubernetes.core` collection, Helm, Kubernetes Python
dependencies, and access to a Kubernetes cluster.

```bash
ansible-playbook main.yaml
```
