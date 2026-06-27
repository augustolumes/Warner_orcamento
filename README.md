# Warner Flores - Gerador de Orçamentos

Uma aplicação web simples, focada em dispositivos móveis, desenvolvida para facilitar a criação, cálculo e compartilhamento de propostas de orçamento para eventos e serviços florais. 

Esta ferramenta funciona diretamente no navegador e permite cadastrar clientes, eventos, listar produtos, calcular frete dinamicamente com base na rota e gerar o orçamento final para ser compartilhado via WhatsApp ou exportado em formato PDF.

## 🌟 Funcionalidades

- **Passo-a-passo Intuitivo:** Navegação estruturada em etapas (Cliente > Evento > Pedido > Frete > Pagamento > Resumo) para facilitar o preenchimento.
- **Gestão de Itens:** Adição e remoção dinâmica de produtos/itens no pedido, com cálculo automático de subtotais.
- **Cálculo de Frete Inteligente:** Integração com a API do Google Maps para calcular distâncias reais de rota e gerar o valor do frete incluindo custos base, margens de lucro e valores mínimos.
- **Formas de Pagamento:** Suporte para incluir taxas percentuais no cartão e opcional de incluir ou não o valor do frete na base de cálculo.
- **Exportação Fácil:**
  - **WhatsApp:** Copia um resumo do orçamento formatado diretamente para a área de transferência do dispositivo.
  - **PDF:** Gera um layout profissional para impressão ou salvamento em PDF para ser enviado ao cliente de forma oficial.
- **Design Responsivo:** Focado na experiência Mobile-First para uso no celular durante o dia a dia.

## 🚀 Tecnologias Utilizadas

A aplicação foi construída visando a simplicidade e a portabilidade, não precisando de etapas de build complicadas:
- **HTML5:** Estruturação semântica.
- **CSS3 (Vanilla):** Variáveis nativas (`:root`), Flexbox, Grid e layout PWA-like.
- **JavaScript (Vanilla):** Toda a lógica de estado, cálculos financeiros, rotulação e integração de APIs.
- **Google Maps API:** Consumo da biblioteca `google.maps.DistanceMatrixService` para cálculo de rotas e distâncias reais.

## 🛠️ Como Instalar e Rodar (Deploy)

Como trata-se de um arquivo estático (HTML/CSS/JS puros), o processo de publicação é o mais simples possível:

1. **Acesso Local:** Basta abrir o arquivo `warner_flores_orcamento.html` em qualquer navegador web (Chrome, Safari, Edge, Firefox).
2. **GitHub Pages (Recomendado):**
   - Suba o arquivo em um repositório do GitHub.
   - Renomeie o arquivo de `warner_flores_orcamento.html` para `index.html`.
   - Vá até `Settings > Pages` e ative o GitHub Pages na branch `main`.
   - Em poucos minutos sua aplicação estará online para acesso em qualquer dispositivo!

## 🗺️ Configuração da API do Google Maps

O aplicativo usa a **Google Maps Distance Matrix API** para os cálculos exatos do frete.

1. Acesse o [Google Cloud Console](https://console.cloud.google.com/apis/credentials).
2. Crie um projeto, habilite a **Distance Matrix API** e a **Maps JavaScript API**.
3. Crie uma **Chave de API** e adicione no arquivo `.html` (procure a função `loadGoogleMapsScript` ou `calcFreteAPI`).
4. **⚠️ Importante para Segurança:** Vá na aba "Restrições de aplicativo" da sua Chave de API, selecione **"Sites HTTP (Referenciadores HTTP)"** e coloque a URL de onde a sua página está hospedada (Ex: `https://seu-usuario.github.io/*`). Isso impede que outras pessoas usem a sua cota caso achem a chave inspecionando o código.

## 📄 Licença
Este projeto é de uso privado para a empresa Warner Flores.
