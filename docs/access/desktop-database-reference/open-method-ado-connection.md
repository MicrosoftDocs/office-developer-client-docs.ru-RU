---
title: Open Method (ADO Connection)
TOCTitle: Open Method (ADO Connection)
ms:assetid: 1adaa17d-dfe1-22e0-3415-720516d138f8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248951(v=office.15)
ms:contentKeyID: 48543525
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 78c20ce6da4c20385bd22488ce910312c737986e
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606334"
---
# <a name="open-method-ado-connection"></a><span data-ttu-id="56524-102">Open Method (ADO Connection)</span><span class="sxs-lookup"><span data-stu-id="56524-102">Open Method (ADO Connection)</span></span>


<span data-ttu-id="56524-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="56524-103">**Applies to**: Access 2013 | Office 2013</span></span>
 

<span data-ttu-id="56524-104">Открывает подключение к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="56524-104">Opens a connection to a data source.</span></span>

## <a name="syntax"></a><span data-ttu-id="56524-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="56524-105">Syntax</span></span>

<span data-ttu-id="56524-106">*подключение*. Откройте*ConnectionString*, *идентификатор пользователя*, *пароль*, *Параметры*</span><span class="sxs-lookup"><span data-stu-id="56524-106">*connection*.Open*ConnectionString*, *UserID*, *Password*, *Options*</span></span>

## <a name="parameters"></a><span data-ttu-id="56524-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="56524-107">Parameters</span></span>

  - <span data-ttu-id="56524-108">*ConnectionString*</span><span class="sxs-lookup"><span data-stu-id="56524-108">*ConnectionString*</span></span>

  - <span data-ttu-id="56524-109">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="56524-109">Optional.</span></span> <span data-ttu-id="56524-110">**Строковое** значение, содержащее сведения о подключении.</span><span class="sxs-lookup"><span data-stu-id="56524-110">A **String** value that contains connection information.</span></span> <span data-ttu-id="56524-111">Свойство [ConnectionString](connectionstring-property-ado.md) для получения дополнительных сведений см на допустимые значения.</span><span class="sxs-lookup"><span data-stu-id="56524-111">See the [ConnectionString](connectionstring-property-ado.md) property for details on valid settings.</span></span>

  - <span data-ttu-id="56524-112">*Идентификатор пользователя*</span><span class="sxs-lookup"><span data-stu-id="56524-112">*UserID*</span></span>

  - <span data-ttu-id="56524-113">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="56524-113">Optional.</span></span> <span data-ttu-id="56524-114">**Строковое** значение, которое содержит имя пользователя для использования при установке подключения.</span><span class="sxs-lookup"><span data-stu-id="56524-114">A **String** value that contains a user name to use when establishing the connection.</span></span>

  - <span data-ttu-id="56524-115">*Password*</span><span class="sxs-lookup"><span data-stu-id="56524-115">*Password*</span></span>

  - <span data-ttu-id="56524-116">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="56524-116">Optional.</span></span> <span data-ttu-id="56524-117">**Строковое** значение, содержащее пароль для использования при установке подключения.</span><span class="sxs-lookup"><span data-stu-id="56524-117">A **String** value that contains a password to use when establishing the connection.</span></span>

  - <span data-ttu-id="56524-118">*Варианты*</span><span class="sxs-lookup"><span data-stu-id="56524-118">*Options*</span></span>

  - <span data-ttu-id="56524-119">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="56524-119">Optional.</span></span> <span data-ttu-id="56524-120">[ConnectOptionEnum](connectoptionenum.md) значение, определяющее, будет ли этот метод должен возвращать после (синхронно) или до (асинхронно) подключения.</span><span class="sxs-lookup"><span data-stu-id="56524-120">A [ConnectOptionEnum](connectoptionenum.md) value that determines whether this method should return after (synchronously) or before (asynchronously) the connection is established.</span></span>

## <a name="remarks"></a><span data-ttu-id="56524-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="56524-121">Remarks</span></span>

<span data-ttu-id="56524-122">С помощью метода **Open** объекта [подключения](connection-object-ado.md) устанавливает физических подключение к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="56524-122">Using the **Open** method on a [Connection](connection-object-ado.md) object establishes the physical connection to a data source.</span></span> <span data-ttu-id="56524-123">После успешного завершения этого метода подключения live можно и выполнение команд его обработки результатов.</span><span class="sxs-lookup"><span data-stu-id="56524-123">After this method successfully completes, the connection is live and you can issue commands against it and process the results.</span></span>

