---
title: Поддержка именуемой свойства
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2e742ecd-2dcd-46a8-9d4e-2cec2c6f795e
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 27625e913f06e858295351ed62de840ae7789915
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434328"
---
# <a name="supporting-named-properties"></a><span data-ttu-id="e0be9-103">Поддержка именуемой свойства</span><span class="sxs-lookup"><span data-stu-id="e0be9-103">Supporting Named Properties</span></span>

  
  
<span data-ttu-id="e0be9-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e0be9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e0be9-105">Any object that implements the [IMAPIProp: IUnknown](imapipropiunknown.md) interface can support named properties.</span><span class="sxs-lookup"><span data-stu-id="e0be9-105">Any object that implements the [IMAPIProp : IUnknown](imapipropiunknown.md) interface can support named properties.</span></span> <span data-ttu-id="e0be9-106">Поддержка именуемой свойства необходима для:</span><span class="sxs-lookup"><span data-stu-id="e0be9-106">Support for named properties is required for:</span></span> 
  
- <span data-ttu-id="e0be9-107">Поставщики адресных книг, которые позволяют скопировать записи от других поставщиков в свои контейнеры.</span><span class="sxs-lookup"><span data-stu-id="e0be9-107">Address book providers that allow entries from other providers to be copied into their containers.</span></span>
    
- <span data-ttu-id="e0be9-108">Поставщики store сообщений, которые могут использоваться для создания произвольных типов сообщений.</span><span class="sxs-lookup"><span data-stu-id="e0be9-108">Message store providers that can be used to create arbitrary message types.</span></span>
    
<span data-ttu-id="e0be9-109">Поддержка именуемого свойства не является обязательной для всех остальных поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="e0be9-109">Named property support is optional for all other service providers.</span></span> <span data-ttu-id="e0be9-110">Поставщики служб, которые поддерживают именуемые свойства, должны реализовать сопоставление имен и идентификаторов в методах [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) и [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md)</span><span class="sxs-lookup"><span data-stu-id="e0be9-110">Service providers that do support named properties must implement name-to-identifier mapping in the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods.</span></span> <span data-ttu-id="e0be9-111">Клиенты вызывать **GetNamesFromIDs,** чтобы получить соответствующие имена для одного или более идентификаторов свойств в диапазоне 0x8000 и **GetIDsFromNames** для создания или извлечения идентификаторов для одного или более имен.</span><span class="sxs-lookup"><span data-stu-id="e0be9-111">Clients call **GetNamesFromIDs** to retrieve the corresponding names for one or more property identifiers in the over 0x8000 range and **GetIDsFromNames** to either create or retrieve the identifiers for one or more names.</span></span> 
  
<span data-ttu-id="e0be9-112">Поставщики услуг, которые не поддерживают именуемые свойства, должны:</span><span class="sxs-lookup"><span data-stu-id="e0be9-112">Service providers that do not support named properties must:</span></span>
  
- <span data-ttu-id="e0be9-113">Сбой вызовов [IMAPIProp::SetProps,](imapiprop-setprops.md) чтобы установить свойства с идентификаторами 0x8000 или более, возвращая MAPI_E_UNEXPECTED_ID в [массиве SPropProblem.](spropproblem.md)</span><span class="sxs-lookup"><span data-stu-id="e0be9-113">Fail calls to [IMAPIProp::SetProps](imapiprop-setprops.md) to set properties with identifiers of 0x8000 or greater by returning MAPI_E_UNEXPECTED_ID in the [SPropProblem](spropproblem.md) array.</span></span> 
    
- <span data-ttu-id="e0be9-114">Возвращает MAPI_E_NO_SUPPORT из методов [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) и [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md)</span><span class="sxs-lookup"><span data-stu-id="e0be9-114">Return MAPI_E_NO_SUPPORT from the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods .</span></span> 
    

