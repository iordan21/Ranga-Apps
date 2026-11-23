# Ranga Apps

O catálogo da loja **Apps** do [Ranga EMU](https://github.com/iordan21/Ranga-EMU): os programas de Windows que abrem por ela, com o controle.

| App | Código |
|---|---|
| Ranga TV | [iordan21/Ranga-TV](https://github.com/iordan21/Ranga-TV) |
| Ranga YTM | [iordan21/Ranga-YTM](https://github.com/iordan21/Ranga-YTM) |
| Ranga Spot | [iordan21/Ranga-YTM](https://github.com/iordan21/Ranga-YTM) (mesmo codigo) |

## Como funciona

- `catalogo.txt` lista os apps: nome, versão, o endereço do zip (um release do repositório do app), o SHA-256 e o tamanho dele.
- `catalogo.sig` é a assinatura do catálogo, com a mesma chave das atualizações do Ranga EMU. Só o PC que publica tem essa chave.
- O Ranga EMU baixa os dois do último release deste repositório. Ele só mostra um catálogo com essa assinatura, só baixa do GitHub de `iordan21` e só instala um zip cujo hash bate com o do catálogo.

## Publicar uma versão de um app

1. Release do app no repositório dele, com o zip.
2. Atualizar `versao`, `zip`, `sha256` e `tamanho` em `catalogo.txt`.
3. No PC que publica: `C:\ps5\RangaEmu.exe --assinar-catalogo "C:\projetos\Ranga-Apps\catalogo.txt"` (o resultado sai em `C:\ps5\salas\publicar.log`).
4. Novo release aqui com `catalogo.txt` e `catalogo.sig`, marcado como o último.

## Licença

MIT (veja [LICENSE](LICENSE)). Vale para o catálogo: cada app tem a licença do repositório dele.
