# COVID-19 no Power BI

### Fonte de dados: https://github.com/CSSEGISandData/COVID-19

* Observações no tratamento dos dados para facilitar seu trabalho:
O ideal é sempre olhar a tabela e planejar os tratamentos que precisam ser feitos: Tipo de dados, nulls, blanks, erros, etc.
    * A tabela tem valores diários, porém acumulados;
    * Necessário criar um Código DAX para Pegar a variação diária(vide arquivo DAX);
    * Depois de pivotar a tabela (os dados estão com data como coluna, ou seja, cada dia é uma coluna), formate o campo data Usando a localizade (Inglês EUA);
    * O script em M para formatar as tabelas, estão na pasta, caso queira pular o tratamento de dados;
    * Não Esqueça de criar uma tabela dCalendário (Use função CALENDARAUTO())
    * Nao esqueça de colocar o caminho do arquivo no seu computador no Script M, a minha VM está assim (mude a parte em negrito, coloque o teu):
     Fonte = Csv.Document(File.Contents **("C:\Users\claudiomattos\Documents\GitHub\COVID-19\csse_covid_19_data\csse_covid_19_time_series\time_series_19-covid-Confirmed.csv")**,[Delimiter=",", Columns=61, Encoding=65001, QuoteStyle=QuoteStyle.None]).
     * Olhe o arquivo DAX, la tem uma parte para edição do pbix.
   
    
 
