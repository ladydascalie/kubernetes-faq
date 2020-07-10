# kube-api-server 

<details>
<summary>
<b>All API usage from nodes and pods terminate at the following control plane components:</b>
</summary>
<b>apiserver</b><hr>no other control plane components exposes remote services
</details>

<details>
<summary>
<b>Nodes should be provisioned with _____ for the cluster such that they can connect securely to the apiserver along with valid client credentials</b>
</summary>
public root certificate
</details>

<details>
<summary>
<b>Pods that wish to securely connect to the apiserver can leverage a _____ so that K8S will automatically inject the public root certificate and valid bearer token into the new pod.</b>
</summary>
service account
</details>

<details>
<summary>
<b>The <b>kubernetes </b>service (in all namespaces) is configured with _____ that is redirected via _____ to the apiserver</b>
</summary>
a virtual IP address
kube-proxy
</details>

<details>
<summary>
<b>the apiserver is configured to listen for remote connections on _____ with one or more forms of _____ enabled</b>
</summary>
a secure HTTPS port
client authentication
</details>

<details>
<summary>
<b>apiserver to kubelet connections are used for</b>
</summary>
Fetching pod logs
<b>kubectl attach</b>'ing into pods
<b>kubectl port-forward</b>'ing into pods
</details>

<details>
<summary>
<b>apiserver to kubelet connections terminate at</b>
</summary>
the kubelet's HTTPS endpoint
</details>

<details>
<summary>
<b>Does the <b>apiserver</b> verify the <b>kubelet's</b> serving certificate by default?</b>
</summary>
No-----The connection is subject to MITM attacks by default
</details>

<details>
<summary>
<b>apiserver to kubelet connection can be verified via</b>
</summary>
SSH tunneling
OR&nbsp;
<b>apiserver --kubelet-certificate-authority</b>
</details>

<details>
<summary>
<b>Are <b>apiserver</b>&nbsp;connections to <b>nodes, pods and services</b>&nbsp;authenticated or encrypted?</b>
</summary>
No :(
They can be run over HTTPS but will not validate the certificate
</details>
