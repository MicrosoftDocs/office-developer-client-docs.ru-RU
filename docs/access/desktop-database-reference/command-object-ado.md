---
title: Объект Command (ADO)
TOCTitle: Command object (ADO)
ms:assetid: 64f4ef03-f858-c004-b891-0c96d13a5e6e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249389(v=office.15)
ms:contentKeyID: 48545303
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231106
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: dc582046ff1981a82fab9c9c551b0064c1e8c1de
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296173"
---
# <a name="command-object-ado"></a>Объект Command (ADO)


**Область применения**: Access 2013, Office 2013

Определяет определенную команду, которую необходимо выполнить для источника данных.

## <a name="remarks"></a>Примечания

Используйте объект **Command** для запроса к базе данных и возвращения записей в объекте [Recordset](recordset-object-ado.md) , для выполнения массовой операции или для управления структурой базы данных. В зависимости от функциональных возможностей поставщика некоторые коллекции **команд** , методы или свойства могут вызывать ошибку при указании ссылки.

С помощью коллекций, методов и свойств объекта **Command** можно выполнить следующие действия:

  - Определите исполняемый текст команды (например, инструкцию SQL) с помощью свойства [CommandText](commandtext-property-ado.md) .

  - Определите параметризованные запросы или аргументы хранимой процедуры с объектами [Parameter](parameter-object-ado.md) и коллекцией [Parameters](parameters-collection-ado.md) .

  - Выполнение команды и возврат объекта **Recordset** , если он подходит методу [EXECUTE](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) .

  - Перед выполнением оптимизации производительности укажите тип команды со свойством [CommandType](commandtype-property-ado.md) перед выполнением.

  - Управляет тем, сохраняет ли поставщик подготовленную (или скомпилированную) версию команды перед выполнением с помощью свойства [preparedd](prepared-property-ado.md) .

  - Задайте количество секунд, в течение которого поставщик будет ожидать выполнения команды со свойством [CommandTimeout](commandtimeout-property-ado.md) .

  - Свяжите открытое подключение с объектом **Command** , задав его свойство [ActiveConnection](activeconnection-property-ado.md) .

  - Задайте свойство [Name](name-property-ado.md) , чтобы оно определяло объект **Command** как метод в связанном объекте [Connection](connection-object-ado.md) .

  - Передайте объект **Command** свойству [Source](source-property-ado-recordset.md) объекта **Recordset** для получения данных.

  - Доступ к атрибутам, зависящим от поставщика, с коллекцией [свойств](properties-collection-ado.md) .

> [!NOTE]
> Чтобы выполнить запрос, не используя объект **Command** , передайте строку запроса методу [EXECUTE](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) объекта **Connection** или методу [Open](open-method-ado-recordset.md) объекта **Recordset** . Однако при необходимости сохранения текста команды и его повторного выполнения или использования параметров запроса требуется объект **Command** .

Чтобы создать объект **команды** независимо от ранее определенного объекта **Connection** , задайте для его свойства **ActiveConnection** допустимую строку подключения. ADO по-прежнему создает объект **Connection** , но он не назначает этот объект объектной переменной. Однако при связывании нескольких объектов **Command** с одним соединением необходимо явно создать и открыть объект **Connection** ; При этом объект **Connection** будет назначен объектной переменной. Если свойство **ActiveConnection** объекта **Command** не задано для этой объектной переменной, ADO создает новый объект **Connection** для каждого объекта **Command** , даже если вы используете одну и ту же строку подключения.

Чтобы выполнить **команду**, просто вызовите ее с помощью свойства [Name](name-property-ado.md) в связанном объекте **Connection** . Для **Свойства** **ActiveConnection** должно быть задано значение объекта **Connection** . Если **команда** имеет параметры, передайте их значения в качестве аргументов в метод.

Если в одном и том же соединении выполняются два или более **командных** объектов, а **Командный** объект — хранимая процедура с выходными параметрами, возникает ошибка. Чтобы выполнить каждый объект **Command** , используйте отдельные подключения или отключите все остальные объекты **команд** от подключения.

Коллекция **Parameters** является членом объекта **Command** по умолчанию. В результате следующие два оператора кода эквивалентны.

