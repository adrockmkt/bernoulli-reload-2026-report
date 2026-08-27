# Bernoulli Reload 2026 - Relatório de Campanha

Documentação técnica da metodologia de mensuração e da arquitetura de dados utilizada no relatório da campanha **Bernoulli Reload 2026**, realizada nos canais do Porvir entre **17 e 30 de agosto de 2026**.

## 1. Contexto

O Bernoulli Educação realizou o **Reload 2026**, encontro direcionado a lideranças e profissionais da educação, com discussões relacionadas a gestão escolar, inteligência artificial, liderança, aprendizagem e transformação da educação.

Após o evento, o Porvir publicou um conteúdo editorial apresentando aprendizados e discussões derivados do encontro:

**Gestão escolar e IA: aprendizados do Reload 2026**

https://porvir.org/gestao-escolar-ia-reload-2026/

A campanha utiliza a audiência do Porvir, formada majoritariamente por profissionais ligados à educação, para ampliar a distribuição desse conteúdo por diferentes canais digitais.

A ação não possui como objetivo principal a inscrição ou participação no evento, uma vez que o Reload 2026 já havia ocorrido.

O objetivo da mensuração é avaliar a capacidade da campanha de:

1. alcançar a audiência;
2. gerar interação com as peças;
3. direcionar usuários para o conteúdo publicado no Porvir;
4. gerar consumo efetivo do conteúdo editorial.

## 2. Período analisado

Período oficial da campanha:

**17/08/2026 a 30/08/2026**

Os dados definitivos serão consolidados após o encerramento da campanha.

Durante o período de veiculação poderão ser utilizados dados parciais exclusivamente para construção, validação e testes do relatório.

## 3. Objetivo do relatório

O relatório busca responder à seguinte questão:

> Qual foi a capacidade da campanha do Bernoulli Reload 2026 de alcançar a audiência qualificada do Porvir, gerar interação, direcioná-la ao conteúdo editorial e produzir consumo efetivo da matéria?

A análise é estruturada em quatro camadas:

**Exposição → Interação → Tráfego → Consumo**

## 4. Modelo de mensuração

### 4.1. Exposição

Mensura a distribuição das peças nos diferentes canais.

Dependendo da disponibilidade de cada plataforma, poderão ser utilizadas métricas como:

- alcance;
- impressões;
- entregas;
- frequência;
- e-mails enviados;
- e-mails entregues;
- aberturas.

### 4.2. Interação

Mensura a resposta da audiência às peças distribuídas.

Dependendo do canal, poderão ser utilizadas:

- reações;
- curtidas;
- comentários;
- compartilhamentos;
- engajamentos;
- cliques;
- cliques no link;
- taxa de engajamento;
- CTR;
- CTOR.

### 4.3. Tráfego

Mensura os usuários efetivamente direcionados para o conteúdo publicado no Porvir.

O Google Analytics 4 será utilizado como principal fonte para esta camada.

Principais métricas:

- usuários;
- sessões;
- visualizações;
- origem;
- mídia;
- campanha;
- conteúdo da campanha;
- identificação da peça.

Os parâmetros UTM serão utilizados para identificar os acessos atribuíveis às ativações da campanha.

### 4.4. Consumo

Mensura a qualidade do acesso após a chegada ao conteúdo.

Principais indicadores:

- usuários que atingiram 50% da matéria;
- taxa de leitura de 50%;
- tempo médio de engajamento;
- comportamento por canal;
- comportamento por origem;
- comportamento por peça, quando tecnicamente identificável.

O evento principal configurado no GA4 relacionado ao consumo de 50% do conteúdo será utilizado como indicador de leitura.

Para fins de comunicação no relatório, esse indicador deverá ser apresentado preferencialmente como **Leitura de 50%** ou equivalente, evitando utilizar apenas o termo genérico "conversão".

## 5. Canais da campanha

A campanha utiliza diferentes pontos de distribuição dentro do ecossistema do Porvir.

### Instagram

- Stories;
- Feed;
- direcionamento por link da bio.

### Facebook

- Feed.

### LinkedIn

- Feed.

### Meta Ads

- impulsionamento e mídia paga relacionada às peças da campanha.

### WhatsApp

Distribuição em comunidades temáticas do Porvir:

- Metodologias Ativas;
- Tecnologia;
- Socioemocional;
- Antirracista.

### Newsletter

Distribuição por e-mail marketing para a base do Porvir.

## 6. Arquitetura de dados

O relatório utiliza duas categorias principais de fontes.

### 6.1. Google Sheets

