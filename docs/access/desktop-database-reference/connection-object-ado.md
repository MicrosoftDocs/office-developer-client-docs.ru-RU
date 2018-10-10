---
title: Connection Object (ADO)
TOCTitle: Connection Object (ADO)
ms:assetid: c16023aa-0321-2513-ee71-255d6ffba03d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249940(v=office.15)
ms:contentKeyID: 48547528
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231105
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 723abd44c8e1c5c502167d4499e1995b9ebd1bb3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480998"
---
# <a name="connection-object-ado"></a><span data-ttu-id="a99ff-102">Connection Object (ADO)</span><span class="sxs-lookup"><span data-stu-id="a99ff-102">Connection Object (ADO)</span></span>

<span data-ttu-id="a99ff-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a99ff-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="a99ff-104">Представляет открытое подключение к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="a99ff-104">Represents an open connection to a data source.</span></span>

## <a name="remarks"></a><span data-ttu-id="a99ff-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="a99ff-105">Remarks</span></span>

<span data-ttu-id="a99ff-106">Объект **подключения** представляет собой уникальный сеанс с источником данных.</span><span class="sxs-lookup"><span data-stu-id="a99ff-106">A **Connection** object represents a unique session with a data source.</span></span> <span data-ttu-id="a99ff-107">В случае системы клиента и сервера базы данных может быть эквивалентен действительное сетевое подключение к серверу.</span><span class="sxs-lookup"><span data-stu-id="a99ff-107">In the case of a client/server database system, it may be equivalent to an actual network connection to the server.</span></span> <span data-ttu-id="a99ff-108">В зависимости от функциональных возможностей, поддерживаемых поставщика, некоторые семейств сайтов, методов или свойств **подключения** объекта могут быть недоступны.</span><span class="sxs-lookup"><span data-stu-id="a99ff-108">Depending on the functionality supported by the provider, some collections, methods, or properties of a **Connection** object may not be available.</span></span>

