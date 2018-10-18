---
title: Open Method (ADO Record)
TOCTitle: Open Method (ADO Record)
ms:assetid: ba71c5c7-326e-d3b6-0e74-e8343ee6896f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249896(v=office.15)
ms:contentKeyID: 48547371
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f29f707f02ed8adbf2b1881b0721ce912b278353
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25605830"
---
# <a name="open-method-ado-record"></a><span data-ttu-id="6904e-102">Open Method (ADO Record)</span><span class="sxs-lookup"><span data-stu-id="6904e-102">Open Method (ADO Record)</span></span>


<span data-ttu-id="6904e-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6904e-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="6904e-104">Открывает существующий объект [записи](record-object-ado.md) или создает новый элемент, представленный **записи** (например, файла или папки).</span><span class="sxs-lookup"><span data-stu-id="6904e-104">Opens an existing [Record](record-object-ado.md) object, or creates a new item represented by the **Record** (such as a file or directory).</span></span>

## <a name="syntax"></a><span data-ttu-id="6904e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6904e-105">Syntax</span></span>

<span data-ttu-id="6904e-106">*Источник*, открывать *ActiveConnection*, *режим*, *CreateOptions*, *Параметры*, *имя пользователя*и *пароль*</span><span class="sxs-lookup"><span data-stu-id="6904e-106">Open *Source*, *ActiveConnection*, *Mode*, *CreateOptions*, *Options*, *UserName*, *Password*</span></span>