As métricas das plataformas que não possuem integração automatizada com o Looker Studio serão coletadas manualmente e armazenadas em Google Sheets.

Isso inclui, conforme disponibilidade:

- Instagram;
- Facebook;
- LinkedIn;
- WhatsApp;
- Newsletter;
- Meta Ads.

Como a campanha possui duração limitada, a coleta manual foi escolhida para evitar a contratação e configuração de conectores pagos exclusivamente para um período curto de análise.

Os dados poderão ser inseridos parcialmente durante a construção do relatório e substituídos pelos valores definitivos após o encerramento da campanha.

### 6.2. Google Analytics 4

O GA4 será conectado diretamente ao Looker Studio.

Será utilizado para analisar:

- tráfego para a matéria;
- usuários;
- sessões;
- visualizações;
- UTMs;
- origem e mídia;
- campanhas;
- consumo do conteúdo;
- evento de leitura de 50%;
- tempo médio de engajamento.

## 7. Fluxo de dados

A arquitetura simplificada do projeto é:

```text
Instagram
Facebook
LinkedIn
Newsletter
WhatsApp
Meta Ads
        |
        v
Coleta manual
        |
        v
Google Sheets
        |
        v
Looker Studio
```

Paralelamente:

```text
Links parametrizados
        |
        v
Site Porvir
        |
        v
GA4
        |
        v
Looker Studio
```

O Looker Studio funciona como camada final de visualização e análise.

## 8. Estrutura prevista do Google Sheets

A estrutura inicial prevista é:

```text
01_pecas
02_instagram
03_facebook
04_linkedin
05_whatsapp
06_newsletter
07_meta_ads
08_resumo
```

A aba `01_pecas` funcionará como cadastro mestre das peças e parâmetros de campanha.

As demais abas armazenarão as métricas coletadas em cada plataforma.

A estrutura definitiva das colunas será documentada separadamente após validação das métricas disponíveis em cada canal.

## 9. Identificação das peças

Sempre que possível, as peças serão identificadas utilizando os parâmetros:

```text
utm_source
utm_medium
utm_campaign
utm_term
utm_content
utm_id
```

Esses parâmetros permitem identificar diferentes dimensões da distribuição, como:

- plataforma;
- canal;
- campanha;
- posicionamento;
- comunidade;
- formato;
- peça.

## 10. Normalização das UTMs

A análise preliminar dos links identificou diferenças na nomenclatura das campanhas entre alguns canais.

Entre os valores existentes estão:

```text
campanha_reload_2026
reload-2026-newsletter22826
reload-2026-linkedin
```

Essas diferenças deverão ser consideradas na construção dos filtros do GA4 e do Looker Studio.

Não será considerado apenas um único valor de `utm_campaign` para identificar todo o tráfego da campanha.

## 11. Inconsistência identificada no LinkedIn

Foi identificada uma inconsistência no link parametrizado utilizado para LinkedIn.

O link contém:

```text
utm_source=instagram
utm_campaign=reload-2026-linkedin
utm_content=linkedin
```

Embora `utm_source` indique Instagram, os parâmetros `utm_campaign` e `utm_content` permitem identificar o tráfego relacionado ao LinkedIn.

Para preservar a consistência histórica dos dados durante a campanha, a análise deverá considerar essa inconsistência por meio de normalização no relatório.

O tráfego cuja campanha seja identificada como:

```text
reload-2026-linkedin
```

deverá ser classificado analiticamente como **LinkedIn**, independentemente do valor registrado em `utm_source`.

## 12. Tráfego da campanha e tráfego total

O conteúdo publicado no Porvir pode receber acessos provenientes de fontes não diretamente relacionadas à campanha, incluindo:

- Organic Search;
- Direct;
- Referral;
- navegação interna do Porvir;
- outros canais.

Por isso, o relatório deverá distinguir:

**Tráfego total da matéria**

e

**Tráfego atribuível aos links parametrizados da campanha Bernoulli Reload 2026**

Essa separação permite analisar a participação da campanha na audiência total gerada pelo conteúdo.

## 13. Indicadores de qualidade

Além das métricas tradicionais de mídia, o projeto prioriza indicadores capazes de demonstrar consumo efetivo do conteúdo.

### Taxa de leitura de 50%

Conceitualmente:

```text
Usuários que atingiram 50% do conteúdo
/
Usuários que acessaram o conteúdo
```

O cálculo definitivo deverá respeitar a implementação e a granularidade do evento existente no GA4 para evitar diferenças entre usuários únicos e contagem de eventos.

