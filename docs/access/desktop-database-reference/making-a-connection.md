---
title: Создание подключения
TOCTitle: Making a Connection
ms:assetid: 188f6794-f4ec-8e8d-5adc-bdee36f4c9ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248932(v=office.15)
ms:contentKeyID: 48543472
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7bd99419a841a8fa876dd0ad30b4d06360a27df1
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882051"
---
# <a name="making-a-connection"></a>Создание подключения

**Применимо к**: Access 2013, Office 2013

Для подключения к источнику данных, необходимо указать *строку подключения*, параметры которого может отличаться для каждого поставщика и источника данных. [Строка подключения](creating-the-connection-string.md)для получения дополнительных сведений см.

Чаще всего ADO открывает подключение с помощью метода **Open** объект **подключения** . Синтаксис метода **Open** показано ниже:

```vb
Dim connection as New ADODB.Connection 
connection.Open ConnectionString, UserID, Password, OpenOptions
```

Кроме того можно вызвать метод ярлык, **Recordset.Open**, для открытия неявные соединения и команды через это подключение за одну операцию. Это сделать, передав в качестве аргумента *ActiveConnection* метода **Open** в это допустимая строка подключения. Ниже приведен синтаксис для каждого метода в Visual Basic.

```vb
Dim recordset as ADODB.Recordset 
Set recordset = New ADODB.Recordset 
recordset.Open Source, ActiveConnection, CursorType, LockType, Options
```

> [!NOTE]
> Когда следует использовать объект **подключения** и ярлык **Recordset.Open** ? Используйте объект **подключения** , если планируется открыть более одного **набора записей**или при выполнении нескольких команд. Подключение по-прежнему создается путем ADO неявно при использовании сочетания **Recordset.Open** .


