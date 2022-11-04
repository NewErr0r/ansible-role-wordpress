<h1>Автоматизация развёртывания платформы Wordpress</h1>

<p>
    <strong>Шаг 1. </strong> Создание playbook для запуска роли
</p>
<p><i>Пример:</i></p>

    ---
    - name: Deploy wordpress
      hosts: all 
      become: true 

      roles: 
        - ansible-role-wordpress

<p>
 <strong>Шаг 2. </strong> Склонировать роль в дирректорию с playbook:
</p>

  <pre>git clone https://github.com/NewErr0r/ansible-role-wordpress.gitt</pre>

<p>
    <strong>Шаг 3.</strong> Запустить playbook для развёртывания платформы wordpress:
</p>
  
  <pre>ansible-playbook -i inventory playbook.yaml</pre>
