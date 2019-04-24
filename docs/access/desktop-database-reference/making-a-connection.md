---
title: Создание подключения
TOCTitle: Making a connection
ms:assetid: 188f6794-f4ec-8e8d-5adc-bdee36f4c9ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248932(v=office.15)
ms:contentKeyID: 48543472
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 487212acd8847928e1fab405593edb172d0172d0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289786"
---
# <a name="making-a-connection"></a>Создание подключения

**Область применения**: Access 2013, Office 2013

Чтобы подключиться к источнику данных, необходимо указать *строку подключения*, параметры, которые могут отличаться для каждого поставщика и источника данных. Дополнительные сведения см. [в разделе Создание строки подключения](creating-the-connection-string.md).

ADO чаще всего открывает подключение с помощью метода **Open** объекта **Connection** . Синтаксис метода **Open** показан ниже:

```vb
Dim connection as New ADODB.Connection 
connection.Open ConnectionString, UserID, Password, OpenOptions
```

Кроме того, вы можете вызвать метод ярлыка, **Recordset. Open**, чтобы открыть неявное подключение и выдать команду на это подключение в одной операции. Для этого необходимо передать допустимую строку подключения в качестве аргумента *ActiveConnection* в метод **Open** . Ниже приведен синтаксис для каждого метода в Visual Basic:

```vb
Dim recordset as ADODB.Recordset 
Set recordset = New ADODB.Recordset 
recordset.Open Source, ActiveConnection, CursorType, LockType, Options
```

> [!NOTE]
> Когда следует использовать объект **Connection** и с ярлыком **Recordset. Open** ? Используйте объект **Connection** , если вы планируете открыть более одного **набора записей**или при выполнении нескольких команд. Подключение по-прежнему создается неявным образом с помощью ADO при использовании ярлыка **Recordset. Open** .


