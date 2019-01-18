---
title: Метод CopyRecord (ADO)
TOCTitle: CopyRecord method (ADO)
ms:assetid: 724e4358-f216-8e47-5bab-c72770ece5a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249459(v=office.15)
ms:contentKeyID: 48545605
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c5aac745bacf0662f6cd389bfefde7182a9676d3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700831"
---
# <a name="copyrecord-method-ado"></a><span data-ttu-id="2489e-102">Метод CopyRecord (ADO)</span><span class="sxs-lookup"><span data-stu-id="2489e-102">CopyRecord method (ADO)</span></span>

<span data-ttu-id="2489e-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2489e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2489e-104">Копирует сущности, представленной в **записи** в другое расположение.</span><span class="sxs-lookup"><span data-stu-id="2489e-104">Copies a entity represented by a **Record** to another location.</span></span>

## <a name="syntax"></a><span data-ttu-id="2489e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2489e-105">Syntax</span></span>

<span data-ttu-id="2489e-106">*Запись*. CopyRecord (*источника*, *назначения*, *имя пользователя*, *пароль*, *Параметры*, *асинхронного*)</span><span class="sxs-lookup"><span data-stu-id="2489e-106">*Record*.CopyRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)</span></span>

## <a name="parameters"></a><span data-ttu-id="2489e-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="2489e-107">Parameters</span></span>

|<span data-ttu-id="2489e-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="2489e-108">Parameter</span></span>|<span data-ttu-id="2489e-109">Описание</span><span class="sxs-lookup"><span data-stu-id="2489e-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="2489e-110">*Source*</span><span class="sxs-lookup"><span data-stu-id="2489e-110">*Source*</span></span> |<span data-ttu-id="2489e-111">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="2489e-111">Optional.</span></span> <span data-ttu-id="2489e-112">**Строковое** значение, содержащее URL-адрес указание сущности для копирования (например, файла или папки).</span><span class="sxs-lookup"><span data-stu-id="2489e-112">A **String** value that contains a URL specifying the entity to be copied (for example, a file or directory).</span></span> <span data-ttu-id="2489e-113">Если *источник* указан или указывает пустая строка, файл или папка, представленное текущей [записи](record-object-ado.md) копируются.</span><span class="sxs-lookup"><span data-stu-id="2489e-113">If *Source* is omitted or specifies an empty string, the file or directory represented by the current [Record](record-object-ado.md) will be copied.</span></span>|
|<span data-ttu-id="2489e-114">*Destination*</span><span class="sxs-lookup"><span data-stu-id="2489e-114">*Destination*</span></span> |<span data-ttu-id="2489e-115">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="2489e-115">Optional.</span></span> <span data-ttu-id="2489e-116">**Строковое** значение, содержащее URL-адрес, определяющее расположение, где будет скопирована *источника* .</span><span class="sxs-lookup"><span data-stu-id="2489e-116">A **String** value that contains a URL specifying the location where *Source* will be copied.</span></span>|
|<span data-ttu-id="2489e-117">*UserName*</span><span class="sxs-lookup"><span data-stu-id="2489e-117">*UserName*</span></span> |<span data-ttu-id="2489e-118">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="2489e-118">Optional.</span></span> <span data-ttu-id="2489e-119">**Строковое** значение, содержащее идентификатор пользователя, при необходимости, авторизует доступ в *место назначения*.</span><span class="sxs-lookup"><span data-stu-id="2489e-119">A **String** value that contains the user ID that, if needed, authorizes access to *Destination*.</span></span>|
|<span data-ttu-id="2489e-120">*Password*</span><span class="sxs-lookup"><span data-stu-id="2489e-120">*Password*</span></span> |<span data-ttu-id="2489e-121">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="2489e-121">Optional.</span></span> <span data-ttu-id="2489e-122">**Строковое** значение, содержащее пароль, при необходимости, выполняется проверка *имени пользователя*.</span><span class="sxs-lookup"><span data-stu-id="2489e-122">A **String** value that contains the password that, if needed, verifies *UserName*.</span></span>|
|<span data-ttu-id="2489e-123">*Варианты*</span><span class="sxs-lookup"><span data-stu-id="2489e-123">*Options*</span></span> |<span data-ttu-id="2489e-124">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="2489e-124">Optional.</span></span> <span data-ttu-id="2489e-125">Значение [CopyRecordOptionsEnum](copyrecordoptionsenum.md) , который имеет значение по умолчанию **adCopyUnspecified**.</span><span class="sxs-lookup"><span data-stu-id="2489e-125">A [CopyRecordOptionsEnum](copyrecordoptionsenum.md) value that has a default value of **adCopyUnspecified**.</span></span> <span data-ttu-id="2489e-126">Задает поведение этого метода.</span><span class="sxs-lookup"><span data-stu-id="2489e-126">Specifies the behavior of this method.</span></span>|
|<span data-ttu-id="2489e-127">*Async*</span><span class="sxs-lookup"><span data-stu-id="2489e-127">*Async*</span></span> |<span data-ttu-id="2489e-128">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="2489e-128">Optional.</span></span> <span data-ttu-id="2489e-129">**Логическое** значение, которое, если **значение True**, указывает, что эта операция должна быть асинхронной.</span><span class="sxs-lookup"><span data-stu-id="2489e-129">A **Boolean** value that, when **True**, specifies that this operation should be asynchronous.</span></span>|

