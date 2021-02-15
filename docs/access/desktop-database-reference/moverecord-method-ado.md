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
# <a name="moverecord-method-ado"></a><span data-ttu-id="17217-102">Метод MoveRecord (ADO)</span><span class="sxs-lookup"><span data-stu-id="17217-102">MoveRecord method (ADO)</span></span>

<span data-ttu-id="17217-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="17217-103">**Applies to**: Access 2013, Office 2013</span></span>
 
<span data-ttu-id="17217-104">Перемещает сущность, представленную [записью,](record-object-ado.md) в другое расположение.</span><span class="sxs-lookup"><span data-stu-id="17217-104">Moves the entity represent by a [Record](record-object-ado.md) to another location.</span></span>

## <a name="syntax"></a><span data-ttu-id="17217-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="17217-105">Syntax</span></span>

<span data-ttu-id="17217-106">*Запись*. MoveRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)</span><span class="sxs-lookup"><span data-stu-id="17217-106">*Record*.MoveRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)</span></span>

## <a name="parameters"></a><span data-ttu-id="17217-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="17217-107">Parameters</span></span>

|<span data-ttu-id="17217-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="17217-108">Parameter</span></span>|<span data-ttu-id="17217-109">Описание</span><span class="sxs-lookup"><span data-stu-id="17217-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="17217-110">*Source*</span><span class="sxs-lookup"><span data-stu-id="17217-110">*Source*</span></span> |<span data-ttu-id="17217-111">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="17217-111">Optional.</span></span> <span data-ttu-id="17217-112">**Строка,** содержаная URL-адрес, идентифицирующий **перемещаемую** запись.</span><span class="sxs-lookup"><span data-stu-id="17217-112">A **String** value that contains a URL identifying the **Record** to be moved.</span></span> <span data-ttu-id="17217-113">Если *source* опущен или указывает пустую строку, объект, представленный этой записью, **перемещается.**</span><span class="sxs-lookup"><span data-stu-id="17217-113">If *Source* is omitted or specifies an empty string, the object represented by this **Record** is moved.</span></span> <span data-ttu-id="17217-114">Например, если **запись** представляет файл, его содержимое перемещается в расположение, указанное в *пункте назначения.*</span><span class="sxs-lookup"><span data-stu-id="17217-114">For example, if the **Record** represents a file, the contents of the file are moved to the location specified by *Destination*.</span></span>|
|<span data-ttu-id="17217-115">*Destination*</span><span class="sxs-lookup"><span data-stu-id="17217-115">*Destination*</span></span> |<span data-ttu-id="17217-116">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="17217-116">Optional.</span></span> <span data-ttu-id="17217-117">**Строка,** содержаная URL-адрес, определяющий *расположение,* куда будет перемещен источник.</span><span class="sxs-lookup"><span data-stu-id="17217-117">A **String** value that contains a URL specifying the location where *Source* will be moved.</span></span>|
|<span data-ttu-id="17217-118">*UserName*</span><span class="sxs-lookup"><span data-stu-id="17217-118">*UserName*</span></span> |<span data-ttu-id="17217-119">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="17217-119">Optional.</span></span> <span data-ttu-id="17217-120">**Строка,** содержаная ид пользователя, который при необходимости разрешает доступ к пункту *назначения.*</span><span class="sxs-lookup"><span data-stu-id="17217-120">A **String** value that contains the user ID that, if needed, authorizes access to *Destination*.</span></span>|
|<span data-ttu-id="17217-121">*Password*</span><span class="sxs-lookup"><span data-stu-id="17217-121">*Password*</span></span> |<span data-ttu-id="17217-122">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="17217-122">Optional.</span></span> <span data-ttu-id="17217-123">**Строка,** содержаная пароль, который при необходимости проверяет *имя пользователя.*</span><span class="sxs-lookup"><span data-stu-id="17217-123">A **String** that contains the password that, if needed, verifies *UserName*.</span></span>|
|<span data-ttu-id="17217-124">*Options*</span><span class="sxs-lookup"><span data-stu-id="17217-124">*Options*</span></span> |<span data-ttu-id="17217-125">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="17217-125">Optional.</span></span> <span data-ttu-id="17217-126">Значение [MoveRecordOptionsEnum,](moverecordoptionsenum.md) значение по умолчанию **— adMoveUnspecified.**</span><span class="sxs-lookup"><span data-stu-id="17217-126">A [MoveRecordOptionsEnum](moverecordoptionsenum.md) value whose default value is **adMoveUnspecified**.</span></span> <span data-ttu-id="17217-127">Указывает поведение этого метода.</span><span class="sxs-lookup"><span data-stu-id="17217-127">Specifies the behavior of this method.</span></span>|
|<span data-ttu-id="17217-128">*Async*</span><span class="sxs-lookup"><span data-stu-id="17217-128">*Async*</span></span> |<span data-ttu-id="17217-129">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="17217-129">Optional.</span></span> <span data-ttu-id="17217-130">**Boolean** value that, when **True,** specifies this operation should be asynchronous.</span><span class="sxs-lookup"><span data-stu-id="17217-130">A **Boolean** value that, when **True**, specifies this operation should be asynchronous.</span></span>|

