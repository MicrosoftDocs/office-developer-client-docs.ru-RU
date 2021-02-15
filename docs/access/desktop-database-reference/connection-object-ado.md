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
# <a name="connection-object-ado"></a><span data-ttu-id="d5644-102">Connection object (ADO)</span><span class="sxs-lookup"><span data-stu-id="d5644-102">Connection object (ADO)</span></span>

<span data-ttu-id="d5644-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d5644-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d5644-104">Представляет открытое подключение к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="d5644-104">Represents an open connection to a data source.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5644-105">Заметки</span><span class="sxs-lookup"><span data-stu-id="d5644-105">Remarks</span></span>

<span data-ttu-id="d5644-106">Объект **Connection** представляет уникальный сеанс с источником данных.</span><span class="sxs-lookup"><span data-stu-id="d5644-106">A **Connection** object represents a unique session with a data source.</span></span> <span data-ttu-id="d5644-107">В случае системы базы данных клиента или сервера она может быть эквивалентна фактическому сетевому подключению к серверу.</span><span class="sxs-lookup"><span data-stu-id="d5644-107">In the case of a client/server database system, it may be equivalent to an actual network connection to the server.</span></span> <span data-ttu-id="d5644-108">В зависимости от функций, поддерживаемых поставщиком, некоторые коллекции, методы или свойства объекта **Connection** могут быть недоступны.</span><span class="sxs-lookup"><span data-stu-id="d5644-108">Depending on the functionality supported by the provider, some collections, methods, or properties of a **Connection** object may not be available.</span></span>

