importar webbrowser
importação os
de datatime importação datatime

# --- Informações para personalizar a carta ---
nome_dela = "Ruth" # Coloque o nome da sua namorada aqui!
seu_nome = "Emanoel" # Coloque o seu nome aqui!
data_inicio_namoro = "2023-06-12" # Formato: YYYY-MM-DD (Ano-Mês-Dia) - Ajuste para a data exata de voz!

# Calcula a duração do namoro
data_inicio = datatime.strptime(data_inicio_namoro, "%Y-% m-% d")
hoje = datatime.now() # O fuso horário local é considerado.

# Calcular anos e meses de forma mais precisa
anos = hoje.ano - dados_inicio.ano
meses = hoje.month - data_inicio.month
se meses < 0 ou (meses == 0 e hoje.day < data_inicio.day):
 anos -= 1
 meses = (hoje.month - data_inicio.month + 12) % 12
 se hoje.day < data_inicio.day:
 meses = (meses - 1 + 12) % 12


# --- Conteúdo da Carta ---
conteudo_carta = f"""
    <p>Minha querida <forte>Rute</forte>,</p>
    <p>Hoje, {hoje.day} de {hoje.strftime ('% B')}, celebramos não apenas o amor que nos une, mas também o privilégio de ter completado <forte>{anos} ano(s)</forte> ao seu lado. Parece que foi ontem que tudo veio, e cada dia tem um presente.</p>
    <p>Sou grato por todo o seu carro, sua compreensão e por cada momento de risada e de apoio que compartilhamos. Você me faz uma pessoa melhor e ilumina meus dias.</p>
    <p>Lembro-me do nosso primeiro encontro, que foi belo e repleto de carro e amor. Amo como você me faz assistir filmes de romance contra a minha voz. Uma primeira vez vez que dissemos que uma amava foi estranho por conta da minha timidez, porém você me aceitou com todo o seu amor. Esses momentos construíram uma base sólida do nosso amor.</p>
    <p>Você é uma pessoa que ilumina meus dias, eu inspira um ser melhor e eu completa de uma forma que nunca imaginei ser possível. Adoro seu jeito carinhoso, sua inteligência e seu senso de humor quebrado e ruim.</p>

    <p style= "alinhamento de texto: centro; estilo de fonte: itálico; margem: 30px 0; cor: #880e4f;">
     "Não Teu Olhar:"<br>
     "Teu olhar é um universo a descobrir,<br>
     Uma viagem sem fim, sempre a mim guiar,<br>
     Com você, o tempo parece parar,<br>
     E neste amor profundo, quero sempre estar."
    </p>

    <p>Que venham muitos e muitos anos mais, repletos de amor, cumplicidade, novas aventuras e uma certeza de que sempre estarei aqui para você, assim como você está para mim. EU TE AMO HOJE E AMANHA AMAREI MAIS AINDA!</p>
    <p>Com todo o meu amor e admiração,</p>
    <p>Seu eterno <strong>Emanoel</strong></p>
"""

