---
title: fast build your own Blog website in 30 minutes ��hexo && github pages��
date: 2016-09-19 14:48:05
tags: initBlog
author: AppariTT
---

### mac�������ã�windows ���ܲ������ã�

    1.�Ȱ�װ node.js, ���������� https://nodejs.org/en/��
    2.�ٰ�װ git�� ���������� https://git-scm.com/���� �����xcode �������˲��ˣ�

### ��װ hexo�� �ٽ��б��ػ�����������
    
    ��������������������������
    1.$ npm install -g hexo-cli --no-optional
    �˰�װΪĬ��λ�ã� ��������Ե���hexo��λ��
    2.$ cd ������Ҫ���ļ���·�� 
    3.$ hexo init  ����ת�ƸղŰ�װ��hexo �����·��
    4.$ npm install �����������
       
    Ȼ�����˵�Ѿ����1/2�ˡ�����
    �������ǲ����Ѿ����ɲ����ˣ�
    a. hexo g ���ǳ������� ��ʾ����Դ�ļ��������ݵ�ָ���ĵط��� һ��������ݶ���Ҫ���д˲���
    b. hexo s �����ڱ��ز���blog�� �����һ����ַ Ϊ http://localhost:4000/ , ������� hexoҳ����Ϊ�ɹ��ˣ� ���û�п����Ļ�����Ҫ�����֮ǰ����һ����©��
    
### github pages ���ã� ���������ͱ�����github�ϣ� �������ܹ����ʵ� Ĭ�ϸ�������Ϊ �û���.github.io
    
    #### ��½���github�ʺ� ��û�н���ע��
    #### ����һ������⣨repository�� ����Ϊ��� [�û���.github.io]
    #### ��һ����Ҫ�������Ե� SSH��Կ �� Account settings -> SSH Keys -> Add SSH Key
       ##### ��λ�ȡ��Կ�أ���������ϸϸ���� 
       ###### git config --global user.email "��ĵ�½����"
       ###### git config --global user.name "����û���" 
       ###### ssh-keygen -t rsa -C "��ĵ�½����" ���ɹ�Կ
              
              ��������������ʾ��Ҫ������Ҫ������Կ��·���� ֱ�ӻس���Ĭ��λ�����ɣ��Ժ������ʾ

Generating public/private rsa key pair.
Enter file in which to save the key (//.ssh/id_rsa): 

���������ʱ�� �Լ����ø����� ����֮�������ʹ��
Enter passphrase (empty for no passphrase):
Enter same passphrase again:

֮�����ֹ�Կ��λ��

Your public key has been saved in xxx\xxx\ssh.pub.

������һ��·����finder�ҵ��ļ�λ�� ȡ������  ����ֱ�� vim xxx\xxx\ssh.pub. Ȼ����ȫ��������

       ###### �����github�����ҵ� Account settings -> SSH Keys -> Add SSH Key����ӳɹ���
    #### Ȼ�����һ��hexo �������ļ� ����֪������Ҫ��Դ�ļ��������ĸ�github����
       ###### �����û�и���֮ǰ��������λ�õĻ� ֱ��vim _config.yml Ȼ������������������������,��Ҫ���һ���ո����ɾ��һ���ո�

deploy:
  type: github      
  repository: git@github.com:�û���/�û���.github.io.git
  branch: master 


       ###### hexo d -g ��������˼Ϊ�������ݲ����ֵ��ղ���Ŀ��У� Ȼ����ʾ��github page�У� ����Ϊ�� �û���.github.io �� Ȼ����˾���ͨ��������������blog���з�����
   

 
##oke�� ���˴󹦸�ɣ��� �·����� �� ����ĸ����� ֮����˵�ɣ�








