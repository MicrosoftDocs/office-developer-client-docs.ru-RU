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
# <a name="command-object-ado"></a><span data-ttu-id="07336-102">Command object (ADO)</span><span class="sxs-lookup"><span data-stu-id="07336-102">Command object (ADO)</span></span>


<span data-ttu-id="07336-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="07336-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="07336-104">Определяет определенную команду, которую вы собираетесь выполнить для источника данных.</span><span class="sxs-lookup"><span data-stu-id="07336-104">Defines a specific command that you intend to execute against a data source.</span></span>

## <a name="remarks"></a><span data-ttu-id="07336-105">Заметки</span><span class="sxs-lookup"><span data-stu-id="07336-105">Remarks</span></span>

<span data-ttu-id="07336-106">Используйте объект **Command** для запроса базы данных и возврата записей в [объекте Recordset,](recordset-object-ado.md) для выполнения массовой операции или для управления структурой базы данных.</span><span class="sxs-lookup"><span data-stu-id="07336-106">Use a **Command** object to query a database and return records in a [Recordset](recordset-object-ado.md) object, to execute a bulk operation, or to manipulate the structure of a database.</span></span> <span data-ttu-id="07336-107">В зависимости от функциональности поставщика при ссылке на некоторые коллекции **команд,** методы или свойства могут возникнуть ошибки.</span><span class="sxs-lookup"><span data-stu-id="07336-107">Depending on the functionality of the provider, some **Command** collections, methods, or properties may generate an error when referenced.</span></span>

