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
# <a name="connection-object-ado"></a><span data-ttu-id="bfbb0-102">Объект Connection (ADO)</span><span class="sxs-lookup"><span data-stu-id="bfbb0-102">Connection object (ADO)</span></span>

<span data-ttu-id="bfbb0-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bfbb0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bfbb0-104">Представляет открытое подключение к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="bfbb0-104">Represents an open connection to a data source.</span></span>

## <a name="remarks"></a><span data-ttu-id="bfbb0-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="bfbb0-105">Remarks</span></span>

<span data-ttu-id="bfbb0-106">Объект **Connection** представляет уникальный сеанс с источником данных.</span><span class="sxs-lookup"><span data-stu-id="bfbb0-106">A **Connection** object represents a unique session with a data source.</span></span> <span data-ttu-id="bfbb0-107">В случае клиент-серверной системы базы данных она может быть эквивалентна фактическому сетевому подключению к серверу.</span><span class="sxs-lookup"><span data-stu-id="bfbb0-107">In the case of a client/server database system, it may be equivalent to an actual network connection to the server.</span></span> <span data-ttu-id="bfbb0-108">В зависимости от функциональных возможностей, поддерживаемых поставщиком, некоторые коллекции, методы или свойства объекта **Connection** могут быть недоступны.</span><span class="sxs-lookup"><span data-stu-id="bfbb0-108">Depending on the functionality supported by the provider, some collections, methods, or properties of a **Connection** object may not be available.</span></span>

