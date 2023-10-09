<html><head><meta http-equiv="Content-Type" content="text/html; charset=utf-8"/><title>Análise de Requisitos Dashboard de Desempenho</title><style>
/* cspell:disable-file */
/* webkit printing magic: print all background colors */
html {
	-webkit-print-color-adjust: exact;
}
* {
	box-sizing: border-box;
	-webkit-print-color-adjust: exact;
}

html,
body {
	margin: 0;
	padding: 0;
}
@media only screen {
	body {
		margin: 2em auto;
		max-width: 900px;
		color: rgb(55, 53, 47);
	}
}

body {
	line-height: 1.5;
	white-space: pre-wrap;
}

a,
a.visited {
	color: inherit;
	text-decoration: underline;
}

.pdf-relative-link-path {
	font-size: 80%;
	color: #444;
}

h1,
h2,
h3 {
	letter-spacing: -0.01em;
	line-height: 1.2;
	font-weight: 600;
	margin-bottom: 0;
}

.page-title {
	font-size: 2.5rem;
	font-weight: 700;
	margin-top: 0;
	margin-bottom: 0.75em;
}

h1 {
	font-size: 1.875rem;
	margin-top: 1.875rem;
}

h2 {
	font-size: 1.5rem;
	margin-top: 1.5rem;
}

h3 {
	font-size: 1.25rem;
	margin-top: 1.25rem;
}

.source {
	border: 1px solid #ddd;
	border-radius: 3px;
	padding: 1.5em;
	word-break: break-all;
}

.callout {
	border-radius: 3px;
	padding: 1rem;
}

figure {
	margin: 1.25em 0;
	page-break-inside: avoid;
}

figcaption {
	opacity: 0.5;
	font-size: 85%;
	margin-top: 0.5em;
}

mark {
	background-color: transparent;
}

.indented {
	padding-left: 1.5em;
}

hr {
	background: transparent;
	display: block;
	width: 100%;
	height: 1px;
	visibility: visible;
	border: none;
	border-bottom: 1px solid rgba(55, 53, 47, 0.09);
}

img {
	max-width: 100%;
}

@media only print {
	img {
		max-height: 100vh;
		object-fit: contain;
	}
}

@page {
	margin: 1in;
}

.collection-content {
	font-size: 0.875rem;
}

.column-list {
	display: flex;
	justify-content: space-between;
}

.column {
	padding: 0 1em;
}

.column:first-child {
	padding-left: 0;
}

.column:last-child {
	padding-right: 0;
}

.table_of_contents-item {
	display: block;
	font-size: 0.875rem;
	line-height: 1.3;
	padding: 0.125rem;
}

.table_of_contents-indent-1 {
	margin-left: 1.5rem;
}

.table_of_contents-indent-2 {
	margin-left: 3rem;
}

.table_of_contents-indent-3 {
	margin-left: 4.5rem;
}

.table_of_contents-link {
	text-decoration: none;
	opacity: 0.7;
	border-bottom: 1px solid rgba(55, 53, 47, 0.18);
}

table,
th,
td {
	border: 1px solid rgba(55, 53, 47, 0.09);
	border-collapse: collapse;
}

table {
	border-left: none;
	border-right: none;
}

th,
td {
	font-weight: normal;
	padding: 0.25em 0.5em;
	line-height: 1.5;
	min-height: 1.5em;
	text-align: left;
}

th {
	color: rgba(55, 53, 47, 0.6);
}

ol,
ul {
	margin: 0;
	margin-block-start: 0.6em;
	margin-block-end: 0.6em;
}

li > ol:first-child,
li > ul:first-child {
	margin-block-start: 0.6em;
}

ul > li {
	list-style: disc;
}

ul.to-do-list {
	padding-inline-start: 0;
}

ul.to-do-list > li {
	list-style: none;
}

.to-do-children-checked {
	text-decoration: line-through;
	opacity: 0.375;
}

ul.toggle > li {
	list-style: none;
}

ul {
	padding-inline-start: 1.7em;
}

ul > li {
	padding-left: 0.1em;
}

ol {
	padding-inline-start: 1.6em;
}

ol > li {
	padding-left: 0.2em;
}

.mono ol {
	padding-inline-start: 2em;
}

.mono ol > li {
	text-indent: -0.4em;
}

.toggle {
	padding-inline-start: 0em;
	list-style-type: none;
}

/* Indent toggle children */
.toggle > li > details {
	padding-left: 1.7em;
}

.toggle > li > details > summary {
	margin-left: -1.1em;
}

.selected-value {
	display: inline-block;
	padding: 0 0.5em;
	background: rgba(206, 205, 202, 0.5);
	border-radius: 3px;
	margin-right: 0.5em;
	margin-top: 0.3em;
	margin-bottom: 0.3em;
	white-space: nowrap;
}

.collection-title {
	display: inline-block;
	margin-right: 1em;
}

.page-description {
    margin-bottom: 2em;
}

.simple-table {
	margin-top: 1em;
	font-size: 0.875rem;
	empty-cells: show;
}
.simple-table td {
	height: 29px;
	min-width: 120px;
}

.simple-table th {
	height: 29px;
	min-width: 120px;
}

.simple-table-header-color {
	background: rgb(247, 246, 243);
	color: black;
}
.simple-table-header {
	font-weight: 500;
}

time {
	opacity: 0.5;
}

.icon {
	display: inline-block;
	max-width: 1.2em;
	max-height: 1.2em;
	text-decoration: none;
	vertical-align: text-bottom;
	margin-right: 0.5em;
}

img.icon {
	border-radius: 3px;
}

.user-icon {
	width: 1.5em;
	height: 1.5em;
	border-radius: 100%;
	margin-right: 0.5rem;
}

.user-icon-inner {
	font-size: 0.8em;
}

.text-icon {
	border: 1px solid #000;
	text-align: center;
}

.page-cover-image {
	display: block;
	object-fit: cover;
	width: 100%;
	max-height: 30vh;
}

.page-header-icon {
	font-size: 3rem;
	margin-bottom: 1rem;
}

.page-header-icon-with-cover {
	margin-top: -0.72em;
	margin-left: 0.07em;
}

.page-header-icon img {
	border-radius: 3px;
}

.link-to-page {
	margin: 1em 0;
	padding: 0;
	border: none;
	font-weight: 500;
}

p > .user {
	opacity: 0.5;
}

td > .user,
td > time {
	white-space: nowrap;
}

input[type="checkbox"] {
	transform: scale(1.5);
	margin-right: 0.6em;
	vertical-align: middle;
}

p {
	margin-top: 0.5em;
	margin-bottom: 0.5em;
}

