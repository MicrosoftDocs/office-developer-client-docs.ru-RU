---
title: Метод MoveRecord (ADO)
TOCTitle: MoveRecord Method (ADO)
ms:assetid: efc341a2-0e08-a838-5925-8d4c46377e48
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250217(v=office.15)
ms:contentKeyID: 48548588
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 56c5b77d09ce568175b992391c8f3e7dcf3e9e15
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872055"
---
# <a name="moverecord-method-ado"></a><span data-ttu-id="e6b23-102">Метод MoveRecord (ADO)</span><span class="sxs-lookup"><span data-stu-id="e6b23-102">MoveRecord Method (ADO)</span></span>


<span data-ttu-id="e6b23-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e6b23-103">**Applies to**: Access 2013, Office 2013</span></span>
 

<span data-ttu-id="e6b23-104">Перемещает сущности представляют [записи](record-object-ado.md) в другое расположение.</span><span class="sxs-lookup"><span data-stu-id="e6b23-104">Moves the entity represent by a [Record](record-object-ado.md) to another location.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6b23-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e6b23-105">Syntax</span></span>

<span data-ttu-id="e6b23-106">*Запись*. MoveRecord (*источника*, *назначения*, *имя пользователя*, *пароль*, *Параметры*, *асинхронного*)</span><span class="sxs-lookup"><span data-stu-id="e6b23-106">*Record*.MoveRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)</span></span>

## <a name="parameters"></a><span data-ttu-id="e6b23-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e6b23-107">Parameters</span></span>

  - <span data-ttu-id="e6b23-108">*Source*</span><span class="sxs-lookup"><span data-stu-id="e6b23-108">*Source*</span></span>

  - <span data-ttu-id="e6b23-109">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="e6b23-109">Optional.</span></span> <span data-ttu-id="e6b23-110">**Строковое** значение, содержащее URL-адрес, идентифицирующий эту **запись** переместить.</span><span class="sxs-lookup"><span data-stu-id="e6b23-110">A **String** value that contains a URL identifying the **Record** to be moved.</span></span> <span data-ttu-id="e6b23-111">Если *источник* указан или указывает пустая строка, перемещается объект, представленный этой **записи** .</span><span class="sxs-lookup"><span data-stu-id="e6b23-111">If *Source* is omitted or specifies an empty string, the object represented by this **Record** is moved.</span></span> <span data-ttu-id="e6b23-112">Например если **запись** представляет файл, содержимое файла перемещаются местоположение, указанное для *назначения*.</span><span class="sxs-lookup"><span data-stu-id="e6b23-112">For example, if the **Record** represents a file, the contents of the file are moved to the location specified by *Destination*.</span></span>

  - <span data-ttu-id="e6b23-113">*Назначения*</span><span class="sxs-lookup"><span data-stu-id="e6b23-113">*Destination*</span></span>

  - <span data-ttu-id="e6b23-114">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="e6b23-114">Optional.</span></span> <span data-ttu-id="e6b23-115">**Строковое** значение, содержащее URL-адрес, указав расположение, где будут перемещены *источника* .</span><span class="sxs-lookup"><span data-stu-id="e6b23-115">A **String** value that contains a URL specifying the location where *Source* will be moved.</span></span>

  - <span data-ttu-id="e6b23-116">*Имя пользователя*</span><span class="sxs-lookup"><span data-stu-id="e6b23-116">*UserName*</span></span>

  - <span data-ttu-id="e6b23-117">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="e6b23-117">Optional.</span></span> <span data-ttu-id="e6b23-118">**Строковое** значение, содержащее идентификатор пользователя, при необходимости, авторизует доступ в *место назначения*.</span><span class="sxs-lookup"><span data-stu-id="e6b23-118">A **String** value that contains the user ID that, if needed, authorizes access to *Destination*.</span></span>

  - <span data-ttu-id="e6b23-119">*Password*</span><span class="sxs-lookup"><span data-stu-id="e6b23-119">*Password*</span></span>

  - <span data-ttu-id="e6b23-120">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="e6b23-120">Optional.</span></span> <span data-ttu-id="e6b23-121">**Строка** , содержащая пароль, при необходимости, выполняется проверка *имени пользователя*.</span><span class="sxs-lookup"><span data-stu-id="e6b23-121">A **String** that contains the password that, if needed, verifies *UserName*.</span></span>

  - <span data-ttu-id="e6b23-122">*Варианты*</span><span class="sxs-lookup"><span data-stu-id="e6b23-122">*Options*</span></span>

  - <span data-ttu-id="e6b23-123">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="e6b23-123">Optional.</span></span> <span data-ttu-id="e6b23-124">Значение [MoveRecordOptionsEnum](moverecordoptionsenum.md) , чье значение по умолчанию — **adMoveUnspecified**.</span><span class="sxs-lookup"><span data-stu-id="e6b23-124">A [MoveRecordOptionsEnum](moverecordoptionsenum.md) value whose default value is **adMoveUnspecified**.</span></span> <span data-ttu-id="e6b23-125">Задает поведение этого метода.</span><span class="sxs-lookup"><span data-stu-id="e6b23-125">Specifies the behavior of this method.</span></span>

  - <span data-ttu-id="e6b23-126">*Async*</span><span class="sxs-lookup"><span data-stu-id="e6b23-126">*Async*</span></span>

  - <span data-ttu-id="e6b23-127">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="e6b23-127">Optional.</span></span> <span data-ttu-id="e6b23-128">**Логическое** значение, которое, если **значение True**, указывает, что эту операцию следует асинхронный.</span><span class="sxs-lookup"><span data-stu-id="e6b23-128">A **Boolean** value that, when **True**, specifies this operation should be asynchronous .</span></span>

