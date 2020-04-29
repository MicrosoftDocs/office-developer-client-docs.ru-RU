---
title: Аннулирование объекта
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
# <a name="invalidating-an-object"></a><span data-ttu-id="e9af0-103">Аннулирование объекта</span><span class="sxs-lookup"><span data-stu-id="e9af0-103">Invalidating an Object</span></span>

  
  
<span data-ttu-id="e9af0-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e9af0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e9af0-105">В рамках процесса завершения работы поставщика может потребоваться сделать объект недействительным.</span><span class="sxs-lookup"><span data-stu-id="e9af0-105">As part of your provider's shutdown process, you might want to invalidate an object.</span></span> <span data-ttu-id="e9af0-106">Аннулирование объекта включает замену его виртуальной таблицы (vtable), которая содержит реализации трех методов **IUnknown** : **AddRef**, **Release**и **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="e9af0-106">Invalidating an object involves replacing its vtable with a vtable that contains implementations for the three **IUnknown** methods: **AddRef**, **Release**, and **QueryInterface**.</span></span> <span data-ttu-id="e9af0-107">Сделать объект недействительным, вызвав [имаписуппорт:: макеинвалид](imapisupport-makeinvalid.md), метод, который включен в объект поддержки каждого из трех типов поставщика.</span><span class="sxs-lookup"><span data-stu-id="e9af0-107">Invalidate an object by calling [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md), a method that is included in the support object of each of the three common provider types.</span></span> <span data-ttu-id="e9af0-108">Поставщики обычно выполняют этот вызов в реализации метода **выхода** объекта logon.</span><span class="sxs-lookup"><span data-stu-id="e9af0-108">Providers typically make this call in the implementation of their logon object's **Logoff** method.</span></span> 
  
<span data-ttu-id="e9af0-109">При аннулировании объекта обеспечивается максимальная ответственность за освобождение памяти, связанной с объектом.</span><span class="sxs-lookup"><span data-stu-id="e9af0-109">Invalidating an object gives MAPI the ultimate responsibility for freeing the memory associated with an object.</span></span> <span data-ttu-id="e9af0-110">Вы можете освободить все ресурсы, подключенные к объекту, а затем вызвать **макеинвалид** , чтобы сделать недействительными все методы в унаследованных интерфейсах.</span><span class="sxs-lookup"><span data-stu-id="e9af0-110">You can free all of the resources connected with an object and then call **MakeInvalid** to invalidate all of the methods in its inherited interfaces.</span></span> <span data-ttu-id="e9af0-111">Вызовы любого из этих методов будут возвращать MAPI_E_INVALID_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="e9af0-111">Calls to any of these methods will return MAPI_E_INVALID_OBJECT.</span></span> <span data-ttu-id="e9af0-112">Использование **макеинвалид** — это параметр, который многие поставщики услуг пропускают.</span><span class="sxs-lookup"><span data-stu-id="e9af0-112">Using **MakeInvalid** is an option that many service providers choose to ignore.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e9af0-113">См. также</span><span class="sxs-lookup"><span data-stu-id="e9af0-113">See also</span></span>



[<span data-ttu-id="e9af0-114">Завершение работы поставщика услуг</span><span class="sxs-lookup"><span data-stu-id="e9af0-114">Shutting Down a Service Provider</span></span>](shutting-down-a-service-provider.md)

