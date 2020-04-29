---
title: Поддержка именованных свойств
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
# <a name="supporting-named-properties"></a><span data-ttu-id="5d924-103">Поддержка именованных свойств</span><span class="sxs-lookup"><span data-stu-id="5d924-103">Supporting Named Properties</span></span>

  
  
<span data-ttu-id="5d924-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5d924-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5d924-105">Any object that implements the [IMAPIProp: IUnknown](imapipropiunknown.md) interface can support named properties.</span><span class="sxs-lookup"><span data-stu-id="5d924-105">Any object that implements the [IMAPIProp : IUnknown](imapipropiunknown.md) interface can support named properties.</span></span> <span data-ttu-id="5d924-106">Поддержка именованных свойств необходима для следующих компонентов:</span><span class="sxs-lookup"><span data-stu-id="5d924-106">Support for named properties is required for:</span></span> 
  
- <span data-ttu-id="5d924-107">Поставщики адресных книг, которые позволяют копировать записи из других поставщиков в свои контейнеры.</span><span class="sxs-lookup"><span data-stu-id="5d924-107">Address book providers that allow entries from other providers to be copied into their containers.</span></span>
    
- <span data-ttu-id="5d924-108">Поставщики хранилищ сообщений, которые можно использовать для создания произвольных типов сообщений.</span><span class="sxs-lookup"><span data-stu-id="5d924-108">Message store providers that can be used to create arbitrary message types.</span></span>
    
<span data-ttu-id="5d924-109">Поддержка именованных свойств является необязательной для всех остальных поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="5d924-109">Named property support is optional for all other service providers.</span></span> <span data-ttu-id="5d924-110">Поставщики услуг, которые поддерживают именованные свойства, должны реализовать сопоставление имен и идентификаторов в методах [IMAPIProp:: жетнамесфромидс](imapiprop-getnamesfromids.md) и [IMAPIProp:: жетидсфромнамес](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="5d924-110">Service providers that do support named properties must implement name-to-identifier mapping in the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods.</span></span> <span data-ttu-id="5d924-111">Клиенты вызывают **жетнамесфромидс** , чтобы получить соответствующие имена для одного или нескольких идентификаторов свойств в диапазоне от 0x8000 и **жетидсфромнамес** , чтобы создать или получить идентификаторы для одного или нескольких имен.</span><span class="sxs-lookup"><span data-stu-id="5d924-111">Clients call **GetNamesFromIDs** to retrieve the corresponding names for one or more property identifiers in the over 0x8000 range and **GetIDsFromNames** to either create or retrieve the identifiers for one or more names.</span></span> 
  
<span data-ttu-id="5d924-112">Поставщики услуг, не поддерживающие именованные свойства, должны:</span><span class="sxs-lookup"><span data-stu-id="5d924-112">Service providers that do not support named properties must:</span></span>
  
- <span data-ttu-id="5d924-113">Вызовы Fail для [IMAPIProp:: SetProps](imapiprop-setprops.md) для задания свойств с идентификаторами 0x8000 и выше, возвращая MAPI_E_UNEXPECTED_ID в массиве [спроппроблем](spropproblem.md) .</span><span class="sxs-lookup"><span data-stu-id="5d924-113">Fail calls to [IMAPIProp::SetProps](imapiprop-setprops.md) to set properties with identifiers of 0x8000 or greater by returning MAPI_E_UNEXPECTED_ID in the [SPropProblem](spropproblem.md) array.</span></span> 
    
- <span data-ttu-id="5d924-114">Возвращает MAPI_E_NO_SUPPORT из методов [IMAPIProp:: жетнамесфромидс](imapiprop-getnamesfromids.md) и [IMAPIProp:: жетидсфромнамес](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="5d924-114">Return MAPI_E_NO_SUPPORT from the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods .</span></span> 
    

