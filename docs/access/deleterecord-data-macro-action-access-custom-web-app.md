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
# <a name="deleterecord-data-macro-action-access-custom-web-app"></a><span data-ttu-id="ea980-103">Макрос данных макрокоманду УдалитьЗапись действие (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="ea980-103">DeleteRecord Data Macro action (Access custom web app)</span></span>

<span data-ttu-id="ea980-104">Чтобы удалить запись, можно использовать **УдалитьЗапись** .</span><span class="sxs-lookup"><span data-stu-id="ea980-104">You can use the **DeleteRecord** action to delete a record.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="ea980-105">Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="ea980-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="ea980-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="ea980-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="setting"></a><span data-ttu-id="ea980-107">Параметр</span><span class="sxs-lookup"><span data-stu-id="ea980-107">Setting</span></span>

<span data-ttu-id="ea980-108">**УдалитьЗапись** имеет следующие аргументы.</span><span class="sxs-lookup"><span data-stu-id="ea980-108">The **DeleteRecord** action has the following arguments.</span></span> 
  
|<span data-ttu-id="ea980-109">**Argument**</span><span class="sxs-lookup"><span data-stu-id="ea980-109">**Argument**</span></span>|<span data-ttu-id="ea980-110">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ea980-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ea980-111">**Запись псевдонима**</span><span class="sxs-lookup"><span data-stu-id="ea980-111">**Record Alias**</span></span> <br/> |<span data-ttu-id="ea980-112">Строка, идентифицирующая записи для удаления.</span><span class="sxs-lookup"><span data-stu-id="ea980-112">A string that identifies the record to delete.</span></span> <span data-ttu-id="ea980-113">Если аргумент *псевдоним* не указан, текущий запись удаляется.</span><span class="sxs-lookup"><span data-stu-id="ea980-113">If the  *Alias*  argument is not specified, then the current record is deleted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ea980-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="ea980-114">Remarks</span></span>

<span data-ttu-id="ea980-115">Локальной переменной **LastCreateRecordIdentity** можно использовать для работы с последней записи, созданной в блоке данных **СоздатьЗапись** .</span><span class="sxs-lookup"><span data-stu-id="ea980-115">You can use the **LastCreateRecordIdentity** local variable to work with last record created in a **CreateRecord** data block.</span></span> <span data-ttu-id="ea980-116">Например используйте следующий синтаксис для ссылки на недавно созданного записи:</span><span class="sxs-lookup"><span data-stu-id="ea980-116">For example, use the following syntax to refer to the most recently created record:</span></span> 
  
`[LastCreateRecordIdentity]`


