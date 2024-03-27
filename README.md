# Relatório sobre Observabilidade do .NET com OpenTelemetry

---

## Introdução

Ao executar um aplicativo, é essencial monitorar seu desempenho e detectar problemas potenciais antes que eles se tornem significativos. Uma abordagem para isso é a observabilidade, que envolve a captura e análise de telemetria, como logs e métricas, para entender o estado e o comportamento do sistema em tempo real.

## O que é Observabilidade?

A observabilidade em sistemas distribuídos refere-se à capacidade de monitorar e analisar a telemetria de cada componente do sistema, identificar mudanças no desempenho e diagnosticar as razões por trás dessas mudanças. Isso envolve o uso de logs, métricas e rastreamento distribuído para obter insights sobre o sistema.

## Os Três Pilares da Observabilidade

- **Logs**: Registram operações individuais, como solicitações de entrada, falhas em componentes específicos e interações entre diferentes partes do sistema.
  
- **Métricas**: Contadores e medidores que fornecem dados quantitativos sobre o sistema, como o número de solicitações concluídas, a latência das solicitações e o número de usuários ativos.
  
- **Rastreamento Distribuído**: Rastreia o fluxo de solicitações através de diferentes componentes do sistema, permitindo a identificação de gargalos de desempenho e a análise de falhas.

## Abordagens de Observabilidade no .NET

Existem várias maneiras de implementar a observabilidade em aplicativos .NET:

- **Explicitamente no código**: Integrando bibliotecas como o OpenTelemetry diretamente no código-fonte para coletar e enviar telemetria.

- **Fora do processo**: Usando ferramentas como o dotnet-monitor para capturar e processar logs e métricas sem modificar o código-fonte.

- **Usando um gancho de inicialização**: Injetando assemblies no processo para coletar instrumentação, como na Instrumentação Automática do .NET OpenTelemetry.

## O que é OpenTelemetry?

O OpenTelemetry (OTel) é um padrão aberto e multiplataforma para coleta e emissão de dados de telemetria. Ele fornece APIs para gravar dados de telemetria, configurar o envio desses dados pela rede e definir convenções semânticas para nomenclatura e conteúdo de dados.

## Prometheus: Coleta de Métricas

O Prometheus é um sistema de banco de dados de série temporal usado para coletar, agregar e armazenar métricas. Ele é configurado com pontos de extremidade de métricas para cada serviço, coletando valores periodicamente e armazenando-os em seu banco de dados. Os dados coletados são instantâneos das métricas do processo, sendo valiosos para análise e detecção de anomalias quando comparados com valores históricos.

## Grafana: Criação de Dashboards

O Grafana é uma ferramenta que permite criar dashboards e alertas com base em fontes de dados como o Prometheus. Com o Grafana, é possível visualizar métricas de forma intuitiva, criar gráficos e painéis personalizados para monitorar o desempenho do sistema e identificar padrões ou problemas.

## Jaeger: Rastreamento Distribuído

O Jaeger é uma plataforma de código aberto para rastreamento distribuído, permitindo acompanhar unidades de trabalho com atividades em um sistema distribuído. Ele correlaciona atividades usando tags como TraceId, SpanId e ParentId, facilitando a visualização do trabalho realizado em cada transação. Com o Jaeger, é possível coletar, armazenar e correlacionar atividades, proporcionando insights detalhados sobre o funcionamento do sistema.

## Conclusão

O OpenTelemetry é uma ferramenta poderosa para implementar a observabilidade em aplicativos .NET, fornecendo um padrão comum para coleta e emissão de dados de telemetria. Com seu uso, os desenvolvedores podem entender melhor o comportamento de seus sistemas em tempo real e tomar medidas proativas para melhorar seu desempenho e confiabilidade.

O uso conjunto do Prometheus, Grafana e Jaeger proporciona uma solução abrangente para observabilidade em sistemas distribuídos. Essas ferramentas permitem monitorar o desempenho, identificar problemas e analisar tendências, facilitando a manutenção e otimização de aplicativos em ambientes complexos e em escala.

Prints da execução: 
![Captura de tela 2024-03-27 094759](https://github.com/Ra2861/Prometheus/assets/99209068/d9d999a4-946e-4c0d-b9a6-bbef09334645)

\metricas

![Captura de tela 2024-03-27 095228](https://github.com/Ra2861/Prometheus/assets/99209068/b3538233-d05e-4812-b771-6db7929e21a4)
