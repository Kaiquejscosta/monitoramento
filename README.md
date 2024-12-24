# 🛠️ Monitoramento

Este repositório é dedicado a soluções de 🖥️ monitoramento utilizando ferramentas como 📊 Grafana, 📡 Prometheus e 🎮 Ping Exporter. Ele inclui dashboards prontos, configurações de exportadores e exemplos de configurações para facilitar a implantação e gestão de ambientes de monitoramento.

## 📂 Conteúdo do Repositório
- **📈 Dashboards do Grafana**:
  Arquivos `.json` contendo dashboards prontos para monitorar 📊 métricas diversas.
- **⚙️ Configurações do Prometheus**:
  Exemplos de configuração do `prometheus.yml` para coleta e armazenamento de métricas.
- **🌐 Configurações do Ping Exporter**:
  Configurações para monitorar a ⏳ latência e a ✅ disponibilidade de hosts.
- **📜 Arquivos Systemd**:
  Configurações para inicializar o Prometheus automaticamente como um serviço no sistema.

## 🛠️ Ferramentas Utilizadas

### 📊 Grafana
Grafana é uma plataforma de visualização e monitoramento que permite criar dashboards dinâmicos para exibir métricas em tempo real.

### 📡 Prometheus
Prometheus é um sistema de monitoramento e banco de dados de séries temporais amplamente utilizado para coletar e armazenar métricas.

### 🌐 Ping Exporter
Exportador utilizado para monitoramento de hosts via ICMP (🔢 ping), integrando com o Prometheus.

## 🚀 Como Utilizar

### 📥 Importar Dashboards do Grafana
1. Acesse o Grafana em seu navegador 🌐.
2. Navegue até a seção de dashboards e clique em "Import".
3. Faça upload de um arquivo `.json` presente na pasta `dashboards` deste repositório.

### ⚙️ Configurar o Prometheus
1. Copie o exemplo de configuração `prometheus.yml` para o diretório de configuração do Prometheus (geralmente `/etc/prometheus/`).
2. Atualize os alvos de monitoramento (⏯ targets) conforme seu ambiente.
3. Copie o arquivo `prometheus.service` para o diretório `/etc/systemd/system/` para configurar o Prometheus como um serviço systemd.
4. Habilite e inicie o serviço Prometheus:
   ```bash
   sudo systemctl enable prometheus.service
   sudo systemctl start prometheus.service
   ```

### 🌐 Configurar o Ping Exporter
1. Edite o arquivo de configuração do Ping Exporter para incluir os hosts que deseja monitorar.
2. Certifique-se de que o Prometheus está configurado para coletar métricas do Ping Exporter.
3. Criar serviço com o arquivo ping_exporter.service.
4. Copiando arquivo `ping_exporter.service` para o diretório `/etc/systemd/system/` para configurar o ping_exporter como um serviço systemd.
   ```bash
   systemctl daemon-reload
   systemctl enable --now ping_exporter.service 
   ```
## 📋 Requisitos
- 📊 Grafana instalado na máquina ou em outro servidor.
- 📡 Prometheus configurado nativamente no sistema.
- 🌐 Ping_exporter configurado como serviço e arquivo targets.yml modificado.
## ⚙️ Instalação e Execução
1. Clone o repositório:
   ```bash
   git clone <url-do-repositorio>
   cd monitoramento
   ```
2. Configure os arquivos de configuração conforme descrito acima.
3. Reinicie ou inicie os serviços conforme necessário:
4. OBS: Grafana rodando em Docker, o comando para restartar o container é outro. Para mais informações clique aqui: [Docker](mailto:<https://github.com/Kaiquejscosta/docker>)
   ```bash
   sudo systemctl restart prometheus.service
   sudo systemctl restart grafana-server
   ```
5. Acesse o Grafana em [http://localhost:3000](http://localhost:3000).

## 🗂️ Estrutura do Repositório
```
monitoramento/
├── dashboard_grafana/
│   ├── exemplo-dashboard1.json
│   ├── exemplo-dashboard2.json
├── prometheus/
│   ├── prometheus.yml
│   ├── prometheus.service
├── ping_exporter/
│   ├── targets.yml
|   ├── ping_exporter.service
└── README.md
```

## 🤝 Contribuições
Contribuições são bem-vindas! Caso tenha sugestões, melhorias ou novos exemplos, fique à vontade para enviar pull requests ou abrir issues.

## 📜 Licença
Este projeto está licenciado sob a Licença MIT. Consulte o arquivo [LICENSE](LICENSE) para mais detalhes.

## 📧 Contato
Para dúvidas ou sugestões, entre em contato com [Kaique](mailto:<www.linkedin.com/in/kaique-costa-0b25ba1b7>) ou abra uma issue neste repositório.