## <a name="return-value"></a><span data-ttu-id="e6b23-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e6b23-129">Return value</span></span>

<span data-ttu-id="e6b23-130">**Строковое** значение.</span><span class="sxs-lookup"><span data-stu-id="e6b23-130">A **String** value.</span></span> <span data-ttu-id="e6b23-131">Как правило возвращается значение *назначения* .</span><span class="sxs-lookup"><span data-stu-id="e6b23-131">Typically, the value of *Destination* is returned.</span></span> <span data-ttu-id="e6b23-132">Тем не менее точное значение, возвращаемое зависит от поставщика.</span><span class="sxs-lookup"><span data-stu-id="e6b23-132">However, the exact value returned is provider-dependent.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6b23-133">Замечания</span><span class="sxs-lookup"><span data-stu-id="e6b23-133">Remarks</span></span>

<span data-ttu-id="e6b23-134">Значения из *источника* и *назначения* не должны совпадать; в противном случае возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="e6b23-134">The values of *Source* and *Destination* must not be identical; otherwise, a run-time error occurs.</span></span> <span data-ttu-id="e6b23-135">По крайней мере имена серверов, пути и ресурсов должны отличаться.</span><span class="sxs-lookup"><span data-stu-id="e6b23-135">At least the server, path, and resource names must differ.</span></span>

<span data-ttu-id="e6b23-136">Для файлов, перемещенных с использованием поставщика публикации Интернета этот метод обновляет все ссылки гиперссылку в файлах, происходит перемещение, если не указано иное, *Параметры*.</span><span class="sxs-lookup"><span data-stu-id="e6b23-136">For files moved using the Internet Publishing Provider, this method updates all hypertext links in files being moved unless otherwise specified by *Options*.</span></span> <span data-ttu-id="e6b23-137">Этот метод не выполняется, если *конечный* идентифицирует существующий объект (например, файла или каталога), если не указано **adMoveOverWrite** .</span><span class="sxs-lookup"><span data-stu-id="e6b23-137">This method fails if *Destination* identifies an existing object (for example, a file or directory), unless **adMoveOverWrite** is specified.</span></span>


> [!NOTE]
> <P><span data-ttu-id="e6b23-138">Параметр <STRONG>adMoveOverWrite</STRONG> внимательно.</span><span class="sxs-lookup"><span data-stu-id="e6b23-138">Use the <STRONG>adMoveOverWrite</STRONG> option judiciously.</span></span> <span data-ttu-id="e6b23-139">Например задание этого параметра при переносе в файл в каталоге будет удалите каталог и замените файл.</span><span class="sxs-lookup"><span data-stu-id="e6b23-139">For example, specifying this option when moving a file to a directory will delete the directory and replace it with the file.</span></span></P>



<span data-ttu-id="e6b23-140">Некоторые атрибуты объекта **записи** , такими как свойство [ParentURL](parenturl-property-ado.md) , не будут обновляться после завершения этой операции.</span><span class="sxs-lookup"><span data-stu-id="e6b23-140">Certain attributes of the **Record** object, such as the [ParentURL](parenturl-property-ado.md) property, will not be updated after this operation completes.</span></span> <span data-ttu-id="e6b23-141">Обновление свойств объекта **записи** , **записи**закрытия, а затем повторно открыть его URL-адрес, где был перемещен в файл или папку.</span><span class="sxs-lookup"><span data-stu-id="e6b23-141">Refresh the **Record** object's properties by closing the **Record**, then re-opening it with the URL of the location where the file or directory was moved.</span></span>

<span data-ttu-id="e6b23-142">Если эта **запись** был получен из [набора записей](recordset-object-ado.md), новое расположение перемещенной файла или папки не будут отражены в **набор записей**сразу же.</span><span class="sxs-lookup"><span data-stu-id="e6b23-142">If this **Record** was obtained from a [Recordset](recordset-object-ado.md), the new location of the moved file or directory will not be reflected immediately in the **Recordset**.</span></span> <span data-ttu-id="e6b23-143">Обновление **набора записей** с закрыть и повторно открыть его.</span><span class="sxs-lookup"><span data-stu-id="e6b23-143">Refresh the **Recordset** by closing and re-opening it.</span></span>


> [!NOTE]
> <span data-ttu-id="e6b23-144">URL-адреса, с помощью схемы http автоматически вызывает [Поставщик Microsoft OLE DB для публикации Интернет](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="e6b23-144">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="e6b23-145">Для получения дополнительных сведений см [абсолютных и относительных URL-адресов](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="e6b23-145">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


