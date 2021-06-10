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

Чтобы подключиться к источнику данных, необходимо указать строку *подключения,* параметры которой могут отличаться для каждого поставщика и источника данных. Дополнительные сведения см. в [строке Создание строки подключения.](creating-the-connection-string.md)

Чаще всего ADO открывает подключение с помощью метода **Open** объекта **Подключения.** Синтаксис метода **Open** показан здесь:

```vb
Dim connection as New ADODB.Connection 
connection.Open ConnectionString, UserID, Password, OpenOptions
```

Кроме того, вы можете вызвать метод ярлыка **Recordset.Open,** чтобы открыть неявное подключение и выдать команду над этим подключением в одной операции. Сделайте это, передав допустимую строку подключения в качестве аргумента *ActiveConnection* **методу Open.** Вот синтаксис для каждого метода в Visual Basic:

```vb
Dim recordset as ADODB.Recordset 
Set recordset = New ADODB.Recordset 
recordset.Open Source, ActiveConnection, CursorType, LockType, Options
```

> [!NOTE]
> Когда следует использовать объект **Подключения** против **ярлыка Recordset.Open?** Используйте объект **Подключение,** если планируется открыть несколько **наборов записей** или при выполнении нескольких команд. Подключение по-прежнему создается ADO неявно при использовании **ярлыка Recordset.Open.**


