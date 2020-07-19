# Template-Football

Criado apenas com CSS e HTML puros apenas (com uso de basico de bibliotecas simples de JS).

## Documentação do template

Deixo aqui nesse documento algo que se aproxime de um guia para uso do template.

### Estrutura do projeto

Dividi o projeto em duas pastas, Dev e Build, na pasta Dev contem os codigos fonte que foram Transpilados para outras linguagens.

#### Pasta Dev

Project.scss ==> Project.css

O código escrito em Sass foi compilado usando o Koala, o código .scss está disponivel parafuturas alterações também.

#### Pasta Build

É a pasta que contém o site disponível para deploy

##### src/css

Aqui contém os arquivos de css do bootstrap e do projeto

##### src/font

Usei como padrão a fonte **Bebas Neue**, é uma fonte com uso 100% gratuito para uso comercial e pessoal e se assemelha a fonte do projeto em que esse foi inspirado.

##### src/fontawesome

Inseri de forma direta o serviço do fontawesome para que o desevolvimento da interface ficasse indepedente do CDN do mesmo, mas é possível adicionar o CDN do fontawesome e retirar essa pasta.

##### src/js

Aqui estão os arquivos referentes ao codigos  JS do bootstrap e do Jquery, também são substituíveis por CDN's

##### src/img

**backgrounds**, são os arquivos com as layers estilizadas do template.

**carousel-items**, arquivos de imagens dos produtos que aparecem em exposição no site

**jogadores**, arquivos dos jogadores em overlay nas camadas do site

**mapas**, imagens (inicialmente para testes) para preenchimento dos eventos na parte inferoior do site

##### index.html

O site está dividido em seis seções além da barra de navegação do bootstrap:

**Barra de navegação**

Usei o *container* do bootstrap para limitar o alcança da barra de navegação assim como na foto original

Navbar com fundo dark, alterado via css para a cor **#121212**, de resto a mantive como padrão, inclusive também com o toggler para colapsar a barra em dispositivos mobile, cada link da barra é um link dentro de uma linha(ul) de uma lista(li)

**Primeira seção**

Por aqui temos o FUTEBOL com as letras intercalando para trás ou para frente do background gradiente, dentro de uma div com a classe **banner** há varios spans com a classe **switch-banner** que joga as letras especificamente para frente do background, em seguida temos uma imagem de um jogador seguindo a linha do layout fornecido com a classe **player-overlay**, o que começa a marcar a característica desse projeto, **quase tudo** neste site está ''flutuando'' fora de seu local padrão com o objetivo de manter as camadas de visualização e linhas de design

**Segunda seção**

A seção de exibição da loja, usei um **carousel** do bootstrap flutuando sobre o background, porém esse componente contém uma curiosidade, para que funcione é necessário que haja pelo menos uma div com a classe **carousel-item** marcada como **active** e então ele se configura por automático, por padrão há uma mostra de 3 itens por quadro, mantive esse número, pois apesar de ser customizável fugiria das linhas de design, *na versão do site para smartphone, há modificações quanto as  versões tablet e pc,* é mostrado apenas 1 um item de cada vez, e para facilitar o desenvolvimento, criei uma classe em css chamada **no-mobile** para esconder os itens que não serão vistos nessa seção, mantive o numero 1 apesar de caber dois itens para não colocar informações demais em uma tela pequena, sendo assim por questões de SEO, penso eu que seja melhor criar umaverificação durante a requisição do site em PHP ou via JS para enviar apenas um item para cada quadro do carousel.

**Terceira seção**

Nessa seção inseri um container para manter o design do preview dos itens alinhados com a imagem enviada como base, **É ALTAMENTE RECOMENDADO QUE SEJA INSERIDO APENAS IMAGENS QUADRADAS (1000x1000, 1200x1200) EM QUALQUER AREA DO SITE**  pois o template funiona muito melhor com imagens assim, há um itens nessa terceira seção cuja imagem é retangular e veja como fica deformado o design. Juntamente com o container inseri uma classe **zero-wasting** para aproveitar somente o alinhamento e haver muito desperdício de uso de tela.

O jogador nessa seção não aparece no celular por questões de quantidade de informação na tela, dentro da classe  **player-overlay2** na media querie referente a exibição em smarfones a um comando, **display: hidden;** retire-o e a imagem aparecerá normalmente

**Quarta seção**

Não há muito o que explicar nessa seção, é apenas um carousel como na seção dois configurado para aprecer os eventos e os mapas como no design original.

**Quinta seção**

Essa é a seção do banner para procurar uma loja, próxima, nessa parte será necessário contratar os serviços de um publicitário ou um editor para produzir um banner que se encaixe na proposta do site, coloquei uma imagem de teste, mas pode-se colocar qualquer uma no lugar, é apenas para mostar que essa área está configurada

**Sexta seção**

É a seção final do site, seria uma repetição da barra de navegação como footer, finalizei com o logo da Liga do Patão.

##### src/css/Project.css

O arquivo principal para alteração do css.
