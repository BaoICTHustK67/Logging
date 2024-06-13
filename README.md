# Fluentbit SetUp Files
## Họ và tên: Hoàng Bá Bảo

- Tạo namespace phục vụ riêng cho việc logging bằng câu lệnh :
```
kubectl apply -f namespace.yaml
```

- Tạo serviceaccount với với clusterrole tương ứng để trao quyền cho fluentbit giám sát các pod của web service và api service :
```
kubectl apply -f serviceaccount.yaml
```

- Tạo config map với các config cho DaemonSet khi triển khai fluentbit để có thể ghi nhận log và bắn lên server ElasticSearch:
```
kubectl apply -f configmap.yaml
```

- Triển khai fluentbit với DaemonSet để theo dõi logging :
```
kubectl apply -f daemonset.yaml
```
