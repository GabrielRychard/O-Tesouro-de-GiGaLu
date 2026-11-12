# O Tesouro de GiGaLu

RPG de turnos em Python (tkinter). Monte uma party com Guerreiro, Mago, Sacerdote e Arqueiro, enfrente 5 hordas de monstros e derrote o dragão Tiamat para chegar ao tesouro.

- 4 heróis, nas versões masculina e feminina, com ações que gastam mana ou têm tempo de recarga
- 5 monstros (Goblin, Morcego, Slime, Ogro e o chefe Tiamat, que enfurece com pouca vida)
- 5 cenários, um por horda, desenhados por código
- Sprites em pixel art originais, gerados com a biblioteca Pillow
- Fogos de artifício e baú de tesouro na vitória; baú vazio na derrota

Feito pelo grupo GGL: Gabriel Rychard, Luiz Henrique e Giovanna Campos.

---

## 1. Como extrair o arquivo ZIP

Não abra o jogo de dentro do ZIP: o jogo precisa dos arquivos extraídos numa pasta.

**Windows**
1. Clique com o botão direito no arquivo `.zip`.
2. Escolha **Extrair tudo...** e depois **Extrair**.
3. Abra a pasta criada. Você deve ver `jogo_rpg.py`, `cenario.py`, `creditos.txt` e a pasta `sprites`.

**macOS**
1. Dê dois cliques no `.zip`. Uma pasta com o mesmo nome aparece ao lado.

**Linux**
1. No terminal: `unzip nome-do-arquivo.zip`
   (ou botão direito no arquivo e **Extrair aqui**).

Confira se estes arquivos ficaram **na mesma pasta**:

| Arquivo | Função |
| --- | --- |
| `jogo_rpg.py` | O jogo (é ele que você abre) |
| `cenario.py` | Cenários, fogos e baús |
| `creditos.txt` | Texto da janela de créditos |
| `gerar_sprites.py` | Gera as animações dos heróis |
| `gerar_monstros.py` | Gera as animações dos monstros |
| `sprites/` | Imagens das animações |

## 2. O que instalar

- **Python 3** (site oficial: python.org). No Windows, marque **Add Python to PATH** na instalação.
- **Pillow**, para os geradores de sprites: `pip install pillow`
- **tkinter**: já vem no Python para Windows e macOS. No Linux: `sudo apt install python3-tk`

## 3. Como abrir o jogo

1. Abra o terminal (ou o Prompt de Comando) **dentro da pasta extraída**.
2. Se a pasta `sprites` não existir (ou você mudou algum desenho), gere as imagens:
   ```
   python gerar_sprites.py
   python gerar_monstros.py
   ```
3. Abra o jogo:
   ```
   python jogo_rpg.py
   ```
   No Windows, `py jogo_rpg.py` também funciona.

## 4. Como jogar

**Montar a party**
1. Digite um nome para cada classe: Guerreiro, Mago, Sacerdote e Arqueiro (sem repetir nomes).
2. Escolha Masculino ou Feminino ao lado de cada nome. Isso muda só o visual e o nome da classe.
3. Clique em **Confirmar Party** e depois em **Iniciar Aventura**.

**Cada turno**
1. Uma seta amarela mostra qual herói joga, na ordem Guerreiro, Mago, Sacerdote, Arqueiro.
2. Marque o alvo na lista **Monstros** (ou o aliado, em **Sua Party**).
3. Clique no botão da ação. Passe o mouse sobre ele para ler o que faz.
4. Depois que os quatro agem, os monstros atacam e começa uma nova rodada.
5. Botão cinza = ação indisponível (recarga, pouca mana ou sem poções). O aviso em vermelho diz o motivo.

**Os heróis**

| Herói | Ações |
| --- | --- |
| Guerreiro | Atacar, Golpe Devastador, Provocar, Bloquear |
| Mago | Magia, Bola de Fogo, Poção de Mana, Cajado |
| Sacerdote | Cura, Cura em Grupo, Reviver, Adaga |
| Arqueiro | Flecha, Tiro Duplo, Tiro Certeiro, Chuva de Flechas |

**Objetivo e regras**
- Vença as 5 hordas. A última é a dragão Tiamat, que enfurece com 30% da vida ou menos.
- Entre as hordas, a party recupera 30% da vida e 40% da mana e ganha +1 Poção de Mana.
- Se os quatro heróis caírem, é derrota. O jogo pergunta se você quer tentar de novo.
- `F11` entra em tela cheia e `Esc` sai.

## 5. Problemas comuns

| Problema | Solução |
| --- | --- |
| `No module named 'tkinter'` | Instale o tkinter (veja o item 2) |
| `No module named 'PIL'` | `pip install pillow` |
| `No module named 'cenario'` | Abra o terminal dentro da pasta, com `cenario.py` ao lado do jogo |
| Personagens não aparecem | A pasta `sprites` está faltando: rode os dois geradores (item 3) |
| O jogo abre e fecha | Rode pelo terminal para ver a mensagem de erro |

## Créditos

Feito por Gabriel Rychard, aluno de GTI na Fatec 2° Semestre
