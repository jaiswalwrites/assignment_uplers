# Debugging Operations in Kubernetes

Kubernetes provides several useful commands for debugging operations. In this guide, we will cover `kubectl get pods`, `kubectl logs`, and `kubectl exec`.

## Prerequisites
Before we begin, you should have a basic understanding of Kubernetes and have `kubectl` installed on your system.

## List available pods
The first command we will use is `kubectl get pods`. This command returns a list of all available pods and their status. To use this command, you must specify the namespace you want to query.

```shell
kubectl get pods --namespace <namespace>
```
This command will return a list of all pods in the specified namespace, along with their current status.

## Retrieve pod logs
The second command we will cover is `kubectl logs`. This command retrieves the logs of a specific pod, which is useful for reviewing logs or debugging a container.

```shell
kubectl logs <pod-name>
```
Replace `<pod-name>` with the name of the pod you want to retrieve logs from. This command will return the logs for the specified pod.

## Debug a container
The last command we will discuss is `kubectl exec`. This command allows you to execute a command in a container, which can be useful for debugging a container from inside or exploring the container's environment.

```shell
kubectl exec -it <pod-name> -- <command>
```
Replace `<pod-name>` with the name of the pod you want to execute the command in, and replace `<command>` with the command you want to execute. This command will open an interactive terminal session in the container and allow you to execute the specified command.

## Conclusion
When debugging in Kubernetes, start with `kubectl get pods`, followed by `kubectl logs`, and lastly, use `kubectl exec` to explore the container's inside and review other log files or configurations. Additionally, you can consider using the `kubectl debug` command to create a clone of a pod that does not terminate if an error occurs inside the container.

# See Also

- [Getting Started](https://kubernetes.io/docs/reference/generated/kubectl/kubectl-commands#-strong-getting-started-strong-)

- [What is Kubernetes](https://kubernetes.io/docs/concepts/overview/)


