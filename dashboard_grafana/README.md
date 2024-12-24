# 🛠️ Explicações sobre Dashboards

1.[dashboard_de_exemplos](https://github.com/Kaiquejscosta/monitoramento/blob/main/dashboard_grafana/dashboard_de_exemplos.json): Dashboard que utiliza prometheus como fonte de dados, utilizando a metricas de perdade pacotes e monitoramentos de serviços
que são coletadas partir de um script em shell, para mais informações dos scripts clique aqui: [ShellScript](https://github.com/Kaiquejscosta/ShellScript)

2.[dashboard_servidores_filiais_finalizado.json](https://github.com/Kaiquejscosta/monitoramento/blob/main/dashboard_grafana/dashboard_servidores_filiais_finalizado.json): Dashboard que utiliza a métrica do ping_exporter/Promtheus ping_loss_ratio que é focado 100% na perda de pacotes e oscilação da rede, onde 0 estável, sem perdar e 1 100% de perda de pacote. ou seja máquina sem rede ou link indisponível, qualuqer valor entre 0 e 1 é instabilidade na rede.
