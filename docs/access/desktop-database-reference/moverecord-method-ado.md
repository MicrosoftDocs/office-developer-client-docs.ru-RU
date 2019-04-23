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
# <a name="moverecord-method-ado"></a><span data-ttu-id="d7707-102">Метод MoveRecord (ADO)</span><span class="sxs-lookup"><span data-stu-id="d7707-102">MoveRecord method (ADO)</span></span>

<span data-ttu-id="d7707-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d7707-103">**Applies to**: Access 2013, Office 2013</span></span>
 
<span data-ttu-id="d7707-104">ПереМещает сущность по [записи](record-object-ado.md) в другое расположение.</span><span class="sxs-lookup"><span data-stu-id="d7707-104">Moves the entity represent by a [Record](record-object-ado.md) to another location.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7707-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d7707-105">Syntax</span></span>

<span data-ttu-id="d7707-106">*Запись*. MoveRecord (*источник*, *назначение*, *имя пользователя*, *пароль*, *Параметры*, *асинхронно*)</span><span class="sxs-lookup"><span data-stu-id="d7707-106">*Record*.MoveRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)</span></span>

## <a name="parameters"></a><span data-ttu-id="d7707-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d7707-107">Parameters</span></span>

|<span data-ttu-id="d7707-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="d7707-108">Parameter</span></span>|<span data-ttu-id="d7707-109">Описание</span><span class="sxs-lookup"><span data-stu-id="d7707-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="d7707-110">*Source*</span><span class="sxs-lookup"><span data-stu-id="d7707-110">*Source*</span></span> |<span data-ttu-id="d7707-111">Необязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="d7707-111">Optional.</span></span> <span data-ttu-id="d7707-112">**Строковое** значение, содержащее URL-адрес, указывающий на перемещаемую **запись** .</span><span class="sxs-lookup"><span data-stu-id="d7707-112">A **String** value that contains a URL identifying the **Record** to be moved.</span></span> <span data-ttu-id="d7707-113">Если параметр *Source* опущен или указывает пустую строку, перемещается объект, представленный этой **записью** .</span><span class="sxs-lookup"><span data-stu-id="d7707-113">If *Source* is omitted or specifies an empty string, the object represented by this **Record** is moved.</span></span> <span data-ttu-id="d7707-114">Например, если **запись** представляет файл, содержимое файла перемещается в расположение, указанное в параметре *Destination*.</span><span class="sxs-lookup"><span data-stu-id="d7707-114">For example, if the **Record** represents a file, the contents of the file are moved to the location specified by *Destination*.</span></span>|
|<span data-ttu-id="d7707-115">*Destination*</span><span class="sxs-lookup"><span data-stu-id="d7707-115">*Destination*</span></span> |<span data-ttu-id="d7707-116">Необязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="d7707-116">Optional.</span></span> <span data-ttu-id="d7707-117">**Строковое** значение, содержащее URL-адрес, указывающий расположение, в которое будет перемещен *источник* .</span><span class="sxs-lookup"><span data-stu-id="d7707-117">A **String** value that contains a URL specifying the location where *Source* will be moved.</span></span>|
|<span data-ttu-id="d7707-118">*UserName*</span><span class="sxs-lookup"><span data-stu-id="d7707-118">*UserName*</span></span> |<span data-ttu-id="d7707-119">Необязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="d7707-119">Optional.</span></span> <span data-ttu-id="d7707-120">**Строковое** значение, содержащее идентификатор пользователя, который при необходимости авторизует доступ к назначению. \*\*</span><span class="sxs-lookup"><span data-stu-id="d7707-120">A **String** value that contains the user ID that, if needed, authorizes access to *Destination*.</span></span>|
|<span data-ttu-id="d7707-121">*Password*</span><span class="sxs-lookup"><span data-stu-id="d7707-121">*Password*</span></span> |<span data-ttu-id="d7707-122">Необязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="d7707-122">Optional.</span></span> <span data-ttu-id="d7707-123">**Строка** , содержащая пароль, при необходимости проверяющий *имя пользователя*.</span><span class="sxs-lookup"><span data-stu-id="d7707-123">A **String** that contains the password that, if needed, verifies *UserName*.</span></span>|
|<span data-ttu-id="d7707-124">*Options*</span><span class="sxs-lookup"><span data-stu-id="d7707-124">*Options*</span></span> |<span data-ttu-id="d7707-125">Необязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="d7707-125">Optional.</span></span> <span data-ttu-id="d7707-126">Значение [моверекордоптионсенум](moverecordoptionsenum.md) , для которого по умолчанию задано значение **адмовеунспеЦифиед**.</span><span class="sxs-lookup"><span data-stu-id="d7707-126">A [MoveRecordOptionsEnum](moverecordoptionsenum.md) value whose default value is **adMoveUnspecified**.</span></span> <span data-ttu-id="d7707-127">Задает поведение этого метода.</span><span class="sxs-lookup"><span data-stu-id="d7707-127">Specifies the behavior of this method.</span></span>|
|<span data-ttu-id="d7707-128">*Асинхронного*</span><span class="sxs-lookup"><span data-stu-id="d7707-128">*Async*</span></span> |<span data-ttu-id="d7707-129">Необязательный атрибут.</span><span class="sxs-lookup"><span data-stu-id="d7707-129">Optional.</span></span> <span data-ttu-id="d7707-130">**Логическое** значение, которое при **значении true**указывает, что эта операция должна быть асинхронной.</span><span class="sxs-lookup"><span data-stu-id="d7707-130">A **Boolean** value that, when **True**, specifies this operation should be asynchronous.</span></span>|