<span data-ttu-id="07336-108">С помощью коллекций, методов и свойств объекта **Command** можно сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="07336-108">With the collections, methods, and properties of a **Command** object, you can do the following:</span></span>

  - <span data-ttu-id="07336-109">Определите исполняемый текст команды (например, SQL) со свойством [CommandText.](commandtext-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="07336-109">Define the executable text of the command (for example, an SQL statement) with the [CommandText](commandtext-property-ado.md) property.</span></span>

  - <span data-ttu-id="07336-110">Определите параметризованные запросы или аргументы хранимых процедур с объектами [Parameter](parameter-object-ado.md) и [коллекцией Parameters.](parameters-collection-ado.md)</span><span class="sxs-lookup"><span data-stu-id="07336-110">Define parameterized queries or stored-procedure arguments with [Parameter](parameter-object-ado.md) objects and the [Parameters](parameters-collection-ado.md) collection.</span></span>

  - <span data-ttu-id="07336-111">Выполните команду и вернете объект **Recordset,** если это необходимо с помощью [метода Execute.](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command)</span><span class="sxs-lookup"><span data-stu-id="07336-111">Execute a command and return a **Recordset** object if appropriate with the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) method.</span></span>

  - <span data-ttu-id="07336-112">Укажите тип команды со свойством [CommandType](commandtype-property-ado.md) перед выполнением для оптимизации производительности.</span><span class="sxs-lookup"><span data-stu-id="07336-112">Specify the type of command with the [CommandType](commandtype-property-ado.md) property prior to execution to optimize performance.</span></span>

  - <span data-ttu-id="07336-113">Уберите, сохраняет ли поставщик подготовленную (или скомпилную) версию команды перед выполнением с помощью свойства [Prepared.](prepared-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="07336-113">Control whether the provider saves a prepared (or compiled) version of the command prior to execution with the [Prepared](prepared-property-ado.md) property.</span></span>

  - <span data-ttu-id="07336-114">Установите время в секундах, в течение которое поставщик будет ждать выполнения команды со свойством [CommandTimeout.](commandtimeout-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="07336-114">Set the number of seconds that a provider will wait for a command to execute with the [CommandTimeout](commandtimeout-property-ado.md) property.</span></span>

  - <span data-ttu-id="07336-115">Связывание открытого подключения с **объектом Command** путем установки его свойства [ActiveConnection.](activeconnection-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="07336-115">Associate an open connection with a **Command** object by setting its [ActiveConnection](activeconnection-property-ado.md) property.</span></span>

  - <span data-ttu-id="07336-116">Установите свойство [Name,](name-property-ado.md) чтобы определить **объект Command** как метод для связанного [объекта Connection.](connection-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="07336-116">Set the [Name](name-property-ado.md) property to identify the **Command** object as a method on the associated [Connection](connection-object-ado.md) object.</span></span>

  - <span data-ttu-id="07336-117">**Передав объект Command** свойству [Source](source-property-ado-recordset.md) объекта **Recordset,** чтобы получить данные.</span><span class="sxs-lookup"><span data-stu-id="07336-117">Pass a **Command** object to the [Source](source-property-ado-recordset.md) property of a **Recordset** in order to obtain data.</span></span>

  - <span data-ttu-id="07336-118">Доступ к атрибутам поставщика с помощью коллекции [Properties.](properties-collection-ado.md)</span><span class="sxs-lookup"><span data-stu-id="07336-118">Access provider-specific attributes with the [Properties](properties-collection-ado.md) collection.</span></span>

> [!NOTE]
> <span data-ttu-id="07336-119">Чтобы выполнить запрос без использования объекта **Command,** передайте строку запроса методу [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) объекта **Connection** или [методу Open](open-method-ado-recordset.md) объекта **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="07336-119">To execute a query without using a **Command** object, pass a query string to the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) method of a **Connection** object or to the [Open](open-method-ado-recordset.md) method of a **Recordset** object.</span></span> <span data-ttu-id="07336-120">Однако объект **Command** необходим, если необходимо сохранить текст команды и выполнить его повторно, или использовать параметры запроса.</span><span class="sxs-lookup"><span data-stu-id="07336-120">However, a **Command** object is required when you want to persist the command text and re-execute it, or use query parameters.</span></span>

<span data-ttu-id="07336-121">Чтобы создать **объект Command** независимо от ранее определенного объекта **Connection,** задайте для его свойства **ActiveConnection** допустимую строку подключения.</span><span class="sxs-lookup"><span data-stu-id="07336-121">To create a **Command** object independently of a previously defined **Connection** object, set its **ActiveConnection** property to a valid connection string.</span></span> <span data-ttu-id="07336-122">ADO по-прежнему создает объект **Connection,** но не назначает этот объект объектной переменной.</span><span class="sxs-lookup"><span data-stu-id="07336-122">ADO still creates a **Connection** object, but it doesn't assign that object to an object variable.</span></span> <span data-ttu-id="07336-123">Однако если вы связываете несколько объектов **Command** с одинаковым подключением, необходимо явно создать и открыть **объект Connection;** При этом объект **Connection назначается** объектной переменной.</span><span class="sxs-lookup"><span data-stu-id="07336-123">However, if you are associating multiple **Command** objects with the same connection, you should explicitly create and open a **Connection** object; this assigns the **Connection** object to an object variable.</span></span> <span data-ttu-id="07336-124">Если свойство **ActiveConnection** объекта **Command** не установлено для этой переменной объекта, ADO создает новый объект **Connection** для каждого объекта **Command,** даже если используется та же строка подключения.</span><span class="sxs-lookup"><span data-stu-id="07336-124">If you do not set the **Command** object's **ActiveConnection** property to this object variable, ADO creates a new **Connection** object for each **Command** object, even if you use the same connection string.</span></span>

<span data-ttu-id="07336-125">Чтобы выполнить **команду,** просто вызовите ее по [свойству Name](name-property-ado.md) связанного **объекта Connection.**</span><span class="sxs-lookup"><span data-stu-id="07336-125">To execute a **Command**, simply call it by its [Name](name-property-ado.md) property on the associated **Connection** object.</span></span> <span data-ttu-id="07336-126">Для **свойства** **ActiveConnection** команды должен быть установлен объект **Connection.**</span><span class="sxs-lookup"><span data-stu-id="07336-126">The **Command** must have its **ActiveConnection** property set to the **Connection** object.</span></span> <span data-ttu-id="07336-127">Если команда **имеет** параметры, передав их значения в качестве аргументов методу.</span><span class="sxs-lookup"><span data-stu-id="07336-127">If the **Command** has parameters, pass their values as arguments to the method.</span></span>

<span data-ttu-id="07336-128">Если два или более **объектов Command** выполняются  в одном подмосковном соединении и любой из них является хранимой процедурой с выходными параметрами, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="07336-128">If two or more **Command** objects are executed on the same connection and either **Command** object is a stored procedure with output parameters, an error occurs.</span></span> <span data-ttu-id="07336-129">Чтобы выполнить **каждый объект Command,** используйте отдельные подключения или отключите все остальные объекты **Command** от подключения.</span><span class="sxs-lookup"><span data-stu-id="07336-129">To execute each **Command** object, use separate connections or disconnect all other **Command** objects from the connection.</span></span>

<span data-ttu-id="07336-130">Коллекция **Parameters** является членом объекта **Command** по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="07336-130">The **Parameters** collection is the default member of the **Command** object.</span></span> <span data-ttu-id="07336-131">В результате два следующих кода являются эквивалентными.</span><span class="sxs-lookup"><span data-stu-id="07336-131">As a result, the following two code statements are equivalent.</span></span>

