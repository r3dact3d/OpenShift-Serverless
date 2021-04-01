# OpenShift-Serverless
----
Install Red Hat OpenShift Serverless
====
oc apply -f openshift-serverless.yaml
====

Validate 
====
oc get csv -n openshift-serverless
====

Install Knative Serving
====
oc apply -f serving.yaml
====

Validate Knative Serving
====
oc get knativeserving.operator.knative.dev/knative-serving -n knative-serving --template='{{range .status.conditions}}{{printf "%s=%s\n" .type .status}}{{end}}'
====
