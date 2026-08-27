# Bernoulli Reload 2026 - Relatório de Campanha

Documentação técnica da metodologia de mensuração e da arquitetura de dados utilizada no relatório da presença digital do **Bernoulli Reload 2026** nos canais do Porvir.

## 1. Contexto

O Bernoulli Educação realizou o **Reload 2026**, encontro direcionado a lideranças e profissionais da educação, com discussões relacionadas a gestão escolar, inteligência artificial, liderança, aprendizagem e transformação da educação.

Após o evento, o Porvir publicou um conteúdo editorial apresentando aprendizados e discussões derivados do encontro:

**Gestão escolar e IA: aprendizados do Reload 2026**

https://porvir.org/gestao-escolar-ia-reload-2026/

A ativação utiliza a audiência qualificada do Porvir para ampliar a presença do Bernoulli e distribuir conteúdos relacionados ao Reload em diferentes canais digitais.

A análise não se limita à campanha de direcionamento para a matéria publicada no Porvir. O universo de mensuração passa a considerar todas as entregas Bernoulli/Reload identificadas nos canais analisados, incluindo conteúdos de pré-evento, cobertura do evento e pós-evento.

## 2. Escopo temporal

A campanha de amplificação da matéria possui como período principal:

**17/08/2026 a 30/08/2026**

Entretanto, os exports brutos das plataformas demonstraram a existência de entregas Bernoulli anteriores a 17/08, relacionadas ao pré-evento e à cobertura do Reload 2026.

Por esse motivo, o relatório diferencia dois conceitos:

- **período da campanha de amplificação da matéria**, de 17/08/2026 a 30/08/2026;
- **universo total de entregas Bernoulli**, que pode incluir conteúdos publicados antes desse período quando relacionados diretamente ao Reload 2026.

Os dados definitivos serão consolidados após o encerramento da campanha. Durante a construção do relatório poderão ser utilizados dados parciais apenas para validação de estrutura, métricas, filtros e visualizações.

## 3. Objetivo do relatório

O relatório busca responder a duas questões complementares:

> Qual foi o impacto da presença do Bernoulli Reload 2026 nos canais do Porvir em termos de exposição, interação e consumo de conteúdo?

E, especificamente para a matéria publicada no Porvir:

> Qual foi a capacidade das ativações com links parametrizados de direcionar usuários para o conteúdo editorial e gerar consumo efetivo da matéria?

A análise é estruturada em quatro camadas:

**Exposição → Interação → Tráfego → Consumo**

## 4. Universo de peças

O inventário de peças não será definido exclusivamente pela planilha original de links parametrizados.

A planilha inicial de UTMs é tratada como uma referência de tracking, mas não como inventário definitivo das entregas.

O universo final de peças será formado por todas as publicações, anúncios, conteúdos de vídeo, disparos e ativações identificadas como relacionadas ao Bernoulli ou ao Reload 2026 nos dados brutos das plataformas.

Isso inclui conteúdos que:

- possuem UTM;
- não possuem UTM;
- possuem link de saída;
- não possuem link de saída;
- têm objetivo de tráfego;
- têm objetivo de engajamento ou consumo de vídeo.

## 5. Fases da campanha

Cada peça poderá ser classificada por uma dimensão analítica chamada `fase_campanha`.

Valores previstos:

```text
pre_evento
cobertura_evento
pos_evento
```

### 5.1. Pré-evento

Conteúdos publicados antes do Reload 2026 com função de divulgação, contextualização ou preparação da audiência.

### 5.2. Cobertura do evento

Conteúdos publicados durante ou imediatamente relacionados ao evento, incluindo registros, entrevistas, bastidores e cobertura editorial.

### 5.3. Pós-evento

Conteúdos destinados a amplificar aprendizados, repercussões, entrevistas, vídeos e a matéria publicada no Porvir após a realização do Reload 2026.

Essa classificação evita comparar diretamente peças com objetivos editoriais ou de mídia diferentes.

## 6. Modelo de mensuração

### 6.1. Exposição

Mensura a distribuição das peças nos diferentes canais.

