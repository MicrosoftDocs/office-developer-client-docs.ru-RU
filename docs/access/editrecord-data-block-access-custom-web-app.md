---
title: Блок данных EditRecord (Доступ к пользовательскому веб-приложению)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 54975434-78b2-4010-b2f9-f277831fa92e
description: Блок данных EditRecord можно использовать для изменения значений, содержащихся в существующей записи.
ms.openlocfilehash: 0d9ef6c7689b44a0304309a7537e744eff97c809
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418346"
---
# <a name="editrecord-data-block-access-custom-web-app"></a><span data-ttu-id="052c1-103">Блок данных EditRecord (Доступ к пользовательскому веб-приложению)</span><span class="sxs-lookup"><span data-stu-id="052c1-103">EditRecord Data Block (Access custom web app)</span></span>

<span data-ttu-id="052c1-104">Блок данных **EditRecord можно** использовать для изменения значений, содержащихся в существующей записи.</span><span class="sxs-lookup"><span data-stu-id="052c1-104">You can use the **EditRecord** data block to change the values contained in an existing record.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="052c1-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="052c1-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="052c1-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="052c1-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="052c1-107">Блок **данных EditRecord** доступен только в макросах данных.</span><span class="sxs-lookup"><span data-stu-id="052c1-107">The **EditRecord** data block is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="052c1-108">Setting</span><span class="sxs-lookup"><span data-stu-id="052c1-108">Setting</span></span>

<span data-ttu-id="052c1-109">Блок **данных EditRecord** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="052c1-109">The **EditRecord** data block has the following arguments.</span></span> 
  
|<span data-ttu-id="052c1-110">**Аргумент**</span><span class="sxs-lookup"><span data-stu-id="052c1-110">**Argument**</span></span>|<span data-ttu-id="052c1-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="052c1-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="052c1-112">**Alias**</span><span class="sxs-lookup"><span data-stu-id="052c1-112">**Alias**</span></span> <br/> |<span data-ttu-id="052c1-113">Строка, идентифицируемая для редактирования записи.</span><span class="sxs-lookup"><span data-stu-id="052c1-113">A string that identifies the record to edit.</span></span> <span data-ttu-id="052c1-114">Если аргумент  *Alias*  не указан, то текущая запись редактирована.</span><span class="sxs-lookup"><span data-stu-id="052c1-114">If the  *Alias*  argument is not specified, then the current record is edited.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="052c1-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="052c1-115">Remarks</span></span>

<span data-ttu-id="052c1-116">После утверждения **EditRecord** можно вставить блок команд, которые будут выполняться до внесения изменений в запись.</span><span class="sxs-lookup"><span data-stu-id="052c1-116">After the **EditRecord** statement, you can insert a block of commands that will execute before the changes to the record are committed.</span></span> <span data-ttu-id="052c1-117">Следующие действия доступны в блоке **данных EditRecord.**</span><span class="sxs-lookup"><span data-stu-id="052c1-117">The following actions are available in an **EditRecord** data block.</span></span> 
  
||
|:-----|
|[<span data-ttu-id="052c1-118">CancelRecordChange Macro Action</span><span class="sxs-lookup"><span data-stu-id="052c1-118">CancelRecordChange Macro Action</span></span>](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="052c1-119">Comment Macro Statement</span><span class="sxs-lookup"><span data-stu-id="052c1-119">Comment Macro Statement</span></span>](comment-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="052c1-120">Group Macro Statement</span><span class="sxs-lookup"><span data-stu-id="052c1-120">Group Macro Statement</span></span>](group-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="052c1-121">Если... Затем... Else Macro Statement</span><span class="sxs-lookup"><span data-stu-id="052c1-121">If...Then...Else Macro Statement</span></span>](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="052c1-122">SetField Macro Action</span><span class="sxs-lookup"><span data-stu-id="052c1-122">SetField Macro Action</span></span>](setfield-macro-action-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="052c1-123">SetLocalVar Macro Action</span><span class="sxs-lookup"><span data-stu-id="052c1-123">SetLocalVar Macro Action</span></span>](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
<span data-ttu-id="052c1-124">Используйте действие **SetField,** чтобы указать новые значения поля в отредактируемой записи.</span><span class="sxs-lookup"><span data-stu-id="052c1-124">Use the **SetField** action to specify the new values of a field in the edited record.</span></span> 
  
<span data-ttu-id="052c1-125">Вы можете использовать **if... Затем... Другое** заявление для выполнения операций на основе условия.</span><span class="sxs-lookup"><span data-stu-id="052c1-125">You can use an **If...Then...Else** statement to perform operations based on a condition.</span></span> 
  
<span data-ttu-id="052c1-126">Чтобы отменить редактирование записи, используйте **действие CancelRecordChange.**</span><span class="sxs-lookup"><span data-stu-id="052c1-126">To cancel the editing of a record, use the **CancelRecordChange** action.</span></span> <span data-ttu-id="052c1-127">Это предотвращает совершение изменений и выход из блока **данных EditRecord.**</span><span class="sxs-lookup"><span data-stu-id="052c1-127">This prevents the changes from being committed and exits the **EditRecord** data block.</span></span> 
  
<span data-ttu-id="052c1-128">Для работы с последней записью, созданной в блоке данных CreateRecord, можно использовать локализованную переменную **LastCreateRecordIdentity.** </span><span class="sxs-lookup"><span data-stu-id="052c1-128">You can use the **LastCreateRecordIdentity** local variable to work with last record created in a **CreateRecord** data block.</span></span> <span data-ttu-id="052c1-129">Например, используйте следующий синтаксис для ссылки на поле AssignedTo последней созданной записи:</span><span class="sxs-lookup"><span data-stu-id="052c1-129">For example, use the following syntax to refer to the AssignedTo field of the most recently created record:</span></span> 
  
`[LastCreateRecordIdentity].[AssignedTo]`


