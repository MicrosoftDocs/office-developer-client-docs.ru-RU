---
title: Подготовка библиотеки DLL к работе в DCOM
TOCTitle: Enabling a DLL to run on DCOM
ms:assetid: b405f767-91f0-c869-d34e-7a953de49106
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249859(v=office.15)
ms:contentKeyID: 48547211
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b97f4e8050cf293621c7b7fc79437c89171d86fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293548"
---
# <a name="enabling-a-dll-to-run-on-dcom"></a>Подготовка библиотеки DLL к работе в DCOM


**Область применения**: Access 2013, Office 2013

В следующих действиях описано, как включить библиотеки динамических ссылок бизнес-объектов для использования DCOM и Microsoft IIS (HTTP) через компонентные службы.

1.  Создание нового пустого пакета в оснастке MMC component Services. Для создания пакета и добавления DLL в этот пакет используется оснастка MMC component Services. Это делает .dll доступным через DCOM, но удаляет доступность через IIS. (Если вы проверяете в реестре для .dll, ключ Inproc теперь пуст; настройка атрибута активации, объясняемая далее в этом разделе, добавляет значение в **ключе Inproc.)** 

2.  Установка бизнес-объекта в пакет. -or- Импорт объекта [RDSServer.DataFactory](datafactory-object-rdsserver.md) в пакет.

3.  Установите атрибут Активация пакета в **процессе** создания (приложение Library). Чтобы сделать .dll доступным с помощью DCOM и IIS на одном компьютере, необходимо установить атрибут активации компонента в оснастке MMC component Services. После набора атрибута в процессе создания вы заметите, что в реестр добавлен ключ сервера **Inproc,** который указывает на суррогатную .dll.