## <a name="return-value"></a><span data-ttu-id="2489e-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2489e-130">Return value</span></span>

<span data-ttu-id="2489e-131">**Строковое** значение, которое обычно возвращает значение *назначения*.</span><span class="sxs-lookup"><span data-stu-id="2489e-131">A **String** value that typically returns the value of *Destination*.</span></span> <span data-ttu-id="2489e-132">Тем не менее точное значение, возвращаемое зависит от поставщика.</span><span class="sxs-lookup"><span data-stu-id="2489e-132">However, the exact value returned is provider-dependent.</span></span>

## <a name="remarks"></a><span data-ttu-id="2489e-133">Замечания</span><span class="sxs-lookup"><span data-stu-id="2489e-133">Remarks</span></span>

<span data-ttu-id="2489e-134">Значения из *источника* и *назначения* не должны совпадать; в противном случае возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="2489e-134">The values of *Source* and *Destination* must not be identical; otherwise, a run-time error occurs.</span></span> <span data-ttu-id="2489e-135">По крайней мере одно из имен сервера, пути или имени ресурса должны отличаться.</span><span class="sxs-lookup"><span data-stu-id="2489e-135">At least one of the server, path, or resource names must differ.</span></span>

<span data-ttu-id="2489e-136">Все дочерние элементы (например, вложенные папки) *источник* , скопированный рекурсивно, если не указано **adCopyNonRecursive** .</span><span class="sxs-lookup"><span data-stu-id="2489e-136">All children (for example, subdirectories) of *Source* are copied recursively, unless **adCopyNonRecursive** is specified.</span></span> <span data-ttu-id="2489e-137">В ходе операции рекурсивный *назначения* не должна быть подкаталог *источника*; в противном случае операция не завершена.</span><span class="sxs-lookup"><span data-stu-id="2489e-137">In a recursive operation, *Destination* must not be a subdirectory of *Source*; otherwise, the operation will not complete.</span></span>

<span data-ttu-id="2489e-138">Этот метод не выполняется, если *конечный* идентифицирует существующей сущности (например, файла или каталога), если не указано **adCopyOverWrite** .</span><span class="sxs-lookup"><span data-stu-id="2489e-138">This method fails if *Destination* identifies an existing entity (for example, a file or directory), unless **adCopyOverWrite** is specified.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2489e-139">Параметр **adCopyOverWrite** внимательно.</span><span class="sxs-lookup"><span data-stu-id="2489e-139">Use the **adCopyOverWrite** option judiciously.</span></span> <span data-ttu-id="2489e-140">Например задание этого параметра при копировании файлов в каталог будет *Удалить* каталог и замените файл.</span><span class="sxs-lookup"><span data-stu-id="2489e-140">For example, specifying this option when copying a file to a directory will *delete* the directory and replace it with the file.</span></span>


> [!NOTE]
> <span data-ttu-id="2489e-141">URL-адреса, с помощью схемы http автоматически вызывает [Поставщик Microsoft OLE DB для публикации Интернет](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="2489e-141">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="2489e-142">Для получения дополнительных сведений см [абсолютных и относительных URL-адресов](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="2489e-142">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


