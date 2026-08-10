# Evidências P4 sobre instrumentação, condições, analytics e governança

**Categoria:** levantamento de referências e síntese de concepção metodológica  
**Recorte temporal:** 3 de agosto de 2026  
**Estado:** histórico e não normativo

Este documento preserva a etapa P4 da investigação sobre instrumentação, condições experimentais, analytics e governança. O pacote antecede o framework integrado de protocolos e dados de pesquisa preservado em `docs/evidencias/protocolos-dados-analytics-2026-08.md`.

O P4 foi produzido como pacote de pesquisa dentro de uma taxonomia histórica de configuração. Rótulos como `accepted`, `completed-package`, `decision` e recomendações de incorporação à taxonomia descrevem a autoridade interna daquela etapa e não constituem decisões vigentes do ARA.

O material não aprova eventos, medidas, construtos, instrumentos, perfis, valores, defaults, precedência, políticas jurídicas, fórmulas, limiares, dashboards, event store, LRS, warehouse, banco de dados, schema, modelo preditivo, arquitetura, interface, stack, coleta com participantes ou implementação.

## 1. Problema investigado

O P4 partiu do risco de converter rastros técnicos em afirmações educacionais sem base metodológica. A síntese propôs manter separadas as seguintes camadas:

```text
pergunta ou finalidade
→ protocolo
→ condição
→ evento autorizado ou instrumento
→ medida
→ construto
→ interpretação
→ decisão ou intervenção
```

A principal restrição registrada foi que nenhuma camada deve ser inferida automaticamente da anterior. Cliques, tempo, atrasos, tentativas, interrupções, navegação ou conclusão estrutural não são medidas diretas de atenção, esforço, engajamento, dificuldade, domínio ou aprendizagem.

A etapa posterior da Issue 5 refinou essa cadeia ao explicitar atribuição à condição e registros de evidência. O P4 permanece útil como procedência da formulação e como corpus de referências.

## 2. Corpus de evidências do P4

O levantamento estruturado reuniu 36 registros entre literatura acadêmica, especificações, legislação, orientações regulatórias, frameworks, políticas institucionais, princípios de governança e padrões técnicos. A presença no corpus não implica adoção pelo ARA.

