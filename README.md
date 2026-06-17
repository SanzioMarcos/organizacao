# Convenções concretas

## As práticas mais comuns de projetos profissionais:

## Commits (Conventional Commits)

Sempre comece com uma flag:

```text
feat: adiciona autenticação JWT
fix: corrige timeout da API
docs: atualiza README
test: adiciona testes do usuário
refactor: reorganiza camada de serviços
chore: atualiza dependências
ci: adiciona workflow GitHub Actions
```

Regra:

```text
<tipo>: descrição curta
```

Tipos mínimos:

```text
feat
fix
docs
test
refactor
chore
ci
```

---

## Estrutura de pastas Python

```text
project/
├── src/
├── tests/
├── docs/
├── .github/
├── Dockerfile
├── requirements.txt
└── README.md
```

Se for API:

```text
src/
├── api/
├── services/
├── models/
├── database/
└── utils/
```

---

## README

Ordem padrão:

```text
# Nome do Projeto

Descrição

Instalação

Uso

API

Testes

Docker

Licença
```

---

## Tratamento de erros

Nunca:

```python
except:
    pass
```

Sempre:

```python
except Exception as e:
    logger.error(str(e))
    raise
```

---

## Testes

Espelhe a estrutura do código.

```text
src/
└── services/
    └── user.py

tests/
└── services/
    └── test_user.py
```

Nome padrão:

```text
test_<arquivo>.py
```

Funções:

```python
def test_create_user():
```

---

## API REST

URLs sempre no plural:

```text
/users
/products
/orders
```

Métodos:

```text
GET
POST
PUT
DELETE
```

Documentação:

```text
Swagger/OpenAPI
```

Hoje isso é praticamente obrigatório.

---

## Docker

Arquivo obrigatório:

```text
Dockerfile
```

Opcional:

```text
docker-compose.yml
```

Comando padrão:

```bash
docker build .
docker run .
```

---

## CI/CD

Pasta padrão:

```text
.github/workflows/
```

Arquivo:

```text
ci.yml
```

Fluxo mínimo:

```text
Checkout
Instalar dependências
Executar testes
Executar lint
```

---

## Engenharia de IA

Além das regras acima:

```text
models/
prompts/
rag/
evaluations/
```

E sempre:

```text
.env.example
```

Nunca:

```text
.env
```

---

**10 regras obrigatórias para qualquer projeto GitHub profissional**:

1. Use Conventional Commits.
2. Código dentro de `src/`.
3. Testes dentro de `tests/`.
4. README com instalação e uso.
5. Dockerfile funcional.
6. Workflow CI automático.
7. Nunca use `except: pass`.
8. APIs documentadas com OpenAPI.
9. Variáveis em `.env.example`.
10. Um commit, uma responsabilidade.

Essas 10 regras já deixam um projeto com um aspecto visualmente profissional.
