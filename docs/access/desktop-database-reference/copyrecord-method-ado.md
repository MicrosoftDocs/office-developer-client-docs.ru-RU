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
# <a name="copyrecord-method-ado"></a><span data-ttu-id="935a3-102">Метод CopyRecord (ADO)</span><span class="sxs-lookup"><span data-stu-id="935a3-102">CopyRecord method (ADO)</span></span>

<span data-ttu-id="935a3-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="935a3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="935a3-104">Копирует объект, представленный **записью,** в другое расположение.</span><span class="sxs-lookup"><span data-stu-id="935a3-104">Copies a entity represented by a **Record** to another location.</span></span>

## <a name="syntax"></a><span data-ttu-id="935a3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="935a3-105">Syntax</span></span>

<span data-ttu-id="935a3-106">*Запись*. CopyRecord (*Источник*, *Назначение*, *Имя пользователя*, *Пароль*, *Параметры*, *Async*)</span><span class="sxs-lookup"><span data-stu-id="935a3-106">*Record*.CopyRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)</span></span>

## <a name="parameters"></a><span data-ttu-id="935a3-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="935a3-107">Parameters</span></span>

|<span data-ttu-id="935a3-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="935a3-108">Parameter</span></span>|<span data-ttu-id="935a3-109">Описание</span><span class="sxs-lookup"><span data-stu-id="935a3-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="935a3-110">*Source*</span><span class="sxs-lookup"><span data-stu-id="935a3-110">*Source*</span></span> |<span data-ttu-id="935a3-111">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="935a3-111">Optional.</span></span> <span data-ttu-id="935a3-112">Значение **String,** содержа которое содержит URL-адрес, указывающий скопированную сущность (например, файл или каталог).</span><span class="sxs-lookup"><span data-stu-id="935a3-112">A **String** value that contains a URL specifying the entity to be copied (for example, a file or directory).</span></span> <span data-ttu-id="935a3-113">Если *source* опущен или указывает пустую строку, файл или [](record-object-ado.md) каталог, представленный текущей записью, будет скопирован.</span><span class="sxs-lookup"><span data-stu-id="935a3-113">If *Source* is omitted or specifies an empty string, the file or directory represented by the current [Record](record-object-ado.md) will be copied.</span></span>|
|<span data-ttu-id="935a3-114">*Destination*</span><span class="sxs-lookup"><span data-stu-id="935a3-114">*Destination*</span></span> |<span data-ttu-id="935a3-115">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="935a3-115">Optional.</span></span> <span data-ttu-id="935a3-116">Значение **String,** содержа которое содержит URL-адрес, указывающий расположение, в котором *будет* скопирован Источник.</span><span class="sxs-lookup"><span data-stu-id="935a3-116">A **String** value that contains a URL specifying the location where *Source* will be copied.</span></span>|
|<span data-ttu-id="935a3-117">*UserName*</span><span class="sxs-lookup"><span data-stu-id="935a3-117">*UserName*</span></span> |<span data-ttu-id="935a3-118">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="935a3-118">Optional.</span></span> <span data-ttu-id="935a3-119">Значение **String,** содержаее пользовательский ID, который при необходимости разрешает доступ к *Пункту назначения.*</span><span class="sxs-lookup"><span data-stu-id="935a3-119">A **String** value that contains the user ID that, if needed, authorizes access to *Destination*.</span></span>|
|<span data-ttu-id="935a3-120">*Password*</span><span class="sxs-lookup"><span data-stu-id="935a3-120">*Password*</span></span> |<span data-ttu-id="935a3-121">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="935a3-121">Optional.</span></span> <span data-ttu-id="935a3-122">Строковое значение, содержаее пароль, который при необходимости проверяет *имя пользователя.* </span><span class="sxs-lookup"><span data-stu-id="935a3-122">A **String** value that contains the password that, if needed, verifies *UserName*.</span></span>|
|<span data-ttu-id="935a3-123">*Options*</span><span class="sxs-lookup"><span data-stu-id="935a3-123">*Options*</span></span> |<span data-ttu-id="935a3-124">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="935a3-124">Optional.</span></span> <span data-ttu-id="935a3-125">Значение [CopyRecordOptionsEnum,](copyrecordoptionsenum.md) которое имеет значение по умолчанию **adCopyUnspecified.**</span><span class="sxs-lookup"><span data-stu-id="935a3-125">A [CopyRecordOptionsEnum](copyrecordoptionsenum.md) value that has a default value of **adCopyUnspecified**.</span></span> <span data-ttu-id="935a3-126">Указывает поведение этого метода.</span><span class="sxs-lookup"><span data-stu-id="935a3-126">Specifies the behavior of this method.</span></span>|
|<span data-ttu-id="935a3-127">*Async*</span><span class="sxs-lookup"><span data-stu-id="935a3-127">*Async*</span></span> |<span data-ttu-id="935a3-128">Необязательный параметр.</span><span class="sxs-lookup"><span data-stu-id="935a3-128">Optional.</span></span> <span data-ttu-id="935a3-129">Значение **Boolean,** которое при **True** указывает, что эта операция должна быть асинхронной.</span><span class="sxs-lookup"><span data-stu-id="935a3-129">A **Boolean** value that, when **True**, specifies that this operation should be asynchronous.</span></span>|