<span data-ttu-id="56524-124">Используйте необязательный аргумент *ConnectionString* , чтобы указать либо строку подключения, содержащую последовательность операторов *= значение* *аргумента* , разделенные точкой с запятой или файла ресурсов каталогов с помощью URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="56524-124">Use the optional *ConnectionString* argument to specify either a connection string containing a series of *argument* *= value* statements separated by semicolons, or a file or directory resource identified with a URL.</span></span> <span data-ttu-id="56524-125">Свойство **ConnectionString** автоматически наследует значение, используемое для аргумента *ConnectionString* .</span><span class="sxs-lookup"><span data-stu-id="56524-125">The **ConnectionString** property automatically inherits the value used for the *ConnectionString* argument.</span></span> <span data-ttu-id="56524-126">Таким образом можно использовать свойство **ConnectionString** объекта **подключения** перед открытием, или используйте аргумент *ConnectionString* задать или переопределить параметры подключения к текущей во время вызова метода **Open** .</span><span class="sxs-lookup"><span data-stu-id="56524-126">Therefore, you can either set the **ConnectionString** property of the **Connection** object before opening it, or use the *ConnectionString* argument to set or override the current connection parameters during the **Open** method call.</span></span>

<span data-ttu-id="56524-127">Если пользователя и пароль, передается в аргументе *ConnectionString* и необязательные аргументы *идентификатор пользователя* и *пароль* , *идентификатор пользователя* и *пароль* аргументы переопределяет значения, заданные в \* ConnectionString\*.</span><span class="sxs-lookup"><span data-stu-id="56524-127">If you pass user and password information both in the *ConnectionString* argument and in the optional *UserID* and *Password* arguments, the *UserID* and *Password* arguments will override the values specified in *ConnectionString*.</span></span>

<span data-ttu-id="56524-128">Когда заключения операции вами через открытое **подключение**, используйте метод [Close](close-method-ado.md) чтобы освободить место на все связанные системные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="56524-128">When you have concluded your operations over an open **Connection**, use the [Close](close-method-ado.md) method to free any associated system resources.</span></span> <span data-ttu-id="56524-129">Закрытие объект не удаляется из памяти; можно изменить параметры его свойства и использовать метод **Open** для открытия попытку позже.</span><span class="sxs-lookup"><span data-stu-id="56524-129">Closing an object does not remove it from memory; you can change its property settings and use the **Open** method to open it again later.</span></span> <span data-ttu-id="56524-130">Чтобы полностью удалить объект из памяти, задайте объектной переменной значение *Nothing*.</span><span class="sxs-lookup"><span data-stu-id="56524-130">To completely eliminate an object from memory, set the object variable to *Nothing*.</span></span>

<span data-ttu-id="56524-131">**Службы удаленных данных об использовании** При использовании на объект **подключения** со стороны клиента, метод **Open** не устанавливает фактически подключения к серверу пока не открывается [набор записей](recordset-object-ado.md) в объекте **подключений** .</span><span class="sxs-lookup"><span data-stu-id="56524-131">**Remote Data Service Usage**When used on a client-side **Connection** object, the **Open** method doesn't actually establish a connection to the server until a [Recordset](recordset-object-ado.md) is opened on the **Connection** object.</span></span>


> [!NOTE]
<span data-ttu-id="56524-132"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="56524-132"><<<<<<< HEAD</span></span>
> <P><span data-ttu-id="56524-133">URL-адреса, с помощью схемы http автоматически вызывает <A href="microsoft-ole-db-provider-for-internet-publishing.md">Поставщик Microsoft OLE DB для публикации Интернет</A>.</span><span class="sxs-lookup"><span data-stu-id="56524-133">URLs using the http scheme will automatically invoke the <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>.</span></span> <span data-ttu-id="56524-134">Для получения дополнительных сведений см <A href="absolute-and-relative-urls.md">абсолютного и относительных URL-адресов</A>.</span><span class="sxs-lookup"><span data-stu-id="56524-134">For more information, see <A href="absolute-and-relative-urls.md">Absolute and Relative URLs</A>.</span></span></P>
=======
> <span data-ttu-id="56524-135">URL-адреса, с помощью схемы http автоматически вызывает [Поставщик Microsoft OLE DB для публикации Интернет](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="56524-135">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="56524-136">Для получения дополнительных сведений см [абсолютных и относительных URL-адресов](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="56524-136">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>
>>>>>>> <span data-ttu-id="56524-137">master</span><span class="sxs-lookup"><span data-stu-id="56524-137">master</span></span>


