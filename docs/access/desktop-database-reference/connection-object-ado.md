---
title: Connection object (ADO)
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
# <a name="connection-object-ado"></a>Connection object (ADO)

**Область применения**: Access 2013, Office 2013

Представляет открытое подключение к источнику данных.

## <a name="remarks"></a>Заметки

Объект **Connection** представляет уникальный сеанс с источником данных. В случае системы базы данных клиента или сервера она может быть эквивалентна фактическому сетевому подключению к серверу. В зависимости от функций, поддерживаемых поставщиком, некоторые коллекции, методы или свойства объекта **Connection** могут быть недоступны.

С помощью коллекций, методов и свойств объекта **Connection** можно сделать следующее:

  - Настройте подключение перед его открытием со [свойствами ConnectionString,](connectionstring-property-ado.md) [ConnectionTimeout](connectiontimeout-property-ado.md)и [Mode.](mode-property-ado.md) **ConnectionString** — это свойство по умолчанию объекта **Connection.**

  - Установите для [свойства CursorLocation](cursorlocation-property-ado.md) клиент, чтобы вызвать службу [курсоров Майкрософт для OLE DB,](microsoft-cursor-service-for-ole-db-ado-service-component.md)которая поддерживает пакетные обновления.

  - Установите базу данных по умолчанию для подключения со [свойством DefaultDatabase.](defaultdatabase-property-ado.md)

  - Установите уровень изоляции для транзакций, открытых при под соединении со свойством [IsolationLevel.](isolationlevel-property-ado.md)

  - Укажите поставщика OLE DB со [свойством Provider.](provider-property-ado.md)

  - Установить и затем разорвать физическое подключение к источнику данных с помощью методов [Open](open-method-ado-connection.md) и [Close.](close-method-ado.md)

  - Выполните команду для подключения к методу [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) и настройте выполнение с помощью свойства [CommandTimeout.](commandtimeout-property-ado.md)
    
    > [!NOTE]
    > Чтобы выполнить запрос без использования объекта Command, передайте строку запроса **методу Execute** объекта **Connection.** Однако объект [Command](command-object-ado.md) необходим, если необходимо сохранить текст команды и выполнить его повторно, или использовать параметры запроса.

  - Управляйте транзакциями открытого подключения, включая вложенные транзакции, если поставщик их поддерживает, с помощью методов [BeginTrans,](begintrans-committrans-and-rollbacktrans-methods-ado.md) [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md)и [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) и свойства [Attributes.](attributes-property-ado.md)

  - Проверьте ошибки, возвращенные из источника данных с [коллекцией ошибок.](errors-collection-ado.md)

  - Прочитайте версию из реализации ADO, используемой со [свойством Version.](version-property-ado.md)

  - Получите сведения о схеме базы данных с помощью метода [OpenSchema.](openschema-method-ado.md)

Объекты **Connection** можно создавать независимо от любого другого ранее определенного объекта.

Можно выполнять команды или хранимые процедуры, как если бы они были методами в **объекте Connection,** как показано ниже.

### <a name="execute-a-command-as-a-native-method-of-a-connection-object"></a>Выполнение команды в качестве нативного метода объекта Connection

Чтобы выполнить команду, придать команде имя с помощью свойства **Command** object [Name.](name-property-ado.md) Установите **подключение** к свойству **ActiveConnection** объекта Command. Затем выдают заявление, в котором имя команды используется так, как если бы это был метод объекта **Connection,** за которым следуют любые параметры, а затем объект **Recordset,** если возвращаются какие-либо строки. Настройте **свойства Набора** записей, чтобы настроить итоговую **настройку набора записей.** Например:

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

### <a name="execute-a-stored-procedure-as-a-native-method-of-a-connection-object"></a>Выполнение хранимой процедуры в качестве метода объекта Connection

Чтобы выполнить хранимую процедуру, выдают заявление, в котором имя хранимой процедуры используется так, как если бы это был метод объекта **Connection,** за которым следуют любые параметры. ADO сделает "лучшее предположение" о типах параметров. Пример:

```vb
    Dim cnn As New ADODB.Connection
    ...
    'Your stored procedure name and any parameters.
    cnn.sp_yourStoredProcedureName "parameter"
```
