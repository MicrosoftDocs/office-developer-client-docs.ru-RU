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
# <a name="copying-mapi-properties"></a><span data-ttu-id="060f6-103">Копирование свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="060f6-103">Copying MAPI Properties</span></span>

  
  
<span data-ttu-id="060f6-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="060f6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="060f6-105">Клиенты и поставщики услуг могут копировать одно или несколько свойств объекта с помощью следующих методов **IMAPIProp** и функций API:</span><span class="sxs-lookup"><span data-stu-id="060f6-105">Clients and service providers can copy one or more of an object's properties with the following **IMAPIProp** methods and API functions:</span></span> 
  
- <span data-ttu-id="060f6-106">Метод [IMAPIProp:: CopyTo](imapiprop-copyto.md) копирует все свойства объекта в другой объект, при необходимости исключая выбранные свойства.</span><span class="sxs-lookup"><span data-stu-id="060f6-106">The [IMAPIProp::CopyTo](imapiprop-copyto.md) method copies all of an object's properties to another object, optionally excluding selected properties.</span></span> <span data-ttu-id="060f6-107">**CopyTo** используется для копирования или перемещения объектов любого типа.</span><span class="sxs-lookup"><span data-stu-id="060f6-107">**CopyTo** is used for copying or moving any type of object.</span></span> 
    
- <span data-ttu-id="060f6-108">Метод [IMAPIProp:: копипропс](imapiprop-copyprops.md) копирует выбранные свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="060f6-108">The [IMAPIProp::CopyProps](imapiprop-copyprops.md) method copies selected properties of an object.</span></span> <span data-ttu-id="060f6-109">**Копипропс** используется в основном с сообщениями.</span><span class="sxs-lookup"><span data-stu-id="060f6-109">**CopyProps** is used mainly with messages.</span></span> <span data-ttu-id="060f6-110">Когда клиент создает переадресованную копию сообщения или ответа, **копипропс** обрабатывает копирование соответствующих свойств из исходного сообщения.</span><span class="sxs-lookup"><span data-stu-id="060f6-110">When a client creates a forwarded copy of a message or a reply, **CopyProps** handles copying the appropriate properties from the original message.</span></span> 
    
- <span data-ttu-id="060f6-111">Функция [пропкопиморе](propcopymore.md) копирует одно значение свойства из одного расположения в другое.</span><span class="sxs-lookup"><span data-stu-id="060f6-111">The [PropCopyMore](propcopymore.md) function copies a single property value from one location to another.</span></span> <span data-ttu-id="060f6-112">Используйте **пропкопиморе** с осторожностью.</span><span class="sxs-lookup"><span data-stu-id="060f6-112">Use **PropCopyMore** with caution.</span></span> <span data-ttu-id="060f6-113">Возможно, при копировании одного значения за раз, чтобы выделить множество небольших блоков памяти и вызвать фрагментацию памяти.</span><span class="sxs-lookup"><span data-stu-id="060f6-113">It is possible — when copying one value at a time — to allocate many small blocks of memory and cause memory to fragment.</span></span> 
    
- <span data-ttu-id="060f6-114">Функция [сккопипропс](sccopyprops.md) копирует значения свойств в пакетном режиме.</span><span class="sxs-lookup"><span data-stu-id="060f6-114">The [ScCopyProps](sccopyprops.md) function copies property values in bulk.</span></span> <span data-ttu-id="060f6-115">**Сккопипропс** может копировать значения свойств, созданных из несвязных блоков памяти.</span><span class="sxs-lookup"><span data-stu-id="060f6-115">**ScCopyProps** can copy property values that have been built from disjointed blocks of memory.</span></span> <span data-ttu-id="060f6-116">Он возвращает новый массив свойств.</span><span class="sxs-lookup"><span data-stu-id="060f6-116">It returns a new property array.</span></span> 
    
- <span data-ttu-id="060f6-117">Если массив свойств, возвращаемый **сккопипропс** , должен храниться на диске, используйте функцию [скрелокпропс](screlocprops.md) для изменения указателей.</span><span class="sxs-lookup"><span data-stu-id="060f6-117">If the property array returned by **ScCopyProps** is to be stored on disk, use the [ScRelocProps](screlocprops.md) function to adjust the pointers.</span></span> <span data-ttu-id="060f6-118">**Скрелокпропс** должен вызываться дважды; один раз, чтобы изменить адреса перед записью операции с данными и затем снова во время операции чтения.</span><span class="sxs-lookup"><span data-stu-id="060f6-118">**ScRelocProps** should be called twice; once to adjust the addresses before writing the data operation and then again during the read operation.</span></span> <span data-ttu-id="060f6-119">Функция **скрелокпропс** предполагает, что массив значений свойства был изначально выделен в виде одного выделения.</span><span class="sxs-lookup"><span data-stu-id="060f6-119">The **ScRelocProps** function assumes that the property value array was originally allocated in a single allocation.</span></span> 
    
<span data-ttu-id="060f6-120">Функции API, описанные в предыдущих свойствах копирования списка в памяти, а не из одного объекта в другой объект.</span><span class="sxs-lookup"><span data-stu-id="060f6-120">The API functions described in the preceding list copy properties in memory rather than from one object to another object.</span></span> <span data-ttu-id="060f6-121">Эти функции в настоящее время поддерживаются, но могут не поддерживаться в будущих выпусках.</span><span class="sxs-lookup"><span data-stu-id="060f6-121">These functions are presently supported, but might not be supported in a future release.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="060f6-122">См. также</span><span class="sxs-lookup"><span data-stu-id="060f6-122">See also</span></span>



[<span data-ttu-id="060f6-123">Обзор свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="060f6-123">MAPI Property Overview</span></span>](mapi-property-overview.md)