## <a name="parameters"></a><span data-ttu-id="6904e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="6904e-107">Parameters</span></span>

  - <span data-ttu-id="6904e-108">*Source*</span><span class="sxs-lookup"><span data-stu-id="6904e-108">*Source*</span></span>

  - <span data-ttu-id="6904e-109">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="6904e-109">Optional.</span></span> <span data-ttu-id="6904e-110">**Variant** , которая может представлять URL-адрес сущности, необходимо представить в виде этой **записи** объекта, **команды**, open [набора записей](recordset-object-ado.md) или другой **записи** , строка, содержащая инструкции SQL SELECT или имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="6904e-110">A **Variant** that may represent the URL of the entity to be represented by this **Record** object, a **Command**, an open [Recordset](recordset-object-ado.md) or another **Record** object, a string containing a SQL SELECT statement or a table name.</span></span>

  - <span data-ttu-id="6904e-111">*ActiveConnection*</span><span class="sxs-lookup"><span data-stu-id="6904e-111">*ActiveConnection*</span></span>

  - <span data-ttu-id="6904e-112">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="6904e-112">Optional.</span></span> <span data-ttu-id="6904e-113">**Variant** , который представляет строку или откройте объект [подключения](connection-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="6904e-113">A **Variant** that represents the connect string or open [Connection](connection-object-ado.md) object.</span></span>

  - <span data-ttu-id="6904e-114">*Mode*</span><span class="sxs-lookup"><span data-stu-id="6904e-114">*Mode*</span></span>

  - <span data-ttu-id="6904e-115">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="6904e-115">Optional.</span></span> <span data-ttu-id="6904e-116">Значение [ConnectModeEnum](connectmodeenum.md) , значение которого по умолчанию — это **adModeUnknown**, указывающее режим доступа для результирующий объект **записи** .</span><span class="sxs-lookup"><span data-stu-id="6904e-116">A [ConnectModeEnum](connectmodeenum.md) value, whose default value is **adModeUnknown**, that specifies the access mode for the resultant **Record** object.</span></span>

  - <span data-ttu-id="6904e-117">*CreateOptions*</span><span class="sxs-lookup"><span data-stu-id="6904e-117">*CreateOptions*</span></span>

  - <span data-ttu-id="6904e-118">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="6904e-118">Optional.</span></span> <span data-ttu-id="6904e-119">Значение [RecordCreateOptionsEnum](recordcreateoptionsenum.md) , чье значение по умолчанию — это **adFailIfNotExists**, открывается существующий файл или каталог, в или новый файл или каталог должен быть создан.</span><span class="sxs-lookup"><span data-stu-id="6904e-119">A [RecordCreateOptionsEnum](recordcreateoptionsenum.md) value, whose default value is **adFailIfNotExists**, that specifies whether an existing file or directory should be opened, or a new file or directory should be created.</span></span> <span data-ttu-id="6904e-120">Если параметр имеет значение по умолчанию, режим доступа к извлекается из свойства [Mode](mode-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="6904e-120">If set to the default value, the access mode is obtained from the [Mode](mode-property-ado.md) property.</span></span> <span data-ttu-id="6904e-121">Этот параметр игнорируется, если параметр *источника* не содержит URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="6904e-121">This parameter is ignored when the *Source* parameter doesnt contain a URL.</span></span>

  - <span data-ttu-id="6904e-122">*Варианты*</span><span class="sxs-lookup"><span data-stu-id="6904e-122">*Options*</span></span>

  - <span data-ttu-id="6904e-123">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="6904e-123">Optional.</span></span> <span data-ttu-id="6904e-124">Значение [RecordOpenOptionsEnum](recordopenoptionsenum.md) , чье значение по умолчанию — это **adOpenRecordUnspecified**, который задает параметры открытия **записи**.</span><span class="sxs-lookup"><span data-stu-id="6904e-124">A [RecordOpenOptionsEnum](recordopenoptionsenum.md) value, whose default value is **adOpenRecordUnspecified**, that specifies options for opening the **Record**.</span></span> <span data-ttu-id="6904e-125">Эти значения можно объединять.</span><span class="sxs-lookup"><span data-stu-id="6904e-125">These values may be combined.</span></span>

  - <span data-ttu-id="6904e-126">*Имя пользователя*</span><span class="sxs-lookup"><span data-stu-id="6904e-126">*UserName*</span></span>

  - <span data-ttu-id="6904e-127">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="6904e-127">Optional.</span></span> <span data-ttu-id="6904e-128">**Строковое** значение, содержащее идентификатор пользователя, при необходимости, авторизует доступ к *источнику*.</span><span class="sxs-lookup"><span data-stu-id="6904e-128">A **String** value that contains the user ID that, if needed, authorizes access to *Source*.</span></span>

  - <span data-ttu-id="6904e-129">*Password*</span><span class="sxs-lookup"><span data-stu-id="6904e-129">*Password*</span></span>

  - <span data-ttu-id="6904e-130">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="6904e-130">Optional.</span></span> <span data-ttu-id="6904e-131">**Строковое** значение, содержащее пароль, при необходимости, выполняется проверка *имени пользователя*.</span><span class="sxs-lookup"><span data-stu-id="6904e-131">A **String** value that contains the password that, if needed, verifies *UserName*.</span></span>

## <a name="remarks"></a><span data-ttu-id="6904e-132">Замечания</span><span class="sxs-lookup"><span data-stu-id="6904e-132">Remarks</span></span>

<span data-ttu-id="6904e-133">*Источник* может быть:</span><span class="sxs-lookup"><span data-stu-id="6904e-133">*Source* may be:</span></span>

  - <span data-ttu-id="6904e-134">URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="6904e-134">A URL.</span></span> <span data-ttu-id="6904e-135">Если протокол для URL-адрес http, поставщика Интернета будет вызван по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6904e-135">If the protocol for the URL is http, then the Internet Provider will be invoked by default.</span></span> <span data-ttu-id="6904e-136">Указывает ли URL-адрес узла, который содержит исполняемый файл сценария (например,. Страница ASP), а затем открывается **запись** , содержащую источник, а не выполнен содержимое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6904e-136">If the URL points to a node that contains an executable script (such as an .ASP page), then a **Record** containing the source rather than the executed contents is opened by default.</span></span> <span data-ttu-id="6904e-137">Чтобы изменить это поведение используйте аргумента *Options* .</span><span class="sxs-lookup"><span data-stu-id="6904e-137">Use the *Options* argument to modify this behavior.</span></span>

  - <span data-ttu-id="6904e-138">Объект **записи** .</span><span class="sxs-lookup"><span data-stu-id="6904e-138">A **Record** object.</span></span> <span data-ttu-id="6904e-139">Объект **записи** , открывается из другой **записи** будет клонируйте исходный объект **записи** .</span><span class="sxs-lookup"><span data-stu-id="6904e-139">A **Record** object opened from another **Record** will clone the original **Record** object.</span></span>

  - <span data-ttu-id="6904e-140">Объект **команды** .</span><span class="sxs-lookup"><span data-stu-id="6904e-140">A **Command** object.</span></span> <span data-ttu-id="6904e-141">Объект открыт **запись** представляет одну строку, возвращаемые при выполнении **команды**.</span><span class="sxs-lookup"><span data-stu-id="6904e-141">The opened **Record** object represents the single row returned by executing the **Command**.</span></span> <span data-ttu-id="6904e-142">Если результаты содержат более чем одной строки, содержимое первой строки помещаются в записи и ошибки могут быть добавлены в коллекцию **ошибок** .</span><span class="sxs-lookup"><span data-stu-id="6904e-142">If the results contain more than a single row, the contents of the first row are placed in the record and an error may be added to the **Errors** collection.</span></span>

  - <span data-ttu-id="6904e-143">Инструкция SQL SELECT.</span><span class="sxs-lookup"><span data-stu-id="6904e-143">A SQL SELECT statement.</span></span> <span data-ttu-id="6904e-144">Объект открыт **запись** представляет одну строку, возвращаемые при выполнении содержимое строки.</span><span class="sxs-lookup"><span data-stu-id="6904e-144">The opened **Record** object represents the single row returned by executing the contents of the string.</span></span> <span data-ttu-id="6904e-145">Если результаты содержат более чем одной строки, содержимое первой строки помещаются в записи и ошибки могут быть добавлены в коллекцию **ошибок** .</span><span class="sxs-lookup"><span data-stu-id="6904e-145">If the results contain more than a single row, the contents of the first row are placed in the record and an error may be added to the **Errors** collection.</span></span>

  - <span data-ttu-id="6904e-146">Имя таблицы.</span><span class="sxs-lookup"><span data-stu-id="6904e-146">A table name.</span></span>

<span data-ttu-id="6904e-147">Если объект **запись** представляет сущности, которая не может получить доступ с помощью URL-адреса (например, в строке **набора записей** , производного от базы данных), затем значения свойства [ParentURL](parenturl-property-ado.md) и поля, доступ к **adRecordURL** Константы имеют значение null.</span><span class="sxs-lookup"><span data-stu-id="6904e-147">If the **Record** object represents an entity that cannot be accessed with a URL (for example, a row of a **Recordset** derived from a database), then the values of both the [ParentURL](parenturl-property-ado.md) property and the field accessed with the **adRecordURL** constant are null.</span></span>


> [!NOTE]
<span data-ttu-id="6904e-148"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="6904e-148"><<<<<<< HEAD</span></span>
> <P><span data-ttu-id="6904e-149">URL-адреса, с помощью схемы http автоматически вызывает <A href="microsoft-ole-db-provider-for-internet-publishing.md">Поставщик Microsoft OLE DB для публикации Интернет</A>.</span><span class="sxs-lookup"><span data-stu-id="6904e-149">URLs using the http scheme will automatically invoke the <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>.</span></span> <span data-ttu-id="6904e-150">Для получения дополнительных сведений см <A href="absolute-and-relative-urls.md">абсолютного и относительных URL-адресов</A>.</span><span class="sxs-lookup"><span data-stu-id="6904e-150">For more information, see <A href="absolute-and-relative-urls.md">Absolute and Relative URLs</A>.</span></span></P>
=======
> <span data-ttu-id="6904e-151">URL-адреса, с помощью схемы http автоматически вызывает [Поставщик Microsoft OLE DB для публикации Интернет](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="6904e-151">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="6904e-152">Для получения дополнительных сведений см [абсолютных и относительных URL-адресов](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="6904e-152">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>
>>>>>>> <span data-ttu-id="6904e-153">master</span><span class="sxs-lookup"><span data-stu-id="6904e-153">master</span></span>


