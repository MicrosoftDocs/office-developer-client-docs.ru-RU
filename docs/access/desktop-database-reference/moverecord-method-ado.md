---
title: Метод MoveRecord (ADO)
TOCTitle: MoveRecord method (ADO)
ms:assetid: efc341a2-0e08-a838-5925-8d4c46377e48
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250217(v=office.15)
ms:contentKeyID: 48548588
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c9937f0ab32c5dba0e4435fdc0ba7e111f5651dc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288681"
---
# <a name="moverecord-method-ado"></a><span data-ttu-id="d0526-102">Метод MoveRecord (ADO)</span><span class="sxs-lookup"><span data-stu-id="d0526-102">MoveRecord method (ADO)</span></span>

<span data-ttu-id="d0526-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d0526-103">**Applies to**: Access 2013, Office 2013</span></span>
 
<span data-ttu-id="d0526-104">Перемещает сущность, представленную [записью,](record-object-ado.md) в другое расположение.</span><span class="sxs-lookup"><span data-stu-id="d0526-104">Moves the entity represent by a [Record](record-object-ado.md) to another location.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0526-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d0526-105">Syntax</span></span>

<span data-ttu-id="d0526-106">*Запись*. MoveRecord (*Источник*, *Назначение*, *Имя пользователя*, *Пароль*, *Параметры*, *Async*)</span><span class="sxs-lookup"><span data-stu-id="d0526-106">*Record*.MoveRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)</span></span>

## <a name="parameters"></a><span data-ttu-id="d0526-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d0526-107">Parameters</span></span>

|<span data-ttu-id="d0526-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="d0526-108">Parameter</span></span>|<span data-ttu-id="d0526-109">Описание</span><span class="sxs-lookup"><span data-stu-id="d0526-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="d0526-110">*Source*</span><span class="sxs-lookup"><span data-stu-id="d0526-110">*Source*</span></span> |<span data-ttu-id="d0526-111">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="d0526-111">Optional.</span></span> <span data-ttu-id="d0526-112">Значение **String,** содержаее URL-адрес, определяющий **перемещаемую** запись.</span><span class="sxs-lookup"><span data-stu-id="d0526-112">A **String** value that contains a URL identifying the **Record** to be moved.</span></span> <span data-ttu-id="d0526-113">Если *source* опущен или указывает пустую строку, объект, представленный этой **записью,** перемещается.</span><span class="sxs-lookup"><span data-stu-id="d0526-113">If *Source* is omitted or specifies an empty string, the object represented by this **Record** is moved.</span></span> <span data-ttu-id="d0526-114">Например, если **запись** представляет файл, содержимое файла перемещается в указанное *назначением расположение.*</span><span class="sxs-lookup"><span data-stu-id="d0526-114">For example, if the **Record** represents a file, the contents of the file are moved to the location specified by *Destination*.</span></span>|
|<span data-ttu-id="d0526-115">*Destination*</span><span class="sxs-lookup"><span data-stu-id="d0526-115">*Destination*</span></span> |<span data-ttu-id="d0526-116">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="d0526-116">Optional.</span></span> <span data-ttu-id="d0526-117">Значение **String,** содержа которое содержит URL-адрес, указывающий расположение, в котором *будет* перемещен Источник.</span><span class="sxs-lookup"><span data-stu-id="d0526-117">A **String** value that contains a URL specifying the location where *Source* will be moved.</span></span>|
|<span data-ttu-id="d0526-118">*UserName*</span><span class="sxs-lookup"><span data-stu-id="d0526-118">*UserName*</span></span> |<span data-ttu-id="d0526-119">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="d0526-119">Optional.</span></span> <span data-ttu-id="d0526-120">Значение **String,** содержаее пользовательский ID, который при необходимости разрешает доступ к *Пункту назначения.*</span><span class="sxs-lookup"><span data-stu-id="d0526-120">A **String** value that contains the user ID that, if needed, authorizes access to *Destination*.</span></span>|
|<span data-ttu-id="d0526-121">*Password*</span><span class="sxs-lookup"><span data-stu-id="d0526-121">*Password*</span></span> |<span data-ttu-id="d0526-122">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="d0526-122">Optional.</span></span> <span data-ttu-id="d0526-123">Строка с паролем, который при необходимости проверяет *имя пользователя.* </span><span class="sxs-lookup"><span data-stu-id="d0526-123">A **String** that contains the password that, if needed, verifies *UserName*.</span></span>|
|<span data-ttu-id="d0526-124">*Options*</span><span class="sxs-lookup"><span data-stu-id="d0526-124">*Options*</span></span> |<span data-ttu-id="d0526-125">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="d0526-125">Optional.</span></span> <span data-ttu-id="d0526-126">Значение [MoveRecordOptionsEnum,](moverecordoptionsenum.md) значение по умолчанию которого **adMoveUnspecified.**</span><span class="sxs-lookup"><span data-stu-id="d0526-126">A [MoveRecordOptionsEnum](moverecordoptionsenum.md) value whose default value is **adMoveUnspecified**.</span></span> <span data-ttu-id="d0526-127">Указывает поведение этого метода.</span><span class="sxs-lookup"><span data-stu-id="d0526-127">Specifies the behavior of this method.</span></span>|
|<span data-ttu-id="d0526-128">*Async*</span><span class="sxs-lookup"><span data-stu-id="d0526-128">*Async*</span></span> |<span data-ttu-id="d0526-129">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="d0526-129">Optional.</span></span> <span data-ttu-id="d0526-130">Значение **Boolean,** которое при **true** указывает эту операцию, должно быть асинхронным.</span><span class="sxs-lookup"><span data-stu-id="d0526-130">A **Boolean** value that, when **True**, specifies this operation should be asynchronous.</span></span>|