# --- Estrutura HTML da Carta com Botão e JavaScript ---
html_content = f"""
<!DOCTYPE html>
<html lang="pt-BR">
<cabeça>
    <meta charset="UTF-8">
    <meta nome="viewport" conteúdo="width=device-width, initial-scale=1.0">
    <título>Para o Amor da Minha Vida️</título>
    <estilo>
 corpo {{
 fonte-família: 'Geórgia', serifa;
 antecedentes: linear-gradiente (para a direita, #ffdde1, #ee9ca7); /* Toneladas de rosa e pêssego */
 exibição: flex;
 flex-direction: coluna; /* Para alinhar o botão acima da carta */
 justifique-conteúdo: centro;
 alinha-itens: centro;
 altura mínima: 100vh;
            margin: 0;
            padding: 20px;
            tamanho caixa: border-box;
        }}
 .carta-contêiner {{
            fundo-cor: #ffffff;
            raio fronteiriço: 15px;
            caixa-sombra: 0 10px 30px rgba(0, 0, 0, 0,2);
            preenchimento: 40px;
            largura máxima: 700px;
            texto-alinhar: centro;
            opacidade: 0; /* Começa invisível */
            transformar: escala(0,9); /* Começa menor */
            transição: opacidade 1,5s aliviar, transformar 1,5s aliviar; /* Transição suave */
            posição: relativo; /* Para a sombra do coração */
            margem superior: 20px; /* Espaço entre o botão e a carta */
        }}
 .carta-container.show {{
            opacidade: 1;
            transformar: escala(1);
        }}
 .carta-contêiner::antes {{
            conteúdo: ' ⁇ ️';
            fonte-tamanho: 80px;
            posição: absoluto;
            topo: -40px;
            esquerda: 50%;
            transformar: traduzirX(-50%);
 índice z: 1;
            filtrado: sombra(0 5px 10px rgba(0,0,0,0,2));
 animação: coraçãoBatida 1,5 s infinito alternar; /* Batimento do coração */
        }}
 h1 {{
            cor: #d81b60; /* Rosa escuro */
            fonte-tamanho: 2.8em;
 margem inferior: 20px;
            texto-sombra: 1px 1px 2px rgba(0,0,0,0,1);
        }}
        p {{
            cor: #4a4a4a;
            fonte-tamanho: 1.2em;
            linha-altura: 1.6;
 margem inferior: 15px;
            texto-alinhar: esquerda; /* Alinha o texto da carta à esquerda */
        }}
 p forte {{
            cor: #c2185b; /* Um rosa mais forte para nomes */
        }}
 .dados {{
 fonte-tamanho: 0,9em;
 cor: #888;
 margem superior: 30px;
 texto-alinhar: direito;
 }}
 .botão aberto {{
 fundo-cor: #e91e63; /* Rosa vibrante */
 cor: branco;
 preenchimento: 15px 30px;
 fronteira: Nenhum;
 raio fronteiriço: 50px; /* Botão arredondido */
 fonte-tamanho: 1,5em;
 cursor: ponteiro;
 caixa-sombra: 0 8px 15px rgba(0,0,0,0,2);
 transição: todos 0,3 s facilidade;
 peso da fonte: ousado;
 espaço entre letras: 1px;
 posição: relativo;
 transbordamento: escondido; /* Para o efeito de brilhante */
 }}
 .botão aberto:emparelhar {{
 fundo-cor: #d81b60; /* Rosa mais escuro sem par */
 transformar: traduzirY(-3px);
 caixa-sombra: 0 12px 20px rgba(0,0,0,0,3);
 }}
 .botão aberto:ativo {{
            transformar: traduzirY(0);
            caixa-sombra: 0 5px 10px rgba(0,0,0,0,2);
        }}
 .botão aberto::depois {{ /* Efeito de brilho ao passar o rato */
            conteúdo: '';
            posição: absoluto;
            topo: -50%;
            esquerda: -50%;
            largura: 0;
            altura: 200%;
 fundo: rgba(255.255.255,0,1);
 transformar: girar(45 graus);
 transição: todos 0,5 s facilidade;
 }}
 .botão aberto:emparelhar::depois {{
 grande: 120%;
 }}

     /* Animações */
     @keyframes heartBeat {{
     da transformada {{: escala translateX(-50%)(1); }}
     para transformada {{: escala translateX(-50%)(1,1); }}
     }}
    </style>
</cabeça>
<corpo>
 <botão classe= "botão aberto" eu= "carta abertaBtn">Abra a Carta, Meu Amor! 💌</botão>
    <div classe="contêiner carta" ue="contêiner Carta">
        <h1>Felizes {anos} Anos de Nós! 💖</h1>
 {conteudo_carta}
        <p classe="dados">Imperatriz, {hoje.day} de {hoje.strftime('% B')} de {hoje.year}</p>
    </div>

    <script>
     document.getElementById('openLetterBtn').addEventListener('click', function() {{
     document.getElementById('cartaContainer').classList.add('show');
     this.style.display = 'none'; // Esconde o botão depois de clicar
     }});
    </script>
</corpo>
</html>
"""

# --- Salvar o HTML em um arquivo temporário e abre-lo ---
nome_arquivo_html = "carta_para_o_amor.html"

tentar:
 com open (nome_arquivo_html, "w", coding="utf-8") como arquivo:
 arquivo.write(html_content)
 imprimir (f"Carta gerada e salva como '{nome_arquivo_html}'")

    # Abre o arquivo HTML no navegador padrão
    webbrowser.open(nome_arquivo_html)
    print ("A carta foi aberta no seu navegador padrão!")

exceto Exceção como e:
 imprimir (f"Ocorreu um erro ao gerar ou abre a carta: {e}")

# Opcional: Removedor o arquivo HTML depois de um tempo (se não quiser que ele fique salva)
# tempo importação
# time.sleep(5) # Espera 5 segundos para que ela possa ver
# os.remove(nome_arquivo_html)
# imprimir(f "Arquivo '{nome_arquivo_html}' removido.")
