---
title: Invalidating an Object
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7d601cee-ffc4-4c7c-8006-40b717dee247
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: bf7ef15ccfd9cd015771785bda9d6ad79415736b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407678"
---
# <a name="invalidating-an-object"></a><span data-ttu-id="1c93d-103">Invalidating an Object</span><span class="sxs-lookup"><span data-stu-id="1c93d-103">Invalidating an Object</span></span>

  
  
<span data-ttu-id="1c93d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1c93d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1c93d-105">В процессе завершения работы поставщика может потребоваться сделать объект недействительным.</span><span class="sxs-lookup"><span data-stu-id="1c93d-105">As part of your provider's shutdown process, you might want to invalidate an object.</span></span> <span data-ttu-id="1c93d-106">При аннулировании объекта необходимо заменить ее ветвь на vtable, которая содержит реализации для трех методов **IUnknown:** **AddRef,** **Release** и **QueryInterface.**</span><span class="sxs-lookup"><span data-stu-id="1c93d-106">Invalidating an object involves replacing its vtable with a vtable that contains implementations for the three **IUnknown** methods: **AddRef**, **Release**, and **QueryInterface**.</span></span> <span data-ttu-id="1c93d-107">Аннулировать объект, вызывая [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md), метод, включенный в объект поддержки каждого из трех типов общих поставщиков.</span><span class="sxs-lookup"><span data-stu-id="1c93d-107">Invalidate an object by calling [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md), a method that is included in the support object of each of the three common provider types.</span></span> <span data-ttu-id="1c93d-108">Поставщики обычно делают этот вызов в реализации метода Logoff объекта **входа.**</span><span class="sxs-lookup"><span data-stu-id="1c93d-108">Providers typically make this call in the implementation of their logon object's **Logoff** method.</span></span> 
  
<span data-ttu-id="1c93d-109">При аннулировании объекта MAPI несет полную ответственность за освободив память, связанную с объектом.</span><span class="sxs-lookup"><span data-stu-id="1c93d-109">Invalidating an object gives MAPI the ultimate responsibility for freeing the memory associated with an object.</span></span> <span data-ttu-id="1c93d-110">Вы можете освободить все ресурсы, связанные с объектом, а затем вызвать **MakeInvalid,** чтобы сделать все методы в унаследованных интерфейсах недействительными.</span><span class="sxs-lookup"><span data-stu-id="1c93d-110">You can free all of the resources connected with an object and then call **MakeInvalid** to invalidate all of the methods in its inherited interfaces.</span></span> <span data-ttu-id="1c93d-111">Вызовы любого из этих методов возвращают MAPI_E_INVALID_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="1c93d-111">Calls to any of these methods will return MAPI_E_INVALID_OBJECT.</span></span> <span data-ttu-id="1c93d-112">Использование **MakeInvalid** — это параметр, который многие поставщики услуг предпочитают игнорировать.</span><span class="sxs-lookup"><span data-stu-id="1c93d-112">Using **MakeInvalid** is an option that many service providers choose to ignore.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1c93d-113">См. также</span><span class="sxs-lookup"><span data-stu-id="1c93d-113">See also</span></span>



[<span data-ttu-id="1c93d-114">Завершение работы поставщика услуг</span><span class="sxs-lookup"><span data-stu-id="1c93d-114">Shutting Down a Service Provider</span></span>](shutting-down-a-service-provider.md)