## <a name="return-value"></a><span data-ttu-id="935a3-130">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="935a3-130">Return value</span></span>

<span data-ttu-id="935a3-131">Значение **String,** которое обычно возвращает значение *Destination.*</span><span class="sxs-lookup"><span data-stu-id="935a3-131">A **String** value that typically returns the value of *Destination*.</span></span> <span data-ttu-id="935a3-132">Однако точное значение, возвращенное, зависит от поставщика.</span><span class="sxs-lookup"><span data-stu-id="935a3-132">However, the exact value returned is provider-dependent.</span></span>

## <a name="remarks"></a><span data-ttu-id="935a3-133">Примечания</span><span class="sxs-lookup"><span data-stu-id="935a3-133">Remarks</span></span>

<span data-ttu-id="935a3-134">Значения источника *и*  назначения не должны быть идентичными; в противном случае возникает ошибка времени запуска.</span><span class="sxs-lookup"><span data-stu-id="935a3-134">The values of *Source* and *Destination* must not be identical; otherwise, a run-time error occurs.</span></span> <span data-ttu-id="935a3-135">По крайней мере одно из имен сервера, пути или ресурсов должно отличаться.</span><span class="sxs-lookup"><span data-stu-id="935a3-135">At least one of the server, path, or resource names must differ.</span></span>

<span data-ttu-id="935a3-136">Все дети (например, поднаправления)  Источника копируется повторно, если не указано **adCopyNonRecursive.**</span><span class="sxs-lookup"><span data-stu-id="935a3-136">All children (for example, subdirectories) of *Source* are copied recursively, unless **adCopyNonRecursive** is specified.</span></span> <span data-ttu-id="935a3-137">В рекурсивной операции *Destination* не должен быть поднаправлением *Источника;* в противном случае операция не будет завершена.</span><span class="sxs-lookup"><span data-stu-id="935a3-137">In a recursive operation, *Destination* must not be a subdirectory of *Source*; otherwise, the operation will not complete.</span></span>

<span data-ttu-id="935a3-138">Этот метод не удается, если *Destination* идентифицирует существующую сущность (например, файл или каталог), если не указан **adCopyOverWrite.**</span><span class="sxs-lookup"><span data-stu-id="935a3-138">This method fails if *Destination* identifies an existing entity (for example, a file or directory), unless **adCopyOverWrite** is specified.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="935a3-139">Разумно используйте **параметр adCopyOverWrite.**</span><span class="sxs-lookup"><span data-stu-id="935a3-139">Use the **adCopyOverWrite** option judiciously.</span></span> <span data-ttu-id="935a3-140">Например, указание этого параметра при копировании файла  в каталог удаляет каталог и заменяет его файлом.</span><span class="sxs-lookup"><span data-stu-id="935a3-140">For example, specifying this option when copying a file to a directory will *delete* the directory and replace it with the file.</span></span>


> [!NOTE]
> <span data-ttu-id="935a3-141">URL-адреса, использующие схему http, автоматически вызывают поставщика DB Microsoft [OLE для публикации в Интернете.](microsoft-ole-db-provider-for-internet-publishing.md)</span><span class="sxs-lookup"><span data-stu-id="935a3-141">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="935a3-142">Дополнительные сведения см. в [url-адресах Absolute и relative.](absolute-and-relative-urls.md)</span><span class="sxs-lookup"><span data-stu-id="935a3-142">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


