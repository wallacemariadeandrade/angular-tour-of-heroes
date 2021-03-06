# Angular Tour of Heroes
Tutorial from https://angular.io/tutorial

## Observações

- As propriedades definidas nos componentes podem ser invocadas na interface de usuário com o operador de interpolação  ```{{}}``` 

- O arquivo ```styles.css``` é a folha de estilo base compartilhada por todos os componentes

- Um componente sempre importa ```Component``` do Angular core library e é anotado com ```@Component``` para especificar os metadados ```selector```, ```templateUrl``` e ```styleUrls``` relativos a si mesmo
    - ```selector``` identifica o seletor CSS e tem o mesmo nome do HTML que identifica o componente dentro do template do seu parente
    - ```templateUrl``` identifica a localização do arquivo de template
    - ```styleUrls``` identifica a localização da folha de estilos de uso privado (pode ser usada a diretiva @Component.styles para definir um array de estilos)
    
- ```NgOnInit()``` é um método invocado logo após a construção do componente e é útil para inicialização de dados, tal como uma requisição a servidor remoto, por exemplo (**O construtor não deve ser usado para esse fim, mas apenas para inicializar variáveis simples**). ```NgOnInit()``` é invocado uma vez só, enquanto o ```NgOnChanges``` é invocado uma vez antes do ```NgOnInit()``` e diversas vezes depois.

- O uso do ```export``` nas classes é necessário para poder importá-la em qualquer lugar, inclusive no ```AppModule```, que é o módulo raíz onde ficam os imports dos demais módulos a serem utilizados pela aplicação

- O ```AppComponent``` é o shell da aplicação e funciona como template base

- O operador pipe ```|``` é útil para formatar strings, dinheiro, datas, etc. antes de exibi-los. O Angular já vem com opções predefinidas, mas é possível criar outras também

- O two way binding do Angular é viabilizado pelo operador ```[(ngModel)]```, pertencente ao módulo ```FormsModule```, aplicado na tag HTML

- **```*ngFor``` é o operador de iteração do Angular e serve para percorrer conjuntos de objetos no HTML do componente**

- **O event binder do Angular é feito colocando o nome do evento entre parênteses na tag HTML**

- **```*ngIf``` é o operador condicional do Angular para uso no HTML do componente**

- **```[]``` é o operador utilizado para property binding**

- O Angular tem um container DI nativo e os serviços são associados a ele por meio da diretiva ```@Injectable``` aplicada na classe

- **Operações assíncronas retornam um ```Observable``` de algo! Sempre se deve fazer o ```subscribe()``` de um ```Observable```, caso contrário a requisição não será enviada!**

- O roteamento é feito pelo ```AppRoutingModule```, que deve ser importado para o ```AppModule```.

- Uma rota em Angular tipicamente possui duas propriedades: string que determina o caminho e o componente a ser criado quando se navega para a rota em questão.

- O ```RouterOutlet``` instrui o roteador sobre qual view exibir

- O ```routerLink``` é um atributo que pode ser aplicado na parte HTML para funcionar como o href, de maneira a indicar a navegação. É o seletor do módulo ```RouterLink```

- ```ActivatedRoute``` é o serviço que armazena informações da rota em questão e pode ser consumido via construtor

- ```Location``` é um serviço para interação com o browser e pode ser consumido via construtor

- ```HttpClient``` é o serviço do Angular para comunicação via HTTP e pertence ao módulo . ```HttpClientModule```.  Seu método ```get()``` por padrão, admite que a resposta da requisição será um JSON.

- RxJS ```catchError()``` é um operador para interceptar o ```Observable``` com erro!

- RxJS ```tap()``` é um operador para interceptar o ```Observable``` e fazer algo com seu conteúdo, porém sem alterá-os!

- Ao iterar sobre um ```Observable``` usa-se o pipe ```async``` para processamento dos dados!

- ```Subject``` é um ```Observable``` que funciona semelhante a um stream de dados que permite leitura e escrita