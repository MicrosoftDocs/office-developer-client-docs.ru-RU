---
title: CopyRecord Method (ADO)
TOCTitle: CopyRecord Method (ADO)
ms:assetid: 724e4358-f216-8e47-5bab-c72770ece5a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249459(v=office.15)
ms:contentKeyID: 48545605
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 73940108f96cf46cb15d646936039c0329373899
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606908"
---
# <a name="copyrecord-method-ado"></a><span data-ttu-id="0fa21-102">CopyRecord Method (ADO)</span><span class="sxs-lookup"><span data-stu-id="0fa21-102">CopyRecord Method (ADO)</span></span>


<span data-ttu-id="0fa21-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0fa21-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0fa21-104">Копирует сущности, представленной в **записи** в другое расположение.</span><span class="sxs-lookup"><span data-stu-id="0fa21-104">Copies a entity represented by a **Record** to another location.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fa21-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0fa21-105">Syntax</span></span>

<span data-ttu-id="0fa21-106">*Запись*. CopyRecord (*источника*, *назначения*, *имя пользователя*, *пароль*, *Параметры*, *асинхронного*)</span><span class="sxs-lookup"><span data-stu-id="0fa21-106">*Record*.CopyRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)</span></span>

## <a name="parameters"></a><span data-ttu-id="0fa21-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="0fa21-107">Parameters</span></span>

  - <span data-ttu-id="0fa21-108">*Source*</span><span class="sxs-lookup"><span data-stu-id="0fa21-108">*Source*</span></span>

  - <span data-ttu-id="0fa21-109">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="0fa21-109">Optional.</span></span> <span data-ttu-id="0fa21-110">**Строковое** значение, содержащее URL-адрес указание сущности для копирования (например, файла или папки).</span><span class="sxs-lookup"><span data-stu-id="0fa21-110">A **String** value that contains a URL specifying the entity to be copied (for example, a file or directory).</span></span> <span data-ttu-id="0fa21-111">Если *источник* указан или указывает пустая строка, файл или папка, представленное текущей [записи](record-object-ado.md) копируются.</span><span class="sxs-lookup"><span data-stu-id="0fa21-111">If *Source* is omitted or specifies an empty string, the file or directory represented by the current [Record](record-object-ado.md) will be copied.</span></span>

  - <span data-ttu-id="0fa21-112">*Назначения*</span><span class="sxs-lookup"><span data-stu-id="0fa21-112">*Destination*</span></span>

  - <span data-ttu-id="0fa21-113">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="0fa21-113">Optional.</span></span> <span data-ttu-id="0fa21-114">**Строковое** значение, содержащее URL-адрес, определяющее расположение, где будет скопирована *источника* .</span><span class="sxs-lookup"><span data-stu-id="0fa21-114">A **String** value that contains a URL specifying the location where *Source* will be copied.</span></span>

  - <span data-ttu-id="0fa21-115">*Имя пользователя*</span><span class="sxs-lookup"><span data-stu-id="0fa21-115">*UserName*</span></span>

  - <span data-ttu-id="0fa21-116">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="0fa21-116">Optional.</span></span> <span data-ttu-id="0fa21-117">**Строковое** значение, содержащее идентификатор пользователя, при необходимости, авторизует доступ в *место назначения*.</span><span class="sxs-lookup"><span data-stu-id="0fa21-117">A **String** value that contains the user ID that, if needed, authorizes access to *Destination*.</span></span>

  - <span data-ttu-id="0fa21-118">*Password*</span><span class="sxs-lookup"><span data-stu-id="0fa21-118">*Password*</span></span>

  - <span data-ttu-id="0fa21-119">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="0fa21-119">Optional.</span></span> <span data-ttu-id="0fa21-120">**Строковое** значение, содержащее пароль, при необходимости, выполняется проверка *имени пользователя*.</span><span class="sxs-lookup"><span data-stu-id="0fa21-120">A **String** value that contains the password that, if needed, verifies *UserName*.</span></span>

  - <span data-ttu-id="0fa21-121">*Варианты*</span><span class="sxs-lookup"><span data-stu-id="0fa21-121">*Options*</span></span>

  - <span data-ttu-id="0fa21-122">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="0fa21-122">Optional.</span></span> <span data-ttu-id="0fa21-123">Значение [CopyRecordOptionsEnum](copyrecordoptionsenum.md) , который имеет значение по умолчанию **adCopyUnspecified**.</span><span class="sxs-lookup"><span data-stu-id="0fa21-123">A [CopyRecordOptionsEnum](copyrecordoptionsenum.md) value that has a default value of **adCopyUnspecified**.</span></span> <span data-ttu-id="0fa21-124">Задает поведение этого метода.</span><span class="sxs-lookup"><span data-stu-id="0fa21-124">Specifies the behavior of this method.</span></span>

  - <span data-ttu-id="0fa21-125">*Async*</span><span class="sxs-lookup"><span data-stu-id="0fa21-125">*Async*</span></span>

  - <span data-ttu-id="0fa21-126">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="0fa21-126">Optional.</span></span> <span data-ttu-id="0fa21-127">**Логическое** значение, которое, если **значение True**, указывает, что эта операция должна быть асинхронной.</span><span class="sxs-lookup"><span data-stu-id="0fa21-127">A **Boolean** value that, when **True**, specifies that this operation should be asynchronous.</span></span>

