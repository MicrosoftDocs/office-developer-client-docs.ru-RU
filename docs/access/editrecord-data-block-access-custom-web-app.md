---
title: Блок данных ИзменитьЗапись (пользовательское веб-приложение для Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 54975434-78b2-4010-b2f9-f277831fa92e
description: Вы можете использовать блок данных ИзменитьЗапись, чтобы изменить значения, хранящиеся в существующей записи.
ms.openlocfilehash: 0d9ef6c7689b44a0304309a7537e744eff97c809
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302522"
---
# <a name="editrecord-data-block-access-custom-web-app"></a><span data-ttu-id="5902a-103">Блок данных ИзменитьЗапись (пользовательское веб-приложение для Access)</span><span class="sxs-lookup"><span data-stu-id="5902a-103">EditRecord Data Block (Access custom web app)</span></span>

<span data-ttu-id="5902a-104">Вы можете использовать блок данных **ИзменитьЗапись** , чтобы изменить значения, хранящиеся в существующей записи.</span><span class="sxs-lookup"><span data-stu-id="5902a-104">You can use the **EditRecord** data block to change the values contained in an existing record.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="5902a-105">Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="5902a-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="5902a-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="5902a-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5902a-107">Блок данных **ИзменитьЗапись** доступен только в макросах данных.</span><span class="sxs-lookup"><span data-stu-id="5902a-107">The **EditRecord** data block is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="5902a-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="5902a-108">Setting</span></span>

<span data-ttu-id="5902a-109">Блок данных **ИзменитьЗапись** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="5902a-109">The **EditRecord** data block has the following arguments.</span></span> 
  
|<span data-ttu-id="5902a-110">**Аргумент**</span><span class="sxs-lookup"><span data-stu-id="5902a-110">**Argument**</span></span>|<span data-ttu-id="5902a-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5902a-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5902a-112">**Alias**</span><span class="sxs-lookup"><span data-stu-id="5902a-112">**Alias**</span></span> <br/> |<span data-ttu-id="5902a-113">Строка, определяющая изменяемую запись.</span><span class="sxs-lookup"><span data-stu-id="5902a-113">A string that identifies the record to edit.</span></span> <span data-ttu-id="5902a-114">Если аргумент *Alias* не указан, текущая запись редактируется.</span><span class="sxs-lookup"><span data-stu-id="5902a-114">If the  *Alias*  argument is not specified, then the current record is edited.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5902a-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="5902a-115">Remarks</span></span>

<span data-ttu-id="5902a-116">После оператора **ИзменитьЗапись** вы можете вставить блок команд, который будет выполняться перед фиксацией изменений записи.</span><span class="sxs-lookup"><span data-stu-id="5902a-116">After the **EditRecord** statement, you can insert a block of commands that will execute before the changes to the record are committed.</span></span> <span data-ttu-id="5902a-117">Следующие действия доступны в блоке данных **ИзменитьЗапись** .</span><span class="sxs-lookup"><span data-stu-id="5902a-117">The following actions are available in an **EditRecord** data block.</span></span> 
  
||
|:-----|
|[<span data-ttu-id="5902a-118">CancelRecordChange Macro Action</span><span class="sxs-lookup"><span data-stu-id="5902a-118">CancelRecordChange Macro Action</span></span>](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="5902a-119">Comment Macro Statement</span><span class="sxs-lookup"><span data-stu-id="5902a-119">Comment Macro Statement</span></span>](comment-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="5902a-120">Group Macro Statement</span><span class="sxs-lookup"><span data-stu-id="5902a-120">Group Macro Statement</span></span>](group-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="5902a-121">If... Then... Оператор else макроса</span><span class="sxs-lookup"><span data-stu-id="5902a-121">If...Then...Else Macro Statement</span></span>](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="5902a-122">SetField Macro Action</span><span class="sxs-lookup"><span data-stu-id="5902a-122">SetField Macro Action</span></span>](setfield-macro-action-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="5902a-123">SetLocalVar Macro Action</span><span class="sxs-lookup"><span data-stu-id="5902a-123">SetLocalVar Macro Action</span></span>](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
<span data-ttu-id="5902a-124">Используйте действие **SetField** для указания новых значений поля в измененной записи.</span><span class="sxs-lookup"><span data-stu-id="5902a-124">Use the **SetField** action to specify the new values of a field in the edited record.</span></span> 
  
<span data-ttu-id="5902a-125">Можно использовать выражение **If... Then... Else** для выполнения операций на основе условия.</span><span class="sxs-lookup"><span data-stu-id="5902a-125">You can use an **If...Then...Else** statement to perform operations based on a condition.</span></span> 
  
<span data-ttu-id="5902a-126">Чтобы отменить редактирование записи, используйте действие **канцелрекордчанже** .</span><span class="sxs-lookup"><span data-stu-id="5902a-126">To cancel the editing of a record, use the **CancelRecordChange** action.</span></span> <span data-ttu-id="5902a-127">Это предотвращает фиксацию изменений и выход из блока данных **ИзменитьЗапись** .</span><span class="sxs-lookup"><span data-stu-id="5902a-127">This prevents the changes from being committed and exits the **EditRecord** data block.</span></span> 
  
<span data-ttu-id="5902a-128">Локальную переменную **ласткреатерекордидентити** можно использовать для работы с последней записью, созданной в блоке данных **СоздатьЗапись** .</span><span class="sxs-lookup"><span data-stu-id="5902a-128">You can use the **LastCreateRecordIdentity** local variable to work with last record created in a **CreateRecord** data block.</span></span> <span data-ttu-id="5902a-129">Например, используйте следующий синтаксис для ссылки на поле AssignedTo последней созданной записи:</span><span class="sxs-lookup"><span data-stu-id="5902a-129">For example, use the following syntax to refer to the AssignedTo field of the most recently created record:</span></span> 
  
`[LastCreateRecordIdentity].[AssignedTo]`