<span data-ttu-id="d5644-109">С помощью коллекций, методов и свойств объекта **Connection** можно сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="d5644-109">With the collections, methods, and properties of a **Connection** object, you can do the following:</span></span>

  - <span data-ttu-id="d5644-110">Настройте подключение перед его открытием со [свойствами ConnectionString,](connectionstring-property-ado.md) [ConnectionTimeout](connectiontimeout-property-ado.md)и [Mode.](mode-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="d5644-110">Configure the connection before opening it with the [ConnectionString](connectionstring-property-ado.md), [ConnectionTimeout](connectiontimeout-property-ado.md), and [Mode](mode-property-ado.md) properties.</span></span> <span data-ttu-id="d5644-111">**ConnectionString** — это свойство по умолчанию объекта **Connection.**</span><span class="sxs-lookup"><span data-stu-id="d5644-111">**ConnectionString** is the default property of the **Connection** object.</span></span>

  - <span data-ttu-id="d5644-112">Установите для [свойства CursorLocation](cursorlocation-property-ado.md) клиент, чтобы вызвать службу [курсоров Майкрософт для OLE DB,](microsoft-cursor-service-for-ole-db-ado-service-component.md)которая поддерживает пакетные обновления.</span><span class="sxs-lookup"><span data-stu-id="d5644-112">Set the [CursorLocation](cursorlocation-property-ado.md) property to client to invoke the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md), which supports batch updates.</span></span>

  - <span data-ttu-id="d5644-113">Установите базу данных по умолчанию для подключения со [свойством DefaultDatabase.](defaultdatabase-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="d5644-113">Set the default database for the connection with the [DefaultDatabase](defaultdatabase-property-ado.md) property.</span></span>

  - <span data-ttu-id="d5644-114">Установите уровень изоляции для транзакций, открытых при под соединении со свойством [IsolationLevel.](isolationlevel-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="d5644-114">Set the level of isolation for the transactions opened on the connection with the [IsolationLevel](isolationlevel-property-ado.md) property.</span></span>

  - <span data-ttu-id="d5644-115">Укажите поставщика OLE DB со [свойством Provider.](provider-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="d5644-115">Specify an OLE DB provider with the [Provider](provider-property-ado.md) property.</span></span>

  - <span data-ttu-id="d5644-116">Установить и затем разорвать физическое подключение к источнику данных с помощью методов [Open](open-method-ado-connection.md) и [Close.](close-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="d5644-116">Establish, and later break, the physical connection to the data source with the [Open](open-method-ado-connection.md) and [Close](close-method-ado.md) methods.</span></span>

  - <span data-ttu-id="d5644-117">Выполните команду для подключения к методу [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) и настройте выполнение с помощью свойства [CommandTimeout.](commandtimeout-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="d5644-117">Execute a command on the connection with the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) method and configure the execution with the [CommandTimeout](commandtimeout-property-ado.md) property.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="d5644-118">Чтобы выполнить запрос без использования объекта Command, передайте строку запроса **методу Execute** объекта **Connection.**</span><span class="sxs-lookup"><span data-stu-id="d5644-118">To execute a query without using a Command object, pass a query string to the **Execute** method of a **Connection** object.</span></span> <span data-ttu-id="d5644-119">Однако объект [Command](command-object-ado.md) необходим, если необходимо сохранить текст команды и выполнить его повторно, или использовать параметры запроса.</span><span class="sxs-lookup"><span data-stu-id="d5644-119">However, a [Command](command-object-ado.md) object is required when you want to persist the command text and re-execute it, or use query parameters.</span></span>

  - <span data-ttu-id="d5644-120">Управляйте транзакциями открытого подключения, включая вложенные транзакции, если поставщик их поддерживает, с помощью методов [BeginTrans,](begintrans-committrans-and-rollbacktrans-methods-ado.md) [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md)и [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) и свойства [Attributes.](attributes-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="d5644-120">Manage transactions on the open connection, including nested transactions if the provider supports them, with the [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md), [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md), and [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) methods and the [Attributes](attributes-property-ado.md) property.</span></span>

  - <span data-ttu-id="d5644-121">Проверьте ошибки, возвращенные из источника данных с [коллекцией ошибок.](errors-collection-ado.md)</span><span class="sxs-lookup"><span data-stu-id="d5644-121">Examine errors returned from the data source with the [Errors](errors-collection-ado.md) collection.</span></span>

  - <span data-ttu-id="d5644-122">Прочитайте версию из реализации ADO, используемой со [свойством Version.](version-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="d5644-122">Read the version from the ADO implementation used with the [Version](version-property-ado.md) property.</span></span>

  - <span data-ttu-id="d5644-123">Получите сведения о схеме базы данных с помощью метода [OpenSchema.](openschema-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="d5644-123">Obtain schema information about your database with the [OpenSchema](openschema-method-ado.md) method.</span></span>

<span data-ttu-id="d5644-124">Объекты **Connection** можно создавать независимо от любого другого ранее определенного объекта.</span><span class="sxs-lookup"><span data-stu-id="d5644-124">You can create **Connection** objects independently of any other previously defined object.</span></span>

<span data-ttu-id="d5644-125">Можно выполнять команды или хранимые процедуры, как если бы они были методами в **объекте Connection,** как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="d5644-125">You can execute commands or stored procedures as if they were native methods on the **Connection** object, as illustrated below.</span></span>

### <a name="execute-a-command-as-a-native-method-of-a-connection-object"></a><span data-ttu-id="d5644-126">Выполнение команды в качестве нативного метода объекта Connection</span><span class="sxs-lookup"><span data-stu-id="d5644-126">Execute a command as a native method of a Connection object</span></span>

<span data-ttu-id="d5644-127">Чтобы выполнить команду, придать команде имя с помощью свойства **Command** object [Name.](name-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="d5644-127">To execute a command, give the command a name using the **Command** object [Name](name-property-ado.md) property.</span></span> <span data-ttu-id="d5644-128">Установите **подключение** к свойству **ActiveConnection** объекта Command.</span><span class="sxs-lookup"><span data-stu-id="d5644-128">Set the **Command** object's **ActiveConnection** property to the connection.</span></span> <span data-ttu-id="d5644-129">Затем выдают заявление, в котором имя команды используется так, как если бы это был метод объекта **Connection,** за которым следуют любые параметры, а затем объект **Recordset,** если возвращаются какие-либо строки.</span><span class="sxs-lookup"><span data-stu-id="d5644-129">Then issue a statement where the command name is used as if it were a method on the **Connection** object, followed by any parameters, then followed by a **Recordset** object if any rows are returned.</span></span> <span data-ttu-id="d5644-130">Настройте **свойства Набора** записей, чтобы настроить итоговую **настройку набора записей.**</span><span class="sxs-lookup"><span data-stu-id="d5644-130">Set the **Recordset** properties to customize the resulting **Recordset**.</span></span> <span data-ttu-id="d5644-131">Например:</span><span class="sxs-lookup"><span data-stu-id="d5644-131">For example:</span></span>

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

### <a name="execute-a-stored-procedure-as-a-native-method-of-a-connection-object"></a><span data-ttu-id="d5644-132">Выполнение хранимой процедуры в качестве метода объекта Connection</span><span class="sxs-lookup"><span data-stu-id="d5644-132">Execute a stored procedure as a native method of a Connection object</span></span>

<span data-ttu-id="d5644-133">Чтобы выполнить хранимую процедуру, выдают заявление, в котором имя хранимой процедуры используется так, как если бы это был метод объекта **Connection,** за которым следуют любые параметры.</span><span class="sxs-lookup"><span data-stu-id="d5644-133">To execute a stored procedure, issue a statement where the stored procedure name is used as if it were a method on the **Connection** object, followed by any parameters.</span></span> <span data-ttu-id="d5644-134">ADO сделает "лучшее предположение" о типах параметров.</span><span class="sxs-lookup"><span data-stu-id="d5644-134">ADO will make a "best guess" of parameter types.</span></span> <span data-ttu-id="d5644-135">Пример:</span><span class="sxs-lookup"><span data-stu-id="d5644-135">For example:</span></span>

```vb
    Dim cnn As New ADODB.Connection
    ...
    'Your stored procedure name and any parameters.
    cnn.sp_yourStoredProcedureName "parameter"
```
