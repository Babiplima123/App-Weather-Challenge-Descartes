
# App-Weather
Um breve aplicativo usando Kotlin para desafio técnico oportunidade Descartes 


# Resumo

O projeto tem como objetivo desenvolver um applicativo Kotlin com os seguintes requisitos:

  - Possuir uma conexão com uma API externa;
  - Fazer tratamento de dados obtidos pela API;

Dados os requisitos enumerados anteriormente, elaborei uma aplicação que devolve dados sobre o clíma da região onde o usuário decidir buscar.

# Recursos utilizados para o desenvolvimento

Para ajudar na criação da interface gráfica foram usadas imagens 
  
  > Designed by macrovector / Freepik & toutiaoap gallery, ícones foram baixados de <a>https://openweathermap.org/</a>

o repositório a seguir serviu como base para estudo 

  > <a>https://github.com/SunayanPradhan/WEATHER-APP.git<a/>

Após ler toda documentaçãao, escolhi a API openweather para fornecer as informações que eu precisava sobre o clíma
  
  > <a>https://openweathermap.org/current</a>

E finalmente, para converter as informações do arquivo json para dados validos no meu programa, utilizei o Plugin JSON no Android Studio
  
  > JSON To Kotlin Class (JsonToKotlinClass)
  
  # Sobre o desenvolvimento
  
  Basicamente o meu projeto seguiu o padrão MVC, meus principais Models são **WeatherModel** que contém as classes que irão receber as informações da API
  
```csharp
    public class WeatherData
    {
        public Coord coord { get; set; }
        public Weather[] weather { get; set; }
        public string _base { get; set; }
        public Main main { get; set; }
        public int visibility { get; set; }
        public Wind wind { get; set; }
        public Clouds clouds { get; set; }
        public int dt { get; set; }
        public Sys sys { get; set; }
        public int timezone { get; set; }
        public int id { get; set; }
        public string name { get; set; }
        public int cod { get; set; }
    }
```
  
 e **UserData**, que irá definir os usuários do sistema
  
  ```csharp
       class UserData
    {
        public String name { get; set; }
        public String password { get; set; }
        public String email { get; set; }

        public UserData(String name, String password, String email)
        {
            this.name = name;
            this.password = password;
            this.email = email;
        }
    }
```

Os outros arquivos principais são as Views, aqui utlizamos uma view para , e uma para tela principal,       onde as informações sobre o clíma serão tratadas e exibidas.
  
# Como funcina
  
 O aplicativo inicia a tela, o app irá encaminhar para a tela principal, nessa tela, possuimos um campo onde pode-se colocar um lugar. Quando o usuário pesquisa por um lugar, é feita uma requisição para API openweather(<a>https://openweathermap.org/current</a>), logo aqpós o usuário recebe as informações sobre o clíma daquela região.



