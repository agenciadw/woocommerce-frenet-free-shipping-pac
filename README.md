=== WooCommerce Frenet Free Shipping PAC ===
Contributors: David William da Costa
Tags: shipping, delivery, woocommerce, frete, frenet
Requires at least: WooCommerce 3.0
Tested up to: 7.6
Requires PHP: 7.6
Stable tag: 1.0
License: GPLv2 or later
License URI: https://www.gnu.org/licenses/gpl-2.0.html

== Description ==
Este plugin integra o serviço PAC da Frenet ao método de Frete Grátis do WooCommerce, exibindo o prazo de entrega em dias úteis diretamente no label do Frete Grátis, sem ocultar outros métodos de entrega.

== Features ==

- Captura o prazo de entrega do PAC Frenet e adiciona ao Free Shipping.
- Não remove nem oculta outros métodos de frete.
- Estrutura modular: core (includes), admin e public.
- Validação de CEP no formato 99999-999 ou 99999999.
- Proteção CSRF via nonce na página de configurações.
- Logs de erro em caso de falha na comunicação com a API Frenet.
- Exibição de contador de dias restantes no carrinho (opcional).

== Installation ==

1. Faça upload da pasta **woocommerce-frenet-free-shipping-pac** para `/wp-content/plugins/`.
2. Ative o plugin em **Plugins > Plugins instalados**.
3. Acesse **WooCommerce > Ajustes > Entrega** e localize a seção **Frenet Free Shipping PAC**.
4. Preencha os campos:
   - **Chave**: Chave de acesso da API Frenet.
   - **Senha**: Senha da API Frenet.
   - **Token**: Token de autenticação.
   - **CEP Origem**: CEP de origem para cálculo (99999-999 ou 99999999).
5. Salve alterações.

== Usage ==

1. Adicione a condição de Frete Grátis no WooCommerce (valor mínimo, cupom etc.).
2. No checkout, ao atender a condição, o método Free Shipping será exibido como:
   **Frete grátis (até X dias úteis)**, onde X é obtido do PAC Frenet.
3. Outros métodos de frete permanecem disponíveis normalmente.

== Changelog ==
= 1.0 =

- Versão inicial completa integrando PAC da Frenet com Frete Grátis.
- Adiciona configuração de Chave, Senha, Token e CEP de origem no admin.
- Validação de CEP (formatos 99999-999 e 99999999).
- Proteção CSRF via nonce na página de configurações.
- Lógica para capturar e exibir o prazo do PAC Frenet no método Free Shipping.
- Prioridade ajustada para garantir o prazo seja copiado após cálculo do Frenet.
- Não oculta outros métodos de envio; apenas substitui o label do Free Shipping.
- Exibição opcional de contador de dias restantes no carrinho.
- Logging de erros em caso de falha na comunicação com a API Frenet.
- Compatível com PHP 7.6+, WooCommerce 3.0+.

== Frequently Asked Questions ==
= Quais versões de PHP são suportadas? =
Requer PHP 7.6 ou superior.

= O plugin oculta outros métodos de entrega? =
Não. Ele apenas oculta o método PAC da Frenet original e ajusta o label do Free Shipping.

= Como validar o CEP corretamente? =
A validação aceita formatos com ou sem hífen: 99999-999 ou 99999999.

== Screenshots ==

1. Página de configurações em WooCommerce > Ajustes > Entrega.
2. Exemplo de label no checkout: "Frete grátis (até 5 dias úteis)".

== Support ==
Para dúvidas ou sugestões, abra uma issue no repositório ou contate o autor.
