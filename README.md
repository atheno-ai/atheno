# Atheno

## Kubernetes IDE with AI Co-pilot

Atheno is a low-code Kubernetes IDE with AI Co-pilot. The low-code IDE has advanced resource filtering, a YAML free form editor, and developer tools like a container terminal and logs. The AI Co-pilot provides interactive troubleshooting.

## Supported AI Models

ChatGPT models gpt-4o and gpt-4-turbo.

## Installation 

### Minimum System Requirements

Atheno installation requires a minimum of `4GB RAM` and `2 vCPUs`

### Firewall Ports

The following incoming firewall ports need to be opened - `30003`.

### Step to install using Helm Charts

Install the chart

```sh
cd helm
helm install atheno ./ --create-namespace -n atheno
```

### Validating the installation

Atheno installation can be validated by waiting for the Atheno services to move to `ready` state.

```sh
kubectl wait --for=condition=ready pod -l released-by=atheno -n atheno
```

One the installation is complete, Atheno dashboard can be accessed at http://[NodeIP]:30003/

NodeIP can be obtained by executing the command below:

```sh
kubectl get nodes -o wide
```

## Usage

Open the `Ask AI` option, select the LLM Type as `OpenAI`, select a model, and provide the API Key.  

To get the OpenAI API Key, check here: [OpenAI API Key](https://platform.openai.com/api-keys). 


