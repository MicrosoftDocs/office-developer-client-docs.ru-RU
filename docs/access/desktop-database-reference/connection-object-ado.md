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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718415"
---
# <a name="connection-object-ado"></a>Объект Connection (ADO)

**Применимо к**: Access 2013, Office 2013

Представляет открытое подключение к источнику данных.

## <a name="remarks"></a>Замечания

Объект **подключения** представляет собой уникальный сеанс с источником данных. В случае системы клиента и сервера базы данных может быть эквивалентен действительное сетевое подключение к серверу. В зависимости от функциональных возможностей, поддерживаемых поставщика, некоторые семейств сайтов, методов или свойств **подключения** объекта могут быть недоступны.

С помощью семейства сайтов, методы и свойства объекта **подключения** выполните следующее:

  - Настройка подключения к перед открытием с помощью свойства [ConnectionString](connectionstring-property-ado.md), [ConnectionTimeout](connectiontimeout-property-ado.md)и [режиме](mode-property-ado.md) . **ConnectionString** является свойством по умолчанию объекта **подключения** .

  - Присвойте свойству [CursorLocation](cursorlocation-property-ado.md) для клиента для вызова [Службы Microsoft курсора для OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md), которая поддерживает пакета обновления.

  - Настройка базы данных по умолчанию для подключения со свойством [DefaultDatabase](defaultdatabase-property-ado.md) .

  - Задайте уровень изоляции для транзакций, открытых на подключение с помощью свойства [IsolationLevel](isolationlevel-property-ado.md) .

  - Укажите поставщика OLE DB с помощью свойства [поставщика](provider-property-ado.md) .

  - Установить и более поздних версий приостановки выполнения, физическое подключение к источнику данных с помощью методов [открытия](open-method-ado-connection.md) и [закрытия](close-method-ado.md) .

  - Выполнить команду на подключение с помощью метода [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) и настройте выполнения со свойством [CommandTimeout](commandtimeout-property-ado.md) .
    
    > [!NOTE]
    > Для выполнения запроса без использования объекта команды, передайте строку запроса метода **Execute** объекта **подключения** . Тем не менее объект [команды](command-object-ado.md) является обязательным, когда необходимо сохранять текст команды и повторно выполнить или используйте параметры запроса.

  - Управление транзакций на открытое подключение, включая вложенные транзакции, если поставщик поддерживает их, с помощью [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md)и [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) методы и свойства [атрибутов](attributes-property-ado.md) .

  - Проверки на наличие ошибок, возвращаемых из источника данных с помощью семейства [Errors](errors-collection-ado.md) .

  - Прочитайте версию от реализации ADO используется совместно со свойством [версии](version-property-ado.md) .

  - Получите сведения о схеме о базе данных с помощью метода [OpenSchema](openschema-method-ado.md) .

Можно создать объекты **подключения** независимо от других ранее определенный объект.

Можно выполнять команды или хранимые процедуры, как если бы они собственные методы объекта **подключения** , как показано ниже.

### <a name="execute-a-command-as-a-native-method-of-a-connection-object"></a>Выполнить команду как собственный метод объект подключения

Для выполнения команды, имя команды с помощью объекта **команду** свойства [Name](name-property-ado.md) . Объект **команды** **ActiveConnection** для свойства подключения. Затем проблему объекта оператор которых используется имя команды, как если бы метод на **подключение** , следуют любые параметры, затем следуют объекта **набора записей** , если возвращаются все строки. Задайте свойства **набора записей** для настройки результирующего **набора записей**. Пример:

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

### <a name="execute-a-stored-procedure-as-a-native-method-of-a-connection-object"></a>Выполнить хранимую процедуру как собственный метод объект подключения

Чтобы выполнить хранимую процедуру, используйте оператор которых используется имя хранимой процедуры, как если бы метод на объект **подключения** , а затем каких-либо параметров. ADO сделает «наиболее подходящий» типы параметров. Например:

```vb
    Dim cnn As New ADODB.Connection
    ...
    'Your stored procedure name and any parameters.
    cnn.sp_yourStoredProcedureName "parameter"
```
