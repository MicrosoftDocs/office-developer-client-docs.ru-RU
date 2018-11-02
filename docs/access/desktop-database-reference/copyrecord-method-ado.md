---
title: Метод CopyRecord (ADO)
TOCTitle: CopyRecord method (ADO)
ms:assetid: 724e4358-f216-8e47-5bab-c72770ece5a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249459(v=office.15)
ms:contentKeyID: 48545605
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0f25d3f7cb576a9fb8ddf79a887bb3c795144682
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919033"
---
# <a name="copyrecord-method-ado"></a><span data-ttu-id="88ca4-102">Метод CopyRecord (ADO)</span><span class="sxs-lookup"><span data-stu-id="88ca4-102">CopyRecord method (ADO)</span></span>


<span data-ttu-id="88ca4-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="88ca4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="88ca4-104">Копирует сущности, представленной в **записи** в другое расположение.</span><span class="sxs-lookup"><span data-stu-id="88ca4-104">Copies a entity represented by a **Record** to another location.</span></span>

## <a name="syntax"></a><span data-ttu-id="88ca4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="88ca4-105">Syntax</span></span>

<span data-ttu-id="88ca4-106">*Запись*. CopyRecord (*источника*, *назначения*, *имя пользователя*, *пароль*, *Параметры*, *асинхронного*)</span><span class="sxs-lookup"><span data-stu-id="88ca4-106">*Record*.CopyRecord (*Source*, *Destination*, *UserName*, *Password*, *Options*, *Async*)</span></span>

## <a name="parameters"></a><span data-ttu-id="88ca4-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="88ca4-107">Parameters</span></span>

  - <span data-ttu-id="88ca4-108">*Source*</span><span class="sxs-lookup"><span data-stu-id="88ca4-108">*Source*</span></span>

  - <span data-ttu-id="88ca4-109">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="88ca4-109">Optional.</span></span> <span data-ttu-id="88ca4-110">**Строковое** значение, содержащее URL-адрес указание сущности для копирования (например, файла или папки).</span><span class="sxs-lookup"><span data-stu-id="88ca4-110">A **String** value that contains a URL specifying the entity to be copied (for example, a file or directory).</span></span> <span data-ttu-id="88ca4-111">Если *источник* указан или указывает пустая строка, файл или папка, представленное текущей [записи](record-object-ado.md) копируются.</span><span class="sxs-lookup"><span data-stu-id="88ca4-111">If *Source* is omitted or specifies an empty string, the file or directory represented by the current [Record](record-object-ado.md) will be copied.</span></span>

  - <span data-ttu-id="88ca4-112">*Назначения*</span><span class="sxs-lookup"><span data-stu-id="88ca4-112">*Destination*</span></span>

  - <span data-ttu-id="88ca4-113">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="88ca4-113">Optional.</span></span> <span data-ttu-id="88ca4-114">**Строковое** значение, содержащее URL-адрес, определяющее расположение, где будет скопирована *источника* .</span><span class="sxs-lookup"><span data-stu-id="88ca4-114">A **String** value that contains a URL specifying the location where *Source* will be copied.</span></span>

  - <span data-ttu-id="88ca4-115">*Имя пользователя*</span><span class="sxs-lookup"><span data-stu-id="88ca4-115">*UserName*</span></span>

  - <span data-ttu-id="88ca4-116">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="88ca4-116">Optional.</span></span> <span data-ttu-id="88ca4-117">**Строковое** значение, содержащее идентификатор пользователя, при необходимости, авторизует доступ в *место назначения*.</span><span class="sxs-lookup"><span data-stu-id="88ca4-117">A **String** value that contains the user ID that, if needed, authorizes access to *Destination*.</span></span>

  - <span data-ttu-id="88ca4-118">*Password*</span><span class="sxs-lookup"><span data-stu-id="88ca4-118">*Password*</span></span>

  - <span data-ttu-id="88ca4-119">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="88ca4-119">Optional.</span></span> <span data-ttu-id="88ca4-120">**Строковое** значение, содержащее пароль, при необходимости, выполняется проверка *имени пользователя*.</span><span class="sxs-lookup"><span data-stu-id="88ca4-120">A **String** value that contains the password that, if needed, verifies *UserName*.</span></span>

  - <span data-ttu-id="88ca4-121">*Варианты*</span><span class="sxs-lookup"><span data-stu-id="88ca4-121">*Options*</span></span>

  - <span data-ttu-id="88ca4-122">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="88ca4-122">Optional.</span></span> <span data-ttu-id="88ca4-123">Значение [CopyRecordOptionsEnum](copyrecordoptionsenum.md) , который имеет значение по умолчанию **adCopyUnspecified**.</span><span class="sxs-lookup"><span data-stu-id="88ca4-123">A [CopyRecordOptionsEnum](copyrecordoptionsenum.md) value that has a default value of **adCopyUnspecified**.</span></span> <span data-ttu-id="88ca4-124">Задает поведение этого метода.</span><span class="sxs-lookup"><span data-stu-id="88ca4-124">Specifies the behavior of this method.</span></span>

  - <span data-ttu-id="88ca4-125">*Async*</span><span class="sxs-lookup"><span data-stu-id="88ca4-125">*Async*</span></span>

  - <span data-ttu-id="88ca4-126">Необязательно указывать.</span><span class="sxs-lookup"><span data-stu-id="88ca4-126">Optional.</span></span> <span data-ttu-id="88ca4-127">**Логическое** значение, которое, если **значение True**, указывает, что эта операция должна быть асинхронной.</span><span class="sxs-lookup"><span data-stu-id="88ca4-127">A **Boolean** value that, when **True**, specifies that this operation should be asynchronous.</span></span>

