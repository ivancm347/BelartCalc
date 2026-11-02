# BelartCalc

**Calculadora de materiais e orçamentos para drywall — BelartGesso**

Aplicação web publicada em: https://ivancm347.github.io/BelartCalc/

## Sobre o projeto

O BelartCalc ajuda a estimar materiais para serviços de drywall e outros tipos de forro. A aplicação foi desenvolvida para uso no navegador, com interface adaptável a computadores e celulares e estrutura PWA para instalação e uso offline após o primeiro carregamento bem-sucedido.

## Recursos

- Cadastro e cálculo de serviços por medidas em metros.
- Estimativa de chapas, perfis, guias, montantes, fixadores e materiais de acabamento.
- Tipos de serviço contemplados no código: parede drywall, forro F530, forro aramado, forro PVC e forro modular.
- Composição de materiais e orçamento.
- Geração de PDF no próprio navegador.
- Manifesto, ícone e service worker para instalação como aplicativo.
- Cache dos arquivos principais para permitir a abertura offline depois que o aplicativo for carregado online.

## Como usar

1. Abra o [BelartCalc](https://ivancm347.github.io/BelartCalc/).
2. Escolha o tipo de serviço.
3. Informe as medidas, quantidades, espaçamentos e opções solicitadas.
4. Confira os materiais calculados.
5. Gere o PDF pelo recurso disponível na aplicação.

> **Importante:** os resultados são estimativas de consumo. Confira as medidas do local, o projeto, as recomendações dos fabricantes, a modulação adotada e as condições reais da obra antes de comprar ou executar os materiais. Recortes, emendas, reforços, vãos, cargas e particularidades da estrutura podem alterar as quantidades.

## Chapas

A configuração padrão da parede utiliza chapa de **1,20 × 1,80 m**, equivalente a **2,16 m² por chapa**. O aplicativo também consulta as demais dimensões disponíveis no catálogo interno. A quantidade é estimada pela área acrescida do percentual de perda informado, dividida pela área da chapa e arredondada para cima.

## Estrutura e arredondamentos

- Os perfis e barras identificados como 3 m são apresentados em unidades de barras, com arredondamento para cima.
- A perda configurada é aplicada às quantidades de materiais indicadas pela regra de cada serviço.
- A modulação de montantes, perfis e pendurais depende dos espaçamentos informados.
- O cálculo não substitui paginação de chapas, plano de corte ou projeto executivo.

## Instalação e uso offline

O projeto contém:

- `manifest.json`: nome, cores, escopo e ícone do aplicativo.
- `icon.svg`: ícone vetorial.
- `sw.js`: service worker responsável pelo cache dos arquivos principais.

Para instalar, abra o site em um navegador compatível e use a opção **Instalar aplicativo** ou **Adicionar à tela inicial**, quando disponível.

Para o primeiro uso offline, abra o aplicativo com internet e aguarde o carregamento completo. O funcionamento offline depende de o navegador permitir service workers e armazenamento local. Recursos externos, como fontes hospedadas fora do GitHub Pages, podem não ficar disponíveis sem conexão; a aplicação deve usar fontes alternativas do sistema nesses casos.

## Publicação

O site é hospedado pelo GitHub Pages a partir do repositório:

https://github.com/ivancm347/BelartCalc

As alterações na branch principal precisam terminar de ser publicadas pelo GitHub Pages antes de aparecerem no endereço público. Se o navegador continuar exibindo uma versão antiga, faça uma atualização forçada da página.

## Desenvolvimento

A aplicação principal está em `index.html`. O projeto é estático e não exige servidor de aplicação ou instalação de dependências para a publicação básica no GitHub Pages.

## Estado da validação

O repositório está em revisão técnica contínua. As fórmulas devem ser conferidas com as medidas e o método de montagem usados em cada obra. Testes no navegador, geração real dos PDFs e teste offline em dispositivo precisam ser realizados após a publicação para confirmar o comportamento no ambiente final.

---

**BelartGesso — Detalhes que transformam seu espaço.**
