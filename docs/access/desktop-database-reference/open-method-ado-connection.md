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
# <a name="open-method-ado-connection"></a><span data-ttu-id="b2239-102">Метод Open (Connection в ADO)</span><span class="sxs-lookup"><span data-stu-id="b2239-102">Open method (ADO Connection)</span></span>

<span data-ttu-id="b2239-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b2239-103">**Applies to**: Access 2013, Office 2013</span></span>
 
<span data-ttu-id="b2239-104">Открывает подключение к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="b2239-104">Opens a connection to a data source.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2239-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b2239-105">Syntax</span></span>

<span data-ttu-id="b2239-106">*подключение*. Open *ConnectionString*, *UserID*, *Пароль*, *Параметры*</span><span class="sxs-lookup"><span data-stu-id="b2239-106">*connection*.Open *ConnectionString*, *UserID*, *Password*, *Options*</span></span>

## <a name="parameters"></a><span data-ttu-id="b2239-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b2239-107">Parameters</span></span>

|<span data-ttu-id="b2239-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="b2239-108">Parameter</span></span>|<span data-ttu-id="b2239-109">Описание</span><span class="sxs-lookup"><span data-stu-id="b2239-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="b2239-110">*ConnectionString*</span><span class="sxs-lookup"><span data-stu-id="b2239-110">*ConnectionString*</span></span> |<span data-ttu-id="b2239-111">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="b2239-111">Optional.</span></span> <span data-ttu-id="b2239-112">Значение **String,** содержаное сведения о подключении.</span><span class="sxs-lookup"><span data-stu-id="b2239-112">A **String** value that contains connection information.</span></span> <span data-ttu-id="b2239-113">Сведения о допустимом параметре см. в свойстве [ConnectionString.](connectionstring-property-ado.md)</span><span class="sxs-lookup"><span data-stu-id="b2239-113">See the [ConnectionString](connectionstring-property-ado.md) property for details on valid settings.</span></span>|
|<span data-ttu-id="b2239-114">*UserID*</span><span class="sxs-lookup"><span data-stu-id="b2239-114">*UserID*</span></span> |<span data-ttu-id="b2239-115">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="b2239-115">Optional.</span></span> <span data-ttu-id="b2239-116">Значение **String,** которое содержит имя пользователя, которое необходимо использовать при создании подключения.</span><span class="sxs-lookup"><span data-stu-id="b2239-116">A **String** value that contains a user name to use when establishing the connection.</span></span>|
|<span data-ttu-id="b2239-117">*Password*</span><span class="sxs-lookup"><span data-stu-id="b2239-117">*Password*</span></span> |<span data-ttu-id="b2239-118">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="b2239-118">Optional.</span></span> <span data-ttu-id="b2239-119">Значение **String,** которое содержит пароль, который необходимо использовать при создании подключения.</span><span class="sxs-lookup"><span data-stu-id="b2239-119">A **String** value that contains a password to use when establishing the connection.</span></span>|
|<span data-ttu-id="b2239-120">*Options*</span><span class="sxs-lookup"><span data-stu-id="b2239-120">*Options*</span></span> |<span data-ttu-id="b2239-121">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="b2239-121">Optional.</span></span> <span data-ttu-id="b2239-122">Установлено [значение ConnectOptionEnum,](connectoptionenum.md) которое определяет, должен ли этот метод возвращаться после (синхронно) или до (асинхронно) подключения.</span><span class="sxs-lookup"><span data-stu-id="b2239-122">A [ConnectOptionEnum](connectoptionenum.md) value that determines whether this method should return after (synchronously) or before (asynchronously) the connection is established.</span></span>|

## <a name="remarks"></a><span data-ttu-id="b2239-123">Примечания</span><span class="sxs-lookup"><span data-stu-id="b2239-123">Remarks</span></span>

<span data-ttu-id="b2239-124">Использование метода **Open** на [объекте Подключение](connection-object-ado.md) устанавливает физическое подключение к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="b2239-124">Using the **Open** method on a [Connection](connection-object-ado.md) object establishes the physical connection to a data source.</span></span> <span data-ttu-id="b2239-125">После успешного завершения этого метода подключение будет подключено в прямом эфире, и вы сможете выдавать ему команды и обрабатывать результаты.</span><span class="sxs-lookup"><span data-stu-id="b2239-125">After this method successfully completes, the connection is live and you can issue commands against it and process the results.</span></span>

