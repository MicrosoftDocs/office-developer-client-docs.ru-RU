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
ms.openlocfilehash: 7fc8648f40e38020e84393e71d0a269a6ba7a6d7
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25922267"
---
# <a name="command-object-ado"></a><span data-ttu-id="b8235-102">Объект Command (ADO)</span><span class="sxs-lookup"><span data-stu-id="b8235-102">Command object (ADO)</span></span>


<span data-ttu-id="b8235-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b8235-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b8235-104">Определяет определенной команде, которые планируется выполнить в источнике данных.</span><span class="sxs-lookup"><span data-stu-id="b8235-104">Defines a specific command that you intend to execute against a data source.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8235-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="b8235-105">Remarks</span></span>

<span data-ttu-id="b8235-106">Использование объекта **команды** для запроса базы данных и возврата записей в объекте [набора записей](recordset-object-ado.md) для выполнения операции массового или для работы с структуры базы данных.</span><span class="sxs-lookup"><span data-stu-id="b8235-106">Use a **Command** object to query a database and return records in a [Recordset](recordset-object-ado.md) object, to execute a bulk operation, or to manipulate the structure of a database.</span></span> <span data-ttu-id="b8235-107">В зависимости от функциональности поставщика некоторые **команды** семейств сайтов, методов или свойств может привести к ошибке при обращении к.</span><span class="sxs-lookup"><span data-stu-id="b8235-107">Depending on the functionality of the provider, some **Command** collections, methods, or properties may generate an error when referenced.</span></span>

