# DEVOPS25 CI/CD Course Repository

Det här repositoryt är tänkt att följa hela kursen **Continuous Integration och Continuous Delivery**.

Nyckelordet är **VARFÖR**. Verktygen används för att göra principerna synliga, inte för att kursen ska bli en verktygskurs.

## Kursens röda tråd

```text
Commit → Build → Test → Artifact/Image → Deploy → Verify → Rollback
```

## Vad repositoryt innehåller

- En liten FastAPI-applikation
- Unit tests och integrationstester
- Dockerfile och docker-compose
- GitHub Actions för CI och en simulerad CD-kedja
- Scripts för lokal körning, verifiering, deployment och rollback
- Studentuppgifter för vecka 1–4
- Projektuppgift och bedömningsstöd

## Snabbstart lokalt

```bash
python -m venv .venv
source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt
pytest
uvicorn app.main:app --reload
```

Öppna sedan: http://127.0.0.1:8000/health

## Docker

```bash
docker build -t devops25-cicd-demo:local .
docker run --rm -p 8000:8000 devops25-cicd-demo:local
```

## Pedagogisk användning

Repositoryt är byggt för att kunna användas stegvis:

1. **Dag 1:** förstå applikationen och varför versionshantering behövs
2. **Dag 2:** skapa första CI-pipelinen
3. **Dag 3:** lägga in tester och quality gates
4. **Dag 4:** bygga artifact/container image
5. **Dag 5:** deploya till testmiljö
6. **Dag 6:** felsöka, verifiera och resonera om rollback
7. **Projekt:** bygga och motivera en egen CI/CD-kedja

## Viktig fråga i varje steg

> Vilket problem löser detta steg, och vad riskerar vi om steget saknas?


## Min Git-övning – Dag 1

Jag har skapat en egen Git-branch för att arbeta utan att ändra main.

Jag har lärt mig att git diff visar ändringar och att git commit sparar ändringarna lokalt.

En Pull Request används för att föreslå ändringar som kan granskas innan de slås ihop med main.
## Dag 2 – Continuous Integration

Under Dag 2 arbetar jag med CI och GitHub Actions.

Syftet med CI är att automatiskt kontrollera kodändringar.

Jag ska testa hur en pipeline startar, läsa loggar och
undersöka vad som händer när ett test misslyckas.