.image {
	border: none;
	margin: 1.5em 0;
	padding: 0;
	border-radius: 0;
	text-align: center;
}

.code,
code {
	background: rgba(135, 131, 120, 0.15);
	border-radius: 3px;
	padding: 0.2em 0.4em;
	border-radius: 3px;
	font-size: 85%;
	tab-size: 2;
}

code {
	color: #eb5757;
}

.code {
	padding: 1.5em 1em;
}

.code-wrap {
	white-space: pre-wrap;
	word-break: break-all;
}

.code > code {
	background: none;
	padding: 0;
	font-size: 100%;
	color: inherit;
}

blockquote {
	font-size: 1.25em;
	margin: 1em 0;
	padding-left: 1em;
	border-left: 3px solid rgb(55, 53, 47);
}

.bookmark {
	text-decoration: none;
	max-height: 8em;
	padding: 0;
	display: flex;
	width: 100%;
	align-items: stretch;
}

.bookmark-title {
	font-size: 0.85em;
	overflow: hidden;
	text-overflow: ellipsis;
	height: 1.75em;
	white-space: nowrap;
}

.bookmark-text {
	display: flex;
	flex-direction: column;
}

.bookmark-info {
	flex: 4 1 180px;
	padding: 12px 14px 14px;
	display: flex;
	flex-direction: column;
	justify-content: space-between;
}

.bookmark-image {
	width: 33%;
	flex: 1 1 180px;
	display: block;
	position: relative;
	object-fit: cover;
	border-radius: 1px;
}

.bookmark-description {
	color: rgba(55, 53, 47, 0.6);
	font-size: 0.75em;
	overflow: hidden;
	max-height: 4.5em;
	word-break: break-word;
}

.bookmark-href {
	font-size: 0.75em;
	margin-top: 0.25em;
}

