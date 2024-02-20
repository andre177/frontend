# frontend

### Importante:

Para que o **frontend** consiga se comunicar com o **backend** no ambiente do Elastic Beanstalk, você deverá substituir o endereço ***localhost*** pela URL de seu ambiente nas duas chamadas à API no arquivo [index.html](https://github.com/andre177/frontend/blob/main/index.html) (linhas 90 e 111):

De:
```javascript
$.getJSON("http://localhost:5000/consulta_cep?cep=" + cep,
$.getJSON("http://localhost:5000/cotacao?moeda1=BRL&moeda2=USD",
```
Para:
```javascript
$.getJSON("http://meu-ambiente.eba-5cpxxnpw.us-east-1.elasticbeanstalk.com:5000/consulta_cep?cep=" + cep,
$.getJSON("http://meu-ambiente.eba-5cpxxnpw.us-east-1.elasticbeanstalk.com:5000/cotacao?moeda1=BRL&moeda2=USD",
```
