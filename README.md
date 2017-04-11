# Corpus do Português e Modelos Diversos

Esse projeto foi criado para dar facilidade no acesso a um Corpus do Português que tenha uma quantidade de palavras e sentenças relevantes. Mesmo com projetos em algumas universidades o acesso não é facilitado e alguns corpus exigem pagamento. 

Primeiramente será criado um Corpus do Português/BR através de um dump do Wikipedia: https://dumps.wikimedia.org

Após será gerado um modelo usando o wordrep da library MITIE: https://github.com/mit-nlp/MITIE/tree/master/tools/wordrep

Serão disponibilizados todas as ferramentas que serão utilizadas, bem como o resultado, como para gerar o modelo do MITIE exige muito processamento e memória é algo que realmente pode ajudar quem precisa de um modelo.

Ajudas bem-vindas:

* Corpus diversos do Português;
* Modelos prontos; 

## Convertendo um dump Wikipedia para somente texto

O pré-processamento do dump do Wikipedia é feita por uma ótima ferramenta, extremamente performática e licenciada sob a licença MIT. Ela é desenvolvida em uma linguagem não muito comum, a Nim, mas ela gera binários para várias plataformas. Mais detalhes pode ser encontrados no repositório do Nim: https://github.com/rspeer/wiki2text

Por padrão o wiki2text inclui o header de cada artigo no formato: == [titulo] == , é necessário remover com grep -v para ficar um corpus mais limpo. O comando para a extração do texto é semelhante a:

``` bunzip2 -c dump_wikipedia_compactado.xml.bz2 | ./wiki2text | grep -v '^=' > ptwiki.txt ```

## Mais do que artigos

Caso deseje um corpus com linguagem mais informal, é só incluir também os metadados do Wikipedia, pois isso inclui as discussões nos artigos, que é geralmente feita por mensagens mais informais entre os membros do Wikipedia. Geralmente quanto mais polêmico o artigo é, mais discussão e mais informalidade, veja um exemplo na seguinte página: https://pt.wikipedia.org/wiki/Discussão:Inri_Cristo

## Downloads

Como os corpus são muito grandes não é possível incluir no Github, estão disponíveis para download através dos links:

| Corpus            | Qtde Palavras | Link                                                          |
|-------------------|---------------|---------------------------------------------------------------|
| Artigos Wikipedia | 244.188.490   | http://fabiomazzo.com/corpusportugues/pt_wiki_244_188_490.zip |


## Licença dos dumps Wikipedia e os corpus gerados

A linceça dos dumps e dos corpus gerados a partir do Wikipedia seguem o licenciamento do Wikipedia, disponível em https://dumps.wikimedia.org/legal.html

## Planejado

Está planejado o desenvolvimento de um webcrawler que leia os principais sites de notícias em português e faça a extração para um Corpus, provavelmente não poderemos compartilhar o corpus por motivos de licenciamento do conteúdo, mas iremos disponibilizar o webcrawler e todas as instruções necessárias.
