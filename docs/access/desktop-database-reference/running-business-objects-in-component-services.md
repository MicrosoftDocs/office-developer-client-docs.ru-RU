---
title: Running Business Objects in Component Services
TOCTitle: Running Business Objects in Component Services
ms:assetid: 12103458-b1dd-10fc-37e8-883fd6c6b9d1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248893(v=office.15)
ms:contentKeyID: 48543328
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 41424fd62e915ecb2d54fdb49c939b788f458804
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480979"
---
# <a name="running-business-objects-in-component-services"></a>Running Business Objects in Component Services


**Применимо к**: Access 2013 | Office 2013

Бизнес-объекты могут быть исполняемых файлов (.exe) или библиотеки динамической компоновки (DLL). Конфигурации, используемые для выполнения бизнес-объекта зависит от объекта .dll или .exe файла:

  - Бизнес-объекты, как файлы .exe можно вызвать через DCOM. Если эти бизнес-объекты используются через Internet Information Services (IIS), они могут быть marshalingof дополнительные данные, что приводит к снижению производительности клиента.

  - Бизнес-объекты, как DLL-файлы можно использовать с помощью служб IIS (и, следовательно, HTTP). Они могут также использоваться через DCOM только с помощью службы компонентов (или сервера транзакций, если вы используете Windows NT). Бизнес-объект библиотеки DLL, необходимо зарегистрировать на компьютере сервера IIS для предоставления специальных возможностей с помощью служб IIS. (Для действий по настройке DLL для запуска на DCOM, обратитесь к разделу «[Включение DLL выполнить на DCOM](enabling-a-dll-to-run-on-dcom.md).»)


> [!NOTE]
> <P>При реализации бизнес-объекты на среднем уровне как компоненты службы компонентов (с помощью <STRONG>GetObjectContext</STRONG>, <STRONG>SetComplete</STRONG>и <STRONG>SetAbort</STRONG>), они могут использовать службы компонентов (или MTS, если вы используете Windows NT) контекст объектов сохранение их состояния между нескольких клиентских вызовов. Этот сценарий можно с помощью DCOM, который обычно реализуются между доверенных клиентов и серверов (интрасеть). В данном случае <A href="dataspace-object-rds.md">RDS. Пространства данных</A> объект и метод <A href="createobject-method-rds.md">CreateObject</A> на стороне клиента, заменяются объект context транзакций и <STRONG>CreateInstance</STRONG> метод (интерфейс <STRONG>ITransactionContext</STRONG> ), реализованные с помощью службы компонентов.</P>