## <a name="return-value"></a><span data-ttu-id="d0526-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d0526-131">Return value</span></span>

<span data-ttu-id="d0526-132">Значение **String.**</span><span class="sxs-lookup"><span data-stu-id="d0526-132">A **String** value.</span></span> <span data-ttu-id="d0526-133">Обычно возвращается значение *Destination.*</span><span class="sxs-lookup"><span data-stu-id="d0526-133">Typically, the value of *Destination* is returned.</span></span> <span data-ttu-id="d0526-134">Однако точное значение, возвращенное, зависит от поставщика.</span><span class="sxs-lookup"><span data-stu-id="d0526-134">However, the exact value returned is provider-dependent.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0526-135">Примечания</span><span class="sxs-lookup"><span data-stu-id="d0526-135">Remarks</span></span>

<span data-ttu-id="d0526-136">Значения источника *и*  назначения не должны быть идентичными; в противном случае возникает ошибка времени запуска.</span><span class="sxs-lookup"><span data-stu-id="d0526-136">The values of *Source* and *Destination* must not be identical; otherwise, a run-time error occurs.</span></span> <span data-ttu-id="d0526-137">По крайней мере, имена серверов, путей и ресурсов должны отличаться.</span><span class="sxs-lookup"><span data-stu-id="d0526-137">At least the server, path, and resource names must differ.</span></span>

<span data-ttu-id="d0526-138">Для перемещений файлов с помощью поставщика публикаций в Интернете этот метод обновляет все гипертекстовы ссылки в перемещаемых файлах, если иное не указано *параметрами*.</span><span class="sxs-lookup"><span data-stu-id="d0526-138">For files moved using the Internet Publishing Provider, this method updates all hypertext links in files being moved unless otherwise specified by *Options*.</span></span> <span data-ttu-id="d0526-139">Этот метод не удается, если *Destination* идентифицирует существующий объект (например, файл или каталог), если не указано **adMoveOverWrite.**</span><span class="sxs-lookup"><span data-stu-id="d0526-139">This method fails if *Destination* identifies an existing object (for example, a file or directory), unless **adMoveOverWrite** is specified.</span></span>

> [!NOTE]
> <span data-ttu-id="d0526-140">Разумно используйте **параметр adMoveOverWrite.**</span><span class="sxs-lookup"><span data-stu-id="d0526-140">Use the **adMoveOverWrite** option judiciously.</span></span> <span data-ttu-id="d0526-141">Например, указание этого параметра при перемещении файла в каталог удаляет каталог и заменяет его файлом.</span><span class="sxs-lookup"><span data-stu-id="d0526-141">For example, specifying this option when moving a file to a directory will delete the directory and replace it with the file.</span></span>

<span data-ttu-id="d0526-142">Некоторые атрибуты объекта **Record,** такие как [свойство ParentURL,](parenturl-property-ado.md) не будут обновляться после завершения этой операции.</span><span class="sxs-lookup"><span data-stu-id="d0526-142">Certain attributes of the **Record** object, such as the [ParentURL](parenturl-property-ado.md) property, will not be updated after this operation completes.</span></span> <span data-ttu-id="d0526-143">**Обновите** свойства объекта **Record,** закрыв запись, а затем повторно открыв ее с URL-адресом расположения, куда был перемещен файл или каталог.</span><span class="sxs-lookup"><span data-stu-id="d0526-143">Refresh the **Record** object's properties by closing the **Record**, then re-opening it with the URL of the location where the file or directory was moved.</span></span>

<span data-ttu-id="d0526-144">Если эта **запись** была получена из [recordset,](recordset-object-ado.md)новое расположение перемещенного файла или каталога не будет немедленно отражено в **Наборе записей.**</span><span class="sxs-lookup"><span data-stu-id="d0526-144">If this **Record** was obtained from a [Recordset](recordset-object-ado.md), the new location of the moved file or directory will not be reflected immediately in the **Recordset**.</span></span> <span data-ttu-id="d0526-145">**Обновите набор записей,** закрыв и открыв его повторно.</span><span class="sxs-lookup"><span data-stu-id="d0526-145">Refresh the **Recordset** by closing and re-opening it.</span></span>

> [!NOTE]
> <span data-ttu-id="d0526-146">URL-адреса, использующие схему http, автоматически вызывают поставщика DB Microsoft [OLE для публикации в Интернете.](microsoft-ole-db-provider-for-internet-publishing.md)</span><span class="sxs-lookup"><span data-stu-id="d0526-146">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="d0526-147">Дополнительные сведения см. в [url-адресах Absolute и relative.](absolute-and-relative-urls.md)</span><span class="sxs-lookup"><span data-stu-id="d0526-147">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


