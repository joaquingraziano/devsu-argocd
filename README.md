Una vez desplegado mediante terraform, podemos utilizar los siguientes comandos para acceder al management de ArgoCD en entorno local:

- Exponer puertos: kubectl port-forward svc/argocd-server -n argocd 8080:443
- Para autenticarse, se debe ingresar el usuario admin y la contraseña se obtiene con el comando kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d && echo