<span data-ttu-id="b8235-108">С помощью семейства сайтов, методы и свойства объекта **команды** сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="b8235-108">With the collections, methods, and properties of a **Command** object, you can do the following:</span></span>

  - <span data-ttu-id="b8235-109">Определение исполняемый текст команды (например, инструкции SQL) с помощью свойства [CommandText](commandtext-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="b8235-109">Define the executable text of the command (for example, an SQL statement) with the [CommandText](commandtext-property-ado.md) property.</span></span>

  - <span data-ttu-id="b8235-110">Определите запросы с параметрами и аргументами хранимую процедуру с помощью [параметра](parameter-object-ado.md) объекты и коллекции [параметров](parameters-collection-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="b8235-110">Define parameterized queries or stored-procedure arguments with [Parameter](parameter-object-ado.md) objects and the [Parameters](parameters-collection-ado.md) collection.</span></span>

  - <span data-ttu-id="b8235-111">Выполнение команды и возвратить объект **набора записей** при необходимости с помощью метода [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) .</span><span class="sxs-lookup"><span data-stu-id="b8235-111">Execute a command and return a **Recordset** object if appropriate with the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) method.</span></span>

  - <span data-ttu-id="b8235-112">Укажите тип команды со свойством [CommandType](commandtype-property-ado.md) , прежде чем начать выполнение для оптимизации производительности.</span><span class="sxs-lookup"><span data-stu-id="b8235-112">Specify the type of command with the [CommandType](commandtype-property-ado.md) property prior to execution to optimize performance.</span></span>

  - <span data-ttu-id="b8235-113">Определяют, является ли поставщик сохраняет готовую (или скомпилированную) версию команды, прежде чем начать выполнение со свойством [подготовленных](prepared-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="b8235-113">Control whether the provider saves a prepared (or compiled) version of the command prior to execution with the [Prepared](prepared-property-ado.md) property.</span></span>

  - <span data-ttu-id="b8235-114">Задайте число секунд, поставщик будет ожидать команду, чтобы выполнить с помощью свойства [CommandTimeout](commandtimeout-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="b8235-114">Set the number of seconds that a provider will wait for a command to execute with the [CommandTimeout](commandtimeout-property-ado.md) property.</span></span>

  - <span data-ttu-id="b8235-115">Связывание открытое подключение с помощью объекта **команды** , присвоив свойству [ActiveConnection](activeconnection-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="b8235-115">Associate an open connection with a **Command** object by setting its [ActiveConnection](activeconnection-property-ado.md) property.</span></span>

  - <span data-ttu-id="b8235-116">[Имя](name-property-ado.md) свойства для идентификации объекта **команду** как метод на связанный объект [подключения](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="b8235-116">Set the [Name](name-property-ado.md) property to identify the **Command** object as a method on the associated [Connection](connection-object-ado.md) object.</span></span>

  - <span data-ttu-id="b8235-117">Передайте объект **команды** свойства [источника](source-property-ado-recordset.md) **записей** для получения данных.</span><span class="sxs-lookup"><span data-stu-id="b8235-117">Pass a **Command** object to the [Source](source-property-ado-recordset.md) property of a **Recordset** in order to obtain data.</span></span>

  - <span data-ttu-id="b8235-118">Атрибуты поставщика доступа с набором [свойств](properties-collection-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="b8235-118">Access provider-specific attributes with the [Properties](properties-collection-ado.md) collection.</span></span>

> [!NOTE]
> <span data-ttu-id="b8235-119">Для выполнения запроса без использования объекта **команды** , передайте строку запроса для метода [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) объект **подключения** или метод [Open](open-method-ado-recordset.md) объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="b8235-119">To execute a query without using a **Command** object, pass a query string to the [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection) method of a **Connection** object or to the [Open](open-method-ado-recordset.md) method of a **Recordset** object.</span></span> <span data-ttu-id="b8235-120">Тем не менее объект **команды** является обязательным, когда необходимо сохранять текст команды и повторно выполнить или используйте параметры запроса.</span><span class="sxs-lookup"><span data-stu-id="b8235-120">However, a **Command** object is required when you want to persist the command text and re-execute it, or use query parameters.</span></span>

<span data-ttu-id="b8235-121">Для создания объекта **команду** независимо от ранее определенный объект **подключения** , установите для свойства **ActiveConnection** это допустимая строка подключения.</span><span class="sxs-lookup"><span data-stu-id="b8235-121">To create a **Command** object independently of a previously defined **Connection** object, set its **ActiveConnection** property to a valid connection string.</span></span> <span data-ttu-id="b8235-122">ADO по-прежнему создает объект **подключения** , но она не назначает этот объект переменной объекта.</span><span class="sxs-lookup"><span data-stu-id="b8235-122">ADO still creates a **Connection** object, but it doesn't assign that object to an object variable.</span></span> <span data-ttu-id="b8235-123">Тем не менее если несколько объектов **команды** будет сопоставлен то же подключение, необходимо явно создать и откройте объект **подключения** ; Это назначает объект **подключения** объектную переменную.</span><span class="sxs-lookup"><span data-stu-id="b8235-123">However, if you are associating multiple **Command** objects with the same connection, you should explicitly create and open a **Connection** object; this assigns the **Connection** object to an object variable.</span></span> <span data-ttu-id="b8235-124">Если свойства **ActiveConnection** объекта **команды** не установлен на эту переменную объекта, ADO создает новый объект **подключения** для каждого объекта **команды** даже в том случае, если вы используете одну и ту же строку подключения.</span><span class="sxs-lookup"><span data-stu-id="b8235-124">If you do not set the **Command** object's **ActiveConnection** property to this object variable, ADO creates a new **Connection** object for each **Command** object, even if you use the same connection string.</span></span>

<span data-ttu-id="b8235-125">Чтобы выполнить **команду**, просто вызовите, его свойство [имя](name-property-ado.md) на связанный объект **подключения** .</span><span class="sxs-lookup"><span data-stu-id="b8235-125">To execute a **Command**, simply call it by its [Name](name-property-ado.md) property on the associated **Connection** object.</span></span> <span data-ttu-id="b8235-126">**Команда** , должен иметь его свойства **ActiveConnection** объект **подключения** .</span><span class="sxs-lookup"><span data-stu-id="b8235-126">The **Command** must have its **ActiveConnection** property set to the **Connection** object.</span></span> <span data-ttu-id="b8235-127">Если **команда** параметры, передачи их значения как аргументы в метод.</span><span class="sxs-lookup"><span data-stu-id="b8235-127">If the **Command** has parameters, pass their values as arguments to the method.</span></span>

<span data-ttu-id="b8235-128">Если любой из этих объектов **команды** не хранимую процедуру с параметрами вывода два или несколько объектов **команды** выполняются в том же соединении, возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="b8235-128">If two or more **Command** objects are executed on the same connection and either **Command** object is a stored procedure with output parameters, an error occurs.</span></span> <span data-ttu-id="b8235-129">Для выполнения каждого объекта **команды** , используйте отдельные подключения или отключите все другие объекты **команды** от подключения.</span><span class="sxs-lookup"><span data-stu-id="b8235-129">To execute each **Command** object, use separate connections or disconnect all other **Command** objects from the connection.</span></span>

<span data-ttu-id="b8235-130">Коллекция **параметров** является элементом по умолчанию объекта **команды** .</span><span class="sxs-lookup"><span data-stu-id="b8235-130">The **Parameters** collection is the default member of the **Command** object.</span></span> <span data-ttu-id="b8235-131">В результате следующих двух операторов кода эквивалентны.</span><span class="sxs-lookup"><span data-stu-id="b8235-131">As a result, the following two code statements are equivalent.</span></span>

