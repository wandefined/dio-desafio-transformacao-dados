# Desafio: Processando e Transformando Dados com Power BI

Nesse desafio, foram extraídos dados de um Banco de dados MySQL. Esses dados
então foram transformados para que a análise fosse criada.

A primeira etapa foi a exclusão dos campos de metadados do banco de dados e 
ajustes nos cabeçalhos e tipos de dados:

![Tipo de Dados](etapas/1_tipos_de_dados.png)

O campo de salário foi ajustado para o tipo double preciso:

![Tipo Monetário](etapas/2_salario.png)

Apenas um employee não tinha Super_ssn, indicando que este era um gerente.
Não havia departamento sem gerente.

As tabelas employee e departament foram mescladas em uma nova tabela chamada
"Employee x Departament", associando o nome dos departamentos aos colaboradores:

![Employee x Departament](etapas/3_employeexdept.png)

Posteriormente, foi realizada a junção dos colaboradores e respectivos nomes dos
gerentes:

![Employee x Departament](etapas/4_colabxgerente.png)

As colunas de Nome e Sobrenome foram mescladas para ter apenas uma coluna, 
definindo os nomes dos colaboradores:

![Nome + Sobrenome](etapas/5_nomexsobrenome.png)

Os nomes de departamentos e localização também foram mesclados. Isso fez com que
cada combinação departamento-local seja único, auxiliando na criação do modelo
estrela:

![Departamento + Local](etapas/6_deptxlocal.png)

Por fim, o seguinte relatório foi construído:

![Relatório](etapas/7_report.png)

## Documentos

- [Arquivo do Projeto - Power BI](Desafio.pbix)
- [Script do Banco de Dados](script_bd.sql)
