---
title: Метод Open (Connection в ADO)
TOCTitle: Open method (ADO Connection)
ms:assetid: 1adaa17d-dfe1-22e0-3415-720516d138f8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248951(v=office.15)
ms:contentKeyID: 48543525
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b3b83eb87b181320c86e1aea91ede70cd173a5ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288429"
---
# <a name="open-method-ado-connection"></a><span data-ttu-id="5fc78-102">Метод Open (Connection в ADO)</span><span class="sxs-lookup"><span data-stu-id="5fc78-102">Open method (ADO Connection)</span></span>

<span data-ttu-id="5fc78-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5fc78-103">**Applies to**: Access 2013, Office 2013</span></span>
 
<span data-ttu-id="5fc78-104">Открывает подключение к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="5fc78-104">Opens a connection to a data source.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fc78-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5fc78-105">Syntax</span></span>

<span data-ttu-id="5fc78-106">*connection .* Open *ConnectionString*, *UserID*, *Password*, *Options*</span><span class="sxs-lookup"><span data-stu-id="5fc78-106">*connection*.Open *ConnectionString*, *UserID*, *Password*, *Options*</span></span>

## <a name="parameters"></a><span data-ttu-id="5fc78-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="5fc78-107">Parameters</span></span>

|<span data-ttu-id="5fc78-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="5fc78-108">Parameter</span></span>|<span data-ttu-id="5fc78-109">Описание</span><span class="sxs-lookup"><span data-stu-id="5fc78-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="5fc78-110">*ConnectionString*</span><span class="sxs-lookup"><span data-stu-id="5fc78-110">*ConnectionString*</span></span> |<span data-ttu-id="5fc78-111">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="5fc78-111">Optional.</span></span> <span data-ttu-id="5fc78-112">**Строковая** строка, содержаная сведения о под подключениех.</span><span class="sxs-lookup"><span data-stu-id="5fc78-112">A **String** value that contains connection information.</span></span> <span data-ttu-id="5fc78-113">Сведения о допустимом параметре см. в свойстве [ConnectionString.](connectionstring-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="5fc78-113">See the [ConnectionString](connectionstring-property-ado.md) property for details on valid settings.</span></span>|
|<span data-ttu-id="5fc78-114">*UserID*</span><span class="sxs-lookup"><span data-stu-id="5fc78-114">*UserID*</span></span> |<span data-ttu-id="5fc78-115">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="5fc78-115">Optional.</span></span> <span data-ttu-id="5fc78-116">**Строка,** которая содержит имя пользователя, которое будет применяться при установлении подключения.</span><span class="sxs-lookup"><span data-stu-id="5fc78-116">A **String** value that contains a user name to use when establishing the connection.</span></span>|
|<span data-ttu-id="5fc78-117">*Password*</span><span class="sxs-lookup"><span data-stu-id="5fc78-117">*Password*</span></span> |<span data-ttu-id="5fc78-118">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="5fc78-118">Optional.</span></span> <span data-ttu-id="5fc78-119">**Строка,** содержаная пароль, который будет применяться при установлении подключения.</span><span class="sxs-lookup"><span data-stu-id="5fc78-119">A **String** value that contains a password to use when establishing the connection.</span></span>|
|<span data-ttu-id="5fc78-120">*Options*</span><span class="sxs-lookup"><span data-stu-id="5fc78-120">*Options*</span></span> |<span data-ttu-id="5fc78-121">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="5fc78-121">Optional.</span></span> <span data-ttu-id="5fc78-122">Значение [ConnectOptionEnum,](connectoptionenum.md) которое определяет, должен ли этот метод возвращаться после (синхронно) или до (асинхронно) установления подключения.</span><span class="sxs-lookup"><span data-stu-id="5fc78-122">A [ConnectOptionEnum](connectoptionenum.md) value that determines whether this method should return after (synchronously) or before (asynchronously) the connection is established.</span></span>|

## <a name="remarks"></a><span data-ttu-id="5fc78-123">Заметки</span><span class="sxs-lookup"><span data-stu-id="5fc78-123">Remarks</span></span>

<span data-ttu-id="5fc78-124">Использование метода **Open** для объекта [Connection](connection-object-ado.md) устанавливает физическое подключение к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="5fc78-124">Using the **Open** method on a [Connection](connection-object-ado.md) object establishes the physical connection to a data source.</span></span> <span data-ttu-id="5fc78-125">После успешного завершения этого метода подключение будет подключено к сети, и вы сможете выполнить команды для него и обработать результаты.</span><span class="sxs-lookup"><span data-stu-id="5fc78-125">After this method successfully completes, the connection is live and you can issue commands against it and process the results.</span></span>

<span data-ttu-id="5fc78-126">Используйте необязательный аргумент *ConnectionString,* чтобы указать строку подключения, содержащую серию аргументов  *=* операторов значений, разделенных точкими с заточки, или файл или ресурс каталога, идентифицированный с помощью URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="5fc78-126">Use the optional *ConnectionString* argument to specify either a connection string containing a series of *argument* *= value* statements separated by semicolons, or a file or directory resource identified with a URL.</span></span> <span data-ttu-id="5fc78-127">Свойство **ConnectionString** автоматически наследует значение, используемую для *аргумента ConnectionString.*</span><span class="sxs-lookup"><span data-stu-id="5fc78-127">The **ConnectionString** property automatically inherits the value used for the *ConnectionString* argument.</span></span> <span data-ttu-id="5fc78-128">Поэтому можно либо установить свойство **ConnectionString** объекта **Connection** перед его открытием, либо использовать аргумент *ConnectionString,* чтобы установить или переопредить текущие параметры подключения во время вызова метода **Open.**</span><span class="sxs-lookup"><span data-stu-id="5fc78-128">Therefore, you can either set the **ConnectionString** property of the **Connection** object before opening it, or use the *ConnectionString* argument to set or override the current connection parameters during the **Open** method call.</span></span>

<span data-ttu-id="5fc78-129">Если передать сведения о пользователе и пароле как в *аргументе ConnectionString,* так и в необязательных аргументах *UserID* и *Password,* аргументы *UserID* и *Password* будут переопределять значения, указанные в *ConnectionString.*</span><span class="sxs-lookup"><span data-stu-id="5fc78-129">If you pass user and password information both in the *ConnectionString* argument and in the optional *UserID* and *Password* arguments, the *UserID* and *Password* arguments will override the values specified in *ConnectionString*.</span></span>

<span data-ttu-id="5fc78-130">После того как вы завершили операции по открытому подключению, используйте метод [Close,](close-method-ado.md) чтобы освободить все связанные системные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="5fc78-130">When you have concluded your operations over an open **Connection**, use the [Close](close-method-ado.md) method to free any associated system resources.</span></span> <span data-ttu-id="5fc78-131">Закрытие объекта не удаляет его из памяти; Вы можете изменить его параметры свойств и использовать метод **Open,** чтобы открыть его позже.</span><span class="sxs-lookup"><span data-stu-id="5fc78-131">Closing an object does not remove it from memory; you can change its property settings and use the **Open** method to open it again later.</span></span> <span data-ttu-id="5fc78-132">Чтобы полностью исключить объект из памяти, установите для объектной переменной значение *Nothing.*</span><span class="sxs-lookup"><span data-stu-id="5fc78-132">To completely eliminate an object from memory, set the object variable to *Nothing*.</span></span>

<span data-ttu-id="5fc78-133">**Использование удаленной службы данных** При этом метод **Open** не устанавливает подключение к серверу, пока в объекте **Connection** не откроется набор **записей.** [](recordset-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="5fc78-133">**Remote Data Service Usage** When used on a client-side **Connection** object, the **Open** method doesn't actually establish a connection to the server until a [Recordset](recordset-object-ado.md) is opened on the **Connection** object.</span></span>

> [!NOTE]
> <span data-ttu-id="5fc78-134">URL-адреса, использующие схему HTTP, автоматически вызывают поставщика [Microsoft OLE DB для интернет-публикации.](microsoft-ole-db-provider-for-internet-publishing.md)</span><span class="sxs-lookup"><span data-stu-id="5fc78-134">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="5fc78-135">Дополнительные сведения см. в [сведениях об абсолютных и относительных URL-адресах.](absolute-and-relative-urls.md)</span><span class="sxs-lookup"><span data-stu-id="5fc78-135">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


