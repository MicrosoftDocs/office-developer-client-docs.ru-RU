---
title: CancelRecordChange Macro Action (пользовательское веб-приложение Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: cbdbee8c-70d6-45df-a56b-5f7c6e5bdc6d
description: Действие CancelRecordChange можно использовать для отмены изменений, примененных к записи в блоке данных CreateRecord или EditRecord, прежде чем изменения будут зафиксированы.
ms.openlocfilehash: fe95718e752513c4b8b700f331fec7b78092e553
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411829"
---
# <a name="cancelrecordchange-macro-action-access-custom-web-app"></a><span data-ttu-id="58158-103">CancelRecordChange Macro Action (пользовательское веб-приложение Access)</span><span class="sxs-lookup"><span data-stu-id="58158-103">CancelRecordChange Macro Action (Access custom web app)</span></span>

<span data-ttu-id="58158-104">Действие **CancelRecordChange** можно использовать для отмены изменений, примененных к записи в блоке данных **[CreateRecord](createrecord-data-block-access-custom-web-app.md)** или **[EditRecord,](editrecord-data-block-access-custom-web-app.md)** прежде чем изменения будут зафиксированы.</span><span class="sxs-lookup"><span data-stu-id="58158-104">You can use the **CancelRecordChange** action to cancel the changes applied to a record in a **[CreateRecord](createrecord-data-block-access-custom-web-app.md)** or **[EditRecord](editrecord-data-block-access-custom-web-app.md)** data block before the changes are committed.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="58158-105">Корпорация Майкрософт в настоящее время не рекомендует создавать и использовать веб-приложения Access в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="58158-105">Microsoft no longer recommends creating and using Access web apps in SharePoint.</span></span> <span data-ttu-id="58158-106">В качестве альтернативы можно использовать [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) для создания бизнес-решений без кода для Интернета и мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="58158-106">As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="58158-107">Действие **CancelRecordChange** доступно только в макросах данных.</span><span class="sxs-lookup"><span data-stu-id="58158-107">The **CancelRecordChange** action is available only in Data Macros.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="58158-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="58158-108">Remarks</span></span>

<span data-ttu-id="58158-109">При вызове действия **CancelRecordChange** блок данных **CreateRecord** или **EditRecord** немедленно выходит из него.</span><span class="sxs-lookup"><span data-stu-id="58158-109">When you call the **CancelRecordChange** action, the **CreateRecord** or **EditRecord** data block is exited immediately.</span></span> 
  