## <a name="return-value"></a><span data-ttu-id="88ca4-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="88ca4-128">Return value</span></span>

<span data-ttu-id="88ca4-129">**Строковое** значение, которое обычно возвращает значение *назначения*.</span><span class="sxs-lookup"><span data-stu-id="88ca4-129">A **String** value that typically returns the value of *Destination*.</span></span> <span data-ttu-id="88ca4-130">Тем не менее точное значение, возвращаемое зависит от поставщика.</span><span class="sxs-lookup"><span data-stu-id="88ca4-130">However, the exact value returned is provider-dependent.</span></span>

## <a name="remarks"></a><span data-ttu-id="88ca4-131">Примечания</span><span class="sxs-lookup"><span data-stu-id="88ca4-131">Remarks</span></span>

<span data-ttu-id="88ca4-132">Значения из *источника* и *назначения* не должны совпадать; в противном случае возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="88ca4-132">The values of *Source* and *Destination* must not be identical; otherwise, a run-time error occurs.</span></span> <span data-ttu-id="88ca4-133">По крайней мере одно из имен сервера, пути или имени ресурса должны отличаться.</span><span class="sxs-lookup"><span data-stu-id="88ca4-133">At least one of the server, path, or resource names must differ.</span></span>

<span data-ttu-id="88ca4-134">Все дочерние элементы (например, вложенные папки) *источник* , скопированный рекурсивно, если не указано **adCopyNonRecursive** .</span><span class="sxs-lookup"><span data-stu-id="88ca4-134">All children (for example, subdirectories) of *Source* are copied recursively, unless **adCopyNonRecursive** is specified.</span></span> <span data-ttu-id="88ca4-135">В ходе операции рекурсивный *назначения* не должна быть подкаталог *источника*; в противном случае операция не завершена.</span><span class="sxs-lookup"><span data-stu-id="88ca4-135">In a recursive operation, *Destination* must not be a subdirectory of *Source*; otherwise, the operation will not complete.</span></span>

<span data-ttu-id="88ca4-136">Этот метод не выполняется, если *конечный* идентифицирует существующей сущности (например, файла или каталога), если не указано **adCopyOverWrite** .</span><span class="sxs-lookup"><span data-stu-id="88ca4-136">This method fails if *Destination* identifies an existing entity (for example, a file or directory), unless **adCopyOverWrite** is specified.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="88ca4-137">Параметр **adCopyOverWrite** внимательно.</span><span class="sxs-lookup"><span data-stu-id="88ca4-137">Use the **adCopyOverWrite** option judiciously.</span></span> <span data-ttu-id="88ca4-138">Например задание этого параметра при копировании файлов в каталог будет *Удалить* каталог и замените файл.</span><span class="sxs-lookup"><span data-stu-id="88ca4-138">For example, specifying this option when copying a file to a directory will *delete* the directory and replace it with the file.</span></span>




> [!NOTE]
> <span data-ttu-id="88ca4-139">URL-адреса, с помощью схемы http автоматически вызывает [Поставщик Microsoft OLE DB для публикации Интернет](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="88ca4-139">URLs using the http scheme will automatically invoke the [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="88ca4-140">Для получения дополнительных сведений см [абсолютных и относительных URL-адресов](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="88ca4-140">For more information, see [Absolute and relative URLs](absolute-and-relative-urls.md).</span></span>