## <a name="return-value"></a><span data-ttu-id="d7707-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d7707-131">Return value</span></span>

<span data-ttu-id="d7707-132">**Строковое** значение.</span><span class="sxs-lookup"><span data-stu-id="d7707-132">A **String** value.</span></span> <span data-ttu-id="d7707-133">Как правило, возвращается значение *Destination* .</span><span class="sxs-lookup"><span data-stu-id="d7707-133">Typically, the value of *Destination* is returned.</span></span> <span data-ttu-id="d7707-134">Тем не менее, возвращаемое значение зависит от поставщика.</span><span class="sxs-lookup"><span data-stu-id="d7707-134">However, the exact value returned is provider-dependent.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7707-135">Замечания</span><span class="sxs-lookup"><span data-stu-id="d7707-135">Remarks</span></span>

<span data-ttu-id="d7707-136">Значения *Source* и *Destination* не должны совпадать; в противном случае возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="d7707-136">The values of *Source* and *Destination* must not be identical; otherwise, a run-time error occurs.</span></span> <span data-ttu-id="d7707-137">По крайней мере имя сервера, путь и имя ресурса должны различаться.</span><span class="sxs-lookup"><span data-stu-id="d7707-137">At least the server, path, and resource names must differ.</span></span>

<span data-ttu-id="d7707-138">Для файлов, перемещенных с помощью поставщика публикации в Интернете, этот метод обновляет все гипертекстовые ссылки в переносимых файлах, \*\* если в параметрах не указано иное.</span><span class="sxs-lookup"><span data-stu-id="d7707-138">For files moved using the Internet Publishing Provider, this method updates all hypertext links in files being moved unless otherwise specified by *Options*.</span></span> <span data-ttu-id="d7707-139">Этот метод завершается с ошибкой, если объект *Destination* определяет существующий объект (например, файл или каталог), если не указан **адмовеоверврите** .</span><span class="sxs-lookup"><span data-stu-id="d7707-139">This method fails if *Destination* identifies an existing object (for example, a file or directory), unless **adMoveOverWrite** is specified.</span></span>

> [!NOTE]
> <span data-ttu-id="d7707-140">Внимательно используйте параметр **адмовеоверврите** .</span><span class="sxs-lookup"><span data-stu-id="d7707-140">Use the **adMoveOverWrite** option judiciously.</span></span> <span data-ttu-id="d7707-141">Например, если указать этот параметр при перемещении файла в каталог, каталог будет удален и заменен файлом.</span><span class="sxs-lookup"><span data-stu-id="d7707-141">For example, specifying this option when moving a file to a directory will delete the directory and replace it with the file.</span></span>

<span data-ttu-id="d7707-142">Некоторые атрибуты объекта **Record** , такие как свойство [ParentURL](parenturl-property-ado.md) , не будут обновляться после завершения этой операции.</span><span class="sxs-lookup"><span data-stu-id="d7707-142">Certain attributes of the **Record** object, such as the [ParentURL](parenturl-property-ado.md) property, will not be updated after this operation completes.</span></span> <span data-ttu-id="d7707-143">Обновите свойства объекта **Record** , закрыв **запись**, а затем повторно ОТКРЫВ ее с URL-адресом расположения, в которое был перемещен файл или каталог.</span><span class="sxs-lookup"><span data-stu-id="d7707-143">Refresh the **Record** object's properties by closing the **Record**, then re-opening it with the URL of the location where the file or directory was moved.</span></span>

<span data-ttu-id="d7707-144">Если эта **запись** была получена из объекта [Recordset](recordset-object-ado.md), новое расположение перемещенного файла или каталога не будет немедленно отражено в **наборе записей**.</span><span class="sxs-lookup"><span data-stu-id="d7707-144">If this **Record** was obtained from a [Recordset](recordset-object-ado.md), the new location of the moved file or directory will not be reflected immediately in the **Recordset**.</span></span> <span data-ttu-id="d7707-145">Обновление **набора записей** путем его закрытия и повторного открытия.</span><span class="sxs-lookup"><span data-stu-id="d7707-145">Refresh the **Recordset** by closing and re-opening it.</span></span>

> [!NOTE]
> <span data-ttu-id="d7707-146">URL-адреса, использующие схему HTTP, автоматически будут вызывать [поставщик Microsoft OLE DB для публикации в Интернете](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="d7707-146">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="d7707-147">Для получения дополнительных сведений см [абсолютные и относительНые URL-адреса](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="d7707-147">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


