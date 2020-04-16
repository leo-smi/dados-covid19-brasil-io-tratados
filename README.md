# Dados covid19 do brasil.io tratados https://brasil.io/dataset/covid19/caso

Este notebook tem por objetivo preencher a lacunas dos dias faltantes nos dados coletados pela equipe do Brasil.io.
Os dados possuem lacunas por causa da falta de publicação de boletins por parte de alguns estados e/ou municípios.

**Critérios para preenchimento das lacunas:**
- Copiar para os dias faltantes o valor do dia anterior;
- Copiar para um dia já incluso no dataset mas que possuem dados incoerentes (dados menores que o dia anterior), já que o critério dos dados 
é de acumular nos próximos dias, logo, o dado do dia posterior deve ser maior ou igual ao dia anterior.

**Possíveis incoerências:**
- Os dados coletados pela equipe do brasil.io é direto dos boletins dos estados, logo podem haver divergências quanto a quantidade 
comparado com o site do ministério da saúde;
- Os dados aqui resultantes DESTE NOTEBOOK não tem validação oficial (por algum órgão), use por sua conta e risco.

**Obs.:** Os casos importados foram desativados pois não possuem latitude e longitude, mas podem ser contados separadamente através de uma implementação rápida.

----------------------------------------------------------------------------------------------------

**Bibliotecas utilizadas:**
- pandas;
- urllib.request;
- geocoder (com api do bing);
- google.colab (se o usuário optar por usar no colab).
