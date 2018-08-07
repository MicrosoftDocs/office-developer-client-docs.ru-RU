---
title: Необходимые функции для поставщиков транспорта
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a0d9a3e0-a500-4d72-8859-ecfd1604fc5b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: eb5d70c31f28df16593fb020f13124ea217476ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812150"
---
# <a name="required-functionality-for-transport-providers"></a><span data-ttu-id="e18cd-103">Необходимые функции для поставщиков транспорта</span><span class="sxs-lookup"><span data-stu-id="e18cd-103">Required Functionality for Transport Providers</span></span>

  
  
<span data-ttu-id="e18cd-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e18cd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e18cd-105">Каждый поставщик транспорта MAPI выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="e18cd-105">Every MAPI transport provider must:</span></span>
  
- <span data-ttu-id="e18cd-106">Общие рекомендации по работе с MAPI и других поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="e18cd-106">Follow the general guidelines for working with MAPI and other service providers.</span></span> <span data-ttu-id="e18cd-107">Для получения дополнительных сведений см [Разработки приложений MAPI](mapi-application-development.md) и [Поставщиков служб MAPI](mapi-service-providers.md).</span><span class="sxs-lookup"><span data-stu-id="e18cd-107">For more information, see [MAPI Application Development](mapi-application-development.md) and [MAPI Service Providers](mapi-service-providers.md).</span></span>
    
- <span data-ttu-id="e18cd-108">У поставщика транспорта DLL делает доступными для MAPI его функции инициализации [XPProviderInit](xpproviderinit.md) .</span><span class="sxs-lookup"><span data-stu-id="e18cd-108">Have its transport provider DLL expose to MAPI its [XPProviderInit](xpproviderinit.md) initialization function.</span></span> 
    
- <span data-ttu-id="e18cd-109">Предоставлять доступ MAPI его реализации [IXPProvider: IUnknown](ixpprovideriunknown.md) и [IXPLogon: IUnknown](ixplogoniunknown.md) интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="e18cd-109">Expose to MAPI its implementation of the [IXPProvider : IUnknown](ixpprovideriunknown.md) and [IXPLogon : IUnknown](ixplogoniunknown.md) interfaces.</span></span> 
    
- <span data-ttu-id="e18cd-110">Предоставлять доступ MAPI и клиентских приложениях его реализации [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e18cd-110">Expose to MAPI and client applications its implementation of the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> <span data-ttu-id="e18cd-111">Дополнительные сведения о реализации **IMAPIStatus**можно [Реализация объекта состояния](status-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="e18cd-111">For more information about implementing **IMAPIStatus**, see [Status Object Implementation](status-object-implementation.md).</span></span> 
    
- <span data-ttu-id="e18cd-112">Реализация диалогового окна Свойства таблицы конфигурации.</span><span class="sxs-lookup"><span data-stu-id="e18cd-112">Implement a property sheet dialog box for configuration.</span></span> <span data-ttu-id="e18cd-113">Дополнительные сведения о реализации свойств можно [Реализация таблицы свойств](property-sheet-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="e18cd-113">For more information about implementing property sheets, see [Property Sheet Implementation](property-sheet-implementation.md).</span></span>
    

