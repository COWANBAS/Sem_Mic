# BLOQUEAR MICROFONE

"Sobrescrita Função getUserMedia"

O script sobrescreve a função "getUserMedia" do objeto "navigator.mediaDevices", função "getUserMedia" é usada pelos sites para solicitar acesso a dispositivos de mídia, como o microfone e a câmera.

![image](https://github.com/user-attachments/assets/8c65e2c2-9f31-4432-80a8-07fc2b2ecd6a)

"Verificar a Restrições de Áudio"

O script verifica se as restrições "constraints" incluem audio, Se o audio estiver presente, a promessa é rejeitada com o erro "Acesso negado", se audio não estiver presente, o script permite o acesso à mídia solicitada, chamando a função original "getUserMedia"

![image](https://github.com/user-attachments/assets/2b45b016-8e08-44c7-8240-0baec43f4bf8)

"Salvando a Função Original"

A função original "getUserMedia" é salva em "navigator.mediaDevices.originalGetUserMedia" para que possa ser usada para outras mídias, como vídeo.

![image](https://github.com/user-attachments/assets/50d5cb30-04b6-4dfa-b09d-f3bd3f0dc834)

# BENEFICIOS

* Privacidade: Impede que sites acessem o microfone do usuário sem permissão explícita, aumentando a privacidade.

* Segurança: Reduz o risco de espionagem ou gravação não autorizada através do microfone.

* Controle: Dá ao usuário mais controle sobre quais sites podem acessar seu microfone.

* Flexibilidade: Permite exceções, como no caso de discord.com, onde o acesso ao microfone ainda é permitido.

Este script é útil para usuários preocupados com a privacidade e segurança de seus dispositivos, garantindo que apenas sites confiáveis possam acessar o microfone.
