Dans le cadre de ma deuxième année de Master Mathématiques, Finance computationnelle, Actuariat, j’ai suivi un enseignement sur la blockchain, l’enseignant m’a, dans le cadre de ce cours, posé la question suivante : "*L'utilisation d'une blockchain comme Ethereum est très différente de celle de la blockchain Hive. Contrastez l'expérience utilisateur de ces deux blockchain en comparant la façon de gérer les noms d'utilisateur, l'authentification, la possibilité (ou pas) de récupérer un mot de passe perdu, etc."

Voici la réponse donnée par ChatGPT:

>Bien sûr, je peux vous aider à comparer l'expérience utilisateur entre Ethereum et Hive en ce qui concerne la gestion des noms d'utilisateur, l'authentification et la récupération de mot de passe perdu.

1. **Noms d'utilisateur**:
    
    - **Ethereum**: Sur Ethereum, les adresses sont souvent utilisées comme identifiants, ce qui signifie que les utilisateurs doivent se souvenir de longues chaînes de caractères hexadécimaux ou QR codes pour s'identifier. Les noms d'utilisateur peuvent être gérés par des services tiers, mais ne sont pas nativement pris en charge par le protocole Ethereum.
    - **Hive**: Hive permet l'utilisation de noms d'utilisateur qui sont plus conviviaux et faciles à mémoriser. Les utilisateurs peuvent choisir leur propre nom d'utilisateur lors de la création de leur compte.
2. **Authentification**:
    
    - **Ethereum**: L'authentification sur Ethereum se fait généralement à l'aide de clés privées. Les utilisateurs doivent garder en sécurité leur clé privée pour accéder à leurs fonds ou effectuer des transactions. Il existe des portefeuilles logiciels et matériel pour faciliter cette gestion.
    - **Hive**: Hive utilise également des clés privées pour l'authentification, mais il existe une variété de méthodes d'authentification, y compris l'utilisation de clés de récupération, ce qui rend le processus un peu plus flexible.
3. **Récupération de mot de passe perdu**:
    
    - **Ethereum**: En cas de perte de mot de passe ou de clé privée sur Ethereum, il est généralement difficile voire impossible de récupérer l'accès aux fonds ou à d'autres ressources. Les utilisateurs doivent prendre des mesures de sécurité appropriées pour éviter la perte de leurs clés.
    - **Hive**: Hive propose un processus de récupération de compte qui permet aux utilisateurs de définir des clés de récupération. En cas de perte de mot de passe, les utilisateurs peuvent utiliser leurs clés de récupération pour restaurer l'accès à leur compte.

>En résumé, Hive offre une expérience utilisateur plus conviviale en fournissant des noms d'utilisateur et des options de récupération de compte plus simples par rapport à Ethereum, qui se concentre davantage sur la sécurité et la décentralisation, au détriment parfois de la convivialité.


# Noms d'utilisateurs 

D'après la réponse de ChatGPT : 
>**Ethereum**: Sur Ethereum, les adresses sont souvent utilisées comme identifiants, ce qui signifie que les utilisateurs doivent se souvenir de longues chaînes de caractères hexadécimaux ou QR codes pour s'identifier. Les noms d'utilisateur peuvent être gérés par des services tiers, mais ne sont pas nativement pris en charge par le protocole Ethereum.

En effet, sur la blockchain même, les noms d'utilisateurs ne sont pas choisis par les utilisateurs, et ces derniers sont représentés par des adresses hexadécimales.

