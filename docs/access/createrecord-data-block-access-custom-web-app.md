---
title: Блок данных СоздатьЗапись (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dd73bae-a8d5-4d8b-b356-01ac72f7e5d9
description: Вы можете использовать блок данных СоздатьЗапись для создания новой записи в указанной таблице.
ms.openlocfilehash: d89b62180dbe50a0c7dab862b70062a47558c25a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421377"
---
# <a name="createrecord-data-block-access-custom-web-app"></a><span data-ttu-id="03468-103">Блок данных СоздатьЗапись (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="03468-103">CreateRecord Data Block (Access custom web app)</span></span>

<span data-ttu-id="03468-104">Вы можете использовать блок данных **СоздатьЗапись** для создания новой записи в указанной таблице.</span><span class="sxs-lookup"><span data-stu-id="03468-104">You can use the **CreateRecord** data block to create a new record in the specified table.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="03468-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="03468-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="03468-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="03468-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="03468-107">Блок данных **СоздатьЗапись** доступен только в макросах данных.</span><span class="sxs-lookup"><span data-stu-id="03468-107">The **CreateRecord** data block is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="03468-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="03468-108">Setting</span></span>

<span data-ttu-id="03468-109">Блок данных **СоздатьЗапись** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="03468-109">The **CreateRecord** data block has the following arguments.</span></span> 
  
<span data-ttu-id="03468-110">Блок данных **СоздатьЗапись** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="03468-110">The **CreateRecord** data block has the following arguments.</span></span> 
  
|<span data-ttu-id="03468-111">**Имя аргумента**</span><span class="sxs-lookup"><span data-stu-id="03468-111">**Argument name**</span></span>|<span data-ttu-id="03468-112">**Обязательный**</span><span class="sxs-lookup"><span data-stu-id="03468-112">**Required**</span></span>|<span data-ttu-id="03468-113">**Описание**</span><span class="sxs-lookup"><span data-stu-id="03468-113">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="03468-114">**Создание записи в**</span><span class="sxs-lookup"><span data-stu-id="03468-114">**Create a Record In**</span></span> <br/> |<span data-ttu-id="03468-115">Да</span><span class="sxs-lookup"><span data-stu-id="03468-115">Yes</span></span>  <br/> |<span data-ttu-id="03468-116">Имя таблицы, в которой создается новая запись.</span><span class="sxs-lookup"><span data-stu-id="03468-116">The name of the table to create the new record in.</span></span>  <br/> |
|<span data-ttu-id="03468-117">**Alias**</span><span class="sxs-lookup"><span data-stu-id="03468-117">**Alias**</span></span> <br/> |<span data-ttu-id="03468-118">Нет</span><span class="sxs-lookup"><span data-stu-id="03468-118">No</span></span>  <br/> |<span data-ttu-id="03468-119">Строка, определяющая запись.</span><span class="sxs-lookup"><span data-stu-id="03468-119">A string that identifies the record.</span></span> <span data-ttu-id="03468-120">Псевдоним записи можно использовать для определения</span><span class="sxs-lookup"><span data-stu-id="03468-120">You can use the record's alias to identify</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="03468-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="03468-121">Remarks</span></span>

<span data-ttu-id="03468-122">Запись, созданная с помощью **макрокоманды СоздатьЗапись** , автоматически становится текущей записью.</span><span class="sxs-lookup"><span data-stu-id="03468-122">The record created by **CreateRecord** automatically becomes the current record.</span></span> 
  
<span data-ttu-id="03468-123">После оператора **СоздатьЗапись** вы можете вставить блок команд, который будет выполняться перед фиксацией новой записи.</span><span class="sxs-lookup"><span data-stu-id="03468-123">After **CreateRecord** statement, you can insert a block of commands that will execute before the new record is committed.</span></span> <span data-ttu-id="03468-124">Следующие действия доступны в блоке данных **СоздатьЗапись** .</span><span class="sxs-lookup"><span data-stu-id="03468-124">The following actions are available in a **CreateRecord** data block.</span></span> 
  
||
|:-----|
|[<span data-ttu-id="03468-125">CancelRecordChange Macro Action</span><span class="sxs-lookup"><span data-stu-id="03468-125">CancelRecordChange Macro Action</span></span>](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="03468-126">Comment Macro Statement</span><span class="sxs-lookup"><span data-stu-id="03468-126">Comment Macro Statement</span></span>](comment-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="03468-127">Group Macro Statement</span><span class="sxs-lookup"><span data-stu-id="03468-127">Group Macro Statement</span></span>](group-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="03468-128">If... Then... Оператор else макроса</span><span class="sxs-lookup"><span data-stu-id="03468-128">If...Then...Else Macro Statement</span></span>](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="03468-129">SetField Macro Action</span><span class="sxs-lookup"><span data-stu-id="03468-129">SetField Macro Action</span></span>](setfield-macro-action-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="03468-130">SetLocalVar Macro Action</span><span class="sxs-lookup"><span data-stu-id="03468-130">SetLocalVar Macro Action</span></span>](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
<span data-ttu-id="03468-131">После того как действие **СоздатьЗапись** создаст запись, используйте действие **SetField** , чтобы указать значение поля в новой записи.</span><span class="sxs-lookup"><span data-stu-id="03468-131">After the **CreateRecord** action creates a record, use the **SetField** action to specify a value of a field in the new record.</span></span> 
  
<span data-ttu-id="03468-132">Можно использовать выражение **If... Then... Else** для выполнения операций на основе условия.</span><span class="sxs-lookup"><span data-stu-id="03468-132">You can use an **If...Then...Else** statement to perform operations based on a condition.</span></span> 
  
<span data-ttu-id="03468-133">Чтобы отменить создание записи, используйте действие **канцелрекордчанже** .</span><span class="sxs-lookup"><span data-stu-id="03468-133">To cancel the creation of a record, use the **CancelRecordChange** action.</span></span> <span data-ttu-id="03468-134">Это предотвращает фиксацию изменений и выход из блока данных **СоздатьЗапись** .</span><span class="sxs-lookup"><span data-stu-id="03468-134">This prevents the changes from being committed and exits the **CreateRecord** data block.</span></span> 
  
<span data-ttu-id="03468-135">После фиксации новой записи можно использовать локальную переменную **ласткреатерекордидентити** для работы с записью.</span><span class="sxs-lookup"><span data-stu-id="03468-135">Once the new record is committed, you can use the **LastCreateRecordIdentity** local variable to work with the record.</span></span> <span data-ttu-id="03468-136">Например, используйте следующий синтаксис, чтобы сослаться на поле AssignedTo недавно созданной записи.</span><span class="sxs-lookup"><span data-stu-id="03468-136">For example, use the following syntax to refer to the AssignedTo field of the most recently created record.</span></span> 
  
`[LastCreateRecordIdentity].[AssignedTo]`


