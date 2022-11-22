# crawlab-k8s-deploy

```bash
# 部署
kubectl apply -f k8s/ns.yaml
kubectl apply -f k8s

# 查看状态
kubectl get pod -n crawlab
kubectl get service -n crawlab

# 端口转发
kubectl port-forward services/crawlab 8000:80 -n crawlab
# 访问
# http://127.0.0.1:8000

# 调整worker数
kubectl scale -n crawlab deployment crawlab-worker --replicas=3
```