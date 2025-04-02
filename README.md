# analise_mercado_futuro
Projeto que visa analisar relações entre as séries temporais de preços relacionadas ao agronegócio

O projeto possui dois notebooks:

1. extrair.ipynb
  Responsável por extrair os dados de cotação dos preços de futuros na B3
    1. Utiliza-se Selenium para realizar a automação
3. análise_de_correlação.ipynb
  Responsável pela análise de correlação e limpeza dos dados
  Os principais tratamentos são:
    1. Transformação de dados tipo string para numéricos
    2. Tratamento da identificação dos vencimentos dos contratos
    3. União de contratos após o vencimento do contrato vigente ***
    4. Novo contrato precisa no mínimo n dias  para ser adicionado a série temporal concatenada pelo item 3
    5. Adicionar a cotação do Dolar PTAX para transformar a cotação da Soja para Reais
