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
# <a name="open-method-ado-connection"></a><span data-ttu-id="4f2e7-102">Метод Open (Connection в ADO)</span><span class="sxs-lookup"><span data-stu-id="4f2e7-102">Open method (ADO Connection)</span></span>

<span data-ttu-id="4f2e7-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4f2e7-103">**Applies to**: Access 2013, Office 2013</span></span>
 
<span data-ttu-id="4f2e7-104">Открывает подключение к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="4f2e7-104">Opens a connection to a data source.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f2e7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4f2e7-105">Syntax</span></span>

<span data-ttu-id="4f2e7-106">*Подключение*. Открыть*ConnectionString*, *UserID*, *пароль*, *Параметры*</span><span class="sxs-lookup"><span data-stu-id="4f2e7-106">*connection*.Open*ConnectionString*, *UserID*, *Password*, *Options*</span></span>

## <a name="parameters"></a><span data-ttu-id="4f2e7-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4f2e7-107">Parameters</span></span>

|<span data-ttu-id="4f2e7-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="4f2e7-108">Parameter</span></span>|<span data-ttu-id="4f2e7-109">Описание</span><span class="sxs-lookup"><span data-stu-id="4f2e7-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="4f2e7-110">*ConnectionString*</span><span class="sxs-lookup"><span data-stu-id="4f2e7-110">*ConnectionString*</span></span> |<span data-ttu-id="4f2e7-111">Необязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="4f2e7-111">Optional.</span></span> <span data-ttu-id="4f2e7-112">**Строковое** значение, содержащее сведения о подключении.</span><span class="sxs-lookup"><span data-stu-id="4f2e7-112">A **String** value that contains connection information.</span></span> <span data-ttu-id="4f2e7-113">Сведения о допустимых параметрах см. в свойстве [ConnectionString](connectionstring-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="4f2e7-113">See the [ConnectionString](connectionstring-property-ado.md) property for details on valid settings.</span></span>|
|<span data-ttu-id="4f2e7-114">*UserID*</span><span class="sxs-lookup"><span data-stu-id="4f2e7-114">*UserID*</span></span> |<span data-ttu-id="4f2e7-115">Необязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="4f2e7-115">Optional.</span></span> <span data-ttu-id="4f2e7-116">**Строковое** значение, содержащее имя пользователя, используемое при установлении подключения.</span><span class="sxs-lookup"><span data-stu-id="4f2e7-116">A **String** value that contains a user name to use when establishing the connection.</span></span>|
|<span data-ttu-id="4f2e7-117">*Password*</span><span class="sxs-lookup"><span data-stu-id="4f2e7-117">*Password*</span></span> |<span data-ttu-id="4f2e7-118">Необязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="4f2e7-118">Optional.</span></span> <span data-ttu-id="4f2e7-119">**Строковое** значение, содержащее пароль, используемый при установлении подключения.</span><span class="sxs-lookup"><span data-stu-id="4f2e7-119">A **String** value that contains a password to use when establishing the connection.</span></span>|
|<span data-ttu-id="4f2e7-120">*Options*</span><span class="sxs-lookup"><span data-stu-id="4f2e7-120">*Options*</span></span> |<span data-ttu-id="4f2e7-121">Необязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="4f2e7-121">Optional.</span></span> <span data-ttu-id="4f2e7-122">Значение [коннектоптионенум](connectoptionenum.md) , которое определяет, должен ли этот метод возвращаться после (синхронно) или до (асинхронно) подключения.</span><span class="sxs-lookup"><span data-stu-id="4f2e7-122">A [ConnectOptionEnum](connectoptionenum.md) value that determines whether this method should return after (synchronously) or before (asynchronously) the connection is established.</span></span>|

## <a name="remarks"></a><span data-ttu-id="4f2e7-123">Замечания</span><span class="sxs-lookup"><span data-stu-id="4f2e7-123">Remarks</span></span>

<span data-ttu-id="4f2e7-124">При использовании метода **Open** для объекта [Connection](connection-object-ado.md) устанавливается физическое подключение к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="4f2e7-124">Using the **Open** method on a [Connection](connection-object-ado.md) object establishes the physical connection to a data source.</span></span> <span data-ttu-id="4f2e7-125">После успешного завершения этого метода подключение становится активным и вы можете выполнять команды для него и обрабатывать результаты.</span><span class="sxs-lookup"><span data-stu-id="4f2e7-125">After this method successfully completes, the connection is live and you can issue commands against it and process the results.</span></span>

<span data-ttu-id="4f2e7-126">Используйте необязательный аргумент *ConnectionString* для указания строки подключения, содержащей ряд операторов *Argument* *= value* , разделенных точкой с запятой, или файл или ресурс каталога, определенный с URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="4f2e7-126">Use the optional *ConnectionString* argument to specify either a connection string containing a series of *argument* *= value* statements separated by semicolons, or a file or directory resource identified with a URL.</span></span> <span data-ttu-id="4f2e7-127">Свойство **ConnectionString** автоматически наследует значение, используемое для аргумента *ConnectionString* .</span><span class="sxs-lookup"><span data-stu-id="4f2e7-127">The **ConnectionString** property automatically inherits the value used for the *ConnectionString* argument.</span></span> <span data-ttu-id="4f2e7-128">Таким образом, можно задать свойство **ConnectionString** для объекта **Connection** перед его открытием или использовать аргумент *ConnectionString* для установки или переопределения текущих параметров подключения во время вызова метода **Open** . .</span><span class="sxs-lookup"><span data-stu-id="4f2e7-128">Therefore, you can either set the **ConnectionString** property of the **Connection** object before opening it, or use the *ConnectionString* argument to set or override the current connection parameters during the **Open** method call.</span></span>

<span data-ttu-id="4f2e7-129">Если вы передаете сведения о пользователе и пароле в аргументе *ConnectionString* и в необязательных аргументах *UserID* и Password, аргументы *UserID* и *Password* переопределяют значения, указанные в \*\* \* Строка\*подключения.</span><span class="sxs-lookup"><span data-stu-id="4f2e7-129">If you pass user and password information both in the *ConnectionString* argument and in the optional *UserID* and *Password* arguments, the *UserID* and *Password* arguments will override the values specified in *ConnectionString*.</span></span>

<span data-ttu-id="4f2e7-130">Выполнив операции через открытое **Подключение**, с помощью метода [Close](close-method-ado.md) Освободите все связанные системные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="4f2e7-130">When you have concluded your operations over an open **Connection**, use the [Close](close-method-ado.md) method to free any associated system resources.</span></span> <span data-ttu-id="4f2e7-131">При закрытии объекта его не удаляются из памяти; Вы можете изменить его параметры, а затем снова открыть его с помощью метода **Open** .</span><span class="sxs-lookup"><span data-stu-id="4f2e7-131">Closing an object does not remove it from memory; you can change its property settings and use the **Open** method to open it again later.</span></span> <span data-ttu-id="4f2e7-132">Чтобы полностью удалить объект из памяти, присвойте переменной объекта значение *Nothing*.</span><span class="sxs-lookup"><span data-stu-id="4f2e7-132">To completely eliminate an object from memory, set the object variable to *Nothing*.</span></span>

<span data-ttu-id="4f2e7-133">**Использование удаленной службы данных** При использовании для объекта **подключения** на стороне клиента метод **Open** не устанавливает подключение к серверу до тех пор, пока не будет открыт [набор записей](recordset-object-ado.md) для объекта **Connection** .</span><span class="sxs-lookup"><span data-stu-id="4f2e7-133">**Remote Data Service Usage**When used on a client-side **Connection** object, the **Open** method doesn't actually establish a connection to the server until a [Recordset](recordset-object-ado.md) is opened on the **Connection** object.</span></span>

> [!NOTE]
> <span data-ttu-id="4f2e7-134">URL-адреса, использующие схему HTTP, автоматически будут вызывать [поставщик Microsoft OLE DB для публикации в Интернете](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="4f2e7-134">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="4f2e7-135">Для получения дополнительных сведений см [абсолютные и относительНые URL-адреса](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="4f2e7-135">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


