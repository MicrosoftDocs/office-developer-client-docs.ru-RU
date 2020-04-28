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
# <a name="command-object-ado"></a><span data-ttu-id="dab67-102">Объект Command (ADO)</span><span class="sxs-lookup"><span data-stu-id="dab67-102">Command object (ADO)</span></span>


<span data-ttu-id="dab67-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dab67-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dab67-104">Определяет определенную команду, которую необходимо выполнить для источника данных.</span><span class="sxs-lookup"><span data-stu-id="dab67-104">Defines a specific command that you intend to execute against a data source.</span></span>

## <a name="remarks"></a><span data-ttu-id="dab67-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="dab67-105">Remarks</span></span>

<span data-ttu-id="dab67-106">Используйте объект **Command** для запроса к базе данных и возвращения записей в объекте [Recordset](recordset-object-ado.md) , для выполнения массовой операции или для управления структурой базы данных.</span><span class="sxs-lookup"><span data-stu-id="dab67-106">Use a **Command** object to query a database and return records in a [Recordset](recordset-object-ado.md) object, to execute a bulk operation, or to manipulate the structure of a database.</span></span> <span data-ttu-id="dab67-107">В зависимости от функциональных возможностей поставщика некоторые коллекции **команд** , методы или свойства могут вызывать ошибку при указании ссылки.</span><span class="sxs-lookup"><span data-stu-id="dab67-107">Depending on the functionality of the provider, some **Command** collections, methods, or properties may generate an error when referenced.</span></span>

