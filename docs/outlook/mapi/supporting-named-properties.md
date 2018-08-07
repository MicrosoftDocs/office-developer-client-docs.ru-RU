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
ms.openlocfilehash: 983cbaf4d3523bf1e5370e5ad3119ab8c1490f8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812425"
---
# <a name="supporting-named-properties"></a><span data-ttu-id="2e505-103">Поддержка именованных свойств</span><span class="sxs-lookup"><span data-stu-id="2e505-103">Supporting Named Properties</span></span>

  
  
<span data-ttu-id="2e505-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2e505-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2e505-105">Any object that implements the [IMAPIProp: IUnknown](imapipropiunknown.md) interface can support named properties.</span><span class="sxs-lookup"><span data-stu-id="2e505-105">Any object that implements the [IMAPIProp : IUnknown](imapipropiunknown.md) interface can support named properties.</span></span> <span data-ttu-id="2e505-106">Поддержка именованных свойств является обязательным для:</span><span class="sxs-lookup"><span data-stu-id="2e505-106">Support for named properties is required for:</span></span> 
  
- <span data-ttu-id="2e505-107">Поставщиками адресных книг, которые позволяют записей от других поставщиков копируются в их контейнеров.</span><span class="sxs-lookup"><span data-stu-id="2e505-107">Address book providers that allow entries from other providers to be copied into their containers.</span></span>
    
- <span data-ttu-id="2e505-108">Сообщение хранилища поставщиков, которые могут использоваться для создания типов произвольных сообщений.</span><span class="sxs-lookup"><span data-stu-id="2e505-108">Message store providers that can be used to create arbitrary message types.</span></span>
    
<span data-ttu-id="2e505-109">Поддержка именованное свойство является необязательным для всех других поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="2e505-109">Named property support is optional for all other service providers.</span></span> <span data-ttu-id="2e505-110">Поставщики услуг, которые поддерживают именованные свойства необходимо реализовать идентификатор имени сопоставления в методы [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) и [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="2e505-110">Service providers that do support named properties must implement name-to-identifier mapping in the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods.</span></span> <span data-ttu-id="2e505-111">Клиенты вызывать **GetNamesFromIDs** для извлечения соответствующих имен для одного или нескольких идентификаторов свойство в более чем диапазон 0x8000 и **GetIDsFromNames** для создания или получения идентификаторов для одно или несколько имен.</span><span class="sxs-lookup"><span data-stu-id="2e505-111">Clients call **GetNamesFromIDs** to retrieve the corresponding names for one or more property identifiers in the over 0x8000 range and **GetIDsFromNames** to either create or retrieve the identifiers for one or more names.</span></span> 
  
<span data-ttu-id="2e505-112">Поставщики услуг, которые не поддерживают именованные свойства выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="2e505-112">Service providers that do not support named properties must:</span></span>
  
- <span data-ttu-id="2e505-113">Не удается вызовы [IMAPIProp::SetProps](imapiprop-setprops.md) , чтобы задать свойства с идентификаторами 0x8000 или более высокой версии, возвращая MAPI_E_UNEXPECTED_ID в массиве [SPropProblem](spropproblem.md) .</span><span class="sxs-lookup"><span data-stu-id="2e505-113">Fail calls to [IMAPIProp::SetProps](imapiprop-setprops.md) to set properties with identifiers of 0x8000 or greater by returning MAPI_E_UNEXPECTED_ID in the [SPropProblem](spropproblem.md) array.</span></span> 
    
- <span data-ttu-id="2e505-114">Возвращает MAPI_E_NO_SUPPORT из методов [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) и [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="2e505-114">Return MAPI_E_NO_SUPPORT from the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods .</span></span> 
    

