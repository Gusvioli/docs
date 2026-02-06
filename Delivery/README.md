# SPID Delivery Extension

Uma extensão para Google Chrome desenvolvida para monitorar e notificar sobre novos pedidos e mudanças de status de entrega na plataforma **Janis.in**.

## 🚀 Funcionalidades

* **Monitoramento Inteligente:** Verifica a lista de pedidos a cada 30 segundos, filtrando apenas pedidos das últimas 24 horas que ainda não foram entregues.
* **Notificações de Desktop:** Exibe alertas visuais persistentes para novos pedidos ou mudanças de status.
* **Alertas Sonoros (TTS):** Anuncia verbalmente as novidades (ex: "Atenção, novo pedido SPID detectado").
* **Interface Moderna:** Popup com lista de pedidos recentes, status coloridos, filtro de busca e opções para forçar atualização ou limpar histórico.
* **Configurações:** Opções para ativar/desativar o recarregamento automático da página e silenciar alertas sonoros.
* **Indicadores de Status (Badge):** O ícone da extensão muda de cor para informar o estado atual:
  * �/🟡 **Piscando (Vermelho/Amarelo):** Indica novos pedidos ou mudanças de status que requerem atenção imediata.
  * � **Verde (Número):** Indica a quantidade de pedidos pendentes (últimas 24h) sendo monitorados.
  * 🟠 **Laranja ("ABRIR"):** Alerta que a aba do Janis não foi encontrada e o monitoramento está pausado.

## 📦 Instalação

Como esta é uma extensão local (não publicada na Chrome Web Store), instale-a seguindo os passos abaixo:

1. Baixe os arquivos deste projeto em uma pasta no seu computador.
2. Abra o Google Chrome e acesse o endereço `chrome://extensions/`.
3. No canto superior direito, ative a chave **"Modo do desenvolvedor"**.
4. Clique no botão **"Carregar sem compactação"** (ou *Load unpacked*).
5. Selecione a pasta onde os arquivos da extensão (`manifest.json`, `src/`, etc.) estão localizados.

## 🛠️ Como Usar

1. Certifique-se de que a extensão está ativa (clique no ícone da extensão para ver o status).
2. Faça login e mantenha aberta uma aba na URL `https://janis.in/`.
3. A extensão detectará automaticamente a tabela de pedidos e começará o monitoramento.
4. Se você fechar a aba do Janis, o ícone da extensão ficará laranja com o texto "ABRIR", indicando que o monitoramento parou.
5. Utilize o botão de atualização (↻) no popup para forçar uma verificação imediata se necessário.

## ⚙️ Permissões

* `storage`: Para salvar o histórico de status dos pedidos e configurações.
* `tabs` & `scripting`: Para acessar a aba do Janis e ler os dados da tabela de pedidos.
* `notifications`: Para exibir alertas no sistema operacional.
* `tts` (Text-to-Speech): Para os avisos sonoros de voz.
* `alarms`: Para agendar a verificação periódica.

## 📝 Autor

**Gustavo Vieira**

## 📝 CO-Autor

**Luiz Fernando**
