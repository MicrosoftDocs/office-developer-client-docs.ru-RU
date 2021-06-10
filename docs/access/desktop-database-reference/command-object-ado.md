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
# <a name="command-object-ado"></a><span data-ttu-id="ff85f-102">Объект Command (ADO)</span><span class="sxs-lookup"><span data-stu-id="ff85f-102">Command object (ADO)</span></span>


<span data-ttu-id="ff85f-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ff85f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ff85f-104">Определяет определенную команду, которую вы собираетесь выполнить в отношении источника данных.</span><span class="sxs-lookup"><span data-stu-id="ff85f-104">Defines a specific command that you intend to execute against a data source.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff85f-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="ff85f-105">Remarks</span></span>

<span data-ttu-id="ff85f-106">Используйте объект **Command** для запроса базы данных и возврата записей в [объекте Recordset,](recordset-object-ado.md) для выполнения объемной операции или для управления структурой базы данных.</span><span class="sxs-lookup"><span data-stu-id="ff85f-106">Use a **Command** object to query a database and return records in a [Recordset](recordset-object-ado.md) object, to execute a bulk operation, or to manipulate the structure of a database.</span></span> <span data-ttu-id="ff85f-107">В зависимости от функциональности поставщика  некоторые коллекции команд, методы или свойства могут создавать ошибки при ссылке.</span><span class="sxs-lookup"><span data-stu-id="ff85f-107">Depending on the functionality of the provider, some **Command** collections, methods, or properties may generate an error when referenced.</span></span>