| ID | Fonte | Ano | Frente | Papel registrado na investigação |
|---|---|---:|---|---|
| P4-01 | SoLAR, *Ethics and Learning Analytics: Charting the (Un)Charted* | 2017 | ética e governança | responsabilidade, transparência, proporcionalidade e consequências não pretendidas |
| P4-02 | Pardo e Siemens, *Ethical and privacy principles for learning analytics* | 2014 | ética e governança | transparência, controle do estudante, segurança, responsabilidade e finalidade educacional |
| P4-03 | Drachsler e Greller, checklist DELICATE | 2016 | ética e governança | finalidade, consentimento, transparência, acesso e responsabilidade |
| P4-04 | Zeide, *Unpacking Student Privacy* | 2017 | privacidade | revisão proativa, transparência e responsabilidade algorítmica além de conformidade formal |
| P4-05 | SoLAR, capítulo sobre measurement do *Handbook of Learning Analytics* | 2017 | medição | teoria, validade, unidades e limites; rastros não são construtos por si sós |
| P4-06 | 1EdTech Caliper Analytics 1.2 | 2020 | interoperabilidade | representação de atividades entre sistemas, sem definir construtos ou ética |
| P4-07 | Experience API, xAPI | 2024 | interoperabilidade | statements e perfis; semântica e governança permanecem responsabilidade da implementação |
| P4-08 | W3C PROV-O | 2013 | proveniência | entidades, atividades, agentes e derivações em artefatos e pesquisa |
| P4-09 | W3C Data Privacy Vocabulary | 2024 | vocabulário de privacidade | finalidades, processamento, bases, categorias de dados, direitos e riscos |
| P4-10 | ANPD, orientação sobre dados pessoais para fins acadêmicos e pesquisa | 2024 | Brasil, governança jurídica | base jurídica, boa-fé, transparência, salvaguardas e análise contextual |
| P4-11 | União Europeia, GDPR artigos 5 e 89 | 2016 | União Europeia, legislação | limitação de finalidade, minimização, exatidão, retenção, segurança e salvaguardas de pesquisa |
| P4-12 | UNESCO, *AI and education: protecting the rights of learners* | 2025 | direitos e governança | abordagem baseada em direitos, inclusão, transparência e responsabilidade |
| P4-13 | NIST AI RMF 1.0 | 2023 | governança de IA | governar, mapear, medir e gerir riscos ao longo do ciclo de vida |
| P4-14 | NIST Generative AI Profile | 2024 | governança de IA | riscos documentados, avaliação, proveniência, incidentes e supervisão humana |
| P4-15 | Open University, política de uso ético de dados de estudantes | 2014/2017 | política institucional | finalidades, responsabilidades, transparência e proteção dos estudantes |
| P4-16 | Sclater, *Code of practice for learning analytics* | 2016 | política institucional | responsabilidade, transparência, consentimento, acesso, validade, intervenção e impactos adversos |
| P4-17 | Willis, Slade e Prinsloo, tipologia de supervisão ética | 2016 | ética e governança | modelos institucionais distintos e necessidade de responsabilidade explícita |
| P4-18 | revisão LAK22 sobre ética e privacidade | 2022 | ética e governança | recorrência de privacidade, equidade, transparência e governança |
| P4-19 | LAK23, *Toward Trustworthy Learning Analytics* | 2023 | analytics confiáveis | uso indevido, equidade, transparência, responsabilidade e consequências não pretendidas |
| P4-20 | AERA, padrões para relato de pesquisa empírica em ciências sociais | 2006 | método de pesquisa | transparência de desenho, amostragem, medidas, análise e limitações |
| P4-21 | APA, *Standards for Educational and Psychological Testing* | 2014 | medição e validade | interpretação de escores exige evidência de validade para usos e populações pretendidos |
| P4-22 | CONSORT | 2010 | relato experimental | alocação, fluxo, outcomes, danos e análise em estudos randomizados |
| P4-23 | TREND | 2004 | relato quase experimental | transparência de desenho e análise em avaliações não randomizadas |
| P4-24 | SPIRIT | 2013 | protocolo de pesquisa | objetivos, outcomes, alocação, dados, monitoramento e análise definidos em protocolo |
| P4-25 | TIDieR | 2014 | descrição de intervenção | materiais, procedimentos, adaptação e fidelidade suficientes para replicação |
| P4-26 | APA JARS | 2018 | relato de métodos mistos | transparência específica para métodos quantitativos, qualitativos e mistos |
| P4-27 | FAIR Guiding Principles | 2016 | gestão de dados | dados encontráveis, acessíveis, interoperáveis e reutilizáveis sob governança e metadados |
| P4-28 | CARE Principles for Indigenous Data Governance | 2019 | governança de dados | benefício coletivo, autoridade para controlar, responsabilidade e ética |
| P4-29 | DataCite Metadata Schema | 2024 | proveniência | identificadores persistentes, citação e versionamento de dados e artefatos |
| P4-30 | Open Science Framework, registrations e preregistration | 2026 | fluxo de pesquisa | registros datados de hipóteses, métodos, outcomes e planos analíticos |
| P4-31 | Research Organization Registry, ROR | 2026 | identidade de pesquisa | identificadores persistentes de organizações para proveniência interinstitucional |
| P4-32 | ORCID | 2026 | identidade de pesquisa | identificadores persistentes de contribuidores para atribuição e proveniência |
| P4-33 | UK ICO, orientação sobre anonimização e pseudonimização | 2025 | privacidade | pseudonimização reduz identificabilidade, mas não elimina risco de reidentificação |
| P4-34 | EDPB, orientação sobre consentimento no GDPR | 2020 | consentimento | consentimento livre, específico, informado, inequívoco e retirável |
| P4-35 | OECD, recomendação sobre acesso e compartilhamento de dados | 2021 | governança de dados | gestão de riscos, direitos, incentivos e responsabilidade |
| P4-36 | OpenTelemetry Semantic Conventions | 2026 | observabilidade técnica | semântica de saúde operacional útil, mas distinta de learning analytics |

