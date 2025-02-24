
## Guia Rápido
O repositórios contém arquivos usados no projeto menor preço, separados em diferentes dir:
* doc: documentos
* data: dados usados no projetos em diferentes arquivos.
  * tupan_*: são dados extraido em diferentes fases;
  * df_nondim: são dados misturados de diferentes fontes como leroy merlin e outros arquivos baixados do orion;
  * full_df: são dados misturados a partir dos outros .csv excepto (df_fs, clean_df);
  * df_fs: são dados filtrados com classes com mais de 200 amostras com objetivo de segmentar modelos;
  * df: é a mesma dataset full_df, porém após aplicação de preprocessamento;
* modelo: contém modelo treinado salvo que pode ser carregado e usado para gerar embeddings;
* notebook: notebooks usado
  * def_data: contém código para preparar dados, combinando todos tupan e non_dim, aplicação de limpeza e segmentação;
  * main_snn: código que treina o modelo utilizando segmentos de datasets;
  * make_datasets: contém funções auxiliares para separação e contrução tripletes;
  * make_embeddings: contém código para carregar USE (universal sentence encoder) e bert para gerar embeddings inicial;
  * make_tune: usado para busca dos melhores Hiperparâmetros;
  * xgboost: classificador auxiliar para testar melhor ponto de segmentação dos dados baseado nas métricas e também utilizada para classificar novos dados;
  * similarity_cluster: clusterização e computação de algumas estatísticas;