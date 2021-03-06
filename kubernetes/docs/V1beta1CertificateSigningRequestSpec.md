

# V1beta1CertificateSigningRequestSpec

This information is immutable after the request is created. Only the Request and Usages fields can be set on creation, other fields are derived by Kubernetes and cannot be modified by users.
## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**extra** | [**Map&lt;String, List&lt;String&gt;&gt;**](List.md) | Extra information about the requesting user. See user.Info interface for details. |  [optional]
**groups** | **List&lt;String&gt;** | Group information about the requesting user. See user.Info interface for details. |  [optional]
**request** | **byte[]** | Base64-encoded PKCS#10 CSR data | 
**signerName** | **String** | Requested signer for the request. It is a qualified name in the form: &#x60;scope-hostname.io/name&#x60;. If empty, it will be defaulted:  1. If it&#39;s a kubelet client certificate, it is assigned     \&quot;kubernetes.io/kube-apiserver-client-kubelet\&quot;.  2. If it&#39;s a kubelet serving certificate, it is assigned     \&quot;kubernetes.io/kubelet-serving\&quot;.  3. Otherwise, it is assigned \&quot;kubernetes.io/legacy-unknown\&quot;. Distribution of trust for signers happens out of band. You can select on this field using &#x60;spec.signerName&#x60;. |  [optional]
**uid** | **String** | UID information about the requesting user. See user.Info interface for details. |  [optional]
**usages** | **List&lt;String&gt;** | allowedUsages specifies a set of usage contexts the key will be valid for. See: https://tools.ietf.org/html/rfc5280#section-4.2.1.3      https://tools.ietf.org/html/rfc5280#section-4.2.1.12 |  [optional]
**username** | **String** | Information about the requesting user. See user.Info interface for details. |  [optional]



