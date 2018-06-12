---
title: Макрос данных макрокоманду УдалитьЗапись действие (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: f6b68a9a-e04a-476e-a407-b1779fea1953
description: Чтобы удалить запись, можно использовать УдалитьЗапись.
ms.openlocfilehash: 64742d73ec57b94474c8e27822fd3946c7673336
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806912"
---
# <a name="deleterecord-data-macro-action-access-custom-web-app"></a><span data-ttu-id="6bb8b-103">Макрос данных макрокоманду УдалитьЗапись действие (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="6bb8b-103">DeleteRecord Data Macro action (Access custom web app)</span></span>

<span data-ttu-id="6bb8b-104">Чтобы удалить запись, можно использовать **УдалитьЗапись** .</span><span class="sxs-lookup"><span data-stu-id="6bb8b-104">You can use the **DeleteRecord** action to delete a record.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="6bb8b-105">Корпорация Майкрософт рекомендует больше не Создание и использование веб-приложениях Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="6bb8b-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="6bb8b-106">Кроме того рекомендуется использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для построения без написания кода бизнес-решений для мобильных устройств и веб.</span><span class="sxs-lookup"><span data-stu-id="6bb8b-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="6bb8b-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="6bb8b-107">Setting</span></span>

<span data-ttu-id="6bb8b-108">**УдалитьЗапись** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="6bb8b-108">The **DeleteRecord** action has the following arguments.</span></span> 
  
|<span data-ttu-id="6bb8b-109">**Аргумент**</span><span class="sxs-lookup"><span data-stu-id="6bb8b-109">**Argument**</span></span>|<span data-ttu-id="6bb8b-110">**Описание**</span><span class="sxs-lookup"><span data-stu-id="6bb8b-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6bb8b-111">**Запись псевдонима**</span><span class="sxs-lookup"><span data-stu-id="6bb8b-111">**Record Alias**</span></span> <br/> |<span data-ttu-id="6bb8b-112">Строка, идентифицирующая записи для удаления.</span><span class="sxs-lookup"><span data-stu-id="6bb8b-112">A string that identifies the record to delete.</span></span> <span data-ttu-id="6bb8b-113">Если аргумент *псевдоним* не указан, текущий запись удаляется.</span><span class="sxs-lookup"><span data-stu-id="6bb8b-113">If the  *Alias*  argument is not specified, then the current record is deleted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6bb8b-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="6bb8b-114">Remarks</span></span>

<span data-ttu-id="6bb8b-115">Локальной переменной **LastCreateRecordIdentity** можно использовать для работы с последней записи, созданной в блоке данных **СоздатьЗапись** .</span><span class="sxs-lookup"><span data-stu-id="6bb8b-115">You can use the **LastCreateRecordIdentity** local variable to work with last record created in a **CreateRecord** data block.</span></span> <span data-ttu-id="6bb8b-116">Например используйте следующий синтаксис для ссылки на недавно созданного записи:</span><span class="sxs-lookup"><span data-stu-id="6bb8b-116">For example, use the following syntax to refer to the most recently created record:</span></span> 
  
`[LastCreateRecordIdentity]`


