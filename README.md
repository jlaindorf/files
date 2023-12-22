<img src="https://github.com/jlaindorf/files/blob/main/halteres-no-chao-de-uma-academia-ai-generative.jpg" width="600" alt="Logo">


# API WORLDGYM

A WorldGym, uma empresa altamente respeitada no ramo de academias, expressou satisfação em relação ao protótipo do projeto front-end desenvolvido no módulo 1. Diante desse êxito, a empresa agora manifestou o interesse em dar continuidade ao projeto, solicitando a criação do back-end da aplicação, disponibilizando de uma API REST completa para que os usuários tenham controle dos seus treinos e alunos .

## Tecnologias Utilizadas
Utilizei para a criação do projeto a linguagem PHP , utilizando o framework Laravel com banco de dados Postgresql e Dbeaver para conexao com o banco de dados . 
<div>
<img src="https://github.com/jlaindorf/files/blob/main/download.png" width="60" alt="laravel">
<img src="https://github.com/jlaindorf/files/blob/main/docker.png" width="60" alt="docker">
<img src="https://github.com/jlaindorf/files/blob/main/dbeaver.jpg" width="60" alt="dbeaver">
</div>

## Ferramentas e plugins 

COMPOSER| DOM PDF | BLADE | DOCKER | MAILTRAP

## Relacionamento do Bancos De Dados

<img src="https://github.com/jlaindorf/files/blob/main/api_academia%20-%20public.png" width="800" alt="relacionamentos db">


## Como executar o projeto 
* Clonar para sua maquina. 
* Abrir terminal 
  * Composer install (para baixar as dependências)
* no arquivo .ENV configurar seu banco de dados
* Abrir Terminal
  * php artisan serve
## Rotas da Aplicação 
| Método | Rota                             | Controlador/Método              | Middleware                   |
|--------|----------------------------------|---------------------------------|------------------------------|
| GET    | /dashboard                       | DashboardController@index       | auth:sanctum                 |
| POST   | /exercises                       | ExerciseController@store        | auth:sanctum                 |
| GET    | /exercises                       | ExerciseController@index        | auth:sanctum                 |
| DELETE | /exercises/{id}                  | ExerciseController@destroy      | auth:sanctum                 |
| GET    | /students/export                 | WorkoutController@showWorkout   | auth:sanctum                 |
| POST   | /students                        | StudentController@store         | auth:sanctum, CheckStudentLimit |
| GET    | /students                        | StudentController@index         | auth:sanctum                 |
| DELETE | /students/{id}                   | StudentController@destroy       | auth:sanctum                 |
| PUT    | /students/{id}                   | StudentController@update        | auth:sanctum                 |
| GET    | /students/{id}                   | StudentController@show          | auth:sanctum                 |
| POST   | /workouts                        | WorkoutController@store         | auth:sanctum                 |
| GET    | /students/{id}/workouts          | WorkoutController@index         | auth:sanctum                 |
| POST   | /users                           | UserController@store            | -                            |
| POST   | /login                           | AuthController@store            | -                            |

