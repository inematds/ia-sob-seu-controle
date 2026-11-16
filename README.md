# IA sob seu controle

[![Sua IA sob controle](guia/assets/banner.jpg)](https://inematds.github.io/ia-sob-seu-controle/guia/)

**🇧🇷 [Português](README.md) · 🇺🇸 [English](README.en.md) · 🇪🇸 [Español](README.es.md)**

## O que é

Kit educativo gratuito do INEMA para escolher onde sua IA roda, quem recebe seus dados e como conferir uma entrega. Inspirado na análise da aula “The 5 Levels of Uncensored AI”, separa liberdade de resposta, privacidade e precisão. Inclui análise autoral, exercício fictício com resposta conhecida, ficha de decisão e conferidor offline. Não instala modelos, não chama APIs e não substitui testes da sua configuração real.

## Guia de uso

**https://inematds.github.io/ia-sob-seu-controle/guia/**

## Começar

Python 3.10+ e Git, sem dependências externas.

```bash
git clone https://github.com/inematds/ia-sob-seu-controle.git
cd ia-sob-seu-controle
python3 -m unittest discover -s tests -v
python3 scripts/conferir.py kit/exemplos/ficha.json
```

O exemplo começa incompleto e retorna `invalida` (código 2). Abra `kit/exemplos/ficha.json` no editor: preencha o modelo e os campos e marque as evidências somente após conferir. `revisar` (código 1) indica pendência; `ficha-conferida` (código 0) indica consistência declarada, não certificação. Os avisos continuam exigindo leitura. No Windows, `py` pode substituir `python3`.

## O processo, do início ao fim

1. Leia a [análise](docs/ANALISE.md) e escolha sua necessidade.
2. Preencha a [ficha](kit/exemplos/ficha.json) com a configuração que pretende usar.
3. Execute a tarefa com o [relatório fictício](kit/exemplos/relatorio-ficticio.md) no aplicativo de IA escolhido.
4. Entregue os dados e o resultado ao [revisor](kit/prompts/revisor.md), e confira com a referência.
5. Se precisa de offline, teste com a rede desligada depois de baixar o modelo.
6. Registre as evidências e execute o conferidor.

## Limites

O conferidor apenas lê JSON local e valida as decisões declaradas. Não inspeciona rede, modelo, hardware ou arquivos do usuário. Não mede qualidade da IA, não garante ausência de vazamento e não instala software. O código é independente do idioma do guia; os exemplos e mensagens do kit estão em português.

## Fonte

[The 5 Levels of Uncensored AI — Jack Roberts](https://youtu.be/FbiOr73tRPk), aula publicada em 15/11/2026. Análise autoral e links de documentação; sem reprodução dos materiais privados.

MIT para o código e textos autorais deste projeto. Marcas e materiais externos pertencem aos respectivos autores.
