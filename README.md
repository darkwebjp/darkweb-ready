# darkweb-ready
About KALI LINUX all the project 
About packaging with GitHub Actions
Dans cet article
Empaquetage dans des workflows d’intégration continue
Workflows pour la publication de packages
Pour aller plus loin
Vous pouvez configurer des workflows dans GitHub Actions pour produire des packages et les charger sur le GitHub Packages ou un autre fournisseur d’hébergement de packages.
Empaquetage dans des workflows d’intégration continue

Une étape d’empaquetage est une partie courante d’un workflow d’intégration continue ou de livraison continue. La création d’un package à la fin d’un workflow d’intégration continue peut vous aider pendant les révisions de code sur une demande de tirage.

Après avoir généré et testé votre code, une étape d’empaquetage peut produire un artefact exécutable ou déployable. Selon le type d’application que vous créez, ce package peut être téléchargé localement pour des tests manuels, mis à la disposition des utilisateurs au téléchargement ou déployé dans un environnement intermédiaire ou de production.

Par exemple, un workflow d’intégration continue pour un projet Java peut exécuter mvn package pour produire un fichier JAR. Ou un workflow CI pour une application Node.js peut créer un conteneur Docker.

À présent, lors de l’examen d’une demande de tirage, vous pourrez examiner l’exécution du workflow et télécharger l’artefact qui a été généré.

Capture d’écran de la section « Artefacts » d’une exécution de workflow. Le nom de l’artefact généré par l’exécution, « artefact », est mis en évidence avec un encadré orange foncé.

Cela vous permet d’exécuter le code dans la demande de tirage sur votre ordinateur, ce qui peut vous aider à déboguer ou à tester la demande de tirage.

Workflows pour la publication de packages

En plus de charger des artefacts d’empaquetage à des fins de test dans un workflow d’intégration continue, vous pouvez créer des workflows qui créent votre projet et publient des packages dans un registre de packages.

Publier des packages sur GitHub Packages GitHub Packages peut servir de service d’hébergement de package pour de nombreux types de packages. Vous pouvez choisir de partager vos packages avec l’ensemble de GitHub, ou des packages privés à partager avec des collaborateurs ou une organisation. Pour plus d’informations, consultez « Présentation de GitHub Packages ».

Vous pouvez publier des packages sur GitHub Packages lors de chaque envoi (push) dans la branche par défaut. Cela permettra aux développeurs de votre projet de toujours pouvoir exécuter et tester facilement la dernière build à partir de la branche par défaut, en l’installant à partir de GitHub Packages.

Publier des packages dans un registre de packages Pour de nombreux projets, la publication dans un registre de packages est effectuée chaque fois qu’une nouvelle version d’un projet est publiée. Par exemple, un projet qui produit un fichier JAR peut charger de nouvelles versions dans le référentiel Maven Central. Ou un projet .NET peut produire un package nuget et le charger dans la galerie NuGet.

Vous pouvez automatiser cela en créant un workflow qui publie des packages dans un registre de packages lors de chaque création de mise en production. Pour plus d’informations, consultez « Gestion des mises en production dans un référentiel ».

Pour aller plus loin

« Publication de packages Node.js »
Appuyez sur Alt + up pour activer
Aide et support
Ce document vous a-t-il aidé ?
