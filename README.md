# Hidrômetro para monitoramento de consumo de água em tempo real com envio de mensagens por telegram.

# Introdução.

O consumo de água representa um dos pilares fundamentais para o desenvolvimento
sustentável das sociedades modernas, especialmente em regiões urbanas propensas a
escassez hídrica, como o estado de São Paulo, e no Brasil. Diariamente, milhões de
residências enfrentam o desafio de gerenciar esse recurso de forma eficiente, sem uma visão
clara do impacto de suas rotinas no volume total consumido ou nos custos associados
[Sabesp, 2023].
O uso adequado dos recursos hídricos está sendo um fator preocupante para as
autoridades que estão buscando destinar recursos para a educação da população sobre o
consumo consciente da água. Principalmente após os períodos de secas severas que
assolaram o brasil desde o início do século XXI. De acordo com os estudos de Coelho,
Cardoso e Firpo (2016) apud Cumplido (2024), afirmaram que a crise hídrica de 2014 foi a
mais severa desde 1960 em termos de déficit pluviométrico. Isso reforça que as secas estão
ficando piores e são necessárias medidas para evitar crises mais severas no futuro.
Em uma pesquisa realizada durante o período de 2019 a 2020, mostra que o consumo
médio de água foi impulsionado durante a pandemia de Covid-19. Hábitos como a lavagem
de roupas, lavagem de carros e banhos foram os maiores contribuidores para o aumento do
consumo. Na mesma pesquisa foi perguntado se os entrevistados possuíam hábitos de
consumo consciente de água, a maioria relatou que possuem os costumes coletar a água da
chuva para a realização de outras tarefas domésticas e reutilizar água proveniente da lavagem
de roupas para a limpeza. No entanto, ainda há perspectiva de aumento do alcance das
políticas educacionais sobre o uso racional da água [PEREIRA; COSTA; ROSSONI, 2022].
Tendo essa situação em vista, o governo busca conscientizar a população sobre o uso
sustentável da água por meio da inserção do assunto no currículo de ensino público com
ênfase no público mais jovem para instituir um pensamento crítico sobre o uso de água
durante as suas necessidades diárias. No entanto, educadores relatam dificuldades em
repassar esses conhecimentos com a mudança contínua das políticas educacionais
[GRANDISOLI; CURVELO; NEIMAN, 2021].

#  Materiais e Métodos.

 A elaboração da solução de monitoramento de consumo de água voltado para
domicílios envolverá a junção de componentes que trabalharão em conjunto para os dados
aos usuários de forma automatizada e integrada com a internet. Para isso iremos utilizar o
Arduino Uno como central lógico da automatização, ele é uma plataforma para permitir a
interação entre o mundo o físico e o computador por meio de sensores associados a ele.
O componente que irá coletar os dados quantitativos de fluxo de água será um sensor
de fluxo de água ligado ao Arduino e instalado no encanamento de registro de água da
residência.
O sensor se trata de uma válvula plástica, um rotor de água e um sensor de efeito
Hall, a água ao passar pelo rotor irá rotacioná-lo e sua velocidade de giro determina o quanto
de água passou por ele e o sensor de efeito Hall emite pulsos elétricos correspondendo ao
rotor e comunicando ao Arduino esses dados.
Segundo Duarte (2023) o sensor de efeito Hall é composto por um imã e um sensor
de campo magnético, quando o imã se desloca ele ativa o sensor de campo magnético e gera
o pulso elétrico, com isso, toda vez que o roter realiza uma volta completa o imã é deslocado
e o pulso é enviado ao Arduino, sendo possível mensurar o quanto de água passou por ele. 

#  Nosso objetivo final.
Queremos criar um dashboar com os principais prinicpais resultados de forma cara e objetiva para que o nosso usário poderá acompanhar os indicadores de desempenho com maior controlem auxiliando na tomada de decisões.

