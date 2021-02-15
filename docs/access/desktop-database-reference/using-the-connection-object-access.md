---
title: Using the Connection Object (Access)
TOCTitle: Using the Connection Object
ms:assetid: e8786411-2be4-8d75-9df7-e345d5a6a7e8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250177(v=office.15)
ms:contentKeyID: 48548423
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d16b802140e2dcbbd85988bee316ae27236c3235
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305924"
---
# <a name="using-the-connection-object-access"></a>Использование объекта Connection (Access)


**Область применения**: Access 2013, Office 2013

Объект **Connection** представляет уникальный сеанс с источником данных. В случае системы базы данных клиента или сервера она может быть эквивалентна фактическому сетевому подключению к серверу. В зависимости от функций, поддерживаемых поставщиком, некоторые коллекции, методы или свойства объекта **Connection** могут быть недоступны.

Перед открытием **объекта Connection** необходимо определить определенные сведения об источнике данных и типе подключения. Параметр *ConnectionString* метода **Connection** object **Open** (или свойство **ConnectionString** в объекте **Connection)** обычно содержит большую часть этих сведений. Строка подключения — это строка символов, которая определяет переменное число аргументов. Аргументы ( некоторые из них необходимы для ADO, но другие для конкретного поставщика) содержат сведения, которые объект **Connection** должен должен выполнять свою работу. Аргументы, которые составляют параметр *ConnectionString,* разделяются с заданными точками (;).

> [!NOTE]
> В строке подключения можно также указать имя источника данных ODBC (DSN) или файл ссылки на данные (UDL). Дополнительные сведения о DSNs см. в части 1 справочника программиста *ODBC.* Дополнительные сведения о UDLs см. в обзоре API ссылок на данные в справочнике *программиста OLE DB.*

В этой статье содержатся следующие разделы:

- [Создание строки подключения](creating-the-connection-string.md)
- [Управление транзакциями](controlling-transactions.md)