<span data-ttu-id="0fa21-128"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="0fa21-128"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="0fa21-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0fa21-129">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="0fa21-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0fa21-130">Return value</span></span>
>>>>>>> <span data-ttu-id="0fa21-131">master</span><span class="sxs-lookup"><span data-stu-id="0fa21-131">master</span></span>

<span data-ttu-id="0fa21-132">**Строковое** значение, которое обычно возвращает значение *назначения*.</span><span class="sxs-lookup"><span data-stu-id="0fa21-132">A **String** value that typically returns the value of *Destination*.</span></span> <span data-ttu-id="0fa21-133">Тем не менее точное значение, возвращаемое зависит от поставщика.</span><span class="sxs-lookup"><span data-stu-id="0fa21-133">However, the exact value returned is provider-dependent.</span></span>

## <a name="remarks"></a><span data-ttu-id="0fa21-134">Замечания</span><span class="sxs-lookup"><span data-stu-id="0fa21-134">Remarks</span></span>

<span data-ttu-id="0fa21-135">Значения из *источника* и *назначения* не должны совпадать; в противном случае возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="0fa21-135">The values of *Source* and *Destination* must not be identical; otherwise, a run-time error occurs.</span></span> <span data-ttu-id="0fa21-136">По крайней мере одно из имен сервера, пути или имени ресурса должны отличаться.</span><span class="sxs-lookup"><span data-stu-id="0fa21-136">At least one of the server, path, or resource names must differ.</span></span>

<span data-ttu-id="0fa21-137">Все дочерние элементы (например, вложенные папки) *источник* , скопированный рекурсивно, если не указано **adCopyNonRecursive** .</span><span class="sxs-lookup"><span data-stu-id="0fa21-137">All children (for example, subdirectories) of *Source* are copied recursively, unless **adCopyNonRecursive** is specified.</span></span> <span data-ttu-id="0fa21-138">В ходе операции рекурсивный *назначения* не должна быть подкаталог *источника*; в противном случае операция не завершена.</span><span class="sxs-lookup"><span data-stu-id="0fa21-138">In a recursive operation, *Destination* must not be a subdirectory of *Source*; otherwise, the operation will not complete.</span></span>

<span data-ttu-id="0fa21-139">Этот метод не выполняется, если *конечный* идентифицирует существующей сущности (например, файла или каталога), если не указано **adCopyOverWrite** .</span><span class="sxs-lookup"><span data-stu-id="0fa21-139">This method fails if *Destination* identifies an existing entity (for example, a file or directory), unless **adCopyOverWrite** is specified.</span></span>


> [!IMPORTANT]
> <P><span data-ttu-id="0fa21-140">Параметр <STRONG>adCopyOverWrite</STRONG> внимательно.</span><span class="sxs-lookup"><span data-stu-id="0fa21-140">Use the <STRONG>adCopyOverWrite</STRONG> option judiciously.</span></span> <span data-ttu-id="0fa21-141">Например задание этого параметра при копировании файлов в каталог будет <EM>Удалить</EM> каталог и замените файл.</span><span class="sxs-lookup"><span data-stu-id="0fa21-141">For example, specifying this option when copying a file to a directory will <EM>delete</EM> the directory and replace it with the file.</span></span></P>




> [!NOTE]
<span data-ttu-id="0fa21-142"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="0fa21-142"><<<<<<< HEAD</span></span>
> <P><span data-ttu-id="0fa21-143">URL-адреса, с помощью схемы http автоматически вызывает <A href="microsoft-ole-db-provider-for-internet-publishing.md">Поставщик Microsoft OLE DB для публикации Интернет</A>.</span><span class="sxs-lookup"><span data-stu-id="0fa21-143">URLs using the http scheme will automatically invoke the <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB Provider for Internet Publishing</A>.</span></span> <span data-ttu-id="0fa21-144">Для получения дополнительных сведений см <A href="absolute-and-relative-urls.md">абсолютного и относительных URL-адресов</A>.</span><span class="sxs-lookup"><span data-stu-id="0fa21-144">For more information, see <A href="absolute-and-relative-urls.md">Absolute and Relative URLs</A>.</span></span></P>
=======
> <span data-ttu-id="0fa21-145">URL-адреса, с помощью схемы http автоматически вызывает [Поставщик Microsoft OLE DB для публикации Интернет](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="0fa21-145">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="0fa21-146">Для получения дополнительных сведений см [абсолютных и относительных URL-адресов](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="0fa21-146">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>
>>>>>>> <span data-ttu-id="0fa21-147">master</span><span class="sxs-lookup"><span data-stu-id="0fa21-147">master</span></span>