<span data-ttu-id="bfbb0-109">С помощью коллекций, методов и свойств объекта **Connection** можно выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="bfbb0-109">With the collections, methods, and properties of a **Connection** object, you can do the following:</span></span>

  - <span data-ttu-id="bfbb0-110">Настройте подключение перед его открытием с помощью свойств [ConnectionString](connectionstring-property-ado.md), [ConnectionTimeout](connectiontimeout-property-ado.md)и [mode](mode-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="bfbb0-110">Configure the connection before opening it with the [ConnectionString](connectionstring-property-ado.md), [ConnectionTimeout](connectiontimeout-property-ado.md), and [Mode](mode-property-ado.md) properties.</span></span> <span data-ttu-id="bfbb0-111">**ConnectionString** является свойством по умолчанию для объекта **Connection** .</span><span class="sxs-lookup"><span data-stu-id="bfbb0-111">**ConnectionString** is the default property of the **Connection** object.</span></span>

  - <span data-ttu-id="bfbb0-112">Задайте для свойства [CursorLocation](cursorlocation-property-ado.md) значение Client, чтобы вызвать [службу Microsoft Cursor для OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md), которая поддерживает пакетное обновление.</span><span class="sxs-lookup"><span data-stu-id="bfbb0-112">Set the [CursorLocation](cursorlocation-property-ado.md) property to client to invoke the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md), which supports batch updates.</span></span>

  - <span data-ttu-id="bfbb0-113">Задайте базу данных по умолчанию для подключения с помощью свойства [DefaultDatabase](defaultdatabase-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="bfbb0-113">Set the default database for the connection with the [DefaultDatabase](defaultdatabase-property-ado.md) property.</span></span>

  - <span data-ttu-id="bfbb0-114">Задайте уровень изоляции для транзакций, открытых в подключении, с помощью свойства [IsolationLevel](isolationlevel-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="bfbb0-114">Set the level of isolation for the transactions opened on the connection with the [IsolationLevel](isolationlevel-property-ado.md) property.</span></span>

  - <span data-ttu-id="bfbb0-115">Укажите поставщика OLE DB с помощью свойства [provider](provider-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="bfbb0-115">Specify an OLE DB provider with the [Provider](provider-property-ado.md) property.</span></span>

  - <span data-ttu-id="bfbb0-116">Установите и приостановите физическое подключение к источнику данных с помощью методов [Open](open-method-ado-connection.md) и [Close](close-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="bfbb0-116">Establish, and later break, the physical connection to the data source with the [Open](open-method-ado-connection.md) and [Close](close-method-ado.md) methods.</span></span>

  - <span data-ttu-id="bfbb0-117">Выполните команду для подключения с помощью метода [EXECUTE](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) и настройте выполнение с помощью свойства [CommandTimeout](commandtimeout-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="bfbb0-117">Execute a command on the connection with the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) method and configure the execution with the [CommandTimeout](commandtimeout-property-ado.md) property.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="bfbb0-118">Чтобы выполнить запрос, не используя объект Command, передайте строку запроса в метод **EXECUTE** объекта **Connection** .</span><span class="sxs-lookup"><span data-stu-id="bfbb0-118">To execute a query without using a Command object, pass a query string to the **Execute** method of a **Connection** object.</span></span> <span data-ttu-id="bfbb0-119">Однако при необходимости сохранения текста команды и его повторного выполнения или использования параметров запроса требуется объект [Command](command-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="bfbb0-119">However, a [Command](command-object-ado.md) object is required when you want to persist the command text and re-execute it, or use query parameters.</span></span>

  - <span data-ttu-id="bfbb0-120">Управление транзакциями в открытом подключении, включая вложенные транзакции, если поставщик поддерживает их, с помощью методов [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md), [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md)и [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) , а [](attributes-property-ado.md) также свойства Attributes.</span><span class="sxs-lookup"><span data-stu-id="bfbb0-120">Manage transactions on the open connection, including nested transactions if the provider supports them, with the [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md), [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md), and [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) methods and the [Attributes](attributes-property-ado.md) property.</span></span>

  - <span data-ttu-id="bfbb0-121">Проверьте ошибки, возвращенные из источника данных, [](errors-collection-ado.md) с помощью коллекции Errors.</span><span class="sxs-lookup"><span data-stu-id="bfbb0-121">Examine errors returned from the data source with the [Errors](errors-collection-ado.md) collection.</span></span>

  - <span data-ttu-id="bfbb0-122">Считывание версии из реализации ADO, используемой со свойством [Version](version-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="bfbb0-122">Read the version from the ADO implementation used with the [Version](version-property-ado.md) property.</span></span>

  - <span data-ttu-id="bfbb0-123">Получение сведений о схеме для базы данных с помощью метода [OpenSchema](openschema-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="bfbb0-123">Obtain schema information about your database with the [OpenSchema](openschema-method-ado.md) method.</span></span>

<span data-ttu-id="bfbb0-124">Вы можете создавать объекты **подключения** независимо от любого ранее определенного объекта.</span><span class="sxs-lookup"><span data-stu-id="bfbb0-124">You can create **Connection** objects independently of any other previously defined object.</span></span>

<span data-ttu-id="bfbb0-125">Вы можете выполнять команды или хранимые процедуры, как если бы они были собственными методами объекта **Connection** , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="bfbb0-125">You can execute commands or stored procedures as if they were native methods on the **Connection** object, as illustrated below.</span></span>

### <a name="execute-a-command-as-a-native-method-of-a-connection-object"></a><span data-ttu-id="bfbb0-126">Выполнение команды в качестве собственного метода объекта подключения</span><span class="sxs-lookup"><span data-stu-id="bfbb0-126">Execute a command as a native method of a Connection object</span></span>

<span data-ttu-id="bfbb0-127">Чтобы выполнить команду, присвойте команде имя, используя свойство [имя](name-property-ado.md) объекта **команды** .</span><span class="sxs-lookup"><span data-stu-id="bfbb0-127">To execute a command, give the command a name using the **Command** object [Name](name-property-ado.md) property.</span></span> <span data-ttu-id="bfbb0-128">Задайте для подключения свойство **ActiveConnection** объекта **Command** .</span><span class="sxs-lookup"><span data-stu-id="bfbb0-128">Set the **Command** object's **ActiveConnection** property to the connection.</span></span> <span data-ttu-id="bfbb0-129">Затем вызовите оператор, где имя команды используется как метод для объекта **Connection** , за которым следуют все параметры, а затем — объект **Recordset** , если возвращаются какие-либо строки.</span><span class="sxs-lookup"><span data-stu-id="bfbb0-129">Then issue a statement where the command name is used as if it were a method on the **Connection** object, followed by any parameters, then followed by a **Recordset** object if any rows are returned.</span></span> <span data-ttu-id="bfbb0-130">Задайте свойствам **набора** записей для настройки результирующего **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="bfbb0-130">Set the **Recordset** properties to customize the resulting **Recordset**.</span></span> <span data-ttu-id="bfbb0-131">Пример:</span><span class="sxs-lookup"><span data-stu-id="bfbb0-131">For example:</span></span>

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

### <a name="execute-a-stored-procedure-as-a-native-method-of-a-connection-object"></a><span data-ttu-id="bfbb0-132">Выполнение хранимой процедуры в качестве собственного метода объекта подключения</span><span class="sxs-lookup"><span data-stu-id="bfbb0-132">Execute a stored procedure as a native method of a Connection object</span></span>

<span data-ttu-id="bfbb0-133">Чтобы выполнить хранимую процедуру, выполните инструкцию, в которой имя хранимой процедуры используется как метод для объекта **Connection** , за которым следуют все параметры.</span><span class="sxs-lookup"><span data-stu-id="bfbb0-133">To execute a stored procedure, issue a statement where the stored procedure name is used as if it were a method on the **Connection** object, followed by any parameters.</span></span> <span data-ttu-id="bfbb0-134">ADO будет делать "наилучшее предположение" для типов параметров.</span><span class="sxs-lookup"><span data-stu-id="bfbb0-134">ADO will make a "best guess" of parameter types.</span></span> <span data-ttu-id="bfbb0-135">Пример:</span><span class="sxs-lookup"><span data-stu-id="bfbb0-135">For example:</span></span>

```vb
    Dim cnn As New ADODB.Connection
    ...
    'Your stored procedure name and any parameters.
    cnn.sp_yourStoredProcedureName "parameter"
```
