https://madhuakula.com/kubernetes-goat/index.html
kubernetes-goat
1. `git-dumper` - для выгрузки файлов с сайта имещие контроль версией
2. `trufflehog` - ПО для поиска секретов в папке
3. `docker-bench-security` - поднимается в k8s pod для анализ контрольных показателей Docker CIS (лаба 6,5)
4. `kube-bench-security` - поднимается в k8s pod для анализ контрольных показателей k8s CIS (лаба 6,6)
5. `nmap` - анализ открытых портов (лаб 6.8)
6. исправление уязвимости helm v2 - https://engineering.bitnami.com/articles/helm-security.html
7. интсрументы для теста `kubectl run -it hacker-container --image=madhuakula/hacker-container -- sh` (лаб 6.14)
8. `Dive` это удивительный инструмент, который помогает анализировать каждый слой изображения.
9. KubeAudit - Аудит кластеров Kubernetes - https://github.com/Shopify/kubeaudit лаб 6.17
10. Sysdig Falco - Мониторинг и Обнаружение безопасности во время выполнения
    `helm repo add falcosecurity https://falcosecurity.github.io/charts
    helm repo update
    helm install falco falcosecurity/falco`
      https://falco.org/
11. Popeye - Дезинфицирующее Средство для кластеров Kubernetes https://github.com/derailed/popeye (лаб 6,19)
