<div align="center">

# 🌙 My Moon Cinemas

**Site de cinema com reserva de assentos, feito com Flask, MySQL e front-end em HTML/CSS/JS.**

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

</div>

## 💡 Sobre

Site de um cinema fictício com catálogo de filmes, páginas institucionais e mapa de assentos por sala. Uma API em Flask cuida do cadastro e login de usuários e da reserva de assentos, gravando tudo em MySQL; as páginas são servidas pelo próprio Flask com templates Jinja.

## ✨ Funcionalidades

- Cadastro e login de usuários
- Catálogo de filmes e página de filme
- Seleção e confirmação de assentos por sala (livre/ocupado)
- Páginas "Quem somos", política de privacidade e termos de uso

## 🛠️ Tecnologias

- **Back-end:** Python, Flask, MySQL (`mysql-connector-python`)
- **Front-end:** HTML5, CSS3, JavaScript

## 📌 Endpoints

| Método | Rota | Descrição |
|--------|------|-----------|
| `POST` | `/criar_usuario/` | Cria usuário (`usuario`, `senha`) |
| `POST` | `/verificar_login/` | Valida login |
| `POST` | `/confirmar_assentos/` | Marca uma lista de assentos como ocupados |
| `GET` | `/consultar_sala/` | Lista os assentos da sala |
| `GET` | `/consultar_sala/<id>/` | Consulta um assento |
| `PUT` | `/atualizar_situacao/<id>/` | Altera a situação do assento (`0` livre, `1` ocupado) |

Páginas: `/home`, `/catalogo`, `/cadastro`, `/login`, `/quemsomos`, `/politica_priv`, `/termo_uso`, `/cinemavip`, `/cadeadora`, `/salaDora`.

## 🚀 Como rodar

Requer Python 3 e MySQL.

1. Importe os scripts de `BD/` (`bd_apipython_login_cinema.sql` e `bd_apipython_sala_cinema.sql`); eles criam o banco `bd_apipython`.
2. Ajuste usuário e senha do MySQL no dicionário `config` em `app.py`.
3. Rode:

```bash
git clone https://github.com/KevinLopes23/My-Moon-Cinemas.git
cd My-Moon-Cinemas
pip install flask mysql-connector-python
python app.py
```

Acesse `http://localhost:5000/home`.

## 📄 Licença

Distribuído sob a licença MIT. Veja [LICENSE](LICENSE).

## 👤 Autor

Feito por [Kevin Lopes](https://github.com/KevinLopes23)
