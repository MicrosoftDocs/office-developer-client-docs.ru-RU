---
title: Копирование свойств MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: a52f4bcd-6e17-4623-a469-53be1f2758b1
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: ae8e553cf2e19ae1ba06ca09aad84eae9f7d1238
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415049"
---
# <a name="copying-mapi-properties"></a><span data-ttu-id="bddec-103">Копирование свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="bddec-103">Copying MAPI Properties</span></span>

  
  
<span data-ttu-id="bddec-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bddec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bddec-105">Клиенты и поставщики услуг могут копировать одно или несколько свойств объекта с помощью следующих методов **IMAPIProp** и функций API:</span><span class="sxs-lookup"><span data-stu-id="bddec-105">Clients and service providers can copy one or more of an object's properties with the following **IMAPIProp** methods and API functions:</span></span> 
  
- <span data-ttu-id="bddec-106">Метод [IMAPIProp::CopyTo](imapiprop-copyto.md) копирует все свойства объекта в другой объект, дополнительно исключая выбранные свойства.</span><span class="sxs-lookup"><span data-stu-id="bddec-106">The [IMAPIProp::CopyTo](imapiprop-copyto.md) method copies all of an object's properties to another object, optionally excluding selected properties.</span></span> <span data-ttu-id="bddec-107">**CopyTo** используется для копирования или перемещения любого типа объекта.</span><span class="sxs-lookup"><span data-stu-id="bddec-107">**CopyTo** is used for copying or moving any type of object.</span></span> 
    
- <span data-ttu-id="bddec-108">Метод [IMAPIProp::CopyProps](imapiprop-copyprops.md) копирует выбранные свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="bddec-108">The [IMAPIProp::CopyProps](imapiprop-copyprops.md) method copies selected properties of an object.</span></span> <span data-ttu-id="bddec-109">**CopyProps** используется главным образом с сообщениями.</span><span class="sxs-lookup"><span data-stu-id="bddec-109">**CopyProps** is used mainly with messages.</span></span> <span data-ttu-id="bddec-110">Когда клиент создает переадрещенную копию сообщения или ответа, **CopyProps** обрабатывает копирование соответствующих свойств из исходного сообщения.</span><span class="sxs-lookup"><span data-stu-id="bddec-110">When a client creates a forwarded copy of a message or a reply, **CopyProps** handles copying the appropriate properties from the original message.</span></span> 
    
- <span data-ttu-id="bddec-111">Функция [PropCopyMore](propcopymore.md) копирует одно значение свойства из одного расположения в другое.</span><span class="sxs-lookup"><span data-stu-id="bddec-111">The [PropCopyMore](propcopymore.md) function copies a single property value from one location to another.</span></span> <span data-ttu-id="bddec-112">Используйте **PropCopyMore с** осторожностью.</span><span class="sxs-lookup"><span data-stu-id="bddec-112">Use **PropCopyMore** with caution.</span></span> <span data-ttu-id="bddec-113">При копировании по одному значению можно выделить много небольших блоков памяти и привести к фрагментации памяти.</span><span class="sxs-lookup"><span data-stu-id="bddec-113">It is possible — when copying one value at a time — to allocate many small blocks of memory and cause memory to fragment.</span></span> 
    
- <span data-ttu-id="bddec-114">Функция [ScCopyProps](sccopyprops.md) массово копирует значения свойств.</span><span class="sxs-lookup"><span data-stu-id="bddec-114">The [ScCopyProps](sccopyprops.md) function copies property values in bulk.</span></span> <span data-ttu-id="bddec-115">**ScCopyProps** может копировать значения свойств, построенные из несоединенных блоков памяти.</span><span class="sxs-lookup"><span data-stu-id="bddec-115">**ScCopyProps** can copy property values that have been built from disjointed blocks of memory.</span></span> <span data-ttu-id="bddec-116">Он возвращает новый массив свойств.</span><span class="sxs-lookup"><span data-stu-id="bddec-116">It returns a new property array.</span></span> 
    
- <span data-ttu-id="bddec-117">Если массив свойств, возвращаемого **ScCopyProps,** должен храниться на диске, используйте функцию [ScRelocProps](screlocprops.md) для настройки указателей.</span><span class="sxs-lookup"><span data-stu-id="bddec-117">If the property array returned by **ScCopyProps** is to be stored on disk, use the [ScRelocProps](screlocprops.md) function to adjust the pointers.</span></span> <span data-ttu-id="bddec-118">**ScRelocProps** должен быть вызван дважды; один раз для настройки адресов перед записью операции с данными, а затем еще раз во время операции чтения.</span><span class="sxs-lookup"><span data-stu-id="bddec-118">**ScRelocProps** should be called twice; once to adjust the addresses before writing the data operation and then again during the read operation.</span></span> <span data-ttu-id="bddec-119">Функция **ScRelocProps** предполагает, что массив значений свойств изначально был выделен в одном выделении.</span><span class="sxs-lookup"><span data-stu-id="bddec-119">The **ScRelocProps** function assumes that the property value array was originally allocated in a single allocation.</span></span> 
    
<span data-ttu-id="bddec-120">Функции API, описанные в предыдущем списке, копируют свойства в памяти, а не из одного объекта в другой.</span><span class="sxs-lookup"><span data-stu-id="bddec-120">The API functions described in the preceding list copy properties in memory rather than from one object to another object.</span></span> <span data-ttu-id="bddec-121">В настоящее время эти функции поддерживаются, но могут не поддерживаться в будущих выпусках.</span><span class="sxs-lookup"><span data-stu-id="bddec-121">These functions are presently supported, but might not be supported in a future release.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bddec-122">См. также</span><span class="sxs-lookup"><span data-stu-id="bddec-122">See also</span></span>



[<span data-ttu-id="bddec-123">Обзор свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="bddec-123">MAPI Property Overview</span></span>](mapi-property-overview.md)