### Tempo médio de engajamento

O tempo médio de engajamento será utilizado para avaliar quanto tempo os usuários permaneceram efetivamente envolvidos com o conteúdo.

Sempre que possível, essa métrica será analisada por canal de aquisição.

## 14. Meta Ads

Para mídia paga, serão priorizadas métricas como:

- investimento;
- alcance;
- impressões;
- frequência;
- cliques no link;
- CTR;
- CPC;
- Landing Page Views.

Quando tecnicamente possível, os dados do Meta Ads serão relacionados ao comportamento observado no GA4.

Isso permitirá análises adicionais como:

```text
Investimento
/
Leituras de 50%
```

resultando em um indicador de **custo por leitura qualificada**.

Esse indicador somente deverá ser utilizado quando houver segurança suficiente na atribuição entre a mídia e o comportamento registrado no GA4.

## 15. WhatsApp

As comunidades de WhatsApp possuem links parametrizados individualmente.

Isso possibilita comparar o tráfego e o consumo do conteúdo entre:

- Metodologias Ativas;
- Tecnologia;
- Socioemocional;
- Antirracista.

Mesmo quando métricas tradicionais de alcance ou impressão não estiverem disponíveis, o GA4 poderá ser utilizado para avaliar o resultado gerado pelos links de cada comunidade.

## 16. Estrutura prevista do relatório

O relatório no Looker Studio deverá ser organizado inicialmente nas seguintes áreas:

### Visão geral

Principais indicadores consolidados da campanha.

### Redes sociais

Desempenho das peças orgânicas distribuídas em Instagram, Facebook e LinkedIn.

### Meta Ads

Desempenho da mídia paga e eficiência na geração de tráfego.

### Newsletter e WhatsApp

Resultados dos canais de relacionamento e distribuição direta.

### Tráfego para o conteúdo

Aquisição observada no GA4 e participação dos diferentes canais.

### Qualidade do consumo

Análise de leitura de 50%, taxa de leitura e tempo médio de engajamento.

## 17. Limitações metodológicas

O relatório mede principalmente o impacto digital **observável e atribuível** aos dados disponíveis.

Os parâmetros UTM permitem identificar acessos originados diretamente dos links parametrizados da campanha.

Entretanto, não é possível atribuir integralmente comportamentos indiretos.

Exemplo:

```text
Usuário visualiza uma publicação
        |
        v
Não clica
        |
        v
Posteriormente pesquisa pelo conteúdo
        |
        v
Acessa a matéria por outro canal
```

Nesse cenário, o acesso poderá ser atribuído pelo GA4 a Organic Search, Direct ou outro canal, mesmo que a exposição inicial à campanha tenha influenciado o comportamento.

Portanto, os resultados não devem ser interpretados como mensuração absoluta de causalidade.

O relatório representa o impacto mensurável por meio das plataformas, dos links parametrizados e do comportamento registrado no GA4.

## 18. Princípio metodológico

O projeto utiliza o seguinte modelo como base para interpretação dos resultados:

```text
EXPOSIÇÃO
    |
    v
INTERAÇÃO
    |
    v
TRÁFEGO
    |
    v
CONSUMO
```

O objetivo não é avaliar apenas o volume de impressões, alcance ou interações isoladamente.

A análise busca compreender a capacidade da campanha de transformar distribuição de mídia em acesso e, posteriormente, em consumo efetivo do conteúdo editorial.

## 19. Ferramentas

- Google Analytics 4
- Google Sheets
- Looker Studio
- Meta Ads Manager
- Plataformas de Social Media
- Plataforma de E-mail Marketing
- GitHub

## 20. Status do projeto

**Fase atual:** planejamento e estruturação da mensuração.

Próximas etapas:

1. definir a estrutura definitiva do Google Sheets;
2. definir as métricas disponíveis por canal;
3. inserir dados parciais para desenvolvimento;
4. conectar o Google Sheets ao Looker Studio;
5. conectar o GA4 ao Looker Studio;
6. validar as UTMs no GA4;
7. validar o evento de leitura de 50%;
8. construir os campos calculados;
9. desenvolver as visualizações;
10. substituir os dados parciais pelos dados definitivos após 30/08/2026;
11. validar os resultados;
12. consolidar as análises finais.

## 21. Responsabilidade técnica

Projeto de mensuração, análise e estruturação de dados desenvolvido pela **Ad Rock Digital Mkt** para suporte ao relatório da campanha Bernoulli Reload 2026 realizada nos canais do Porvir.
