---
title: Метод MoveRecord (ADO)
TOCTitle: MoveRecord method (ADO)
ms:assetid: efc341a2-0e08-a838-5925-8d4c46377e48
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250217(v=office.15)
ms:contentKeyID: 48548588
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 022db96a00253793505df6e89603070a6d429a8d
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998870"
---
# <a name="moverecord-method-ado"></a><span data-ttu-id="fe10e-102">Метод MoveRecord (ADO)</span><span class="sxs-lookup"><span data-stu-id="fe10e-102">MoveRecord method (ADO)</span></span>

<span data-ttu-id="fe10e-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fe10e-103">**Applies to**: Access 2013, Office 2013</span></span>
 
<span data-ttu-id="fe10e-104">Перемещает сущности представляют [записи](record-object-ado.md) в другое расположение.</span><span class="sxs-lookup"><span data-stu-id="fe10e-104">Moves the entity represent by a [Record](record-object-ado.md) to another location.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe10e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fe10e-105">Syntax</span></span>

<span data-ttu-id="fe10e-106">*Запись*. MoveRecord (*источника*, *назначения*, *имя пользователя*, *пароль*, *Параметры*, *асинхронного*)</span><span class="sxs-lookup"><span data-stu-id="fe10e-106">*Record*.MoveRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)</span></span>

## <a name="parameters"></a><span data-ttu-id="fe10e-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="fe10e-107">Parameters</span></span>

|<span data-ttu-id="fe10e-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="fe10e-108">Parameter</span></span>|<span data-ttu-id="fe10e-109">Описание</span><span class="sxs-lookup"><span data-stu-id="fe10e-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="fe10e-110">*Source*</span><span class="sxs-lookup"><span data-stu-id="fe10e-110">*Source*</span></span> |<span data-ttu-id="fe10e-111">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="fe10e-111">Optional.</span></span> <span data-ttu-id="fe10e-112">**Строковое** значение, содержащее URL-адрес, идентифицирующий эту **запись** переместить.</span><span class="sxs-lookup"><span data-stu-id="fe10e-112">A **String** value that contains a URL identifying the **Record** to be moved.</span></span> <span data-ttu-id="fe10e-113">Если *источник* указан или указывает пустая строка, перемещается объект, представленный этой **записи** .</span><span class="sxs-lookup"><span data-stu-id="fe10e-113">If *Source* is omitted or specifies an empty string, the object represented by this **Record** is moved.</span></span> <span data-ttu-id="fe10e-114">Например если **запись** представляет файл, содержимое файла перемещаются местоположение, указанное для *назначения*.</span><span class="sxs-lookup"><span data-stu-id="fe10e-114">For example, if the **Record** represents a file, the contents of the file are moved to the location specified by *Destination*.</span></span>|
|<span data-ttu-id="fe10e-115">*Назначения*</span><span class="sxs-lookup"><span data-stu-id="fe10e-115">*Destination*</span></span> |<span data-ttu-id="fe10e-116">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="fe10e-116">Optional.</span></span> <span data-ttu-id="fe10e-117">**Строковое** значение, содержащее URL-адрес, указав расположение, где будут перемещены *источника* .</span><span class="sxs-lookup"><span data-stu-id="fe10e-117">A **String** value that contains a URL specifying the location where *Source* will be moved.</span></span>|
|<span data-ttu-id="fe10e-118">*Имя пользователя*</span><span class="sxs-lookup"><span data-stu-id="fe10e-118">*UserName*</span></span> |<span data-ttu-id="fe10e-119">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="fe10e-119">Optional.</span></span> <span data-ttu-id="fe10e-120">**Строковое** значение, содержащее идентификатор пользователя, при необходимости, авторизует доступ в *место назначения*.</span><span class="sxs-lookup"><span data-stu-id="fe10e-120">A **String** value that contains the user ID that, if needed, authorizes access to *Destination*.</span></span>|
|<span data-ttu-id="fe10e-121">*Password*</span><span class="sxs-lookup"><span data-stu-id="fe10e-121">*Password*</span></span> |<span data-ttu-id="fe10e-122">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="fe10e-122">Optional.</span></span> <span data-ttu-id="fe10e-123">**Строка** , содержащая пароль, при необходимости, выполняется проверка *имени пользователя*.</span><span class="sxs-lookup"><span data-stu-id="fe10e-123">A **String** that contains the password that, if needed, verifies *UserName*.</span></span>|
|<span data-ttu-id="fe10e-124">*Варианты*</span><span class="sxs-lookup"><span data-stu-id="fe10e-124">*Options*</span></span> |<span data-ttu-id="fe10e-125">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="fe10e-125">Optional.</span></span> <span data-ttu-id="fe10e-126">Значение [MoveRecordOptionsEnum](moverecordoptionsenum.md) , чье значение по умолчанию — **adMoveUnspecified**.</span><span class="sxs-lookup"><span data-stu-id="fe10e-126">A [MoveRecordOptionsEnum](moverecordoptionsenum.md) value whose default value is **adMoveUnspecified**.</span></span> <span data-ttu-id="fe10e-127">Задает поведение этого метода.</span><span class="sxs-lookup"><span data-stu-id="fe10e-127">Specifies the behavior of this method.</span></span>|
|<span data-ttu-id="fe10e-128">*Async*</span><span class="sxs-lookup"><span data-stu-id="fe10e-128">*Async*</span></span> |<span data-ttu-id="fe10e-129">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="fe10e-129">Optional.</span></span> <span data-ttu-id="fe10e-130">**Логическое** значение, которое, если **значение True**, указывает, что эту операцию следует асинхронный.</span><span class="sxs-lookup"><span data-stu-id="fe10e-130">A **Boolean** value that, when **True**, specifies this operation should be asynchronous.</span></span>|

