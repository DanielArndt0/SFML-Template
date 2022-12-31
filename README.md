
# Dependências adicionais

## Debug:

> sfml-graphics-d.lib; sfml-window-d.lib; sfml-system-d.lib; sfml-audio-d.lib;

## Release:

> winmm.lib; opengl32.lib; freetype.lib; sfml-graphics-s.lib; sfml-window-s.lib; sfml-system-s.lib; sfml-audio-s.lib;

# Debug Enviroment:

> PATH=(SFML FOLDER)


# Problemas/Soluções:
Tente novamente com um projeto totalmente novo.

Configure um caminho para seu .dll para sua versão de depuração em Depuração. Você tem que fazer isso para TODOS os projetos.

Certifique-se de selecionar as configurações corretas antes de tentar fazer alterações nas propriedades do projeto.

Certifique-se de usar o sufixo -s para lançamento e -d para depuração.

Sempre aplique as alterações antes de mudar a configuração ou fechar a janela.

Sua versão do SFML pode ter um layout diferente da minha, edite seus caminhos de acordo.

# Exemplo de código:
```
#include  "SFML/Graphics.hpp"

int main()
{
   sf::RenderWindow window(sf::VideoMode(800, 600), "SFML");
 
   sf::Event event;
 
   while (window.isOpen()) {
 
      while (window.pollEvent(event)) {
 
         if (event.type == sf::Event::Closed) {
 
            window.close();
         }
      }
   }
   return 0;
}
```