## <a name="return-value"></a><span data-ttu-id="17217-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="17217-131">Return value</span></span>

<span data-ttu-id="17217-132">**Строка.**</span><span class="sxs-lookup"><span data-stu-id="17217-132">A **String** value.</span></span> <span data-ttu-id="17217-133">Обычно возвращается *значение Destination.*</span><span class="sxs-lookup"><span data-stu-id="17217-133">Typically, the value of *Destination* is returned.</span></span> <span data-ttu-id="17217-134">Однако точное значение зависит от поставщика.</span><span class="sxs-lookup"><span data-stu-id="17217-134">However, the exact value returned is provider-dependent.</span></span>

## <a name="remarks"></a><span data-ttu-id="17217-135">Заметки</span><span class="sxs-lookup"><span data-stu-id="17217-135">Remarks</span></span>

<span data-ttu-id="17217-136">Значения *"Источник"* и *"Назначение"* не должны быть идентичными; в противном случае возникает ошибка во время запуска.</span><span class="sxs-lookup"><span data-stu-id="17217-136">The values of *Source* and *Destination* must not be identical; otherwise, a run-time error occurs.</span></span> <span data-ttu-id="17217-137">Имена серверов, путей и ресурсов должны отличаться по крайней мере.</span><span class="sxs-lookup"><span data-stu-id="17217-137">At least the server, path, and resource names must differ.</span></span>

<span data-ttu-id="17217-138">Для файлов, перемещающихся с помощью поставщика интернет-публикации, этот метод обновляет все гипертекст-ссылки в перемещаемом файле, если не указано иное в *параметрах.*</span><span class="sxs-lookup"><span data-stu-id="17217-138">For files moved using the Internet Publishing Provider, this method updates all hypertext links in files being moved unless otherwise specified by *Options*.</span></span> <span data-ttu-id="17217-139">Этот метод не удается, если *Destination* идентифицирует существующий объект (например, файл или каталог), если не указан **adMoveOverWrite.**</span><span class="sxs-lookup"><span data-stu-id="17217-139">This method fails if *Destination* identifies an existing object (for example, a file or directory), unless **adMoveOverWrite** is specified.</span></span>

> [!NOTE]
> <span data-ttu-id="17217-140">Используйте **параметр adMoveOverWrite** тщательно.</span><span class="sxs-lookup"><span data-stu-id="17217-140">Use the **adMoveOverWrite** option judiciously.</span></span> <span data-ttu-id="17217-141">Например, при указании этого параметра при перемещении файла в каталог каталог удаляется и заменяется файлом.</span><span class="sxs-lookup"><span data-stu-id="17217-141">For example, specifying this option when moving a file to a directory will delete the directory and replace it with the file.</span></span>

<span data-ttu-id="17217-142">Некоторые атрибуты объекта **Record,** такие как свойство [ParentURL,](parenturl-property-ado.md) не будут обновлены после завершения этой операции.</span><span class="sxs-lookup"><span data-stu-id="17217-142">Certain attributes of the **Record** object, such as the [ParentURL](parenturl-property-ado.md) property, will not be updated after this operation completes.</span></span> <span data-ttu-id="17217-143">Обновите свойства объекта **Record,** закров **запись,** а затем повторно открыв ее с URL-адресом расположения, куда был перемещен файл или каталог.</span><span class="sxs-lookup"><span data-stu-id="17217-143">Refresh the **Record** object's properties by closing the **Record**, then re-opening it with the URL of the location where the file or directory was moved.</span></span>

<span data-ttu-id="17217-144">Если эта **запись** была получена из [recordset,](recordset-object-ado.md)новое расположение перемещенного файла или каталога не будет сразу отражено в **наборе записей.**</span><span class="sxs-lookup"><span data-stu-id="17217-144">If this **Record** was obtained from a [Recordset](recordset-object-ado.md), the new location of the moved file or directory will not be reflected immediately in the **Recordset**.</span></span> <span data-ttu-id="17217-145">**Обновите набор записей,** закрыв и снова открывая его.</span><span class="sxs-lookup"><span data-stu-id="17217-145">Refresh the **Recordset** by closing and re-opening it.</span></span>

> [!NOTE]
> <span data-ttu-id="17217-146">URL-адреса, использующие схему HTTP, автоматически вызывают поставщика [Microsoft OLE DB для интернет-публикации.](microsoft-ole-db-provider-for-internet-publishing.md)</span><span class="sxs-lookup"><span data-stu-id="17217-146">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="17217-147">Дополнительные сведения см. в [сведениях об абсолютных и относительных URL-адресах.](absolute-and-relative-urls.md)</span><span class="sxs-lookup"><span data-stu-id="17217-147">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


