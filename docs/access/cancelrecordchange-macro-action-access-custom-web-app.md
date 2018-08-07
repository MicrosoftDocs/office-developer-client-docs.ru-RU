---
title: Действия макроса CancelRecordChange (приложение настраиваемых web Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: cbdbee8c-70d6-45df-a56b-5f7c6e5bdc6d
description: Отмена изменения, примененные к записи блока данных СоздатьЗапись или ИзменитьЗапись до изменения, можно использовать действие CancelRecordChange.
ms.openlocfilehash: 5f5d131ce8662dbd290a30ea08594cb413791d5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806964"
---
# <a name="cancelrecordchange-macro-action-access-custom-web-app"></a><span data-ttu-id="83bd5-103">Действия макроса CancelRecordChange (приложение настраиваемых web Access)</span><span class="sxs-lookup"><span data-stu-id="83bd5-103">CancelRecordChange Macro Action (Access custom web app)</span></span>

<span data-ttu-id="83bd5-104">Отмена изменения, примененные к записи блока данных **[СоздатьЗапись](createrecord-data-block-access-custom-web-app.md)** или **[ИзменитьЗапись](editrecord-data-block-access-custom-web-app.md)** до изменения, можно использовать действие **CancelRecordChange** .</span><span class="sxs-lookup"><span data-stu-id="83bd5-104">You can use the **CancelRecordChange** action to cancel the changes applied to a record in a **[CreateRecord](createrecord-data-block-access-custom-web-app.md)** or **[EditRecord](editrecord-data-block-access-custom-web-app.md)** data block before the changes are committed.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="83bd5-105">Корпорация Майкрософт больше не рекомендует создавать и использовать веб-приложения для Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="83bd5-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="83bd5-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/), чтобы создавать бизнес-решения без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="83bd5-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="83bd5-107">Действие **CancelRecordChange** доступна только в макросов данных.</span><span class="sxs-lookup"><span data-stu-id="83bd5-107">The **CancelRecordChange** action is available only in Data Macros.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="83bd5-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="83bd5-108">Remarks</span></span>

<span data-ttu-id="83bd5-109">При вызове действие **CancelRecordChange** блок данных **СоздатьЗапись** или **ИзменитьЗапись** немедленно прекращается.</span><span class="sxs-lookup"><span data-stu-id="83bd5-109">When you call the **CancelRecordChange** action, the **CreateRecord** or **EditRecord** data block is exited immediately.</span></span> 
  

