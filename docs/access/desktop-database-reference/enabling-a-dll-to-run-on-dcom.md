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

Ниже описано, как включить библиотеки динамической связи бизнес-объектов для использования DCOM и Microsoft IIS (HTTP) через службы компонентов.

1.  Создайте пустой пакет в оснастке MMC "Службы компонентов". Для создания пакета и добавления DLL в этот пакет используется оснастка MMC "Службы компонентов". Это делает DLL-DLL доступным через DCOM, но удаляет их с помощью IIS. (Если вы зарегиструете реестр для DLL, ключ **Inproc** будет пустым. При установке атрибута Активация, как поясняется далее в этом разделе, добавляется значение в ключ **Inproc.)**

2.  Установите в пакет бизнес-объект. -or- Импортировать [объект RDSServer.DataFactory](datafactory-object-rdsserver.md) в пакет.

3.  Установите для атрибута Activation для пакета параметр **In the creator's process** (Library application). Чтобы сделать DLL-DLL доступным через DCOM и IIS на одном компьютере, необходимо установить атрибут активации компонента в оснастке MMC "Службы компонентов". После того как вы установите для атрибута значение In **the creator's process,** вы заметите, что в реестр добавлен ключ **inproc-сервера,** который указывает на заменяющие DLL службы компонентов.