<span data-ttu-id="b2239-126">Используйте необязательный аргумент *ConnectionString,* чтобы указать строку подключения, содержащую серию аргументов  *=* операторов значений, разделенных зайколонами, или файл или ресурс каталога, идентифицированный с URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="b2239-126">Use the optional *ConnectionString* argument to specify either a connection string containing a series of *argument* *= value* statements separated by semicolons, or a file or directory resource identified with a URL.</span></span> <span data-ttu-id="b2239-127">Свойство **ConnectionString** автоматически наследует значение, используемую для *аргумента ConnectionString.*</span><span class="sxs-lookup"><span data-stu-id="b2239-127">The **ConnectionString** property automatically inherits the value used for the *ConnectionString* argument.</span></span> <span data-ttu-id="b2239-128">Поэтому перед открытием объекта ConnectionString можно  либо задать свойство **ConnectionString,** либо использовать аргумент *ConnectionString* для задания или переопределения текущих параметров подключения во время вызова метода **Open.**</span><span class="sxs-lookup"><span data-stu-id="b2239-128">Therefore, you can either set the **ConnectionString** property of the **Connection** object before opening it, or use the *ConnectionString* argument to set or override the current connection parameters during the **Open** method call.</span></span>

<span data-ttu-id="b2239-129">Если вы передаете сведения о пользователях и паролях как в *аргументе ConnectionString,* так и в необязательных аргументах *UserID* и *Password,* аргументы *UserID* и *Password* переопределяют значения, указанные в *ConnectionString.*</span><span class="sxs-lookup"><span data-stu-id="b2239-129">If you pass user and password information both in the *ConnectionString* argument and in the optional *UserID* and *Password* arguments, the *UserID* and *Password* arguments will override the values specified in *ConnectionString*.</span></span>

<span data-ttu-id="b2239-130">Когда вы завершили операции по открытому подключению, используйте метод [Close,](close-method-ado.md) чтобы освободить все связанные ресурсы системы.</span><span class="sxs-lookup"><span data-stu-id="b2239-130">When you have concluded your operations over an open **Connection**, use the [Close](close-method-ado.md) method to free any associated system resources.</span></span> <span data-ttu-id="b2239-131">Закрытие объекта не удаляет его из памяти; Вы можете изменить его параметры свойств и использовать метод **Open,** чтобы открыть его снова позже.</span><span class="sxs-lookup"><span data-stu-id="b2239-131">Closing an object does not remove it from memory; you can change its property settings and use the **Open** method to open it again later.</span></span> <span data-ttu-id="b2239-132">Чтобы полностью исключить объект из памяти, установите переменную объекта *в Nothing*.</span><span class="sxs-lookup"><span data-stu-id="b2239-132">To completely eliminate an object from memory, set the object variable to *Nothing*.</span></span>

<span data-ttu-id="b2239-133">**Удаленное использование службы данных** При этом метод **Open** не устанавливает подключение к серверу до открытия [recordset](recordset-object-ado.md) на  **объекте Подключение.**</span><span class="sxs-lookup"><span data-stu-id="b2239-133">**Remote Data Service Usage** When used on a client-side **Connection** object, the **Open** method doesn't actually establish a connection to the server until a [Recordset](recordset-object-ado.md) is opened on the **Connection** object.</span></span>

> [!NOTE]
> <span data-ttu-id="b2239-134">URL-адреса, использующие схему http, автоматически вызывают поставщика DB Microsoft [OLE для публикации в Интернете.](microsoft-ole-db-provider-for-internet-publishing.md)</span><span class="sxs-lookup"><span data-stu-id="b2239-134">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="b2239-135">Дополнительные сведения см. в [url-адресах Absolute и relative.](absolute-and-relative-urls.md)</span><span class="sxs-lookup"><span data-stu-id="b2239-135">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


