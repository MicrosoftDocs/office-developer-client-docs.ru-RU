---
title: MoveRecord Method (ADO)
TOCTitle: MoveRecord Method (ADO)
ms:assetid: efc341a2-0e08-a838-5925-8d4c46377e48
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250217(v=office.15)
ms:contentKeyID: 48548588
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fd7496efe7c38fcd78800ad087730bb21a19c32e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481355"
---
# <a name="moverecord-method-ado"></a><span data-ttu-id="ccfce-102">MoveRecord Method (ADO)</span><span class="sxs-lookup"><span data-stu-id="ccfce-102">MoveRecord Method (ADO)</span></span>


<span data-ttu-id="ccfce-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ccfce-103">**Applies to**: Access 2013 | Office 2013</span></span>
 

<span data-ttu-id="ccfce-104">Перемещает сущности представляют [записи](record-object-ado.md) в другое расположение.</span><span class="sxs-lookup"><span data-stu-id="ccfce-104">Moves the entity represent by a [Record](record-object-ado.md) to another location.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccfce-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ccfce-105">Syntax</span></span>

<span data-ttu-id="ccfce-106">*Запись*. MoveRecord (*источника*, *назначения*, *имя пользователя*, *пароль*, *Параметры*, *асинхронного*)</span><span class="sxs-lookup"><span data-stu-id="ccfce-106">*Record*.MoveRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)</span></span>

## <a name="parameters"></a><span data-ttu-id="ccfce-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ccfce-107">Parameters</span></span>

  - <span data-ttu-id="ccfce-108">*Source*</span><span class="sxs-lookup"><span data-stu-id="ccfce-108">*Source*</span></span>

  - <span data-ttu-id="ccfce-109">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="ccfce-109">Optional.</span></span> <span data-ttu-id="ccfce-110">**Строковое** значение, содержащее URL-адрес, идентифицирующий эту **запись** переместить.</span><span class="sxs-lookup"><span data-stu-id="ccfce-110">A **String** value that contains a URL identifying the **Record** to be moved.</span></span> <span data-ttu-id="ccfce-111">Если *источник* указан или указывает пустая строка, перемещается объект, представленный этой **записи** .</span><span class="sxs-lookup"><span data-stu-id="ccfce-111">If *Source* is omitted or specifies an empty string, the object represented by this **Record** is moved.</span></span> <span data-ttu-id="ccfce-112">Например если **запись** представляет файл, содержимое файла перемещаются местоположение, указанное для *назначения*.</span><span class="sxs-lookup"><span data-stu-id="ccfce-112">For example, if the **Record** represents a file, the contents of the file are moved to the location specified by *Destination*.</span></span>

  - <span data-ttu-id="ccfce-113">*Назначения*</span><span class="sxs-lookup"><span data-stu-id="ccfce-113">*Destination*</span></span>

  - <span data-ttu-id="ccfce-114">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="ccfce-114">Optional.</span></span> <span data-ttu-id="ccfce-115">**Строковое** значение, содержащее URL-адрес, указав расположение, где будут перемещены *источника* .</span><span class="sxs-lookup"><span data-stu-id="ccfce-115">A **String** value that contains a URL specifying the location where *Source* will be moved.</span></span>

  - <span data-ttu-id="ccfce-116">*Имя пользователя*</span><span class="sxs-lookup"><span data-stu-id="ccfce-116">*UserName*</span></span>

  - <span data-ttu-id="ccfce-117">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="ccfce-117">Optional.</span></span> <span data-ttu-id="ccfce-118">**Строковое** значение, содержащее идентификатор пользователя, при необходимости, авторизует доступ в *место назначения*.</span><span class="sxs-lookup"><span data-stu-id="ccfce-118">A **String** value that contains the user ID that, if needed, authorizes access to *Destination*.</span></span>

  - <span data-ttu-id="ccfce-119">*Password*</span><span class="sxs-lookup"><span data-stu-id="ccfce-119">*Password*</span></span>

  - <span data-ttu-id="ccfce-120">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="ccfce-120">Optional.</span></span> <span data-ttu-id="ccfce-121">**Строка** , содержащая пароль, при необходимости, выполняется проверка *имени пользователя*.</span><span class="sxs-lookup"><span data-stu-id="ccfce-121">A **String** that contains the password that, if needed, verifies *UserName*.</span></span>

  - <span data-ttu-id="ccfce-122">*Варианты*</span><span class="sxs-lookup"><span data-stu-id="ccfce-122">*Options*</span></span>

  - <span data-ttu-id="ccfce-123">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="ccfce-123">Optional.</span></span> <span data-ttu-id="ccfce-124">Значение [MoveRecordOptionsEnum](moverecordoptionsenum.md) , чье значение по умолчанию — **adMoveUnspecified**.</span><span class="sxs-lookup"><span data-stu-id="ccfce-124">A [MoveRecordOptionsEnum](moverecordoptionsenum.md) value whose default value is **adMoveUnspecified**.</span></span> <span data-ttu-id="ccfce-125">Задает поведение этого метода.</span><span class="sxs-lookup"><span data-stu-id="ccfce-125">Specifies the behavior of this method.</span></span>

  - <span data-ttu-id="ccfce-126">*Async*</span><span class="sxs-lookup"><span data-stu-id="ccfce-126">*Async*</span></span>

  - <span data-ttu-id="ccfce-127">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="ccfce-127">Optional.</span></span> <span data-ttu-id="ccfce-128">**Логическое** значение, которое, если **значение True**, указывает, что эту операцию следует асинхронный.</span><span class="sxs-lookup"><span data-stu-id="ccfce-128">A **Boolean** value that, when **True**, specifies this operation should be asynchronous .</span></span>

