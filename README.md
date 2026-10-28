# keda-pr-gate-test

Test fixture for the runtimez deployment-risk GitHub Action's KEDA rules. `main` holds what is deployed today
(`k8s/keda.yaml`); the `keda-pr` branch changes it so that each object trips one KEDA rule. Open a PR from
`keda-pr` to `main`: the `deployment-risk` check should fail and its PR comment should list the 13 KEDA findings
named in the comments of `k8s/keda.yaml`. Nothing here is applied to any cluster.
