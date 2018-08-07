---
title: Блок данных СоздатьЗапись (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dd73bae-a8d5-4d8b-b356-01ac72f7e5d9
description: Блок данных СоздатьЗапись можно использовать для создания новой записи в указанную таблицу.
ms.openlocfilehash: dc4be7653081c7c02426d84c74b7b56e597706fa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806987"
---
# <a name="createrecord-data-block-access-custom-web-app"></a><span data-ttu-id="d7fad-103">Блок данных СоздатьЗапись (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="d7fad-103">CreateRecord Data Block (Access custom web app)</span></span>

<span data-ttu-id="d7fad-104">Блок данных **СоздатьЗапись** можно использовать для создания новой записи в указанную таблицу.</span><span class="sxs-lookup"><span data-stu-id="d7fad-104">You can use the **CreateRecord** data block to create a new record in the specified table.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="d7fad-105">Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="d7fad-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="d7fad-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="d7fad-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d7fad-107">Блок данных **СоздатьЗапись** доступна только в макросов данных.</span><span class="sxs-lookup"><span data-stu-id="d7fad-107">The **CreateRecord** data block is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="d7fad-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="d7fad-108">Setting</span></span>

<span data-ttu-id="d7fad-109">Блок данных **СоздатьЗапись** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="d7fad-109">The **CreateRecord** data block has the following arguments.</span></span> 
  
<span data-ttu-id="d7fad-110">Блок данных **СоздатьЗапись** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="d7fad-110">The **CreateRecord** data block has the following arguments.</span></span> 
  
|<span data-ttu-id="d7fad-111">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="d7fad-111">**Argument name**</span></span>|<span data-ttu-id="d7fad-112">**Обязательное**</span><span class="sxs-lookup"><span data-stu-id="d7fad-112">**Required**</span></span>|<span data-ttu-id="d7fad-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d7fad-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d7fad-114">**Создание записи в**</span><span class="sxs-lookup"><span data-stu-id="d7fad-114">**Create a Record In**</span></span> <br/> |<span data-ttu-id="d7fad-115">Да</span><span class="sxs-lookup"><span data-stu-id="d7fad-115">Yes</span></span>  <br/> |<span data-ttu-id="d7fad-116">Имя таблицы для создания новой записи в.</span><span class="sxs-lookup"><span data-stu-id="d7fad-116">The name of the table to create the new record in.</span></span>  <br/> |
|<span data-ttu-id="d7fad-117">**Alias**</span><span class="sxs-lookup"><span data-stu-id="d7fad-117">**Alias**</span></span> <br/> |<span data-ttu-id="d7fad-118">Нет</span><span class="sxs-lookup"><span data-stu-id="d7fad-118">No</span></span>  <br/> |<span data-ttu-id="d7fad-119">Строка, идентифицирующая эту запись.</span><span class="sxs-lookup"><span data-stu-id="d7fad-119">A string that identifies the record.</span></span> <span data-ttu-id="d7fad-120">Можно использовать эту запись псевдонима для идентификации</span><span class="sxs-lookup"><span data-stu-id="d7fad-120">You can use the record's alias to identify</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d7fad-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="d7fad-121">Remarks</span></span>

<span data-ttu-id="d7fad-122">Записи, созданной **СоздатьЗапись** автоматически становится текущей.</span><span class="sxs-lookup"><span data-stu-id="d7fad-122">The record created by **CreateRecord** automatically becomes the current record.</span></span> 
  
<span data-ttu-id="d7fad-123">После оператора **СоздатьЗапись** можно вставить блок команды, которые будут выполняться перед сохранением новую запись.</span><span class="sxs-lookup"><span data-stu-id="d7fad-123">After **CreateRecord** statement, you can insert a block of commands that will execute before the new record is committed.</span></span> <span data-ttu-id="d7fad-124">В блоке данных **СоздатьЗапись** доступны следующие действия.</span><span class="sxs-lookup"><span data-stu-id="d7fad-124">The following actions are available in a **CreateRecord** data block.</span></span> 
  
||
|:-----|
|[<span data-ttu-id="d7fad-125">CancelRecordChange Macro Action</span><span class="sxs-lookup"><span data-stu-id="d7fad-125">CancelRecordChange Macro Action</span></span>](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="d7fad-126">Comment Macro Statement</span><span class="sxs-lookup"><span data-stu-id="d7fad-126">Comment Macro Statement</span></span>](comment-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="d7fad-127">Group Macro Statement</span><span class="sxs-lookup"><span data-stu-id="d7fad-127">Group Macro Statement</span></span>](group-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="d7fad-128">If... Затем... Оператор Else макросов</span><span class="sxs-lookup"><span data-stu-id="d7fad-128">If...Then...Else Macro Statement</span></span>](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="d7fad-129">SetField Macro Action</span><span class="sxs-lookup"><span data-stu-id="d7fad-129">SetField Macro Action</span></span>](setfield-macro-action-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="d7fad-130">SetLocalVar Macro Action</span><span class="sxs-lookup"><span data-stu-id="d7fad-130">SetLocalVar Macro Action</span></span>](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
<span data-ttu-id="d7fad-131">После **СоздатьЗапись** действие создает запись, используйте действие **SetField** для указания значения поля в новую запись.</span><span class="sxs-lookup"><span data-stu-id="d7fad-131">After the **CreateRecord** action creates a record, use the **SetField** action to specify a value of a field in the new record.</span></span> 
  
<span data-ttu-id="d7fad-132">**Можно использовать, если... Затем... Else** оператора для выполнения операций на основе условия.</span><span class="sxs-lookup"><span data-stu-id="d7fad-132">You can use an **If...Then...Else** statement to perform operations based on a condition.</span></span> 
  
<span data-ttu-id="d7fad-133">Чтобы отменить создание записи, используйте действие **CancelRecordChange** .</span><span class="sxs-lookup"><span data-stu-id="d7fad-133">To cancel the creation of a record, use the **CancelRecordChange** action.</span></span> <span data-ttu-id="d7fad-134">Это предотвращает фиксации изменений и выполняет выход из блока **СоздатьЗапись** данных.</span><span class="sxs-lookup"><span data-stu-id="d7fad-134">This prevents the changes from being committed and exits the **CreateRecord** data block.</span></span> 
  
<span data-ttu-id="d7fad-135">После фиксации новую запись локальной переменной **LastCreateRecordIdentity** можно использовать для работы с записью.</span><span class="sxs-lookup"><span data-stu-id="d7fad-135">Once the new record is committed, you can use the **LastCreateRecordIdentity** local variable to work with the record.</span></span> <span data-ttu-id="d7fad-136">Например используйте следующий синтаксис для ссылки на поля Кому назначено недавно созданного записи.</span><span class="sxs-lookup"><span data-stu-id="d7fad-136">For example, use the following syntax to refer to the AssignedTo field of the most recently created record.</span></span> 
  
`[LastCreateRecordIdentity].[AssignedTo]`