### Endereços registrados no corpus

- `https://www.solaresearch.org/publications/hla-17/hla17-chapter4/`
- `https://doi.org/10.1111/bjet.12152`
- `https://doi.org/10.1145/2883851.2883893`
- `https://www.solaresearch.org/publications/hla-17/hla17-chapter28/`
- `https://www.solaresearch.org/publications/hla-17/`
- `https://www.1edtech.org/standards/caliper`
- `https://github.com/adlnet/xAPI-Spec`
- `https://www.w3.org/TR/prov-o/`
- `https://w3c.github.io/dpv/`
- `https://www.gov.br/anpd/pt-br/centrais-de-conteudo/materiais-educativos-e-publicacoes/guia-orientativo-tratamento-de-dados-pessoais-para-fins-academicos-e-para-a-realizacao-de-estudos-e-pesquisas`
- `https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:32016R0679`
- `https://www.unesco.org/en/articles/ai-and-education-protecting-rights-learners`
- `https://airc.nist.gov/airmf-resources/airmf/`
- `https://doi.org/10.6028/NIST.AI.600-1`
- `https://help.open.ac.uk/documents/policies/ethical-use-of-student-data`
- `https://doi.org/10.18608/jla.2016.31.6`
- `https://doi.org/10.1007/s11423-016-9463-4`
- `https://www.solaresearch.org/lak_toc/lak22.html`
- `https://www.solaresearch.org/core/lak23-companion-proceedings/`
- `https://www.aera.net/Publications/Standards-for-Research-Conduct`
- `https://www.testingstandards.net/`
- `https://www.consort-statement.org/`
- `https://www.cdc.gov/trendstatement/`
- `https://www.spirit-statement.org/`
- `https://www.equator-network.org/reporting-guidelines/tidier/`
- `https://apastyle.apa.org/jars`
- `https://doi.org/10.1038/sdata.2016.18`
- `https://www.gida-global.org/care`
- `https://schema.datacite.org/`
- `https://help.osf.io/article/330-welcome-to-registrations`
- `https://ror.org/`
- `https://info.orcid.org/`
- `https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/data-sharing/anonymisation/`
- `https://www.edpb.europa.eu/our-work-tools/our-documents/guidelines/guidelines-052020-consent-under-regulation-2016679_en`
- `https://legalinstruments.oecd.org/en/instruments/OECD-LEGAL-0463`
- `https://opentelemetry.io/docs/specs/semconv/`

Os endereços e anos acima preservam o levantamento histórico. Padrões, documentos jurídicos, orientações e páginas institucionais podem mudar. Qualquer uso futuro deve revalidar versão, vigência e aplicabilidade conforme `RES-002`.

## 3. Trinta e uma dimensões históricas

O P4 organizou 31 dimensões como uma taxonomia candidata. O estado histórico `accepted` significava aceitação dentro daquele pacote e não aprovação pública atual.

### Protocolo, condição e participante

- `protocol.purpose`: finalidade explícita do protocolo;
- `protocol.version_lock`: versões mantidas fixas quando a comparação exige;
- `condition.definition`: definição versionada da condição;
- `condition.assignment`: método de atribuição à condição;
- `participant.eligibility`: critérios de elegibilidade;
- `participant.identity_mode`: modo de identidade.

### Direitos e governança do participante

- `consent.status`: estado de consentimento quando aplicável;
- `withdrawal.policy`: efeitos e procedimentos de retirada.

### Eventos, medidas e interpretação

- `event.authorization`: autorização explícita de coleta por finalidade;
- `event.semantic_profile`: vocabulário e versão semântica do evento;
- `measure.definition`: definição versionada da medida;
- `construct.definition`: definição teórica do construto;
- `interpretation.rule`: afirmações permitidas e proibidas;
- `analysis.plan`: plano de análise;
- `outcome.role`: papel do outcome;
- `missing_data.policy`: tratamento e classificação de dados ausentes.