## <a name="return-value"></a><span data-ttu-id="ccfce-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ccfce-129">Return Value</span></span>

<span data-ttu-id="ccfce-130">**Строковое** значение.</span><span class="sxs-lookup"><span data-stu-id="ccfce-130">A **String** value.</span></span> <span data-ttu-id="ccfce-131">Как правило возвращается значение *назначения* .</span><span class="sxs-lookup"><span data-stu-id="ccfce-131">Typically, the value of *Destination* is returned.</span></span> <span data-ttu-id="ccfce-132">Тем не менее точное значение, возвращаемое зависит от поставщика.</span><span class="sxs-lookup"><span data-stu-id="ccfce-132">However, the exact value returned is provider-dependent.</span></span>

## <a name="remarks"></a><span data-ttu-id="ccfce-133">Замечания</span><span class="sxs-lookup"><span data-stu-id="ccfce-133">Remarks</span></span>

<span data-ttu-id="ccfce-134">Значения из *источника* и *назначения* не должны совпадать; в противном случае возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="ccfce-134">The values of *Source* and *Destination* must not be identical; otherwise, a run-time error occurs.</span></span> <span data-ttu-id="ccfce-135">По крайней мере имена серверов, пути и ресурсов должны отличаться.</span><span class="sxs-lookup"><span data-stu-id="ccfce-135">At least the server, path, and resource names must differ.</span></span>

<span data-ttu-id="ccfce-136">Для файлов, перемещенных с использованием поставщика публикации Интернета этот метод обновляет все ссылки гиперссылку в файлах, происходит перемещение, если не указано иное, *Параметры*.</span><span class="sxs-lookup"><span data-stu-id="ccfce-136">For files moved using the Internet Publishing Provider, this method updates all hypertext links in files being moved unless otherwise specified by *Options*.</span></span> <span data-ttu-id="ccfce-137">Этот метод не выполняется, если *конечный* идентифицирует существующий объект (например, файла или каталога), если не указано **adMoveOverWrite** .</span><span class="sxs-lookup"><span data-stu-id="ccfce-137">This method fails if *Destination* identifies an existing object (for example, a file or directory), unless **adMoveOverWrite** is specified.</span></span>


> [!NOTE]
> <P><span data-ttu-id="ccfce-138">Параметр <STRONG>adMoveOverWrite</STRONG> внимательно.</span><span class="sxs-lookup"><span data-stu-id="ccfce-138">Use the <STRONG>adMoveOverWrite</STRONG> option judiciously.</span></span> <span data-ttu-id="ccfce-139">Например задание этого параметра при переносе в файл в каталоге будет удалите каталог и замените файл.</span><span class="sxs-lookup"><span data-stu-id="ccfce-139">For example, specifying this option when moving a file to a directory will delete the directory and replace it with the file.</span></span></P>



<span data-ttu-id="ccfce-140">Некоторые атрибуты объекта **записи** , такими как свойство [ParentURL](parenturl-property-ado.md) , не будут обновляться после завершения этой операции.</span><span class="sxs-lookup"><span data-stu-id="ccfce-140">Certain attributes of the **Record** object, such as the [ParentURL](parenturl-property-ado.md) property, will not be updated after this operation completes.</span></span> <span data-ttu-id="ccfce-141">Обновление свойств объекта **записи** , **записи**закрытия, а затем повторно открыть его URL-адрес, где был перемещен в файл или папку.</span><span class="sxs-lookup"><span data-stu-id="ccfce-141">Refresh the **Record** object's properties by closing the **Record**, then re-opening it with the URL of the location where the file or directory was moved.</span></span>

<span data-ttu-id="ccfce-142">Если эта **запись** был получен из [набора записей](recordset-object-ado.md), новое расположение перемещенной файла или папки не будут отражены в **набор записей**сразу же.</span><span class="sxs-lookup"><span data-stu-id="ccfce-142">If this **Record** was obtained from a [Recordset](recordset-object-ado.md), the new location of the moved file or directory will not be reflected immediately in the **Recordset**.</span></span> <span data-ttu-id="ccfce-143">Обновление **набора записей** с закрыть и повторно открыть его.</span><span class="sxs-lookup"><span data-stu-id="ccfce-143">Refresh the **Recordset** by closing and re-opening it.</span></span>


> [!NOTE]
> <P><span data-ttu-id="ccfce-144">URL-адреса, с помощью схемы http автоматически вызывает <A href="microsoft-ole-db-provider-for-internet-publishing.md">Поставщик Microsoft OLE DB для публикации Интернет</A>.</span><span class="sxs-lookup"><span data-stu-id="ccfce-144">URLs using the http scheme will automatically invoke the <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>.</span></span> <span data-ttu-id="ccfce-145">Для получения дополнительных сведений см <A href="absolute-and-relative-urls.md">абсолютного и относительных URL-адресов</A>.</span><span class="sxs-lookup"><span data-stu-id="ccfce-145">For more information, see <A href="absolute-and-relative-urls.md">Absolute and Relative URLs</A>.</span></span></P>