Dependendo da disponibilidade de cada plataforma, poderão ser utilizadas métricas como:

- alcance;
- impressões;
- visualizações;
- entregas;
- frequência;
- e-mails enviados;
- e-mails entregues;
- aberturas;
- reproduções de vídeo.

### 6.2. Interação

Mensura a resposta da audiência às peças distribuídas.

Dependendo do canal, poderão ser utilizadas:

- reações;
- curtidas;
- comentários;
- compartilhamentos;
- salvamentos;
- respostas;
- engajamentos;
- cliques;
- cliques no link;
- taxa de engajamento;
- CTR;
- CTOR;
- ThruPlays;
- percentuais de consumo de vídeo.

### 6.3. Tráfego

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

Os parâmetros UTM serão utilizados para identificar os acessos atribuíveis às ativações com links parametrizados.

Uma peça pode fazer parte do relatório de exposição e interação mesmo quando não possui URL de saída ou UTM.

### 6.4. Consumo

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

## 7. Canais analisados

### Instagram

- Feed;
- Reels;
- Stories;
- link da bio.

### Facebook

- Feed;
- demais publicações Bernoulli identificadas no export da plataforma.

### LinkedIn

- Feed;
- demais publicações Bernoulli identificadas no export da plataforma.

### Meta Ads

A mídia paga possui objetivos diferentes e deverá ser segmentada analiticamente.

Campanhas identificadas:

```text
(2026)Bernoulli Tráfego - Post 1
(2026)Bernoulli Engajamento - Reel 1
(2026)Bernoulli Engajamento - Reel 2
(2026)Bernoulli Engajamento - Reel 3
```

A campanha de tráfego possui link de saída para a matéria.

Os três Reels de engajamento não possuem link de saída de forma intencional. O objetivo dessas peças é consumo e interação com o vídeo dentro do ambiente da Meta.

Por isso, os Reels não devem ser avaliados pelos mesmos KPIs da campanha de tráfego.

### WhatsApp

Distribuição em comunidades temáticas do Porvir:

- Metodologias Ativas;
- Tecnologia;
- Socioemocional;
- Antirracista.

### Newsletter

Distribuição por e-mail marketing para a base do Porvir.

## 8. Fontes de dados

O relatório utiliza três categorias principais de fonte.

### 8.1. Exports brutos das plataformas

Os exports das plataformas são utilizados para:

- identificar o universo completo de peças Bernoulli;
- validar datas de publicação;
- preservar IDs técnicos das publicações;
- coletar métricas de exposição e interação;
- localizar entregas que não constavam na planilha inicial de links.

Os exports brutos devem ser preservados sem alterações como evidência da origem dos dados.

### 8.2. Google Sheets

As métricas utilizadas no Looker Studio serão organizadas manualmente em Google Sheets.

Isso inclui, conforme disponibilidade:

- Instagram;
- Facebook;
- LinkedIn;
- WhatsApp;
- Newsletter;
- Meta Ads.

Como o projeto possui duração limitada, a coleta manual foi escolhida para evitar contratação e configuração de conectores pagos exclusivamente para uma campanha curta.

### 8.3. Google Analytics 4

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

## 9. Fluxo de dados

