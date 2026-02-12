# Documentação do Projeto: Jogo do Número Secreto

Este documento descreve a estrutura do projeto web para o jogo de adivinhação numérica.

---

## 1. Tecnologias e Dependências
O projeto utiliza uma combinação de recursos locais e externos:
* **ResponsiveVoice**: Biblioteca externa carregada via CDN para permitir que o jogo "fale" com o usuário.
* **Google Fonts**: Importação das fontes **Chakra Petch** e **Inter**.
* **CSS**: Estilização personalizada através do arquivo `style.css`.
* **JavaScript**: Lógica do jogo contida em `app.js`, carregada com o atributo `defer`.

---

## 2. Estrutura da Interface
A interface foi projetada para ser simples e intuitiva, contendo os seguintes elementos:

### Área de Interação
* **Título (`h1`)**: Título principal com destaque visual na cor azul.
* **Instruções (`p`)**: Parágrafo com a classe `.texto__paragrafo` que orienta o usuário sobre o intervalo do número secreto.
* **Entrada de Dados (`input`)**: Campo do tipo numérico (`type="number"`) com limites entre 1 e 10.

### Controles (Botões)
O jogo possui dois estados principais controlados por botões:
1. **Chutar**: Chama a função `verificarChute()`. É o botão principal de interação.
2. **Novo Jogo (`#reiniciar`)**: Chama a função `reiniciarJogo()`. Este botão inicia com o atributo `disabled`, sendo habilitado via JavaScript apenas quando o jogador acerta o número.

---

## 3. Fluxo de Funcionamento
O comportamento esperado da aplicação segue este fluxo:
1. O usuário digita um número no campo de entrada.
2. Ao clicar em **Chutar**, a lógica verifica se o número é igual, maior ou menor que o número secreto gerado aleatoriamente.
3. O texto na tela é atualizado dinamicamente para dar feedback ao jogador.
4. Ao vencer, o botão **Novo jogo** é desbloqueado para permitir o reinício da partida.

---

## 4. Elementos Visuais
* **Container**: Centraliza o conteúdo na tela.
* **Imagem**: Uma ilustração (`./img/ia.png`) posicionada ao lado dos controles para compor o layout visual.

---

> **Aviso**: Para que o recurso de voz funcione, certifique-se de que a chave da API do ResponsiveVoice esteja configurada corretamente ou que a biblioteca esteja acessível via internet.
<img width="1802" height="854" alt="Image" src="https://github.com/user-attachments/assets/f2b03b9f-77e6-4ad2-9f71-2377cd669e8e" />