<span data-ttu-id="dab67-108">С помощью коллекций, методов и свойств объекта **Command** можно выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="dab67-108">With the collections, methods, and properties of a **Command** object, you can do the following:</span></span>

  - <span data-ttu-id="dab67-109">Определите исполняемый текст команды (например, инструкцию SQL) с помощью свойства [CommandText](commandtext-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="dab67-109">Define the executable text of the command (for example, an SQL statement) with the [CommandText](commandtext-property-ado.md) property.</span></span>

  - <span data-ttu-id="dab67-110">Определите параметризованные запросы или аргументы хранимой процедуры с объектами [Parameter](parameter-object-ado.md) и коллекцией [Parameters](parameters-collection-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="dab67-110">Define parameterized queries or stored-procedure arguments with [Parameter](parameter-object-ado.md) objects and the [Parameters](parameters-collection-ado.md) collection.</span></span>

  - <span data-ttu-id="dab67-111">Выполнение команды и возврат объекта **Recordset** , если он подходит методу [EXECUTE](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) .</span><span class="sxs-lookup"><span data-stu-id="dab67-111">Execute a command and return a **Recordset** object if appropriate with the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) method.</span></span>

  - <span data-ttu-id="dab67-112">Перед выполнением оптимизации производительности укажите тип команды со свойством [CommandType](commandtype-property-ado.md) перед выполнением.</span><span class="sxs-lookup"><span data-stu-id="dab67-112">Specify the type of command with the [CommandType](commandtype-property-ado.md) property prior to execution to optimize performance.</span></span>

  - <span data-ttu-id="dab67-113">Управляет тем, сохраняет ли поставщик подготовленную (или скомпилированную) версию команды перед выполнением с помощью свойства [preparedd](prepared-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="dab67-113">Control whether the provider saves a prepared (or compiled) version of the command prior to execution with the [Prepared](prepared-property-ado.md) property.</span></span>

  - <span data-ttu-id="dab67-114">Задайте количество секунд, в течение которого поставщик будет ожидать выполнения команды со свойством [CommandTimeout](commandtimeout-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="dab67-114">Set the number of seconds that a provider will wait for a command to execute with the [CommandTimeout](commandtimeout-property-ado.md) property.</span></span>

  - <span data-ttu-id="dab67-115">Свяжите открытое подключение с объектом **Command** , задав его свойство [ActiveConnection](activeconnection-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="dab67-115">Associate an open connection with a **Command** object by setting its [ActiveConnection](activeconnection-property-ado.md) property.</span></span>

  - <span data-ttu-id="dab67-116">Задайте свойство [Name](name-property-ado.md) , чтобы оно определяло объект **Command** как метод в связанном объекте [Connection](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="dab67-116">Set the [Name](name-property-ado.md) property to identify the **Command** object as a method on the associated [Connection](connection-object-ado.md) object.</span></span>

  - <span data-ttu-id="dab67-117">Передайте объект **Command** свойству [Source](source-property-ado-recordset.md) объекта **Recordset** для получения данных.</span><span class="sxs-lookup"><span data-stu-id="dab67-117">Pass a **Command** object to the [Source](source-property-ado-recordset.md) property of a **Recordset** in order to obtain data.</span></span>

  - <span data-ttu-id="dab67-118">Доступ к атрибутам, зависящим от поставщика, с коллекцией [свойств](properties-collection-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="dab67-118">Access provider-specific attributes with the [Properties](properties-collection-ado.md) collection.</span></span>

> [!NOTE]
> <span data-ttu-id="dab67-119">Чтобы выполнить запрос, не используя объект **Command** , передайте строку запроса методу [EXECUTE](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) объекта **Connection** или методу [Open](open-method-ado-recordset.md) объекта **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="dab67-119">To execute a query without using a **Command** object, pass a query string to the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) method of a **Connection** object or to the [Open](open-method-ado-recordset.md) method of a **Recordset** object.</span></span> <span data-ttu-id="dab67-120">Однако при необходимости сохранения текста команды и его повторного выполнения или использования параметров запроса требуется объект **Command** .</span><span class="sxs-lookup"><span data-stu-id="dab67-120">However, a **Command** object is required when you want to persist the command text and re-execute it, or use query parameters.</span></span>

<span data-ttu-id="dab67-121">Чтобы создать объект **команды** независимо от ранее определенного объекта **Connection** , задайте для его свойства **ActiveConnection** допустимую строку подключения.</span><span class="sxs-lookup"><span data-stu-id="dab67-121">To create a **Command** object independently of a previously defined **Connection** object, set its **ActiveConnection** property to a valid connection string.</span></span> <span data-ttu-id="dab67-122">ADO по-прежнему создает объект **Connection** , но он не назначает этот объект объектной переменной.</span><span class="sxs-lookup"><span data-stu-id="dab67-122">ADO still creates a **Connection** object, but it doesn't assign that object to an object variable.</span></span> <span data-ttu-id="dab67-123">Однако при связывании нескольких объектов **Command** с одним соединением необходимо явно создать и открыть объект **Connection** ; При этом объект **Connection** будет назначен объектной переменной.</span><span class="sxs-lookup"><span data-stu-id="dab67-123">However, if you are associating multiple **Command** objects with the same connection, you should explicitly create and open a **Connection** object; this assigns the **Connection** object to an object variable.</span></span> <span data-ttu-id="dab67-124">Если свойство **ActiveConnection** объекта **Command** не задано для этой объектной переменной, ADO создает новый объект **Connection** для каждого объекта **Command** , даже если вы используете одну и ту же строку подключения.</span><span class="sxs-lookup"><span data-stu-id="dab67-124">If you do not set the **Command** object's **ActiveConnection** property to this object variable, ADO creates a new **Connection** object for each **Command** object, even if you use the same connection string.</span></span>

<span data-ttu-id="dab67-125">Чтобы выполнить **команду**, просто вызовите ее с помощью свойства [Name](name-property-ado.md) в связанном объекте **Connection** .</span><span class="sxs-lookup"><span data-stu-id="dab67-125">To execute a **Command**, simply call it by its [Name](name-property-ado.md) property on the associated **Connection** object.</span></span> <span data-ttu-id="dab67-126">Для **Свойства** **ActiveConnection** должно быть задано значение объекта **Connection** .</span><span class="sxs-lookup"><span data-stu-id="dab67-126">The **Command** must have its **ActiveConnection** property set to the **Connection** object.</span></span> <span data-ttu-id="dab67-127">Если **команда** имеет параметры, передайте их значения в качестве аргументов в метод.</span><span class="sxs-lookup"><span data-stu-id="dab67-127">If the **Command** has parameters, pass their values as arguments to the method.</span></span>

<span data-ttu-id="dab67-128">Если в одном и том же соединении выполняются два или более **командных** объектов, а **Командный** объект — хранимая процедура с выходными параметрами, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="dab67-128">If two or more **Command** objects are executed on the same connection and either **Command** object is a stored procedure with output parameters, an error occurs.</span></span> <span data-ttu-id="dab67-129">Чтобы выполнить каждый объект **Command** , используйте отдельные подключения или отключите все остальные объекты **команд** от подключения.</span><span class="sxs-lookup"><span data-stu-id="dab67-129">To execute each **Command** object, use separate connections or disconnect all other **Command** objects from the connection.</span></span>

<span data-ttu-id="dab67-130">Коллекция **Parameters** является членом объекта **Command** по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="dab67-130">The **Parameters** collection is the default member of the **Command** object.</span></span> <span data-ttu-id="dab67-131">В результате следующие два оператора кода эквивалентны.</span><span class="sxs-lookup"><span data-stu-id="dab67-131">As a result, the following two code statements are equivalent.</span></span>