```text
Exports das plataformas
        |
        v
Identificação das peças Bernoulli
        |
        v
Normalização e coleta manual
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

## 10. Estrutura do Google Sheets

Estrutura atual:

```text
01_pecas
02_instagram
03_facebook
04_linkedin
05_whatsapp
06_newsletter
07_meta_ads
```

A aba `01_pecas` funciona como cadastro mestre das entregas da campanha.

As demais abas armazenam as métricas específicas de cada plataforma.

Uma aba consolidada adicional somente será criada se houver necessidade analítica que não possa ser resolvida diretamente no Looker Studio.

## 11. Cadastro mestre de peças

A aba `01_pecas` deverá conter, quando disponível:

- ID interno da peça;
- canal;
- grupo de canal;
- tipo de distribuição;
- fase da campanha;
- data de publicação;
- parâmetros UTM originais;
- parâmetros normalizados;
- URL de destino;
- URL parametrizada;
- link encurtado;
- status de tracking;
- observações técnicas.

Quando os exports fornecerem identificadores técnicos da plataforma, como ID da publicação ou permalink, esses dados poderão ser preservados nas abas específicas para facilitar auditoria e rastreabilidade.

## 12. Identificação das peças e UTMs

Sempre que possível, as peças com tráfego para o site serão identificadas utilizando:

```text
utm_source
utm_medium
utm_campaign
utm_term
utm_content
utm_id
```

Entretanto, a presença de UTM não é requisito para uma peça pertencer ao universo Bernoulli.

A regra metodológica adotada é:

> UTM identifica e atribui tráfego. O universo da campanha é definido pelas entregas Bernoulli identificadas nas plataformas.

## 13. Normalização das UTMs

A análise preliminar dos links identificou diferenças na nomenclatura das campanhas entre alguns canais.

Entre os valores existentes estão:

```text
campanha_reload_2026
reload-2026-newsletter22826
reload-2026-linkedin
```

Essas diferenças deverão ser consideradas nos filtros do GA4 e do Looker Studio.

A camada analítica poderá utilizar uma campanha normalizada, preservando simultaneamente os valores originais registrados no GA4.

## 14. Inconsistência identificada no LinkedIn

Foi identificada uma inconsistência no link parametrizado utilizado para LinkedIn:

```text
utm_source=instagram
utm_campaign=reload-2026-linkedin
utm_content=linkedin
```

Embora `utm_source` indique Instagram, `utm_campaign` e `utm_content` permitem identificar o tráfego relacionado ao LinkedIn.

O tráfego cuja campanha seja:

```text
reload-2026-linkedin
```

deverá ser classificado analiticamente como **LinkedIn**, independentemente do valor registrado em `utm_source`.

## 15. Meta Ads e normalização de origem

A campanha de tráfego Meta Ads utiliza:

```text
utm_source=instagram
utm_medium=paid_social
utm_campaign=campanha_reload_2026
utm_term=meta_porvir
utm_content=image_ad
utm_id=img_01
```

O valor original de `utm_source` será preservado, mas a combinação `paid_social` + `meta_porvir` permite classificar essa origem analiticamente como **Meta Ads**.

As campanhas de Reels não possuem links de saída e, portanto, não entram na atribuição de tráfego do GA4.

## 16. Presença global versus tráfego atribuível

O relatório deverá separar duas perspectivas.

### 16.1. Presença global Bernoulli

Considera todas as entregas relacionadas ao Bernoulli Reload 2026 identificadas nos canais do Porvir.

Pode incluir:

- conteúdos sem link;
- vídeos;
- cobertura do evento;
- conteúdos de pré-evento;
- conteúdos de pós-evento;
- mídia paga de engajamento.

Essa perspectiva mede principalmente exposição, interação e consumo de mídia.

### 16.2. Tráfego atribuível à matéria

Considera somente acessos que possam ser relacionados à matéria por meio dos dados observáveis no GA4 e dos parâmetros de campanha.

Essa perspectiva mede:

- usuários;
- sessões;
- visualizações;
- leitura de 50%;
- tempo médio de engajamento;
- qualidade do tráfego.

As duas perspectivas não devem ser somadas como se representassem a mesma etapa do funil.

## 17. Tráfego da campanha e tráfego total da matéria

A matéria pode receber acessos provenientes de fontes não diretamente relacionadas às ativações Bernoulli, incluindo:

- Organic Search;
- Direct;
- Referral;
- navegação interna do Porvir;
- outros canais.

Por isso, o relatório deverá distinguir:

**Tráfego total da matéria**

versus

**Tráfego atribuível às ativações Bernoulli com links parametrizados**

Essa separação permite analisar o peso da campanha sobre a audiência total do conteúdo.

## 18. Indicadores de qualidade

### Taxa de leitura de 50%

Conceitualmente:

```text
Usuários que atingiram 50% do conteúdo
/
Usuários que acessaram o conteúdo
```

O cálculo definitivo deverá respeitar a implementação e a granularidade do evento existente no GA4, evitando misturar usuários únicos com contagem de eventos.

### Tempo médio de engajamento

O tempo médio de engajamento será utilizado para avaliar quanto tempo os usuários permaneceram efetivamente envolvidos com a matéria.

Sempre que possível, essa métrica será analisada por canal de aquisição.

## 19. Métricas de Meta Ads

### Campanha de tráfego

Priorizar:

- investimento;
- alcance;
- impressões;
- frequência;
- cliques no link;
- Landing Page Views;
- CTR;
- CPC.

Quando tecnicamente possível, poderão ser calculados indicadores como:

```text
Investimento
/
Leituras de 50%
```

resultando em custo por leitura qualificada.

### Campanhas de Reels

Priorizar:

- investimento;
- alcance;
- impressões;
- frequência;
- reproduções;
- visualizações em 25%;
- visualizações em 50%;
- visualizações em 75%;
- visualizações em 95%;
- visualizações em 100%;
- ThruPlays;
- custo por ThruPlay;
- interações.

## 20. WhatsApp

As comunidades possuem links parametrizados individualmente.

Isso possibilita comparar o tráfego e o consumo do conteúdo entre:

- Metodologias Ativas;
- Tecnologia;
- Socioemocional;
- Antirracista.

Mesmo quando métricas tradicionais de alcance ou impressão não estiverem disponíveis, o GA4 poderá ser utilizado para avaliar os acessos gerados pelos links de cada comunidade.

## 21. Estrutura prevista do relatório

### Visão geral

Principais indicadores consolidados da presença Bernoulli e da campanha.

### Linha do tempo e fases

Separação entre pré-evento, cobertura e pós-evento, quando útil para interpretação.

### Redes sociais

Desempenho das peças orgânicas distribuídas em Instagram, Facebook e LinkedIn.

### Meta Ads

Separação entre campanhas de geração de tráfego e campanhas de consumo de vídeo.

### Newsletter e WhatsApp

Resultados dos canais de relacionamento e distribuição direta.

### Tráfego para o conteúdo

Aquisição observada no GA4 e participação dos diferentes canais.

### Qualidade do consumo

Leitura de 50%, taxa de leitura e tempo médio de engajamento.

## 22. Limitações metodológicas

O relatório mede principalmente o impacto digital **observável e atribuível** aos dados disponíveis.

Os parâmetros UTM permitem identificar acessos originados diretamente dos links parametrizados.

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

Da mesma forma, conteúdos sem link podem gerar impacto de marca, informação ou lembrança sem produzir um acesso diretamente atribuível.

Portanto, os resultados não devem ser interpretados como mensuração absoluta de causalidade.

## 23. Princípio metodológico

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

Nem todas as peças percorrem obrigatoriamente todas as etapas.

Um Reel sem link pode gerar exposição, interação e consumo de vídeo, mas não tráfego direto para o site.

Uma peça de tráfego pode ser avaliada até a etapa de consumo da matéria.

O objetivo é respeitar o papel de cada formato e evitar comparações entre KPIs de objetivos diferentes.

## 24. Ferramentas

- Google Analytics 4
- Google Sheets
- Looker Studio
- Meta Business Suite
- Meta Ads Manager
- plataformas de Social Media
- plataforma de e-mail marketing
- GitHub

## 25. Status do projeto

**Fase atual:** estruturação e coleta de dados.

Etapas em andamento:

1. inventariar todas as peças Bernoulli nos exports das plataformas;
2. classificar as peças por fase da campanha;
3. atualizar a tabela mestre `01_pecas`;
4. alimentar as abas específicas de cada canal;
5. validar as UTMs no GA4;
6. validar o evento de leitura de 50%;
7. conectar Google Sheets e GA4 ao Looker Studio;
8. construir campos calculados e normalizações;
9. desenvolver as visualizações;
10. substituir dados parciais pelos dados definitivos após 30/08/2026;
11. validar os resultados;
12. consolidar as análises finais.

## 26. Responsabilidade técnica

Projeto de mensuração, análise e estruturação de dados desenvolvido pela **Ad Rock Digital Mkt** para suporte ao relatório da presença do Bernoulli Reload 2026 nos canais do Porvir.