<span data-ttu-id="ff85f-108">С помощью коллекций, методов и свойств объекта **Command** можно сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="ff85f-108">With the collections, methods, and properties of a **Command** object, you can do the following:</span></span>

  - <span data-ttu-id="ff85f-109">Определите исполняемый текст команды (например, SQL) с [свойством CommandText.](commandtext-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="ff85f-109">Define the executable text of the command (for example, an SQL statement) with the [CommandText](commandtext-property-ado.md) property.</span></span>

  - <span data-ttu-id="ff85f-110">Определите параметризированные запросы или аргументы с сохраненной процедурой с объектами [Parameter](parameter-object-ado.md) и коллекцией [Параметры.](parameters-collection-ado.md)</span><span class="sxs-lookup"><span data-stu-id="ff85f-110">Define parameterized queries or stored-procedure arguments with [Parameter](parameter-object-ado.md) objects and the [Parameters](parameters-collection-ado.md) collection.</span></span>

  - <span data-ttu-id="ff85f-111">Выполните команду и верни объект **Recordset,** если это уместно с помощью [метода Execute.](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command)</span><span class="sxs-lookup"><span data-stu-id="ff85f-111">Execute a command and return a **Recordset** object if appropriate with the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) method.</span></span>

  - <span data-ttu-id="ff85f-112">Укажите тип команды с свойством [CommandType](commandtype-property-ado.md) перед выполнением, чтобы оптимизировать производительность.</span><span class="sxs-lookup"><span data-stu-id="ff85f-112">Specify the type of command with the [CommandType](commandtype-property-ado.md) property prior to execution to optimize performance.</span></span>

  - <span data-ttu-id="ff85f-113">Управление сохранением подготовленной (или компилировать) версии команды перед выполнением с помощью свойства [Prepared.](prepared-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="ff85f-113">Control whether the provider saves a prepared (or compiled) version of the command prior to execution with the [Prepared](prepared-property-ado.md) property.</span></span>

  - <span data-ttu-id="ff85f-114">Установите количество секунд, которые поставщик будет ждать выполнения команды с [свойством CommandTimeout.](commandtimeout-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="ff85f-114">Set the number of seconds that a provider will wait for a command to execute with the [CommandTimeout](commandtimeout-property-ado.md) property.</span></span>

  - <span data-ttu-id="ff85f-115">Связать открытое подключение с **объектом Command,** установив его свойство [ActiveConnection.](activeconnection-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="ff85f-115">Associate an open connection with a **Command** object by setting its [ActiveConnection](activeconnection-property-ado.md) property.</span></span>

  - <span data-ttu-id="ff85f-116">Установите свойство [Name,](name-property-ado.md) чтобы определить **объект Command** как метод на связанном [объекте Подключения.](connection-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="ff85f-116">Set the [Name](name-property-ado.md) property to identify the **Command** object as a method on the associated [Connection](connection-object-ado.md) object.</span></span>

  - <span data-ttu-id="ff85f-117">**Передай объект Command** свойству [Source](source-property-ado-recordset.md) **recordset** для получения данных.</span><span class="sxs-lookup"><span data-stu-id="ff85f-117">Pass a **Command** object to the [Source](source-property-ado-recordset.md) property of a **Recordset** in order to obtain data.</span></span>

  - <span data-ttu-id="ff85f-118">Доступ к атрибутам, определенным поставщиком, с [коллекцией Свойств.](properties-collection-ado.md)</span><span class="sxs-lookup"><span data-stu-id="ff85f-118">Access provider-specific attributes with the [Properties](properties-collection-ado.md) collection.</span></span>

> [!NOTE]
> <span data-ttu-id="ff85f-119">Чтобы выполнить запрос без использования объекта **Command,** передайте строку запроса методу [Выполнения](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) объекта **Подключения** или методу [Open](open-method-ado-recordset.md) объекта **Recordset.**</span><span class="sxs-lookup"><span data-stu-id="ff85f-119">To execute a query without using a **Command** object, pass a query string to the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) method of a **Connection** object or to the [Open](open-method-ado-recordset.md) method of a **Recordset** object.</span></span> <span data-ttu-id="ff85f-120">Однако для **сохраняемого** командного текста и его повторного выполнения или использования параметров запроса требуется объект Command.</span><span class="sxs-lookup"><span data-stu-id="ff85f-120">However, a **Command** object is required when you want to persist the command text and re-execute it, or use query parameters.</span></span>

<span data-ttu-id="ff85f-121">Чтобы создать **объект Command** независимо от ранее определенного объекта **Подключения,** задайте его свойство **ActiveConnection** допустимой строке подключения.</span><span class="sxs-lookup"><span data-stu-id="ff85f-121">To create a **Command** object independently of a previously defined **Connection** object, set its **ActiveConnection** property to a valid connection string.</span></span> <span data-ttu-id="ff85f-122">ADO по-прежнему создает объект **Connection,** но не назначает этот объект переменной объекта.</span><span class="sxs-lookup"><span data-stu-id="ff85f-122">ADO still creates a **Connection** object, but it doesn't assign that object to an object variable.</span></span> <span data-ttu-id="ff85f-123">Однако если вы связываете несколько объектов **Command** с одинаковым подключением, необходимо явно создать и открыть объект **Подключения;** это назначает объект **Подключение** к переменной объекта.</span><span class="sxs-lookup"><span data-stu-id="ff85f-123">However, if you are associating multiple **Command** objects with the same connection, you should explicitly create and open a **Connection** object; this assigns the **Connection** object to an object variable.</span></span> <span data-ttu-id="ff85f-124">Если свойство **ActiveConnection** объекта Command не задайте этой переменной объекта,  ADO создает новый объект Подключения для каждого объекта  **Command,** даже если вы используете ту же строку подключения.</span><span class="sxs-lookup"><span data-stu-id="ff85f-124">If you do not set the **Command** object's **ActiveConnection** property to this object variable, ADO creates a new **Connection** object for each **Command** object, even if you use the same connection string.</span></span>

<span data-ttu-id="ff85f-125">Чтобы выполнить **команду,** просто назовите ее [свойством Name](name-property-ado.md) на связанном **объекте Подключения.**</span><span class="sxs-lookup"><span data-stu-id="ff85f-125">To execute a **Command**, simply call it by its [Name](name-property-ado.md) property on the associated **Connection** object.</span></span> <span data-ttu-id="ff85f-126">Свойство **ActiveConnection** должно иметь свойство **ActiveConnection** для объекта **Подключение.**</span><span class="sxs-lookup"><span data-stu-id="ff85f-126">The **Command** must have its **ActiveConnection** property set to the **Connection** object.</span></span> <span data-ttu-id="ff85f-127">Если команда **имеет** параметры, передай их значения в качестве аргументов методу.</span><span class="sxs-lookup"><span data-stu-id="ff85f-127">If the **Command** has parameters, pass their values as arguments to the method.</span></span>

<span data-ttu-id="ff85f-128">Если два или несколько объектов **Command** выполняются на одном и том же соединении, а любой объект **Command** — это сохраненная процедура с параметрами вывода, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="ff85f-128">If two or more **Command** objects are executed on the same connection and either **Command** object is a stored procedure with output parameters, an error occurs.</span></span> <span data-ttu-id="ff85f-129">Чтобы выполнить **каждый объект Command,** используйте отдельные подключения или отключите все другие объекты **Команды** от подключения.</span><span class="sxs-lookup"><span data-stu-id="ff85f-129">To execute each **Command** object, use separate connections or disconnect all other **Command** objects from the connection.</span></span>

<span data-ttu-id="ff85f-130">Коллекция **Параметры** является по умолчанию членом **объекта Command.**</span><span class="sxs-lookup"><span data-stu-id="ff85f-130">The **Parameters** collection is the default member of the **Command** object.</span></span> <span data-ttu-id="ff85f-131">В результате два следующих кода эквивалентны.</span><span class="sxs-lookup"><span data-stu-id="ff85f-131">As a result, the following two code statements are equivalent.</span></span>

