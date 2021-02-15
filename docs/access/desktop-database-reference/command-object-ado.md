---
title: Command object (ADO)
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
# <a name="command-object-ado"></a>Command object (ADO)


**Область применения**: Access 2013, Office 2013

Определяет определенную команду, которую вы собираетесь выполнить для источника данных.

## <a name="remarks"></a>Заметки

Используйте объект **Command** для запроса базы данных и возврата записей в [объекте Recordset,](recordset-object-ado.md) для выполнения массовой операции или для управления структурой базы данных. В зависимости от функциональности поставщика при ссылке на некоторые коллекции **команд,** методы или свойства могут возникнуть ошибки.

С помощью коллекций, методов и свойств объекта **Command** можно сделать следующее:

  - Определите исполняемый текст команды (например, SQL) со свойством [CommandText.](commandtext-property-ado.md)

  - Определите параметризованные запросы или аргументы хранимых процедур с объектами [Parameter](parameter-object-ado.md) и [коллекцией Parameters.](parameters-collection-ado.md)

  - Выполните команду и вернете объект **Recordset,** если это необходимо с помощью [метода Execute.](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command)

  - Укажите тип команды со свойством [CommandType](commandtype-property-ado.md) перед выполнением для оптимизации производительности.

  - Уберите, сохраняет ли поставщик подготовленную (или скомпилную) версию команды перед выполнением с помощью свойства [Prepared.](prepared-property-ado.md)

  - Установите время в секундах, в течение которое поставщик будет ждать выполнения команды со свойством [CommandTimeout.](commandtimeout-property-ado.md)

  - Связывание открытого подключения с **объектом Command** путем установки его свойства [ActiveConnection.](activeconnection-property-ado.md)

  - Установите свойство [Name,](name-property-ado.md) чтобы определить **объект Command** как метод для связанного [объекта Connection.](connection-object-ado.md)

  - **Передав объект Command** свойству [Source](source-property-ado-recordset.md) объекта **Recordset,** чтобы получить данные.

  - Доступ к атрибутам поставщика с помощью коллекции [Properties.](properties-collection-ado.md)

> [!NOTE]
> Чтобы выполнить запрос без использования объекта **Command,** передайте строку запроса методу [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) объекта **Connection** или [методу Open](open-method-ado-recordset.md) объекта **Recordset.** Однако объект **Command** необходим, если необходимо сохранить текст команды и выполнить его повторно, или использовать параметры запроса.

Чтобы создать **объект Command** независимо от ранее определенного объекта **Connection,** задайте для его свойства **ActiveConnection** допустимую строку подключения. ADO по-прежнему создает объект **Connection,** но не назначает этот объект объектной переменной. Однако если вы связываете несколько объектов **Command** с одинаковым подключением, необходимо явно создать и открыть **объект Connection;** При этом объект **Connection назначается** объектной переменной. Если свойство **ActiveConnection** объекта **Command** не установлено для этой переменной объекта, ADO создает новый объект **Connection** для каждого объекта **Command,** даже если используется та же строка подключения.

Чтобы выполнить **команду,** просто вызовите ее по [свойству Name](name-property-ado.md) связанного **объекта Connection.** Для **свойства** **ActiveConnection** команды должен быть установлен объект **Connection.** Если команда **имеет** параметры, передав их значения в качестве аргументов методу.

Если два или более **объектов Command** выполняются  в одном подмосковном соединении и любой из них является хранимой процедурой с выходными параметрами, возникает ошибка. Чтобы выполнить **каждый объект Command,** используйте отдельные подключения или отключите все остальные объекты **Command** от подключения.

Коллекция **Parameters** является членом объекта **Command** по умолчанию. В результате два следующих кода являются эквивалентными.

