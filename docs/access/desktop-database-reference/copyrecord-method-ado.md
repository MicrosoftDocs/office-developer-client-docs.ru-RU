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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295529"
---
# <a name="copyrecord-method-ado"></a><span data-ttu-id="6d6af-102">Метод CopyRecord (ADO)</span><span class="sxs-lookup"><span data-stu-id="6d6af-102">CopyRecord method (ADO)</span></span>

<span data-ttu-id="6d6af-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6d6af-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6d6af-104">Копирует объект, представленный **записью** , в другое расположение.</span><span class="sxs-lookup"><span data-stu-id="6d6af-104">Copies a entity represented by a **Record** to another location.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d6af-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6d6af-105">Syntax</span></span>

<span data-ttu-id="6d6af-106">*Запись*. CopyRecord (*источник*, *назначение*, *имя пользователя*, *пароль*, *Параметры*, *асинхронно*)</span><span class="sxs-lookup"><span data-stu-id="6d6af-106">*Record*.CopyRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)</span></span>

## <a name="parameters"></a><span data-ttu-id="6d6af-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="6d6af-107">Parameters</span></span>

|<span data-ttu-id="6d6af-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="6d6af-108">Parameter</span></span>|<span data-ttu-id="6d6af-109">Описание</span><span class="sxs-lookup"><span data-stu-id="6d6af-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="6d6af-110">*Source*</span><span class="sxs-lookup"><span data-stu-id="6d6af-110">*Source*</span></span> |<span data-ttu-id="6d6af-111">Необязательное.</span><span class="sxs-lookup"><span data-stu-id="6d6af-111">Optional.</span></span> <span data-ttu-id="6d6af-112">**Строковое** значение, содержащее URL-адрес, указывающий копируемую сущность (например, файл или каталог).</span><span class="sxs-lookup"><span data-stu-id="6d6af-112">A **String** value that contains a URL specifying the entity to be copied (for example, a file or directory).</span></span> <span data-ttu-id="6d6af-113">Если параметр *Source* опущен или указывает пустую строку, будет скопирован файл или каталог, представленный текущей [записью](record-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="6d6af-113">If *Source* is omitted or specifies an empty string, the file or directory represented by the current [Record](record-object-ado.md) will be copied.</span></span>|
|<span data-ttu-id="6d6af-114">*Destination*</span><span class="sxs-lookup"><span data-stu-id="6d6af-114">*Destination*</span></span> |<span data-ttu-id="6d6af-115">Необязательное.</span><span class="sxs-lookup"><span data-stu-id="6d6af-115">Optional.</span></span> <span data-ttu-id="6d6af-116">**Строковое** значение, содержащее URL-адрес, указывающий расположение, в которое будет скопирован *источник* .</span><span class="sxs-lookup"><span data-stu-id="6d6af-116">A **String** value that contains a URL specifying the location where *Source* will be copied.</span></span>|
|<span data-ttu-id="6d6af-117">*UserName*</span><span class="sxs-lookup"><span data-stu-id="6d6af-117">*UserName*</span></span> |<span data-ttu-id="6d6af-118">Необязательное.</span><span class="sxs-lookup"><span data-stu-id="6d6af-118">Optional.</span></span> <span data-ttu-id="6d6af-119">**Строковое** значение, содержащее идентификатор пользователя, который при необходимости авторизует доступ к *назначению*.</span><span class="sxs-lookup"><span data-stu-id="6d6af-119">A **String** value that contains the user ID that, if needed, authorizes access to *Destination*.</span></span>|
|<span data-ttu-id="6d6af-120">*Password*</span><span class="sxs-lookup"><span data-stu-id="6d6af-120">*Password*</span></span> |<span data-ttu-id="6d6af-121">Необязательное.</span><span class="sxs-lookup"><span data-stu-id="6d6af-121">Optional.</span></span> <span data-ttu-id="6d6af-122">**Строковое** значение, которое содержит пароль, при необходимости проверяющий *имя пользователя*.</span><span class="sxs-lookup"><span data-stu-id="6d6af-122">A **String** value that contains the password that, if needed, verifies *UserName*.</span></span>|
|<span data-ttu-id="6d6af-123">*Параметры*</span><span class="sxs-lookup"><span data-stu-id="6d6af-123">*Options*</span></span> |<span data-ttu-id="6d6af-124">Необязательное.</span><span class="sxs-lookup"><span data-stu-id="6d6af-124">Optional.</span></span> <span data-ttu-id="6d6af-125">Значение [копирекордоптионсенум](copyrecordoptionsenum.md) , значение которого по умолчанию — **адкопюнспеЦифиед**.</span><span class="sxs-lookup"><span data-stu-id="6d6af-125">A [CopyRecordOptionsEnum](copyrecordoptionsenum.md) value that has a default value of **adCopyUnspecified**.</span></span> <span data-ttu-id="6d6af-126">Задает поведение этого метода.</span><span class="sxs-lookup"><span data-stu-id="6d6af-126">Specifies the behavior of this method.</span></span>|
|<span data-ttu-id="6d6af-127">*Асинхронного*</span><span class="sxs-lookup"><span data-stu-id="6d6af-127">*Async*</span></span> |<span data-ttu-id="6d6af-128">Необязательное.</span><span class="sxs-lookup"><span data-stu-id="6d6af-128">Optional.</span></span> <span data-ttu-id="6d6af-129">**Логическое** значение, которое при **значении true**указывает, что эта операция должна быть асинхронной.</span><span class="sxs-lookup"><span data-stu-id="6d6af-129">A **Boolean** value that, when **True**, specifies that this operation should be asynchronous.</span></span>|

## <a name="return-value"></a><span data-ttu-id="6d6af-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6d6af-130">Return value</span></span>

<span data-ttu-id="6d6af-131">**Строковое** значение, которое обычно возвращает значение *Destination*.</span><span class="sxs-lookup"><span data-stu-id="6d6af-131">A **String** value that typically returns the value of *Destination*.</span></span> <span data-ttu-id="6d6af-132">Тем не менее, возвращаемое значение зависит от поставщика.</span><span class="sxs-lookup"><span data-stu-id="6d6af-132">However, the exact value returned is provider-dependent.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d6af-133">Примечания</span><span class="sxs-lookup"><span data-stu-id="6d6af-133">Remarks</span></span>

<span data-ttu-id="6d6af-134">Значения *Source* и *Destination* не должны совпадать; в противном случае возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="6d6af-134">The values of *Source* and *Destination* must not be identical; otherwise, a run-time error occurs.</span></span> <span data-ttu-id="6d6af-135">По крайней мере один из имен серверов, путей или ресурсов должен отличаться.</span><span class="sxs-lookup"><span data-stu-id="6d6af-135">At least one of the server, path, or resource names must differ.</span></span>

<span data-ttu-id="6d6af-136">Все дочерние объекты (например, подкаталоги) *источника* копируются рекурсивно, если не указан **адкопинонрекурсиве** .</span><span class="sxs-lookup"><span data-stu-id="6d6af-136">All children (for example, subdirectories) of *Source* are copied recursively, unless **adCopyNonRecursive** is specified.</span></span> <span data-ttu-id="6d6af-137">В рекурсивной операции *назначение* не должно быть подкаталогом *источника*; в противном случае операция не будет завершена.</span><span class="sxs-lookup"><span data-stu-id="6d6af-137">In a recursive operation, *Destination* must not be a subdirectory of *Source*; otherwise, the operation will not complete.</span></span>

<span data-ttu-id="6d6af-138">Этот метод завершается с ошибкой, если *объект Destination* определяет существующую сущность (например, файл или каталог), если не указан **адкопйоверврите** .</span><span class="sxs-lookup"><span data-stu-id="6d6af-138">This method fails if *Destination* identifies an existing entity (for example, a file or directory), unless **adCopyOverWrite** is specified.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6d6af-139">Внимательно используйте параметр **адкопйоверврите** .</span><span class="sxs-lookup"><span data-stu-id="6d6af-139">Use the **adCopyOverWrite** option judiciously.</span></span> <span data-ttu-id="6d6af-140">Например, при указании этого параметра при копировании файла в каталог *удаляется* каталог и заменяется файлом.</span><span class="sxs-lookup"><span data-stu-id="6d6af-140">For example, specifying this option when copying a file to a directory will *delete* the directory and replace it with the file.</span></span>


> [!NOTE]
> <span data-ttu-id="6d6af-141">URL-адреса, использующие схему HTTP, автоматически будут вызывать [поставщик Microsoft OLE DB для публикации в Интернете](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="6d6af-141">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="6d6af-142">Для получения дополнительных сведений см [абсолютные и относительные URL-адреса](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="6d6af-142">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


