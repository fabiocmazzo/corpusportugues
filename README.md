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
