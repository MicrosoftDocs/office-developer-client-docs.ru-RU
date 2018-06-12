---
title: Блок данных ИзменитьЗапись (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 54975434-78b2-4010-b2f9-f277831fa92e
description: Чтобы изменить значения, содержащиеся в существующей записи можно использовать блок данных ИзменитьЗапись.
ms.openlocfilehash: 6c214e48326a93cff220b5436d7e7802cd6e3431
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806942"
---
# <a name="editrecord-data-block-access-custom-web-app"></a><span data-ttu-id="142d2-103">Блок данных ИзменитьЗапись (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="142d2-103">EditRecord Data Block (Access custom web app)</span></span>

<span data-ttu-id="142d2-104">Чтобы изменить значения, содержащиеся в существующей записи можно использовать блок данных **ИзменитьЗапись** .</span><span class="sxs-lookup"><span data-stu-id="142d2-104">You can use the **EditRecord** data block to change the values contained in an existing record.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="142d2-105">Корпорация Майкрософт рекомендует больше не Создание и использование веб-приложениях Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="142d2-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="142d2-106">Кроме того рекомендуется использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для построения без написания кода бизнес-решений для мобильных устройств и веб.</span><span class="sxs-lookup"><span data-stu-id="142d2-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="142d2-107">Блок данных **ИзменитьЗапись** доступна только в макросов данных.</span><span class="sxs-lookup"><span data-stu-id="142d2-107">The **EditRecord** data block is available only in Data Macros.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="142d2-108">Параметр</span><span class="sxs-lookup"><span data-stu-id="142d2-108">Setting</span></span>

<span data-ttu-id="142d2-109">Блок данных **ИзменитьЗапись** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="142d2-109">The **EditRecord** data block has the following arguments.</span></span> 
  
|<span data-ttu-id="142d2-110">**Аргумент**</span><span class="sxs-lookup"><span data-stu-id="142d2-110">**Argument**</span></span>|<span data-ttu-id="142d2-111">**Описание**</span><span class="sxs-lookup"><span data-stu-id="142d2-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="142d2-112">**Псевдоним**</span><span class="sxs-lookup"><span data-stu-id="142d2-112">**Alias**</span></span> <br/> |<span data-ttu-id="142d2-113">Строка, идентифицирующая записи для редактирования.</span><span class="sxs-lookup"><span data-stu-id="142d2-113">A string that identifies the record to edit.</span></span> <span data-ttu-id="142d2-114">Если аргумент *псевдоним* не задан, изменяется текущей записи.</span><span class="sxs-lookup"><span data-stu-id="142d2-114">If the  *Alias*  argument is not specified, then the current record is edited.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="142d2-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="142d2-115">Remarks</span></span>

<span data-ttu-id="142d2-116">После оператора **ИзменитьЗапись** можно вставить блок команды, которые будут выполняться до подтверждения изменений в запись.</span><span class="sxs-lookup"><span data-stu-id="142d2-116">After the **EditRecord** statement, you can insert a block of commands that will execute before the changes to the record are committed.</span></span> <span data-ttu-id="142d2-117">В блока данных **ИзменитьЗапись** доступны следующие действия.</span><span class="sxs-lookup"><span data-stu-id="142d2-117">The following actions are available in an **EditRecord** data block.</span></span> 
  
||
|:-----|
|[<span data-ttu-id="142d2-118">Действия макроса CancelRecordChange</span><span class="sxs-lookup"><span data-stu-id="142d2-118">CancelRecordChange Macro Action</span></span>](cancelrecordchange-macro-action-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="142d2-119">Оператор комментария макросов</span><span class="sxs-lookup"><span data-stu-id="142d2-119">Comment Macro Statement</span></span>](comment-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="142d2-120">Оператор группы макросов</span><span class="sxs-lookup"><span data-stu-id="142d2-120">Group Macro Statement</span></span>](group-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="142d2-121">If... Затем... Оператор Else макросов</span><span class="sxs-lookup"><span data-stu-id="142d2-121">If...Then...Else Macro Statement</span></span>](ifthenelse-macro-block-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="142d2-122">Действия SetField макроса</span><span class="sxs-lookup"><span data-stu-id="142d2-122">SetField Macro Action</span></span>](setfield-macro-action-access-custom-web-app.md) <br/> |
|[<span data-ttu-id="142d2-123">Действия макроса SetLocalVar</span><span class="sxs-lookup"><span data-stu-id="142d2-123">SetLocalVar Macro Action</span></span>](setlocalvar-macro-action-access-custom-web-app.md) <br/> |
   
<span data-ttu-id="142d2-124">Действие **SetField** используется для указания нового значения поля в измененной записи.</span><span class="sxs-lookup"><span data-stu-id="142d2-124">Use the **SetField** action to specify the new values of a field in the edited record.</span></span> 
  
<span data-ttu-id="142d2-125">**Можно использовать, если... Затем... Else** оператора для выполнения операций на основе условия.</span><span class="sxs-lookup"><span data-stu-id="142d2-125">You can use an **If...Then...Else** statement to perform operations based on a condition.</span></span> 
  
<span data-ttu-id="142d2-126">Чтобы отменить редактирование записи, используйте действие **CancelRecordChange** .</span><span class="sxs-lookup"><span data-stu-id="142d2-126">To cancel the editing of a record, use the **CancelRecordChange** action.</span></span> <span data-ttu-id="142d2-127">Это предотвращает фиксации изменений и выполняет выход из блока данных **ИзменитьЗапись** .</span><span class="sxs-lookup"><span data-stu-id="142d2-127">This prevents the changes from being committed and exits the **EditRecord** data block.</span></span> 
  
<span data-ttu-id="142d2-128">Локальной переменной **LastCreateRecordIdentity** можно использовать для работы с последней записи, созданной в блоке данных **СоздатьЗапись** .</span><span class="sxs-lookup"><span data-stu-id="142d2-128">You can use the **LastCreateRecordIdentity** local variable to work with last record created in a **CreateRecord** data block.</span></span> <span data-ttu-id="142d2-129">Например используйте следующий синтаксис для ссылки на поля Кому назначено недавно созданного записи:</span><span class="sxs-lookup"><span data-stu-id="142d2-129">For example, use the following syntax to refer to the AssignedTo field of the most recently created record:</span></span> 
  
`[LastCreateRecordIdentity].[AssignedTo]`