### Instrumentos

- `instrument.type`: família ou tipo de instrumento;
- `instrument.administration`: modo, tempo, idioma e condições de administração.

### Proveniência, variantes e fidelidade

- `provenance.snapshot`: versões pertinentes à reprodução e auditoria;
- `variant.diff_policy`: diferenças entre variantes e condições;
- `fidelity.monitoring`: fidelidade técnica, pedagógica e de participação.

### Governança de dados

- `data.purpose_binding`: vinculação de cada dado à finalidade;
- `data.retention`: retenção por categoria e finalidade;
- `data.access_policy`: acesso por papel, finalidade e escopo;
- `export.policy`: escopo, desidentificação, proveniência e autorização de exportação.

### Analytics e intervenção

- `personal_analytics.mode`: analytics pessoais opt-in e separados de terceiros;
- `role_dashboard.question`: visão organizada por pergunta e papel, não por despejo de eventos;
- `analytics.explanation`: fonte, fórmula, janela, limitações e significado dos indicadores;
- `alert.intervention_policy`: autoridade, revisão humana e proporcionalidade antes de intervenção.

### Interoperabilidade e operação

- `cross_deployment.equivalence`: equivalência semântica entre implantações;
- `operational.telemetry_separation`: separação entre observabilidade operacional e dados educacionais ou de pesquisa.

Nenhum identificador, enum, valor, autoridade, precedência, dependência, incompatibilidade ou handoff desse registro foi aprovado como contrato do ARA.

## 4. Nove perfis de contraste

O P4 registrou nove perfis para examinar combinações de finalidade, coleta, instrumentos, interpretação, autoridade, visibilidade e retenção:

| Perfil histórico | Contexto | Limite principal |
|---|---|---|
| `aralearn-reference` | estudo pessoal autodirigido | apenas estado funcional de referência; nenhuma inferência de aprendizagem |
| `personal-reflective` | estudo pessoal com adesão | analytics descritivos privados, sem exposição institucional automática |
| `formal-formative-course` | ensino e tutoria | agregados e instrumentos autorizados; sem inferência punitiva de rastros brutos |
| `research-between-participant` | comparação entre participantes | atribuição, snapshots e instrumentos dependem do protocolo |
| `research-within-participant` | comparação intraparticipante | ordem e carryover precisam ser tratados explicitamente |
| `qualitative-development` | pesquisa qualitativa e de desenvolvimento | artefatos, entrevistas e observações não são substituídos por contagens de eventos |
| `institutional-quality-assurance` | garantia institucional de qualidade | agregação limitada; sem ranking individual por padrão |
| `participant-rights-overlay` | direitos em pesquisa | direitos e retirada podem restringir outros perfis |
| `offline-research-overlay` | pesquisa em uso offline | atrasos de sincronização e perda de dispositivo são problemas de qualidade de dados, não outcomes educacionais |

Os nove perfis são casos de contraste. Não constituem catálogo, configuração padrão ou política de acesso vigente.

## 5. Precedência histórica

A síntese P4 registrou a seguinte ordem candidata de precedência:

1. lei, segurança, ética e acessibilidade;
2. direitos do participante, consentimento e retirada;
3. protocolo de pesquisa aprovado;
4. política institucional;
5. autoridade do autor do curso;
6. escolha pessoal do estudante;
7. default do produto;
8. disponibilidade técnica.

Essa ordem ajuda a explicitar o problema de conflitos de autoridade, mas não é uma regra vigente. A definição de precedência continua aberta em `PARAM-002`, e questões de direitos e governança permanecem em `DATA-002`.

## 6. Recomendações e limites históricos

O P4 recomendava, dentro da etapa de pesquisa:

