---
title: Объект подключения (ADO)
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
# <a name="connection-object-ado"></a>Объект подключения (ADO)

**Область применения**: Access 2013, Office 2013

Представляет открытое подключение к источнику данных.

## <a name="remarks"></a>Примечания

Объект **Connection** представляет собой уникальный сеанс с источником данных. В случае системы клиентских и серверных баз данных она может быть эквивалентна фактическому сетевому подключению к серверу. В зависимости от функций, поддерживаемых поставщиком, некоторые коллекции, методы или свойства объекта **Подключения** могут быть недоступны.

С помощью коллекций, методов и свойств объекта **Connection** можно сделать следующее:

  - Настройте подключение перед открытием со свойствами [ConnectionString,](connectionstring-property-ado.md) [ConnectionTimeout](connectiontimeout-property-ado.md)и [Mode.](mode-property-ado.md) **ConnectionString —** это свойство подключения по **умолчанию.**

  - Установите свойство [CursorLocation](cursorlocation-property-ado.md) клиенту для вызова [службы Microsoft Cursor для OLE DB,](microsoft-cursor-service-for-ole-db-ado-service-component.md)которая поддерживает пакетные обновления.

  - Установите базу данных по умолчанию для подключения к [свойству DefaultDatabase.](defaultdatabase-property-ado.md)

  - Установите уровень изоляции для транзакций, открытых при подстройке к свойству [IsolationLevel.](isolationlevel-property-ado.md)

  - Укажите поставщика OLE DB с [свойством Provider.](provider-property-ado.md)

  - Установить физическое подключение к источнику данных с помощью методов [Open](open-method-ado-connection.md) и [Close.](close-method-ado.md)

  - Выполните команду по подключению к методу [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) и настройте выполнение с помощью [свойства CommandTimeout.](commandtimeout-property-ado.md)
    
    > [!NOTE]
    > Чтобы выполнить запрос без использования объекта Command, передайте строку запроса **методу Выполнения** объекта **Подключения.** Однако для [сохраняемого](command-object-ado.md) командного текста и его повторного выполнения или использования параметров запроса требуется объект Command.

  - Управление транзакциями на открытом подключении, включая вложенные транзакции, если поставщик поддерживает их, с помощью методов [BeginTrans,](begintrans-committrans-and-rollbacktrans-methods-ado.md) [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md)и [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) и свойства [Attributes.](attributes-property-ado.md)

  - Изучите ошибки, возвращаемые из источника данных с помощью коллекции [Ошибок.](errors-collection-ado.md)

  - Ознакомьтесь с версией из реализации ADO, используемой с [свойством Version.](version-property-ado.md)

  - Получение сведений о схеме базы данных с помощью [метода OpenSchema.](openschema-method-ado.md)

Объекты **Подключения можно** создавать независимо от любого другого ранее определенного объекта.

Можно выполнять команды или сохраненные процедуры так, как если бы они были родными методами на **объекте Подключение,** как показано ниже.

### <a name="execute-a-command-as-a-native-method-of-a-connection-object"></a>Выполните команду как родной метод объекта Подключения

Чтобы выполнить команду, дайте команде имя с помощью свойства **Command** object [Name.](name-property-ado.md) Установите **свойство** **ActiveConnection объекта Command** к подключению. Затем выдай заявление, в котором имя команды используется так, как если бы это был метод на объекте **Подключение,** а затем любые параметры, а затем объект **Recordset,** если какие-либо строки возвращаются. Установите свойства **Recordset** для настройки результативного **набора записей.** Пример.

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

### <a name="execute-a-stored-procedure-as-a-native-method-of-a-connection-object"></a>Выполнение сохраненной процедуры в качестве родного метода объекта Подключения

Чтобы выполнить сохраненную процедуру, выдай заявление, в котором сохраненное имя процедуры используется так, как если бы это был метод на объекте **Подключение,** за которым следуют любые параметры. ADO сделает "наилучшее предположение" типов параметров. Пример:

```vb
    Dim cnn As New ADODB.Connection
    ...
    'Your stored procedure name and any parameters.
    cnn.sp_yourStoredProcedureName "parameter"
```
