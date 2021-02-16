---
title: EditRecord Data Block (Access custom web app)
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
# <a name="editrecord-data-block-access-custom-web-app"></a><span data-ttu-id="5b207-103">EditRecord Data Block (Access custom web app)</span><span class="sxs-lookup"><span data-stu-id="5b207-103">EditRecord Data Block (Access custom web app)</span></span>

<span data-ttu-id="5b207-104">Блок данных **EditRecord можно** использовать для изменения значений, содержащихся в существующей записи.</span><span class="sxs-lookup"><span data-stu-id="5b207-104">You can use the **EditRecord** data block to change the values contained in an existing record.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="5b207-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="5b207-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="5b207-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="5b207-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5b207-107">Блок **данных EditRecord** доступен только в макросах данных.</span><span class="sxs-lookup"><span data-stu-id="5b207-107">The **EditRecord** data block is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="5b207-108">Setting</span><span class="sxs-lookup"><span data-stu-id="5b207-108">Setting</span></span>

<span data-ttu-id="5b207-109">Блок **данных EditRecord** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="5b207-109">The **EditRecord** data block has the following arguments.</span></span> 
  
|<span data-ttu-id="5b207-110">**Аргумент**</span><span class="sxs-lookup"><span data-stu-id="5b207-110">**Argument**</span></span>|<span data-ttu-id="5b207-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="5b207-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5b207-112">**Alias**</span><span class="sxs-lookup"><span data-stu-id="5b207-112">**Alias**</span></span> <br/> |<span data-ttu-id="5b207-113">Строка, идентифицирует запись, которую необходимо изменить.</span><span class="sxs-lookup"><span data-stu-id="5b207-113">A string that identifies the record to edit.</span></span> <span data-ttu-id="5b207-114">Если  *аргумент Alias*  не указан, то текущая запись будет изменена.</span><span class="sxs-lookup"><span data-stu-id="5b207-114">If the  *Alias*  argument is not specified, then the current record is edited.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5b207-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="5b207-115">Remarks</span></span>

<span data-ttu-id="5b207-116">После выполнения **команды EditRecord** можно вставить блок команд, которые будут выполняться до того, как будут зафиксированы изменения записи.</span><span class="sxs-lookup"><span data-stu-id="5b207-116">After the **EditRecord** statement, you can insert a block of commands that will execute before the changes to the record are committed.</span></span> <span data-ttu-id="5b207-117">В блоке данных **EditRecord** доступны следующие действия.</span><span class="sxs-lookup"><span data-stu-id="5b207-117">The following actions are available in an **EditRecord** data block.</span></span> 
  
||
|:-----|
|[<span data-ttu-id="5b207-118">CancelRecordChange Macro Action</span><span class="sxs-lookup"><span data-stu-id="5b207-118">CancelRecordChange Macro Action</span></span>](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="5b207-119">Comment Macro Statement</span><span class="sxs-lookup"><span data-stu-id="5b207-119">Comment Macro Statement</span></span>](comment-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="5b207-120">Group Macro Statement</span><span class="sxs-lookup"><span data-stu-id="5b207-120">Group Macro Statement</span></span>](group-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="5b207-121">If... Затем... Else Macro Statement</span><span class="sxs-lookup"><span data-stu-id="5b207-121">If...Then...Else Macro Statement</span></span>](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="5b207-122">SetField Macro Action</span><span class="sxs-lookup"><span data-stu-id="5b207-122">SetField Macro Action</span></span>](setfield-macro-action-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="5b207-123">SetLocalVar Macro Action</span><span class="sxs-lookup"><span data-stu-id="5b207-123">SetLocalVar Macro Action</span></span>](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
<span data-ttu-id="5b207-124">Используйте действие **SetField,** чтобы указать новые значения поля в измененной записи.</span><span class="sxs-lookup"><span data-stu-id="5b207-124">Use the **SetField** action to specify the new values of a field in the edited record.</span></span> 
  
<span data-ttu-id="5b207-125">Вы можете использовать **if... Затем... Заявление Else** для выполнения операций на основе условия.</span><span class="sxs-lookup"><span data-stu-id="5b207-125">You can use an **If...Then...Else** statement to perform operations based on a condition.</span></span> 
  
<span data-ttu-id="5b207-126">Чтобы отменить редактирование записи, используйте действие **CancelRecordChange.**</span><span class="sxs-lookup"><span data-stu-id="5b207-126">To cancel the editing of a record, use the **CancelRecordChange** action.</span></span> <span data-ttu-id="5b207-127">Это предотвращает зафиксирование изменений и выход из блока данных **EditRecord.**</span><span class="sxs-lookup"><span data-stu-id="5b207-127">This prevents the changes from being committed and exits the **EditRecord** data block.</span></span> 
  
<span data-ttu-id="5b207-128">Локализованную переменную **LastCreateRecordIdentity** можно использовать для работы с последней записью, созданной в блоке данных **CreateRecord.**</span><span class="sxs-lookup"><span data-stu-id="5b207-128">You can use the **LastCreateRecordIdentity** local variable to work with last record created in a **CreateRecord** data block.</span></span> <span data-ttu-id="5b207-129">Например, используйте следующий синтаксис для ссылки на поле AssignedTo последней созданной записи:</span><span class="sxs-lookup"><span data-stu-id="5b207-129">For example, use the following syntax to refer to the AssignedTo field of the most recently created record:</span></span> 
  
`[LastCreateRecordIdentity].[AssignedTo]`


