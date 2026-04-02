# Template Insper de Trabalho Acadêmico

> **Fork do projeto original [gabs-acc/inspertex](https://github.com/gabs-acc/inspertex).**  
> O objetivo deste fork é atualizar a capa para o novo modelo gráfico exigido pelo Insper,
> substituindo o layout anterior pelas imagens institucionais (`FundoPreto`, `FundoCinza` e
> `FundoVermelho`) e centralizando a definição da capa no arquivo dedicado `capa_insper.tex`,
> compatível com a classe `insper-abntex2`.

---

Este repositório contém um template para a redação de documentos acadêmicos. O objetivo é fornecer uma estrutura básica que facilite a organização e formatação de trabalhos acadêmicos seguindo as normas ABNT e o padrão visual atualizado do Insper.

## O que mudou neste fork

- **Nova capa institucional**: a capa foi redesenhada para seguir o modelo visual atualizado do Insper, com três blocos gráficos sobrepostos (preto, cinza e vermelho) renderizados via TikZ.
- **Arquivo dedicado `capa_insper.tex`**: a lógica da capa foi extraída do `main.tex` para um arquivo próprio, facilitando manutenção e reuso. Basta adicionar `\input{capa_insper}` ao preamble do seu documento.
- **Compatibilidade preservada**: todas as demais funcionalidades do template original (estrutura ABNT, glossário, índice remissivo, bibliografia com `biblatex`) permanecem inalteradas.

### Arquivos necessários para a capa

Certifique-se de que os seguintes arquivos estejam na raiz do projeto:

| Arquivo | Descrição |
|---|---|
| `insper-logo.png` | Logo institucional do Insper |
| `FundoPreto.png` | Bloco preto central (recebe título e autor) |
| `FundoCinza.png` | Bloco cinza decorativo |
| `FundoVermelho.png` | Bloco vermelho decorativo |

---

## Como Utilizar

### Uso Local

1. **Clone o Repositório**: Faça o clone deste repositório para o seu ambiente local.
    ```bash
    git clone https://github.com/Hic-Tayfour/inspertex.git
    ```
2. **Editando o Conteúdo**: Substitua o conteúdo dos arquivos `.tex` nas seções correspondentes com o texto do seu trabalho acadêmico.
3. **Compilando o Documento**: Utilize um compilador XeTeX ou LuaLaTeX para gerar o documento final em PDF. Por exemplo, no terminal:
    ```bash
    xelatex main.tex
    ```
    ou
    ```bash
    lualatex main.tex
    ```
    > **Importante:** compile **duas vezes** seguidas para que os elementos TikZ da capa sejam posicionados corretamente pela segunda passagem.

4. **Usando IDEs**:
    - **VS Code**: Instale a extensão [LaTeX Workshop](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop). Abra o arquivo `main.tex` e utilize os comandos da extensão para compilar o documento.
    - **TeXstudio**: Abra o arquivo `main.tex` e selecione XeLaTeX ou LuaLaTeX como o compilador. Em seguida, compile o documento. Como um editor projetado especificamente para LaTeX, o TeXstudio é uma ferramenta fácil e intuitiva, mas não tão poderosa quanto outros IDEs.

### Uso Online

1. **Trabalhando com o Overleaf** (indicado para iniciantes)
    - **Overleaf**: Acesse o template diretamente [neste link](https://www.overleaf.com/read/hjxwfjwcmnrn). Será necessário copiar o projeto para poder editá-lo (no canto superior esquerdo, acesse Menu → Copy Project). Ainda na aba Menu, selecione **XeLaTeX** como compilador.
    - **Overleaf + VS Code**: É possível integrar os dois ambientes com a extensão [Overleaf Workshop](https://marketplace.visualstudio.com/items?itemName=iamhyc.overleaf-workshop). Assim, será possível acessar diretamente seu documento armazenado no Overleaf ainda se valendo das comodidades do VS Code.
    - **Overleaf + Outros**: Para sincronizar o Overleaf com algum outro editor local, o projeto [Overleaf-Sync](https://github.com/moritzgloeckl/overleaf-sync) pode ser um facilitador.

2. **Vantagens de usar o Overleaf**
    - **Interface Amigável**: A interface do Overleaf é simples e intuitiva, adequada para quem não quer gastar horas configurando o ambiente para ter uma experiência razoável.
    - **Sem Instalações**: Além de não precisar instalar um editor, o Overleaf suporta por padrão [mais de 5.000 pacotes](https://www.overleaf.com/learn/latex/Overleaf_and_TeX_Live) sem necessidade de instalação adicional — incluindo as fontes Arial e Times New Roman utilizadas neste template.
    - **Fácil Integração com Outras IDEs**: Mesmo no plano grátis, é possível trabalhar sincronamente com o Overleaf e seu editor local de preferência (ver seção anterior).
    - **Rich Text**: O usuário tem a opção de usar um editor na forma [WYSIWYG](https://en.wikipedia.org/wiki/WYSIWYG). Útil para editar tabelas e outros elementos visuais do texto.

---

## Dicas

- Mantenha a consistência na formatação e estilo ao longo do documento.
- Revise o documento para garantir que todas as seções estejam completas e bem estruturadas.
- Utilize ferramentas de revisão de texto para corrigir erros gramaticais e ortográficos.
- Ao compilar localmente, execute o compilador **duas vezes** para garantir o posicionamento correto da capa.

## Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para abrir issues e enviar pull requests — tanto para o template em geral quanto para eventuais ajustes na capa conforme o modelo institucional evolua.

## Créditos

Template original desenvolvido por [gabs-acc](https://github.com/gabs-acc/inspertex). Este fork adiciona suporte ao novo modelo de capa exigido pelo Insper.

## Licença

Este projeto está licenciado sob a licença MIT. Veja o arquivo `LICENSE` para mais detalhes.