<span data-ttu-id="a99ff-109">С помощью семейства сайтов, методы и свойства объекта **подключения** выполните следующее:</span><span class="sxs-lookup"><span data-stu-id="a99ff-109">With the collections, methods, and properties of a **Connection** object, you can do the following:</span></span>

  - <span data-ttu-id="a99ff-110">Настройка подключения к перед открытием с помощью свойства [ConnectionString](connectionstring-property-ado.md), [ConnectionTimeout](connectiontimeout-property-ado.md)и [режиме](mode-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="a99ff-110">Configure the connection before opening it with the [ConnectionString](connectionstring-property-ado.md), [ConnectionTimeout](connectiontimeout-property-ado.md), and [Mode](mode-property-ado.md) properties.</span></span> <span data-ttu-id="a99ff-111">**ConnectionString** является свойством по умолчанию объекта **подключения** .</span><span class="sxs-lookup"><span data-stu-id="a99ff-111">**ConnectionString** is the default property of the **Connection** object.</span></span>

  - <span data-ttu-id="a99ff-112">Присвойте свойству [CursorLocation](cursorlocation-property-ado.md) для клиента для вызова [Службы Microsoft курсора для OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md), которая поддерживает пакета обновления.</span><span class="sxs-lookup"><span data-stu-id="a99ff-112">Set the [CursorLocation](cursorlocation-property-ado.md) property to client to invoke the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md), which supports batch updates.</span></span>

  - <span data-ttu-id="a99ff-113">Настройка базы данных по умолчанию для подключения со свойством [DefaultDatabase](defaultdatabase-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="a99ff-113">Set the default database for the connection with the [DefaultDatabase](defaultdatabase-property-ado.md) property.</span></span>

  - <span data-ttu-id="a99ff-114">Задайте уровень изоляции для транзакций, открытых на подключение с помощью свойства [IsolationLevel](isolationlevel-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="a99ff-114">Set the level of isolation for the transactions opened on the connection with the [IsolationLevel](isolationlevel-property-ado.md) property.</span></span>

  - <span data-ttu-id="a99ff-115">Укажите поставщика OLE DB с помощью свойства [поставщика](provider-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="a99ff-115">Specify an OLE DB provider with the [Provider](provider-property-ado.md) property.</span></span>

  - <span data-ttu-id="a99ff-116">Установить и более поздних версий приостановки выполнения, физическое подключение к источнику данных с помощью методов [открытия](open-method-ado-connection.md) и [закрытия](close-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="a99ff-116">Establish, and later break, the physical connection to the data source with the [Open](open-method-ado-connection.md) and [Close](close-method-ado.md) methods.</span></span>

  - <span data-ttu-id="a99ff-117">Выполнить команду на подключение с помощью метода [Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\)) и настройте выполнения со свойством [CommandTimeout](commandtimeout-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="a99ff-117">Execute a command on the connection with the [Execute](https://msdn.microsoft.com/library/jj249832\(v=office.15\)) method and configure the execution with the [CommandTimeout](commandtimeout-property-ado.md) property.</span></span>
    

    > [!NOTE]
    > <span data-ttu-id="a99ff-118">Для выполнения запроса без использования объекта команды, передайте строку запроса метода **Execute** объекта **подключения** .</span><span class="sxs-lookup"><span data-stu-id="a99ff-118">To execute a query without using a Command object, pass a query string to the **Execute** method of a **Connection** object.</span></span> <span data-ttu-id="a99ff-119">Тем не менее объект [команды](command-object-ado.md) является обязательным, когда необходимо сохранять текст команды и повторно выполнить или используйте параметры запроса.</span><span class="sxs-lookup"><span data-stu-id="a99ff-119">However, a [Command](command-object-ado.md) object is required when you want to persist the command text and re-execute it, or use query parameters.</span></span>

  - <span data-ttu-id="a99ff-120">Управление транзакций на открытое подключение, включая вложенные транзакции, если поставщик поддерживает их, с помощью [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md)и [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) методы и свойства [атрибутов](attributes-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="a99ff-120">Manage transactions on the open connection, including nested transactions if the provider supports them, with the [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md), [CommitTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md), and [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md) methods and the [Attributes](attributes-property-ado.md) property.</span></span>

  - <span data-ttu-id="a99ff-121">Проверки на наличие ошибок, возвращаемых из источника данных с помощью семейства [Errors](errors-collection-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="a99ff-121">Examine errors returned from the data source with the [Errors](errors-collection-ado.md) collection.</span></span>

  - <span data-ttu-id="a99ff-122">Прочитайте версию от реализации ADO используется совместно со свойством [версии](version-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="a99ff-122">Read the version from the ADO implementation used with the [Version](version-property-ado.md) property.</span></span>

  - <span data-ttu-id="a99ff-123">Получите сведения о схеме о базе данных с помощью метода [OpenSchema](openschema-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="a99ff-123">Obtain schema information about your database with the [OpenSchema](openschema-method-ado.md) method.</span></span>

<span data-ttu-id="a99ff-124">Можно создать объекты **подключения** независимо от других ранее определенный объект.</span><span class="sxs-lookup"><span data-stu-id="a99ff-124">You can create **Connection** objects independently of any other previously defined object.</span></span>

<span data-ttu-id="a99ff-125">Можно выполнять команды или хранимые процедуры, как если бы они собственные методы объекта **подключения** , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="a99ff-125">You can execute commands or stored procedures as if they were native methods on the **Connection** object, as illustrated below.</span></span>

### <a name="execute-a-command-as-a-native-method-of-a-connection-object"></a><span data-ttu-id="a99ff-126">Выполнить команду как собственный метод объект подключения</span><span class="sxs-lookup"><span data-stu-id="a99ff-126">Execute a command as a native method of a Connection object</span></span>

<span data-ttu-id="a99ff-127">Для выполнения команды, имя команды с помощью объекта **команду** свойства [Name](name-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="a99ff-127">To execute a command, give the command a name using the **Command** object [Name](name-property-ado.md) property.</span></span> <span data-ttu-id="a99ff-128">Объект **команды** **ActiveConnection** для свойства подключения.</span><span class="sxs-lookup"><span data-stu-id="a99ff-128">Set the **Command** object's **ActiveConnection** property to the connection.</span></span> <span data-ttu-id="a99ff-129">Затем проблему объекта оператор которых используется имя команды, как если бы метод на **подключение** , следуют любые параметры, затем следуют объекта **набора записей** , если возвращаются все строки.</span><span class="sxs-lookup"><span data-stu-id="a99ff-129">Then issue a statement where the command name is used as if it were a method on the **Connection** object, followed by any parameters, then followed by a **Recordset** object if any rows are returned.</span></span> <span data-ttu-id="a99ff-130">Задайте свойства **набора записей** для настройки результирующего **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="a99ff-130">Set the **Recordset** properties to customize the resulting **Recordset**.</span></span> <span data-ttu-id="a99ff-131">Пример:</span><span class="sxs-lookup"><span data-stu-id="a99ff-131">For example:</span></span>

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

### <a name="execute-a-stored-procedure-as-a-native-method-of-a-connection-object"></a><span data-ttu-id="a99ff-132">Выполнить хранимую процедуру как собственный метод объект подключения</span><span class="sxs-lookup"><span data-stu-id="a99ff-132">Execute a stored procedure as a native method of a Connection object</span></span>

<span data-ttu-id="a99ff-133">Чтобы выполнить хранимую процедуру, используйте оператор которых используется имя хранимой процедуры, как если бы метод на объект **подключения** , а затем каких-либо параметров.</span><span class="sxs-lookup"><span data-stu-id="a99ff-133">To execute a stored procedure, issue a statement where the stored procedure name is used as if it were a method on the **Connection** object, followed by any parameters.</span></span> <span data-ttu-id="a99ff-134">ADO сделает «наиболее подходящий» типы параметров.</span><span class="sxs-lookup"><span data-stu-id="a99ff-134">ADO will make a "best guess" of parameter types.</span></span> <span data-ttu-id="a99ff-135">Например:</span><span class="sxs-lookup"><span data-stu-id="a99ff-135">For example:</span></span>

```vb
    Dim cnn As New ADODB.Connection
    ...
    'Your stored procedure name and any parameters.
    cnn.sp_yourStoredProcedureName "parameter"
```
