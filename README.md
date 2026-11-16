# IA sob seu controle

[![Sua IA sob controle](guia/assets/banner.jpg)](https://inematds.github.io/ia-sob-seu-controle/guia/)

**🇧🇷 [Português](README.md) · 🇺🇸 [English](README.en.md) · 🇪🇸 [Español](README.es.md)**

## O que é

Este é um kit gratuito de decisão e verificação para quem usa IA no trabalho. Ele separa duas escolhas: quem pode acessar os dados e quais pedidos o modelo aceita responder. O kit traz um exercício com resposta conhecida, uma ficha preenchível e um conferidor local para registrar suas decisões. Para entender o assunto, basta ler; para executar o conferidor, você precisa de Python. Ele não instala nem configura modelos de IA.

Este repo entrega um kit de decisão e verificação. Ele ajuda você a avaliar privacidade, liberdade de resposta e qualidade separadamente. Não instala uma IA privada nem um modelo sem censura.

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


MIT para o código e textos autorais deste projeto. Marcas e materiais externos pertencem aos respectivos autores.
