---
title: Объявление объекта недействительным
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7d601cee-ffc4-4c7c-8006-40b717dee247
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2346ec8541e1a8b7f5ea198722833447f9f5a289
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566476"
---
# <a name="invalidating-an-object"></a><span data-ttu-id="cdc0d-103">Объявление объекта недействительным</span><span class="sxs-lookup"><span data-stu-id="cdc0d-103">Invalidating an Object</span></span>

  
  
<span data-ttu-id="cdc0d-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cdc0d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cdc0d-105">В процессе завершения работы ваш поставщик необходимо объявить недействительным объекта.</span><span class="sxs-lookup"><span data-stu-id="cdc0d-105">As part of your provider's shutdown process, you might want to invalidate an object.</span></span> <span data-ttu-id="cdc0d-106">Аннулирование объект включает в себя заменив его vtable vtable, содержащий реализации для трех методов **IUnknown** : **AddRef**, **версии**и **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="cdc0d-106">Invalidating an object involves replacing its vtable with a vtable that contains implementations for the three **IUnknown** methods: **AddRef**, **Release**, and **QueryInterface**.</span></span> <span data-ttu-id="cdc0d-107">Объект недействительными, вызвав [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md), метод, который включен в объекте поддержку каждого из трех распространенных типов поставщиков.</span><span class="sxs-lookup"><span data-stu-id="cdc0d-107">Invalidate an object by calling [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md), a method that is included in the support object of each of the three common provider types.</span></span> <span data-ttu-id="cdc0d-108">Поставщики обычно позвонить в реализации метода **выхода** их объекта входа в систему.</span><span class="sxs-lookup"><span data-stu-id="cdc0d-108">Providers typically make this call in the implementation of their logon object's **Logoff** method.</span></span> 
  
<span data-ttu-id="cdc0d-109">Аннулирование объекта дает MAPI ultimate ответственность за освобождение памяти, связанного с объектом.</span><span class="sxs-lookup"><span data-stu-id="cdc0d-109">Invalidating an object gives MAPI the ultimate responsibility for freeing the memory associated with an object.</span></span> <span data-ttu-id="cdc0d-110">Можно освободить все ресурсы, подключенных с помощью объекта и затем вызвать **MakeInvalid** на все методы в его наследуемых интерфейсов недействительными.</span><span class="sxs-lookup"><span data-stu-id="cdc0d-110">You can free all of the resources connected with an object and then call **MakeInvalid** to invalidate all of the methods in its inherited interfaces.</span></span> <span data-ttu-id="cdc0d-111">Вызовы любого из этих методов возвращает MAPI_E_INVALID_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="cdc0d-111">Calls to any of these methods will return MAPI_E_INVALID_OBJECT.</span></span> <span data-ttu-id="cdc0d-112">С помощью **MakeInvalid** — это параметр, который многие поставщики услуг выберите игнорирование.</span><span class="sxs-lookup"><span data-stu-id="cdc0d-112">Using **MakeInvalid** is an option that many service providers choose to ignore.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="cdc0d-113">См. также</span><span class="sxs-lookup"><span data-stu-id="cdc0d-113">See also</span></span>



[<span data-ttu-id="cdc0d-114">Завершение работы поставщика службы</span><span class="sxs-lookup"><span data-stu-id="cdc0d-114">Shutting Down a Service Provider</span></span>](shutting-down-a-service-provider.md)

