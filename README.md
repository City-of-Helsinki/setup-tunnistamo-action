# setup-tunnistamo-action

Action to set up tunnistamo for review environments

This actions allow to use authentication backend at review environments.

## Configuration

Following input variables are used in the action

| Name                   | Description                                                                                                                                                          |
| ---------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `kubeconfig_raw`       | Kubeconfig as text to allow access to cluster and namespaces (RBAC) having Tunnistamo and review environment.                                                        |
| `review_namespace`     | Namespace of review environment (used as name of the dynamic client)                                                                                                 |
| `tunnistamo_namespace` | Namespace that holds Tunnistamo in same cluster than review app                                                                                                      |
| `response_types`       | Responses (authentication flow) needed for the client. Note that valid type should be enclosed with double quotes. Multiple values can be given separated with space |
| `callback_path`        | Where authentication should return to                                                                                                                                |
| `login_methods`        | Which login methods are offered for the client. Multiple values can be given separated with space                                                                    |
| `api_scope`            | API Scope for client to be bound with                                                                                                                                |
