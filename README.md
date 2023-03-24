# rest_tlppcore

 Configurações e exemplo de um Serviço rest protheus utilizando o TLPP CORE TL++

### Configuração do AppServer para o REST TLPP

1. O rest TLPP requer uma configuração diferente e independente do serviço REST padrão que normalmente subimos para utilizar o WSRESTFUL
2. Essas configurações podem ser utilizadas no mesmo appserver que ja roda o REST atual ou em um appserver separado
3. Adicone a seguinte configuração(basica) no seu appserver.ini. Pode colocar após a ultima linha do seu arquivo:


; SESSOES DE CONFGURACAO DO REST SEVER PARA TL++ TLPP

[HTTPSERVER]<br>
Enable=1
Servers=HTTP_REST


[HTTP_REST]
hostname=localhost
port=9995
locations=HTTP_ROOT

[HTTP_ROOT]
Path=/apitlpp
RootPath=C:\My Docs\Totvs\Protheus\bin\appserver\appmon\web
DefaultPage=index.html
ThreadPool=THREAD_POOL

[THREAD_POOL]
Environment=P12
MinThreads=1