- manter o perfil funcional mínimo do AraLearn como baseline pessoal;
- versionar protocolos e condições;
- autorizar eventos seletivamente por finalidade;
- separar eventos, medidas, construtos, interpretações e intervenções;
- exigir fórmula, unidade, janela, tratamento de dados ausentes, limitações e uso permitido para medidas;
- organizar analytics por perguntas e papéis;
- manter analytics pessoais sob adesão e sem exposição automática a instituições ou pesquisadores;
- tratar direitos, consentimento quando aplicável, retirada, minimização, retenção, acesso e exportação como dimensões explícitas;
- mapear padrões externos sem adotá-los como domínio interno do ARA;
- registrar diferenças e proveniência entre variantes;
- separar telemetria operacional de analytics educacionais e de pesquisa.

Essas formulações foram posteriormente refinadas pelo framework da Issue 5 e hoje permanecem evidência e investigação em `DATA-001`, `DATA-002`, `DATA-003`, `PED-003`, `PROV-004`, `PARAM-001`, `PARAM-002`, `VAL-001` e `VAL-002`.

A recomendação histórica de usar o perfil data-minimal como "default pessoal" não é decisão vigente. A experiência anterior permanece referência funcional e caso de contraste conforme `DEC-006`.

## 7. Caminhos rejeitados ou não recomendados no P4

O pacote registrou como inadequados ou não recomendados:

- coletar todos os eventos tecnicamente possíveis por padrão;
- tratar cliques, tempo, atraso, repetição, interrupção ou navegação como medidas diretas de atenção, esforço, engajamento, dificuldade ou domínio;
- usar um único dashboard para todos os papéis;
- expor dados individuais a professores, instituições ou pesquisadores apenas porque existem;
- tratar pseudonimização como anonimização;
- reter dados identificáveis indefinidamente para usos futuros não especificados;
- tratar Caliper, xAPI ou outro padrão externo como modelo completo de analytics do ARA;
- combinar logs operacionais com analytics educacionais sem finalidade e autorização explícitas;
- usar predição opaca para decisões punitivas ou de alta consequência;
- usar rótulos como randomizado, causal, pré-registrado ou reproduzível sem os métodos e registros correspondentes.

Esses registros são evidência negativa do espaço de desenho. Quando houver regra vigente, sua autoridade decorre das fontes canônicas atuais, não do rótulo histórico do P4.

## 8. Candidatos adiados

O P4 adiou explicitamente:

- schema de eventos de produção;
- catálogo de métricas de produção;
- early warning preditivo;
- inferência causal automatizada;
- dashboard universal;
- transferência automática de alegações de domínio entre cursos;
- recrutamento ou coleta de dados de participantes.

A síntese também declarou sem autorização:

- event store de produção;
- schema de banco de dados;
- implementação de dashboard;
- fórmulas de métricas em produção;
- experimentos com participantes;
- modelo preditivo ou sistema de alerta precoce;
- telemetria como default;
- seleção de arquitetura ou stack;
- implementação de UX.

## 9. Relação com o framework posterior

O framework posterior da Issue 5 retomou grande parte do P4, ampliando a separação metodológica e formalizando candidatos para eventos, instrumentos, medidas, governança e cenários. Na consolidação atual:

- `DATA-001` mantém aberta a definição de protocolos, condições, atribuição e snapshots reproduzíveis;
- `DATA-002` mantém aberta a governança de dados e direitos de participantes;
- `DATA-003` mantém aberta a instrumentação, medidas, analytics e interoperabilidade;
- `PED-003` limita interpretações de rastros e resultados;
- `PROV-004` separa proveniência operacional de uso em pesquisa;
- `PARAM-001` e `PARAM-002` tratam taxonomia, perfis, autoridade e configuração efetiva;
- `VAL-001` e `VAL-002` tratam cenários, estados e evidências de validação;
- `DEC-006` mantém AraLearn como referência funcional, não default universal;
- `DEC-007` impede que o P4 autorize arquitetura, UX ou implementação.

O P4 não constitui resultado validado de produto, aprendizagem, usabilidade, segurança, acessibilidade ou conformidade jurídica. Não houve estudo com participantes neste pacote.