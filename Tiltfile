custom_build(
    ref = 'catalog-service-v2',
    command = './gradlew bootBuildImage --imageName $EXPECTED_REF',
    deps = ['build.gradle', 'src']
)

k8s_yaml(['k8s/deployment.yaml', 'k8s/service.yml'])

k8s_resource('catalog-service', port_forwards=['9001'])
