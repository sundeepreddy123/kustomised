User / Browser
      |
      |  http://<NODE-IP>:32100
      ▼

┌──────────────────────────┐
│ Kubernetes Node          │
│  NodePort Service        │
│  (Port: 32100)           │
└───────────┬──────────────┘
            ▼
┌──────────────────────────┐
│ Istio Ingress Gateway    │
│  (Gateway Resource)      │
└───────────┬──────────────┘
            ▼
┌──────────────────────────┐
│ Istio VirtualService     │
│  (Routing Rules)         │
└───────────┬──────────────┘
            ▼
┌──────────────────────────┐
│ Kubernetes Service       │
│  (ClusterIP)             │
└───────────┬──────────────┘
            ▼
┌──────────────────────────┐
│ Deployment (Pods)        │
│  NGINX / App Container   │
└───────────┬──────────────┘
            ▼
┌──────────────────────────┐
│ HPA                      │
│ Auto-scales Pods         │
└──────────────────────────┘

this is the basic struture of the application this will enhance in future.