## <a name="return-value"></a><span data-ttu-id="fe10e-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fe10e-131">Return value</span></span>

<span data-ttu-id="fe10e-132">**Строковое** значение.</span><span class="sxs-lookup"><span data-stu-id="fe10e-132">A **String** value.</span></span> <span data-ttu-id="fe10e-133">Как правило возвращается значение *назначения* .</span><span class="sxs-lookup"><span data-stu-id="fe10e-133">Typically, the value of *Destination* is returned.</span></span> <span data-ttu-id="fe10e-134">Тем не менее точное значение, возвращаемое зависит от поставщика.</span><span class="sxs-lookup"><span data-stu-id="fe10e-134">However, the exact value returned is provider-dependent.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe10e-135">Примечания</span><span class="sxs-lookup"><span data-stu-id="fe10e-135">Remarks</span></span>

<span data-ttu-id="fe10e-136">Значения из *источника* и *назначения* не должны совпадать; в противном случае возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="fe10e-136">The values of *Source* and *Destination* must not be identical; otherwise, a run-time error occurs.</span></span> <span data-ttu-id="fe10e-137">По крайней мере имена серверов, пути и ресурсов должны отличаться.</span><span class="sxs-lookup"><span data-stu-id="fe10e-137">At least the server, path, and resource names must differ.</span></span>

<span data-ttu-id="fe10e-138">Для файлов, перемещенных с использованием поставщика публикации Интернета этот метод обновляет все ссылки гиперссылку в файлах, происходит перемещение, если не указано иное, *Параметры*.</span><span class="sxs-lookup"><span data-stu-id="fe10e-138">For files moved using the Internet Publishing Provider, this method updates all hypertext links in files being moved unless otherwise specified by *Options*.</span></span> <span data-ttu-id="fe10e-139">Этот метод не выполняется, если *конечный* идентифицирует существующий объект (например, файла или каталога), если не указано **adMoveOverWrite** .</span><span class="sxs-lookup"><span data-stu-id="fe10e-139">This method fails if *Destination* identifies an existing object (for example, a file or directory), unless **adMoveOverWrite** is specified.</span></span>

> [!NOTE]
> <span data-ttu-id="fe10e-140">Параметр **adMoveOverWrite** внимательно.</span><span class="sxs-lookup"><span data-stu-id="fe10e-140">Use the **adMoveOverWrite** option judiciously.</span></span> <span data-ttu-id="fe10e-141">Например задание этого параметра при переносе в файл в каталоге будет удалите каталог и замените файл.</span><span class="sxs-lookup"><span data-stu-id="fe10e-141">For example, specifying this option when moving a file to a directory will delete the directory and replace it with the file.</span></span>

<span data-ttu-id="fe10e-142">Некоторые атрибуты объекта **записи** , такими как свойство [ParentURL](parenturl-property-ado.md) , не будут обновляться после завершения этой операции.</span><span class="sxs-lookup"><span data-stu-id="fe10e-142">Certain attributes of the **Record** object, such as the [ParentURL](parenturl-property-ado.md) property, will not be updated after this operation completes.</span></span> <span data-ttu-id="fe10e-143">Обновление свойств объекта **записи** , **записи**закрытия, а затем повторно открыть его URL-адрес, где был перемещен в файл или папку.</span><span class="sxs-lookup"><span data-stu-id="fe10e-143">Refresh the **Record** object's properties by closing the **Record**, then re-opening it with the URL of the location where the file or directory was moved.</span></span>

<span data-ttu-id="fe10e-144">Если эта **запись** был получен из [набора записей](recordset-object-ado.md), новое расположение перемещенной файла или папки не будут отражены в **набор записей**сразу же.</span><span class="sxs-lookup"><span data-stu-id="fe10e-144">If this **Record** was obtained from a [Recordset](recordset-object-ado.md), the new location of the moved file or directory will not be reflected immediately in the **Recordset**.</span></span> <span data-ttu-id="fe10e-145">Обновление **набора записей** с закрыть и повторно открыть его.</span><span class="sxs-lookup"><span data-stu-id="fe10e-145">Refresh the **Recordset** by closing and re-opening it.</span></span>

> [!NOTE]
> <span data-ttu-id="fe10e-146">URL-адреса, с помощью схемы http автоматически вызывает [Поставщик Microsoft OLE DB для публикации Интернет](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="fe10e-146">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="fe10e-147">Для получения дополнительных сведений см [абсолютных и относительных URL-адресов](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="fe10e-147">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


