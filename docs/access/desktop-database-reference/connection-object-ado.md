---
title: Объект Connection (ADO)
TOCTitle: Connection object (ADO)
ms:assetid: c16023aa-0321-2513-ee71-255d6ffba03d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249940(v=office.15)
ms:contentKeyID: 48547528
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231105
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: ed736a0e52ff45cd0fed63f1ba5bd7060d7a2380
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295879"
---
# <a name="connection-object-ado"></a>Объект Connection (ADO)

**Область применения**: Access 2013, Office 2013

Представляет открытое подключение к источнику данных.

## <a name="remarks"></a>Замечания

Объект **Connection** представляет уникальный сеанс с источником данных. В случае клиент-серверной системы базы данных она может быть эквивалентна фактическому сетевому подключению к серверу. В зависимости от функциональных возможностей, поддерживаемых поставщиком, некоторые коллекции, методы или свойства объекта **Connection** могут быть недоступны.

С помощью коллекций, методов и свойств объекта **Connection** можно выполнить следующие действия:

  - Настройте подключение перед его открытием с помощью свойств [ConnectionString](connectionstring-property-ado.md), [ConnectionTimeout](connectiontimeout-property-ado.md)и [mode](mode-property-ado.md) . **ConnectionString** является свойством по умолчанию для объекта **Connection** .

  - Задайте для свойства [CursorLocation](cursorlocation-property-ado.md) значение Client, чтобы вызвать [службу Microsoft Cursor для OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md), которая поддерживает пакетное обновление.

  - Задайте базу данных по умолчанию для подключения с помощью свойства [DefaultDatabase](defaultdatabase-property-ado.md) .

  - Задайте уровень изоляции для транзакций, открытых в подключении, с помощью свойства [IsolationLevel](isolationlevel-property-ado.md) .

  - Укажите поставщика OLE DB с помощью свойства [provider](provider-property-ado.md) .

  - Установите и приостановите физическое подключение к источнику данных с помощью методов [Open](open-method-ado-connection.md) и [Close](close-method-ado.md) .

  - Выполните команду для подключения с помощью метода [EXECUTE](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) и настройте выполнение с помощью свойства [CommandTimeout](commandtimeout-property-ado.md) .
    
    > [!NOTE]
    > Чтобы выполнить запрос, не используя объект Command, передайте строку запроса в метод **EXECUTE** объекта **Connection** . Однако при необходимости сохранения текста команды и его повторного выполнения или использования параметров запроса требуется объект [Command](command-object-ado.md) .

  - Управление транзакциями в открытом подключении, включая вложенные транзакции, если поставщик поддерживает их, с помощью методов [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md), [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md)и [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) , а [](attributes-property-ado.md) также свойства Attributes.

  - Проверьте ошибки, возвращенные из источника данных, [](errors-collection-ado.md) с помощью коллекции Errors.

  - Считывание версии из реализации ADO, используемой со свойством [Version](version-property-ado.md) .

  - Получение сведений о схеме для базы данных с помощью метода [OpenSchema](openschema-method-ado.md) .

Вы можете создавать объекты **подключения** независимо от любого ранее определенного объекта.

Вы можете выполнять команды или хранимые процедуры, как если бы они были собственными методами объекта **Connection** , как показано ниже.

### <a name="execute-a-command-as-a-native-method-of-a-connection-object"></a>Выполнение команды в качестве собственного метода объекта подключения

Чтобы выполнить команду, присвойте команде имя, используя свойство [имя](name-property-ado.md) объекта **команды** . Задайте для подключения свойство **ActiveConnection** объекта **Command** . Затем вызовите оператор, где имя команды используется как метод для объекта **Connection** , за которым следуют все параметры, а затем — объект **Recordset** , если возвращаются какие-либо строки. Задайте свойствам **набора** записей для настройки результирующего **набора записей**. Пример:

```vb
    Dim cnn As New ADODB.Connection
    Dim cmd As New ADODB.Command
    Dim rst As New ADODB.Recordset
    ...
    cnn.Open "..."
    cmd.Name = "yourCommandName"
    cmd.ActiveConnection = cnn
    ...
    'Your command name, any parameters, and an optional Recordset.
    cnn.yourCommandName "parameter", rst
```

### <a name="execute-a-stored-procedure-as-a-native-method-of-a-connection-object"></a>Выполнение хранимой процедуры в качестве собственного метода объекта подключения

Чтобы выполнить хранимую процедуру, выполните инструкцию, в которой имя хранимой процедуры используется как метод для объекта **Connection** , за которым следуют все параметры. ADO будет делать "наилучшее предположение" для типов параметров. Пример:

```vb
    Dim cnn As New ADODB.Connection
    ...
    'Your stored procedure name and any parameters.
    cnn.sp_yourStoredProcedureName "parameter"
```
