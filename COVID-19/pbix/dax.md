# DAX

Crie uma coluna calculada com o código abaixo:

```
Confirmados =
    VAR DiaAnterior='time_series_19-covid-Confirmed'[Date]-1
    VAR Pais= 'time_series_19-covid-Confirmed'[Country/Region]
    VAR State= 'time_series_19-covid-Confirmed'[Province/State]
    VAR CasosTotais='time_series_19-covid-Confirmed'[Confirmeds]
    RETURN
    CasosTotais-
    CALCULATE(VALUES('time_series_19-covid-Confirmed'[Confirmeds]);
    FILTER(ALL('time_series_19-covid-Confirmed');
    'time_series_19-covid-Confirmed'[Date]=DiaAnterior &&
    'time_series_19-covid-Confirmed'[Country/Region]=Pais &&
    'time_series_19-covid-Confirmed'[Province/State]=State
    ))

    ```


### Após aplicar o código na coluna, clique na tabela  e tire os casos menores que 0.
### Faça o mesmo para as outras tabelas, só mude a tabela de referência.
