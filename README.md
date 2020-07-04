# 『OUROBOROS』：ラズパイで作る！Kubernetesクラスターを基盤とした自宅プライベートクラウド構築プロジェクト


## 本プロジェクトの背景

本プロジェクトは、Kubernetesクラスターを構築し、そのクラスター上でAmazon EC2やGCEのような仮想マシンを動作させることができるある種のWebサービスである『はりぼてクラウドサービス』を提供するクラウドシステムが稼働する自宅プライベートクラウドを物理マシンにRaspberry Piを使用して構築に取り組んでいきます。

そしてこのプロジェクトの最終成果物として、プロジェクトを通して構築した自宅プライベートクラウド上で稼働する『はりぼてクラウドサービス』を提供するクラウドシステムを利用して、自分自身である自宅プライベートクラウドを構築してみたいと思います。

言い換えますとクラウド上にそのクラウド自身を構築することが可能な自己言及性のあるシステムの構築を目指します。

これは自宅プライベートクラウドの構築にInfrastructure as Codeを用いることで、構築されたクラウド上で自身を構築することができると考えています。

つまり、Ansibleのような構成管理ツールを使用してを構築されたK8sクラスター上でKubernetesマニュフェストファイルとして管理されているクラウドサービスを提供するクラウドシステムに対して、このシステムが提供するクラウドサービスを利用して構築された仮想マシン上にクラウドシステムを構成するこれらのコードを適用することで、クラウドシステム上に自分自身であるクラウドシステムを構築することが可能となるのです。

&nbsp;



## 本プロジェクトの目的
下記に本プロジェクトの目的を示します。

***物理マシンにRaspberry Piを使用して、Infrastructure as Codeを適用して構築したKubernetesクラスター上でAmazon EC2やGCEのような仮想マシンを動作させることができるある種のWebサービスである『はりぼてクラウドサービス』を提供するクラウドシステムを稼働させることができ、さらに、このクラウドシステム上にそのクラウドシステム自身を構築することが可能な自己言及性を持つシステムとして自宅プライベートクラウドの構築を行う。***

&nbsp;



## 本プロジェクトのおおまかな工程

1. Raspberry Piのセットアップと物理インフラの構築
2. Ansibleを用いたKubernetesクラスターの構築
3. KubernetesのチュートリアルとしてのWebサービス開発
4. 『はりぼてクラウドサービス』の開発とKubernetesクラスター上へのデプロイ
5. クラウドシステム上で稼働する『はりぼてクラウドサービス』を利用した、Kubernetesクラスターの構築
6. 『はりぼてクラウドサービス』をクラウドシステム上に構築したKubernetesクラスター上にデプロイ

&nbsp;

![Ouroboros](/images/ouroboros.png)



```
$ ansible --version
ansible 2.5.1
  config file = /etc/ansible/ansible.cfg
  configured module search path = [u'/home/taichi/.ansible/plugins/modules', u'/usr/share/ansible/plugins/modules']
  ansible python module location = /usr/lib/python2.7/dist-packages/ansible
  executable location = /usr/bin/ansible
  python version = 2.7.17 (default, Apr 15 2020, 17:20:14) [GCC 7.5.0]
```



&nbsp;
