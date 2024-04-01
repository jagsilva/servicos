Exemplo de como criar um serviço em linux
  sudo nano /etc/systemd/system/js_servico_faz_qq_coisa.service

conteudo do ficheiro:
'''
  [Unit]
  Description=Meu serviço Python
  
  [Service]
  Type=simple
  ExecStart=/usr/bin/python3 /home/pi/js_meu_script.py
  
  [Install]
  WantedBy=multi-user.target
'''
O conteudo deste ficheiro pode ser um dos exemplos em cima. Este deverá ser o mais simples.

Recarregar os serviços:
  sudo systemctl daemon-reload

Habilitar o serviço
  sudo systemctl enable js_servico_faz_qq_coisa.service

Arrancar o serviço
 sudo systemctl start js_servico_faz_qq_coisa.service

Estado do serviço
  sudo systemctl status js_servico_faz_qq_coisa.service

Parar o serviço
  sudo systemctl stop js_servico_faz_qq_coisa.service


