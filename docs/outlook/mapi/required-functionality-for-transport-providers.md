---
title: Необходимые функциональные возможности для поставщиков транспорта
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a0d9a3e0-a500-4d72-8859-ecfd1604fc5b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 7f9768d47cf740bdf50b439ee3af4b0d2a191602
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404444"
---
# <a name="required-functionality-for-transport-providers"></a><span data-ttu-id="17c2d-103">Необходимые функциональные возможности для поставщиков транспорта</span><span class="sxs-lookup"><span data-stu-id="17c2d-103">Required Functionality for Transport Providers</span></span>

  
  
<span data-ttu-id="17c2d-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="17c2d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="17c2d-105">Каждый поставщик транспорта MAPI должен:</span><span class="sxs-lookup"><span data-stu-id="17c2d-105">Every MAPI transport provider must:</span></span>
  
- <span data-ttu-id="17c2d-106">Следуйте общим рекомендациям по работе с MAPI и другими поставщиками услуг.</span><span class="sxs-lookup"><span data-stu-id="17c2d-106">Follow the general guidelines for working with MAPI and other service providers.</span></span> <span data-ttu-id="17c2d-107">Дополнительные сведения см. в [приложении MAPI Development](mapi-application-development.md) и [MAPI Service Providers.](mapi-service-providers.md)</span><span class="sxs-lookup"><span data-stu-id="17c2d-107">For more information, see [MAPI Application Development](mapi-application-development.md) and [MAPI Service Providers](mapi-service-providers.md).</span></span>
    
- <span data-ttu-id="17c2d-108">Чтобы поставщик транспорта DLL выставил MAPI функцию инициализации [XPProviderInit.](xpproviderinit.md)</span><span class="sxs-lookup"><span data-stu-id="17c2d-108">Have its transport provider DLL expose to MAPI its [XPProviderInit](xpproviderinit.md) initialization function.</span></span> 
    
- <span data-ttu-id="17c2d-109">Подвергайте MAPI реализации [интерфейсов IXPProvider : IUnknown](ixpprovideriunknown.md) и [IXPLogon: IUnknown.](ixplogoniunknown.md)</span><span class="sxs-lookup"><span data-stu-id="17c2d-109">Expose to MAPI its implementation of the [IXPProvider : IUnknown](ixpprovideriunknown.md) and [IXPLogon : IUnknown](ixplogoniunknown.md) interfaces.</span></span> 
    
- <span data-ttu-id="17c2d-110">Подвергайте MAPI и клиентские приложения реализации [интерфейса IMAPIStatus : IMAPIProp.](imapistatusimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="17c2d-110">Expose to MAPI and client applications its implementation of the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="17c2d-111">Дополнительные сведения о реализации **IMAPIStatus** см. в дополнительных сведениях [о реализации объектов status.](status-object-implementation.md)</span><span class="sxs-lookup"><span data-stu-id="17c2d-111">For more information about implementing **IMAPIStatus**, see [Status Object Implementation](status-object-implementation.md).</span></span> 
    
- <span data-ttu-id="17c2d-112">Реализация диалоговое окно листа свойств для настройки.</span><span class="sxs-lookup"><span data-stu-id="17c2d-112">Implement a property sheet dialog box for configuration.</span></span> <span data-ttu-id="17c2d-113">Дополнительные сведения о реализации листов свойств см. в см. [в рубке Реализация листов свойств.](property-sheet-implementation.md)</span><span class="sxs-lookup"><span data-stu-id="17c2d-113">For more information about implementing property sheets, see [Property Sheet Implementation](property-sheet-implementation.md).</span></span>
    