![[Pasted image 20240425150627.png]]
*Les "noms d'utilisateurs" ne sont rien de plus que des chaines de caractères apparemment aléatoires, complexes et effectivement compliquées à retenir, image fournie par [Etherscan](https://etherscan.io/)*


>**Hive**: Hive permet l'utilisation de noms d'utilisateur qui sont plus conviviaux et faciles à mémoriser. Les utilisateurs peuvent choisir leur propre nom d'utilisateur lors de la création de leur compte.

La blockchain Hive permet bel et bien de directement choisir un pseudonyme, qui apparaîtra sur les transactions de la blockchain.
![[Pasted image 20240425153911.png]]
*comme on peut le constater, les utilisateurs (ici @pboulet et @mbrn2023mfca ) sont identifiés grâce à leur pseudonyme, via [HiveExplorer](https://hivexplorer.com/)*
# Authentification

>**Ethereum**: L'authentification sur Ethereum se fait généralement à l'aide de clés privées. Les utilisateurs doivent garder en sécurité leur clé privée pour accéder à leurs fonds ou effectuer des transactions. Il existe des portefeuilles logiciels et matériel pour faciliter cette gestion.

Il existe deux types de comptes sur la blockchain Ethereum : les comptes utilisateurs (externally-owned accounts, ou EOA), et les comptes contrat, gérés par des smart contracts, pour la suite de l'article, nous nous concentrerons sur les comptes utilisateurs. 

Lorsque l'on crée un "compte" sur la blockchain Ethereum en utilisant un wallet (une application qui permet de créer et de gérer un compte Ethereum), il nous est fourni une clé publique ainsi qu'une clé privée,  ce qui permettra l'échange de transactions sur la blockchain avec le même fonctionnement général qu'un échange de message sur un protocole de cryptage traditionnel, par exemple.

![[Pasted image 20240427122000.png]]
*Alice utilise sa clé publique pour crypter l'ordre d'envoi d'un token à Jimmy, et Ethereum (l'EVM Ethereum) décrypte l'ordre d'Alice avec sa clé publique pour exécuter le contrat, via [Medium](https://medium.com/@colin_71603/asymmetric-cryptography-on-the-ethereum-blockchain-961e2c2017a1)*


Pour Hive, le procédé est un peu plus complexe

>**Hive**: Hive utilise également des clés privées pour l'authentification, mais il existe une variété de méthodes d'authentification, y compris l'utilisation de clés de récupération, ce qui rend le processus un peu plus flexible.

Lors de la création d'un compte Hive, 4 clés privées sont fournies à l'utilisateur, qui sont, dans l'ordre croissant des permissions  :
- Une Posting Key, qui permet les intéractions dans les réseaux sociaux de la blockchain, elle permet donc de commenter, de voter, de *follow* ou encore de poster des articles.
- Une Active Key, qui en plus de détenir les permissions de la Posting Key, permet entre autres les actions monétaires, comme les transferts de token, ou la conversion en HBD, 
- Une Owner Key, qui permet entre autres de modifier les autres clés privées ou encore de récuperer son compte Hive en cas de perte du mot de passe.


![[Pasted image 20240427125608.png]]
*La hiérarchie des permissions des clés privées Hive, via [wallet.hive.blog](https://wallet.hive.blog/@yourusername/permissions)*


La dernière clé est la Memo Key, qui permet de décrypter et d'encrypter des messages envoyés à travers la blockchain Hive, mais son utilisation dans les dApps reste marginale.

# Récupération des mots de passe perdus 

 >**Ethereum**: En cas de perte de mot de passe ou de clé privée sur Ethereum, il est généralement difficile voire impossible de récupérer l'accès aux fonds ou à d'autres ressources. Les utilisateurs doivent prendre des mesures de sécurité appropriées pour éviter la perte de leurs clés.

En effet, lors d'une perte de clé privée sur la blockchain Ethereum, il est impossible de la récupérer si l'on n'utilise pas une application tierce, c'est pourquoi il est recommandé d'utiliser un *wallet* pour la gestion du compte Ethereum, comme par exemple Rainbow, qui permet l'authentification via un mot de passe, et permet à un utilisateur ayant perdu ses identifiants la récupération de son compte via des *recovery phrases*, une liste de mots à conserver précieusement permettant le rétablissement d'un compte Ethereum. 

>**Hive**: Hive propose un processus de récupération de compte qui permet aux utilisateurs de définir des clés de récupération. En cas de perte de mot de passe, les utilisateurs peuvent utiliser leurs clés de récupération pour restaurer l'accès à leur compte.

Hive permet nativement, via un compte dis de récupération détenu par une personne de confiance, de restituer un compte et ses clés à un utilisateur qui aurait égaré ses identifiants ou subi un vol, le processus de récupération est détaillé dans cet article : [Hive Account Recovery - Guide de l'utilisateur | PeakD](https://peakd.com/hive/@hive.recovery/userguide-fr).

# Frais de transactions

Un autre point, non mentionné par ChatGPT, est celui des frais de transactions, là encore, les fonctionnements des blockchains Ethereum et Hive diffèrent radicalement.

![[Pasted image 20240428143103.png]]

Pour la blockchain Ethereum, les frais de transactions (qui sont variables de jour en jour) sont appelé *gas*, ou essence, et sont requis pour toutes les opérations sur la blockchain, ces frais sont généralement calculés en *gwei*, ou $10^{-9}$ ETH, ce *gas* est utilisé pour payer les mineurs. Les utilisateurs peuvent aussi payer un *tip* (pourboire), afin de voir leurs transactions traitées plus rapidement.

Pour ce qui est de la blockchain Hive, le fonctionnement est encore une fois un peu plus compliqué. 

Les utilisateurs disposent de *resource credits* (souvent abrégés en RC), qui sont dépensés lors de la réalisation des diverses transactions sur la blockchain Hive, ces RC sont plafonnés et régénérés automatiquement, à hauteur de ~20% du total par jour, un utilisateur peut donc intéragir avec la blockchain sans y avoir investi financièrement.

Si l'on souhaite disposer de plus de RC, il faut détenir du Hive Power (HP) en *stakant* des Hive (la cryptomonnaie de la blockchain Hive), ou en en gagnant lorsqu'un poste que l'on a écrit recoit des *upvotes*, par exemple. On peut aussi s'en voir délégué par un autre utilisateur de la communauté, cela permettra un plus grand nombre de transactions par jour. 