.sans { font-family: ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol"; }
.code { font-family: "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace; }
.serif { font-family: Lyon-Text, Georgia, ui-serif, serif; }
.mono { font-family: iawriter-mono, Nitti, Menlo, Courier, monospace; }
.pdf .sans { font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol", 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK JP'; }
.pdf:lang(zh-CN) .sans { font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol", 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK SC'; }
.pdf:lang(zh-TW) .sans { font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol", 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK TC'; }
.pdf:lang(ko-KR) .sans { font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol", 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK KR'; }
.pdf .code { font-family: Source Code Pro, "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK JP'; }
.pdf:lang(zh-CN) .code { font-family: Source Code Pro, "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK SC'; }
.pdf:lang(zh-TW) .code { font-family: Source Code Pro, "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK TC'; }
.pdf:lang(ko-KR) .code { font-family: Source Code Pro, "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK KR'; }
.pdf .serif { font-family: PT Serif, Lyon-Text, Georgia, ui-serif, serif, 'Twemoji', 'Noto Color Emoji', 'Noto Serif CJK JP'; }
.pdf:lang(zh-CN) .serif { font-family: PT Serif, Lyon-Text, Georgia, ui-serif, serif, 'Twemoji', 'Noto Color Emoji', 'Noto Serif CJK SC'; }
.pdf:lang(zh-TW) .serif { font-family: PT Serif, Lyon-Text, Georgia, ui-serif, serif, 'Twemoji', 'Noto Color Emoji', 'Noto Serif CJK TC'; }
.pdf:lang(ko-KR) .serif { font-family: PT Serif, Lyon-Text, Georgia, ui-serif, serif, 'Twemoji', 'Noto Color Emoji', 'Noto Serif CJK KR'; }
.pdf .mono { font-family: PT Mono, iawriter-mono, Nitti, Menlo, Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK JP'; }
.pdf:lang(zh-CN) .mono { font-family: PT Mono, iawriter-mono, Nitti, Menlo, Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK SC'; }
.pdf:lang(zh-TW) .mono { font-family: PT Mono, iawriter-mono, Nitti, Menlo, Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK TC'; }
.pdf:lang(ko-KR) .mono { font-family: PT Mono, iawriter-mono, Nitti, Menlo, Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK KR'; }
.highlight-default {
	color: rgba(55, 53, 47, 1);
}
.highlight-gray {
	color: rgba(120, 119, 116, 1);
	fill: rgba(120, 119, 116, 1);
}
.highlight-brown {
	color: rgba(159, 107, 83, 1);
	fill: rgba(159, 107, 83, 1);
}
.highlight-orange {
	color: rgba(217, 115, 13, 1);
	fill: rgba(217, 115, 13, 1);
}
.highlight-yellow {
	color: rgba(203, 145, 47, 1);
	fill: rgba(203, 145, 47, 1);
}
.highlight-teal {
	color: rgba(68, 131, 97, 1);
	fill: rgba(68, 131, 97, 1);
}
.highlight-blue {
	color: rgba(51, 126, 169, 1);
	fill: rgba(51, 126, 169, 1);
}
.highlight-purple {
	color: rgba(144, 101, 176, 1);
	fill: rgba(144, 101, 176, 1);
}
.highlight-pink {
	color: rgba(193, 76, 138, 1);
	fill: rgba(193, 76, 138, 1);
}
.highlight-red {
	color: rgba(212, 76, 71, 1);
	fill: rgba(212, 76, 71, 1);
}
.highlight-gray_background {
	background: rgba(241, 241, 239, 1);
}
.highlight-brown_background {
	background: rgba(244, 238, 238, 1);
}
.highlight-orange_background {
	background: rgba(251, 236, 221, 1);
}
.highlight-yellow_background {
	background: rgba(251, 243, 219, 1);
}
.highlight-teal_background {
	background: rgba(237, 243, 236, 1);
}
.highlight-blue_background {
	background: rgba(231, 243, 248, 1);
}
.highlight-purple_background {
	background: rgba(244, 240, 247, 0.8);
}
.highlight-pink_background {
	background: rgba(249, 238, 243, 0.8);
}
.highlight-red_background {
	background: rgba(253, 235, 236, 1);
}
.block-color-default {
	color: inherit;
	fill: inherit;
}
.block-color-gray {
	color: rgba(120, 119, 116, 1);
	fill: rgba(120, 119, 116, 1);
}
.block-color-brown {
	color: rgba(159, 107, 83, 1);
	fill: rgba(159, 107, 83, 1);
}
.block-color-orange {
	color: rgba(217, 115, 13, 1);
	fill: rgba(217, 115, 13, 1);
}
.block-color-yellow {
	color: rgba(203, 145, 47, 1);
	fill: rgba(203, 145, 47, 1);
}
.block-color-teal {
	color: rgba(68, 131, 97, 1);
	fill: rgba(68, 131, 97, 1);
}
.block-color-blue {
	color: rgba(51, 126, 169, 1);
	fill: rgba(51, 126, 169, 1);
}
.block-color-purple {
	color: rgba(144, 101, 176, 1);
	fill: rgba(144, 101, 176, 1);
}
.block-color-pink {
	color: rgba(193, 76, 138, 1);
	fill: rgba(193, 76, 138, 1);
}
.block-color-red {
	color: rgba(212, 76, 71, 1);
	fill: rgba(212, 76, 71, 1);
}
.block-color-gray_background {
	background: rgba(241, 241, 239, 1);
}
.block-color-brown_background {
	background: rgba(244, 238, 238, 1);
}
.block-color-orange_background {
	background: rgba(251, 236, 221, 1);
}
.block-color-yellow_background {
	background: rgba(251, 243, 219, 1);
}
.block-color-teal_background {
	background: rgba(237, 243, 236, 1);
}
.block-color-blue_background {
	background: rgba(231, 243, 248, 1);
}
.block-color-purple_background {
	background: rgba(244, 240, 247, 0.8);
}
.block-color-pink_background {
	background: rgba(249, 238, 243, 0.8);
}
.block-color-red_background {
	background: rgba(253, 235, 236, 1);
}
.select-value-color-interactiveBlue { background-color: rgba(35, 131, 226, .07); }
.select-value-color-pink { background-color: rgba(245, 224, 233, 1); }
.select-value-color-purple { background-color: rgba(232, 222, 238, 1); }
.select-value-color-green { background-color: rgba(219, 237, 219, 1); }
.select-value-color-gray { background-color: rgba(227, 226, 224, 1); }
.select-value-color-translucentGray { background-color: rgba(255, 255, 255, 0.0375); }
.select-value-color-orange { background-color: rgba(250, 222, 201, 1); }
.select-value-color-brown { background-color: rgba(238, 224, 218, 1); }
.select-value-color-red { background-color: rgba(255, 226, 221, 1); }
.select-value-color-yellow { background-color: rgba(253, 236, 200, 1); }
.select-value-color-blue { background-color: rgba(211, 229, 239, 1); }
.select-value-color-pageGlass { background-color: undefined; }
.select-value-color-washGlass { background-color: undefined; }

.checkbox {
	display: inline-flex;
	vertical-align: text-bottom;
	width: 16;
	height: 16;
	background-size: 16px;
	margin-left: 2px;
	margin-right: 5px;
}

.checkbox-on {
	background-image: url("data:image/svg+xml;charset=UTF-8,%3Csvg%20width%3D%2216%22%20height%3D%2216%22%20viewBox%3D%220%200%2016%2016%22%20fill%3D%22none%22%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%3E%0A%3Crect%20width%3D%2216%22%20height%3D%2216%22%20fill%3D%22%2358A9D7%22%2F%3E%0A%3Cpath%20d%3D%22M6.71429%2012.2852L14%204.9995L12.7143%203.71436L6.71429%209.71378L3.28571%206.2831L2%207.57092L6.71429%2012.2852Z%22%20fill%3D%22white%22%2F%3E%0A%3C%2Fsvg%3E");
}

.checkbox-off {
	background-image: url("data:image/svg+xml;charset=UTF-8,%3Csvg%20width%3D%2216%22%20height%3D%2216%22%20viewBox%3D%220%200%2016%2016%22%20fill%3D%22none%22%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%3E%0A%3Crect%20x%3D%220.75%22%20y%3D%220.75%22%20width%3D%2214.5%22%20height%3D%2214.5%22%20fill%3D%22white%22%20stroke%3D%22%2336352F%22%20stroke-width%3D%221.5%22%2F%3E%0A%3C%2Fsvg%3E");
}
	
</style></head><body><article id="822f255e-4c44-4afc-b8cd-3c1805c3d36b" class="page sans"><header><h1 class="page-title">Análise de Requisitos Dashboard de Desempenho</h1><p class="page-description"></p></header><div class="page-body"><p id="0d93f877-75e8-4048-9852-603eaa804f82" class="">
</p><h1 id="c42e351f-2efe-49a5-8db7-0a3a55d553ef" class="">1. Introdução</h1><h2 id="61a431d4-b73a-42d0-bec6-81e97292e97c" class="">1.1. Objetivo</h2><p id="c0a80acb-e76b-45c3-9ea4-e2fb7608dcd0" class="">A especificação de requisitos descreve detalhadamente a feature da Dashboard de Gerenciamento de Lojas para a Pigz. A dashboard fornecerá informações essenciais para os lojistas acompanharem o desempenho de suas lojas, incluindo total de vendas, total de pedidos, ticket médio, dias e horários de pico, e comparativos de desempenho. A análise foi baseada em entrevistas com lojistas e pesquisa de serviços concorrentes, garantindo funcionalidades cruciais para tomadas de decisões estratégicas e otimização operacional.</p><h2 id="d18bf0af-74bc-4a17-a2f9-d441997e1bf2" class="">1.2. Escopo</h2><p id="9fe2edd7-a7e5-4a74-96f6-318a9a733d7f" class=""><strong>O que o Produto Vai Fazer:</strong>
A Dashboard de Gerenciamento de Lojas da Pigz é uma aplicação de software que fornecerá aos lojistas informações detalhadas e em tempo real sobre o desempenho de suas lojas. Ela permitirá que os lojistas analisem o histórico de vendas, identifiquem padrões de pedidos, otimizem recursos, visualizem dias e horários de pico e comparem o desempenho ao longo do tempo. Além disso, a aplicação oferecerá recursos interativos, como gráficos e filtros, para facilitar a análise e interpretação dos dados.</p><p id="53b5ec5d-00ec-4911-892e-456cb4443c8d" class=""><strong>O que o Produto Não Vai Fazer:</strong>
A aplicação não realizará transações de vendas ou processamento de pagamentos. Além disso, não será uma plataforma de vendas online independente; em vez disso, será uma ferramenta de análise e tomada de decisões para os lojistas da Pigz.</p><p id="83627c32-ee86-4158-9a03-a78bb2cf82f7" class=""><strong>Descrição da Aplicação de Software:</strong>
A Dashboard de Gerenciamento de Lojas da Pigz é uma ferramenta web intuitiva e interativa projetada para lojistas de food service. Seus principais benefícios incluem:</p><ul id="4aefbf3b-541e-42ce-8412-e29a2bf2189c" class="bulleted-list"><li style="list-style-type:disc"><strong>Análise Detalhada:</strong> Fornecer uma análise detalhada do desempenho da loja, incluindo total de vendas, total de pedidos e ticket médio em diferentes períodos (diário, semanal, mensal, anual).</li></ul><ul id="d9671dd8-f0ff-4884-b4f6-79c8f763e9f6" class="bulleted-list"><li style="list-style-type:disc"><strong>Otimização de Recursos:</strong> Identificar dias e horários de pico para permitir aos lojistas ajustar a equipe conforme a demanda, garantindo um atendimento eficiente aos clientes.</li></ul><ul id="2dc9ea5b-707a-46af-bc14-3c6d3a366277" class="bulleted-list"><li style="list-style-type:disc"><strong>Comparativos de Desempenho:</strong> Apresentar gráficos comparativos que permitem aos lojistas identificar tendências ao longo do tempo, facilitando ajustes em promoções ou operações com base nessas tendências.</li></ul><p id="92b162f9-df82-437b-9c6d-bce8038dfbf3" class=""><strong>Benefícios, Objetivos e Metas:</strong></p><ul id="0c1e7045-f463-4ac6-9b83-9d30075e2d49" class="bulleted-list"><li style="list-style-type:disc"><strong>Benefícios:</strong> A aplicação proporcionará aos lojistas uma visão aprofundada do desempenho de suas lojas, promovendo uma tomada de decisões informada e estratégica. Isso resultará em operações otimizadas, melhorias na eficiência e, em última análise, um aumento nas vendas e na satisfação do cliente.</li></ul><ul id="96d55462-9fd8-4d33-8d99-697c98811f17" class="bulleted-list"><li style="list-style-type:disc"><strong>Objetivos:</strong> O principal objetivo é capacitar os lojistas com informações relevantes e em tempo real para impulsionar o sucesso de suas operações, promovendo uma gestão mais eficaz dos negócios.</li></ul><ul id="ef6dc1da-9293-4558-98f5-d894fb1513af" class="bulleted-list"><li style="list-style-type:disc"><strong>Metas:</strong> A aplicação tem como metas oferecer uma interface intuitiva e fácil de usar, garantindo uma experiência de usuário positiva. Além disso, visa fornecer dados precisos e atualizados, permitindo análises precisas e decisões estratégicas fundamentadas.</li></ul><p id="06901907-a8ec-40c8-bd0d-95b2502e8018" class=""><strong>Consistência com Outras Especificações:</strong>
Este escopo é consistente com as diretrizes estabelecidas em outras especificações de alto nível do sistema, se existirem, garantindo que a Dashboard de Gerenciamento de Lojas da Pigz esteja alinhada com as expectativas gerais da empresa e dos usuários.</p><h2 id="d53e301c-a6dc-4dac-a680-49e9acde2d47" class="">1.5. Visão geral</h2><p id="872f29fe-6f77-48dd-b09c-c6a794c8e26e" class="">O documento apresenta uma especificação detalhada para a criação da Dashboard de Gerenciamento de Lojas da Pigz. A especificação é organizada em seções claras para facilitar a compreensão e o desenvolvimento da aplicação.</p><h3 id="3ac0ba12-12f9-4f98-b9e1-c2633169bc63" class=""><strong>1. Introdução:</strong></h3><p id="58c80808-4d17-4545-ae66-d2c85549da81" class="">Nesta seção, é explicado o propósito da especificação, detalhando o que a Dashboard de Gerenciamento de Lojas deve fazer e o que não deve fazer. Também são apresentados os benefícios, objetivos e metas do projeto.</p><h3 id="ba71da27-9fbf-44b8-8175-526015e2dcc2" class=""><strong>2. Descrição Geral:</strong></h3><p id="4acf894f-43e0-435b-8c68-0afd817ce122" class="">Esta seção contém os requisitos funcionais, de interface e os atributos de qualidade da aplicação.</p><ul id="2329ccf6-c0db-42fc-9e11-7dd3b020341f" class="bulleted-list"><li style="list-style-type:disc"><strong>2.1. Requisitos Funcionais:</strong> Descreve as funcionalidades essenciais, desejáveis e opcionais da aplicação, incluindo análises detalhadas, otimização de recursos, comparativos de desempenho, interatividade, personalização, alertas e suporte móvel.</li></ul><ul id="0d78771d-03f3-4b93-b777-4d4ad0c7d139" class="bulleted-list"><li style="list-style-type:disc"><strong>2.2. Requisitos de Interface:</strong> Detalha a interação da aplicação com pessoas, hardware do sistema e outros sistemas, além de apresentar esboços das telas principais.</li></ul><ul id="7a8ac0bf-2d22-4591-acdb-277b678696ea" class="bulleted-list"><li style="list-style-type:disc"><strong>2.3. Atributos de Qualidade:</strong> Define requisitos como velocidade de processamento, tempo de resposta, portabilidade, manutenibilidade, confiabilidade e segurança da aplicação.</li></ul><ul id="5d810a3a-dec1-4269-a218-4ac8658a87b2" class="bulleted-list"><li style="list-style-type:disc"><strong>2.4. Características dos Usuários:</strong> Descreve os diferentes tipos de usuários, incluindo lojistas, gestores, equipes administrativas, equipes de desenvolvimento, e gerentes de produto, destacando suas habilidades e conhecimentos necessários para usar a aplicação.</li></ul><ul id="c498a4ee-409c-4f16-ac81-02234762b3a9" class="bulleted-list"><li style="list-style-type:disc"><strong>2.5. Suposições e Dependências:</strong> Lista as suposições feitas durante o desenvolvimento da especificação, como conectividade com a internet, integração com sistemas de backend, atualização e manutenção, segurança dos dados, adoção e treinamento do usuário, feedback dos usuários e conformidade com regulamentações.</li></ul><h1 id="0849ac61-b6e3-4a49-bfe5-fcf033df68ef" class="">2. Descrição Geral</h1><h2 id="5001ef33-6091-47b3-be8f-6f62a8c2febb" class="">2.1. Requisitos funcionais</h2><ol type="1" id="aac68257-8b98-42e7-9485-59629d5f3d6a" class="numbered-list" start="1"><li><strong>Visão Geral:</strong><ul id="d4ebd7f6-1d27-4deb-8b65-ec9495eba061" class="bulleted-list"><li style="list-style-type:disc"><strong>Obrigatório:</strong> Exibir total de vendas, total de pedidos e ticket médio em diferentes períodos (diário, semanal, mensal, anual).</li></ul><ul id="4ddacad7-fa0e-4d07-8fbe-bc7a9088525f" class="bulleted-list"><li style="list-style-type:disc"><strong>Desejável:</strong> Permitir filtragem dos dados por período escolhido.</li></ul></li></ol><ol type="1" id="f8697a36-6326-4e2b-8880-19ae4b368305" class="numbered-list" start="2"><li><strong>Dias e Horários de Pico:</strong><ul id="fe41e777-6d82-48cf-a478-af00e119812a" class="bulleted-list"><li style="list-style-type:disc"><strong>Obrigatório:</strong> Apresentar um gráfico de barras ou de calor mostrando os horários e os dias da semana com mais vendas.</li></ul><ul id="65ab8f81-0fad-4a1f-8973-b77c7ce7216d" class="bulleted-list"><li style="list-style-type:disc"><strong>Desejável:</strong> Permitir interação, como cliques em barras ou células de calor, para visualizar detalhes específicos, como vendas exatas em determinados horários.</li></ul></li></ol><ol type="1" id="f62f1dbd-c988-4dc4-a46c-1a7ee1dc67da" class="numbered-list" start="3"><li><strong>Comparativo de Desempenho:</strong><ul id="396496b0-82e4-476e-b1f1-9f9f192d7903" class="bulleted-list"><li style="list-style-type:disc"><strong>Obrigatório:</strong> Apresentar um gráfico de comparação de desempenho entre os dias da semana.</li></ul><ul id="fa7902b4-f30d-4048-8eea-9bf2a7f77fc0" class="bulleted-list"><li style="list-style-type:disc"><strong>Desejável:</strong> Oferecer a opção de comparativo de desempenho entre fins de semana.</li></ul><ul id="0c6e16c8-3d8a-46de-b650-afea1c878e43" class="bulleted-list"><li style="list-style-type:disc"><strong>Opcional:</strong> Permitir ajuste de período para análises personalizadas.</li></ul></li></ol><ol type="1" id="5050883f-45bd-490f-b827-bb89b8944fb8" class="numbered-list" start="4"><li><strong>Detalhamento de Dados:</strong><ul id="8cd1b589-e139-4859-9a58-fa7beaceec10" class="bulleted-list"><li style="list-style-type:disc"><strong>Obrigatório:</strong> Exibir o total de vendas durante o período selecionado.</li></ul><ul id="bc1d468c-68ca-4da5-8ebb-35949662b2d7" class="bulleted-list"><li style="list-style-type:disc"><strong>Obrigatório:</strong> Mostrar o número total de pedidos feitos pelos clientes na loja durante o período especificado.</li></ul><ul id="e9d980a9-f10a-47f9-b972-28cf72b41d54" class="bulleted-list"><li style="list-style-type:disc"><strong>Obrigatório:</strong> Calcular e mostrar o ticket médio das vendas por pedido.</li></ul></li></ol><ol type="1" id="3d41addb-35cd-4d09-8cb4-5ad8c813c7a0" class="numbered-list" start="5"><li><strong>Interatividade:</strong><ul id="5316b8bc-6c42-4078-b2b1-f167d7279b96" class="bulleted-list"><li style="list-style-type:disc"><strong>Desejável:</strong> Permitir aos lojistas fazerem comparações entre diferentes períodos com facilidade.</li></ul><ul id="f2b6f9bb-3879-4b2c-a6de-5e1017a634e7" class="bulleted-list"><li style="list-style-type:disc"><strong>Opcional:</strong> Oferecer a opção de exportar os dados para formatos como CSV ou Excel.</li></ul></li></ol><ol type="1" id="e72cb3f1-821c-42ff-9d2c-5eaf22a7db0e" class="numbered-list" start="6"><li><strong>Personalização:</strong><ul id="9d0d9225-ff39-41bd-a4c0-73063ac23dbf" class="bulleted-list"><li style="list-style-type:disc"><strong>Desejável:</strong> Permitir aos lojistas personalizar os períodos de análise, como selecionar datas específicas.</li></ul><ul id="f635d7c8-4540-4844-9df9-e278707e099a" class="bulleted-list"><li style="list-style-type:disc"><strong>Opcional:</strong> Oferecer a capacidade de personalizar a aparência da dashboard, como escolher temas de cores.</li></ul></li></ol><ol type="1" id="a7872d66-6f71-42a7-83d1-c0af847cd6f2" class="numbered-list" start="7"><li><strong>Alertas e Notificações:</strong><ul id="6e5deac2-b68d-4e47-93c4-1c855ff589c2" class="bulleted-list"><li style="list-style-type:disc"><strong>Desejável:</strong> Implementar um sistema de alertas para notificar os lojistas sobre picos inesperados ou padrões de vendas.</li></ul><ul id="71edb3b8-1c6e-40a5-aaf9-8d034a1b5081" class="bulleted-list"><li style="list-style-type:disc"><strong>Opcional:</strong> Permitir aos lojistas configurar alertas personalizados com base em critérios específicos.</li></ul></li></ol><ol type="1" id="9846fd1d-afa7-430d-9836-ba5ab547d626" class="numbered-list" start="8"><li><strong>Suporte Móvel:</strong><ul id="34b3d3f5-4c9d-442c-b76f-646488e04056" class="bulleted-list"><li style="list-style-type:disc"><strong>Opcional:</strong> Desenvolver uma versão responsiva ou um aplicativo móvel para permitir que os lojistas acessem a dashboard em dispositivos móveis.</li></ul></li></ol><p id="8083f69d-f013-4bc4-8aad-bbacd129f499" class=""><strong>Classificação das Funcionalidades:</strong></p><ul id="6f497d9b-9166-460a-b217-ca374174658e" class="bulleted-list"><li style="list-style-type:disc"><strong>Obrigatórias:</strong> Funcionalidades essenciais para a operação básica da aplicação. Sem essas funcionalidades, a aplicação não seria útil.</li></ul><ul id="432d481b-3d93-4809-9fbf-cfa4c1b72e6f" class="bulleted-list"><li style="list-style-type:disc"><strong>Desejáveis:</strong> Funcionalidades que melhoram significativamente a experiência do usuário e adicionam valor à aplicação. Sua implementação é altamente recomendada, mas a aplicação ainda é utilizável sem elas.</li></ul><ul id="11edf034-58e9-4526-a4fd-54b7bb2df6a9" class="bulleted-list"><li style="list-style-type:disc"><strong>Opcionais:</strong> Funcionalidades adicionais que, se implementadas, proporcionariam benefícios extras aos usuários. Sua inclusão depende de recursos e prioridades de desenvolvimento, sendo menos essenciais do que as funcionalidades obrigatórias e desejáveis.</li></ul><h2 id="020f32c7-fc69-480b-a785-60fc98fdeae9" class="">2.2. Requisitos de interface</h2><p id="9e9cf0f0-5f50-4033-9b72-d0c749eff208" class=""><strong>Interatividade com Pessoas:</strong>
A aplicação interage com os usuários por meio de uma interface web intuitiva e fácil de usar. Os usuários podem acessar a Dashboard de Gerenciamento de Lojas da Pigz através de navegadores web em seus computadores ou dispositivos móveis. A interação é baseada em cliques, arrastar e soltar, além de interações com gráficos e filtros para explorar dados detalhados.</p><p id="48ce8485-841a-41e8-9d69-8945922cae81" class=""><strong>Interação com Hardware do Sistema:</strong>
A aplicação não requer interação direta com hardware específico do sistema. No entanto, é essencial que os usuários tenham dispositivos com conexão à internet e navegadores web modernos para acessar a aplicação.</p><p id="aa2633cc-a77a-40c0-9f4e-9c2bc0f2db11" class=""><strong>Interação com Outros Sistemas:</strong>
A aplicação pode interagir com sistemas de banco de dados para recuperar e armazenar dados relevantes. Além disso, pode se integrar a sistemas de notificação para enviar alertas aos lojistas. A integração com APIs de pagamento pode ser necessária para facilitar a visualização de dados de transações financeiras.</p><p id="8a9019fe-df61-4f8d-9348-abb45f5fc86d" class=""><strong>Detalhes das Interfaces do Produto:</strong>
A interface da aplicação é projetada para ser limpa, intuitiva e responsiva. As principais funcionalidades, como a Visão Geral, Dias e Horários de Pico e Comparativo de Desempenho, são acessíveis através de uma barra de navegação no topo da página. Os gráficos interativos são exibidos centralmente, permitindo aos usuários interagir com eles para obter informações detalhadas.</p><p id="ae01a6b2-b72f-4f59-9c10-acce1f1fbd19" class=""><em>Desenho das Telas Principais (Esboço Conceitual)</em>:</p><ol type="1" id="cd828139-bba4-471c-8586-e91aa7a68f5a" class="numbered-list" start="1"><li><strong>Página Inicial / Visão Geral:</strong><ul id="77f7c298-2c74-49cc-81ae-5cd5de679e74" class="bulleted-list"><li style="list-style-type:disc">[Esboço da Tela Principal com Gráficos Interativos]</li></ul><ul id="b47ab6e5-4dce-4e91-931b-b78e12947dfc" class="bulleted-list"><li style="list-style-type:disc"><strong>Elementos:</strong> Gráficos de barras e de linha para total de vendas, total de pedidos e ticket médio em diferentes períodos.</li></ul></li></ol><ol type="1" id="9c86bb3f-9f3d-4dbd-a1de-c3575b4fe222" class="numbered-list" start="2"><li><strong>Dias e Horários de Pico:</strong><ul id="ffbbcede-1abd-4601-89dc-948e099729af" class="bulleted-list"><li style="list-style-type:disc">[Esboço da Tela de Dias e Horários de Pico]</li></ul><ul id="bf699f43-250b-4656-9e52-c103c0ccfce5" class="bulleted-list"><li style="list-style-type:disc"><strong>Elementos:</strong> Gráfico de barras ou de calor mostrando os dias da semana no eixo horizontal e as horas do dia no eixo vertical.</li></ul></li></ol><ol type="1" id="24e17082-16e9-45dd-a9ff-c0a910a3da9e" class="numbered-list" start="3"><li><strong>Comparativo de Desempenho:</strong><ul id="692638fd-1068-4aa9-87a7-a2840583f2ed" class="bulleted-list"><li style="list-style-type:disc">[Esboço da Tela de Comparativo de Desempenho]</li></ul><ul id="6d95fb38-0d3d-4cea-a32c-a1e199c50594" class="bulleted-list"><li style="list-style-type:disc"><strong>Elementos:</strong> Gráfico de linha comparando o desempenho entre os dias da semana ou fins de semana selecionados.</li></ul></li></ol><p id="8664c5e3-a40f-4339-b664-7fb22955ce6d" class=""><strong>Integração com Outros Sistemas:</strong></p><ul id="c3c6b6cb-80c2-41f2-8993-5dfe0d810257" class="bulleted-list"><li style="list-style-type:disc"><strong>Banco de Dados:</strong> A aplicação se integra a um banco de dados para armazenamento e recuperação de dados relevantes.</li></ul><ul id="36c42878-c6e6-46a3-838b-e9402f1325e2" class="bulleted-list"><li style="list-style-type:disc"><strong>APIs de Pagamento:</strong> Integração com APIs de pagamento para visualização de dados de transações financeiras.</li></ul><ul id="0296391c-ce7d-4849-9c89-54a1ebc25881" class="bulleted-list"><li style="list-style-type:disc"><strong>Sistemas de Notificação:</strong> Implementação de sistemas de notificação para alertar os lojistas sobre eventos importantes, como picos inesperados nas vendas.</li></ul><h2 id="efefe79a-e2c4-445b-8602-93b51bdfdcde" class="">

2.3. Atributos de qualidade</h2><ol type="1" id="e11ec1b3-20d7-47fe-be31-e9ef436cfacf" class="numbered-list" start="1"><li><strong>Velocidade de Processamento:</strong><ul id="b12d4b7c-6079-487d-981a-f785019ab9f1" class="bulleted-list"><li style="list-style-type:disc"><strong>Obrigatório:</strong> A aplicação deve processar e exibir dados em tempo real, garantindo que as informações sejam atualizadas instantaneamente após as transações.</li></ul></li></ol><ol type="1" id="1c6c7102-0d27-436e-a5b7-591fc52c4268" class="numbered-list" start="2"><li><strong>Tempo de Resposta:</strong><ul id="85bf28b4-6809-40d2-adbe-def0e6ad88d5" class="bulleted-list"><li style="list-style-type:disc"><strong>Obrigatório:</strong> O tempo de resposta para consultas e interações do usuário deve ser inferior a 1 segundo para manter uma experiência de usuário fluida e responsiva.</li></ul></li></ol><p id="b0aedd1a-8c97-4584-9fcd-4f1ed8401e8f" class=""><strong>Outros Aspectos para Garantir Qualidade:</strong></p><ol type="1" id="711235ad-f8da-4baa-a715-a00e8c00a201" class="numbered-list" start="1"><li><strong>Portabilidade:</strong><ul id="7103b80f-0799-4d60-872e-7b4abcf834d3" class="bulleted-list"><li style="list-style-type:disc"><strong>Obrigatório:</strong> A aplicação deve ser compatível com os principais navegadores web, como Chrome, Firefox, Safari e Edge, garantindo uma experiência consistente em diferentes plataformas.</li></ul></li></ol><ol type="1" id="b9b5f75b-b7ef-483a-9111-050c7ec9233d" class="numbered-list" start="2"><li><strong>Manutenibilidade:</strong><ul id="9128439d-e864-419d-9055-bc5db2cf2986" class="bulleted-list"><li style="list-style-type:disc"><strong>Obrigatório:</strong> O código deve ser estruturado e documentado de forma clara para facilitar a manutenção futura. Deve-se adotar boas práticas de programação para tornar o sistema fácil de entender e modificar.</li></ul></li></ol><ol type="1" id="ba6b4eaa-55f5-4edb-ab42-73d43220e44c" class="numbered-list" start="3"><li><strong>Confiabilidade:</strong><ul id="d3e6b2c4-9d11-465b-ab2a-22da9306f349" class="bulleted-list"><li style="list-style-type:disc"><strong>Obrigatório:</strong> A aplicação deve ser altamente confiável, minimizando a ocorrência de falhas e erros. Deve ser capaz de lidar com altas cargas de usuários sem interrupções significativas no serviço.</li></ul></li></ol><ol type="1" id="b930710b-9258-46a6-88f0-4931d1dded93" class="numbered-list" start="4"><li><strong>Segurança:</strong><ul id="8408556b-b64d-49a3-9905-e078433126c4" class="bulleted-list"><li style="list-style-type:disc"><strong>Obrigatório:</strong> A segurança dos dados dos lojistas e dos clientes deve ser uma prioridade. A aplicação deve implementar práticas de segurança, como criptografia de dados, autenticação segura e autorização adequada para proteger informações sensíveis.</li></ul></li></ol><p id="db93e814-2338-42b9-b7b2-5cea42c20d39" class=""><strong>Classificação e Revisão dos Requisitos:</strong></p><ol type="1" id="1df05049-9705-4430-b4d7-529ec3beca93" class="numbered-list" start="1"><li><strong>Requisitos de Desempenho:</strong><ul id="3611d264-6dfd-4b95-ad58-2c94b9dcfec3" class="bulleted-list"><li style="list-style-type:disc"><strong>Obrigatório:</strong> Velocidade de processamento em tempo real e tempo de resposta inferior a 1 segundo.</li></ul></li></ol><ol type="1" id="681e5fa1-1643-45b2-95a2-fb49467199f6" class="numbered-list" start="2"><li><strong>Outros Aspectos para Garantir Qualidade:</strong><ul id="61848c71-6178-4c88-b304-4cef27e303e9" class="bulleted-list"><li style="list-style-type:disc"><strong>Obrigatório:</strong> Portabilidade, manutenibilidade e confiabilidade, incluindo práticas de segurança robustas.</li></ul></li></ol><h2 id="f9a460b4-5783-4d9b-82be-073b87e8af3c" class="">
2.4. Características dos usuários</h2><ol type="1" id="dab345d7-8c51-470b-b76b-dbab7193fbfc" class="numbered-list" start="1"><li><strong>Lojistas de Food Service:</strong><ul id="bed3c757-6e29-41c1-b9ee-634374a5f199" class="bulleted-list"><li style="list-style-type:disc"><strong>Conhecimento do Negócio:</strong> Possuem conhecimento prático do funcionamento de uma loja de food service, incluindo gestão de estoque, atendimento ao cliente e estratégias de vendas.</li></ul><ul id="93d2cf27-8d78-4062-b2fe-ae039e8cafb4" class="bulleted-list"><li style="list-style-type:disc"><strong>Familiaridade com Tecnologia:</strong> Têm experiência básica em tecnologia, sendo capazes de usar dispositivos eletrônicos e navegadores web com facilidade.</li></ul></li></ol><ol type="1" id="bae93368-59bd-4727-b373-8bb62a55362c" class="numbered-list" start="2"><li><strong>Gestores e Proprietários de Lojas:</strong><ul id="b6096a55-afde-4344-a205-965e4f73ff72" class="bulleted-list"><li style="list-style-type:disc"><strong>Experiência em Gestão:</strong> Têm experiência em gerenciamento de negócios, incluindo análise de dados de vendas, planejamento operacional e tomada de decisões estratégicas.</li></ul><ul id="729d2f24-b08c-4675-b549-636c678eb8dd" class="bulleted-list"><li style="list-style-type:disc"><strong>Habilidades Analíticas:</strong> Possuem habilidades analíticas para interpretar dados e identificar padrões, permitindo a tomada de decisões informadas.</li></ul></li></ol><ol type="1" id="63a12fe1-5060-47b2-b381-4f7db53987cf" class="numbered-list" start="3"><li><strong>Equipe Administrativa e de Marketing:</strong><ul id="efb66e03-3047-48de-9ce7-8582266f16cf" class="bulleted-list"><li style="list-style-type:disc"><strong>Conhecimento em Marketing:</strong> Possuem conhecimento em estratégias de marketing e promoções para ajudar na interpretação dos dados e ajustes nas campanhas promocionais.</li></ul><ul id="404c33d5-2769-4f38-9b6d-8275bdd34fae" class="bulleted-list"><li style="list-style-type:disc"><strong>Habilidades em Comunicação:</strong> Têm habilidades de comunicação para colaborar eficazmente com a equipe de lojistas e apresentar análises de desempenho.</li></ul></li></ol><ol type="1" id="7da0f54b-4e52-48cf-a43c-a95bccb8bcd4" class="numbered-list" start="4"><li><strong>Equipe de Desenvolvimento e Suporte Técnico:</strong><ul id="403f38aa-b9ee-4602-91e5-59fe75e2d4ec" class="bulleted-list"><li style="list-style-type:disc"><strong>Habilidades Técnicas:</strong> Possuem habilidades técnicas avançadas para desenvolver, manter e oferecer suporte técnico à aplicação.</li></ul><ul id="2ece4226-4cb7-4f28-b492-1a76c78a821e" class="bulleted-list"><li style="list-style-type:disc"><strong>Experiência em Interface do Usuário (UI) e Experiência do Usuário (UX):</strong> Têm conhecimento em design de interfaces de usuário e experiência do usuário para criar uma aplicação intuitiva e fácil de usar.</li></ul></li></ol><ol type="1" id="3e74d9c7-bb34-4141-9cb7-7b0aeeb952aa" class="numbered-list" start="5"><li><strong>Gerentes de Produto e Planejamento Estratégico:</strong><ul id="0c654c0e-7923-4db8-8c13-5163744c1c4b" class="bulleted-list"><li style="list-style-type:disc"><strong>Visão Estratégica:</strong> Têm uma visão estratégica do negócio e do mercado de food service, ajudando a orientar o desenvolvimento da aplicação de acordo com as necessidades do setor.</li></ul><ul id="cf4cd09c-3959-446d-92cb-f0b2dcf3d86d" class="bulleted-list"><li style="list-style-type:disc"><strong>Conhecimento em Competitividade:</strong> Possuem conhecimento sobre o mercado competitivo de food service, auxiliando na diferenciação da aplicação em relação aos concorrentes.</li></ul></li></ol><h2 id="2d77c255-e389-4d9e-8bf6-0841f62dd25d" class="">



2.5. Suposições e dependências</h2><p id="a48a3f05-934d-4837-abb7-2a9433e5b835" class="">
</p><ol type="1" id="c0cd48bc-3fae-478e-81e1-bb0c982f5b81" class="numbered-list" start="1"><li><strong>Conectividade com a Internet:</strong><ul id="62f64208-23b1-486f-8c21-2d60cfca6e60" class="bulleted-list"><li style="list-style-type:disc"><strong>Suposição:</strong> É assumido que os usuários terão acesso estável à internet para usar a Dashboard de Gerenciamento de Lojas da Pigz.</li></ul><ul id="88ad57e3-2291-486d-b742-b8004a78711a" class="bulleted-list"><li style="list-style-type:disc"><strong>Dependência:</strong> A funcionalidade da aplicação depende de uma conexão de internet ativa e confiável para acessar dados em tempo real e garantir a interatividade.</li></ul></li></ol><ol type="1" id="b903c81e-0490-4cb3-8f5f-68ba71bd0dbe" class="numbered-list" start="2"><li><strong>Integração com Sistemas de Backend:</strong><ul id="702f0ee0-4eae-4b2b-aba0-ea8e51c3c35e" class="bulleted-list"><li style="list-style-type:disc"><strong>Suposição:</strong> É suposto que a aplicação será integrada a sistemas de backend, como bancos de dados e APIs de pagamento, para coletar e processar dados relevantes.</li></ul><ul id="8acd8bbc-f3c6-4eb7-acc6-948505567bc4" class="bulleted-list"><li style="list-style-type:disc"><strong>Dependência:</strong> A funcionalidade da aplicação depende da integridade e confiabilidade desses sistemas de backend para garantir a precisão dos dados apresentados aos usuários.</li></ul></li></ol><ol type="1" id="673aa385-802c-4820-bb06-e36cafdae24b" class="numbered-list" start="3"><li><strong>Atualização e Manutenção:</strong><ul id="cc92cb5a-21f2-45c3-971b-59d0dccbc085" class="bulleted-list"><li style="list-style-type:disc"><strong>Suposição:</strong> Presume-se que a aplicação será regularmente atualizada e mantida para corrigir bugs, adicionar novos recursos e garantir a segurança dos dados.</li></ul><ul id="487dd99a-0abc-45a5-af40-d941ae0fce0c" class="bulleted-list"><li style="list-style-type:disc"><strong>Dependência:</strong> Os usuários dependem das atualizações regulares para acessar funcionalidades aprimoradas e manter a segurança da aplicação.</li></ul></li></ol><ol type="1" id="2a39fa41-e885-4f62-893b-4459a44f51d9" class="numbered-list" start="4"><li><strong>Segurança dos Dados:</strong><ul id="1e0ad0c7-f897-42b1-98c6-b628a4623263" class="bulleted-list"><li style="list-style-type:disc"><strong>Suposição:</strong> É suposto que medidas de segurança, como criptografia de dados e autenticação segura, serão implementadas para proteger as informações sensíveis dos usuários.</li></ul><ul id="74569320-d082-4ab5-8b18-c635fdd73b94" class="bulleted-list"><li style="list-style-type:disc"><strong>Dependência:</strong> A confiança dos usuários na aplicação depende da implementação eficaz dessas medidas de segurança para proteger suas informações pessoais e de negócios.</li></ul></li></ol><ol type="1" id="df9a86ec-9188-408c-9393-bd5c452f505e" class="numbered-list" start="5"><li><strong>Adoção e Treinamento do Usuário:</strong><ul id="3acd5e41-e313-4041-a74b-e2f9167cf349" class="bulleted-list"><li style="list-style-type:disc"><strong>Suposição:</strong> Assume-se que os usuários receberão treinamento adequado para utilizar todas as funcionalidades da aplicação.</li></ul><ul id="2729e41e-f928-4c6e-93e8-77eed9fae394" class="bulleted-list"><li style="list-style-type:disc"><strong>Dependência:</strong> A adoção bem-sucedida da aplicação pelos usuários depende do treinamento eficaz e do suporte contínuo para resolver dúvidas e problemas.</li></ul></li></ol><ol type="1" id="4a62313f-08b0-400d-b829-0fe91e34d917" class="numbered-list" start="6"><li><strong>Feedback dos Usuários:</strong><ul id="7bd0c6fa-c0ab-4883-a7f8-0d9f8500aba0" class="bulleted-list"><li style="list-style-type:disc"><strong>Suposição:</strong> É assumido que os usuários fornecerão feedback regular sobre a usabilidade e a eficácia da aplicação.</li></ul><ul id="c92f1075-9195-4fc6-8b79-ee48ab6d7b47" class="bulleted-list"><li style="list-style-type:disc"><strong>Dependência:</strong> A melhoria contínua da aplicação depende do feedback dos usuários para identificar áreas de melhoria e implementar ajustes conforme necessário.</li></ul></li></ol><ol type="1" id="30dfa51b-c198-44f0-be89-48fceade5503" class="numbered-list" start="7"><li><strong>Conformidade com Regulamentações:</strong><ul id="b3542c3a-00d0-4850-beef-be6c021a6214" class="bulleted-list"><li style="list-style-type:disc"><strong>Suposição:</strong> É suposto que a aplicação será desenvolvida em conformidade com as regulamentações locais e internacionais, incluindo leis de proteção de dados e privacidade.</li></ul><ul id="02e218da-d262-4351-962e-e795724ea25d" class="bulleted-list"><li style="list-style-type:disc"><strong>Dependência:</strong> A operação contínua da aplicação depende da conformidade com regulamentações legais para evitar problemas legais e garantir a confiança dos usuários.</li></ul></li></ol><p id="47bb30c9-cf91-4692-a8ea-b8b3dc5f476c" class="">
</p></div></article></body></html>
