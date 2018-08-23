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
ms.openlocfilehash: 556ea9faedf0d9a02b0cff1bb2f1750289cc4d1e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565083"
---
# <a name="copying-mapi-properties"></a><span data-ttu-id="df857-103">Копирование свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="df857-103">Copying MAPI Properties</span></span>

  
  
<span data-ttu-id="df857-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df857-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df857-105">Клиенты и поставщиков услуг можно скопировать один или несколько свойств объекта с помощью следующих методов **IMAPIProp** и функции интерфейса API:</span><span class="sxs-lookup"><span data-stu-id="df857-105">Clients and service providers can copy one or more of an object's properties with the following **IMAPIProp** methods and API functions:</span></span> 
  
- <span data-ttu-id="df857-106">Метод [IMAPIProp::CopyTo](imapiprop-copyto.md) копирует все свойства объекта в другой объект, при необходимости за исключением выбранных свойств.</span><span class="sxs-lookup"><span data-stu-id="df857-106">The [IMAPIProp::CopyTo](imapiprop-copyto.md) method copies all of an object's properties to another object, optionally excluding selected properties.</span></span> <span data-ttu-id="df857-107">**CopyTo** используется для копирования или перемещения любой тип объекта.</span><span class="sxs-lookup"><span data-stu-id="df857-107">**CopyTo** is used for copying or moving any type of object.</span></span> 
    
- <span data-ttu-id="df857-108">Метод [IMAPIProp::CopyProps](imapiprop-copyprops.md) копирует выбранных свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="df857-108">The [IMAPIProp::CopyProps](imapiprop-copyprops.md) method copies selected properties of an object.</span></span> <span data-ttu-id="df857-109">**CopyProps** используется главным образом с сообщениями.</span><span class="sxs-lookup"><span data-stu-id="df857-109">**CopyProps** is used mainly with messages.</span></span> <span data-ttu-id="df857-110">Когда клиента создает копию переадресованных сообщение или ответ, **CopyProps** значками копирование соответствующие свойства из исходного сообщения.</span><span class="sxs-lookup"><span data-stu-id="df857-110">When a client creates a forwarded copy of a message or a reply, **CopyProps** handles copying the appropriate properties from the original message.</span></span> 
    
- <span data-ttu-id="df857-111">Функция [PropCopyMore](propcopymore.md) копирует значения одного свойства из одного места в другое.</span><span class="sxs-lookup"><span data-stu-id="df857-111">The [PropCopyMore](propcopymore.md) function copies a single property value from one location to another.</span></span> <span data-ttu-id="df857-112">Используйте **PropCopyMore** с осторожностью.</span><span class="sxs-lookup"><span data-stu-id="df857-112">Use **PropCopyMore** with caution.</span></span> <span data-ttu-id="df857-113">Возможно — при копировании одно значение за раз — для размещения множество небольших блоков памяти и привести к памяти для фрагментов.</span><span class="sxs-lookup"><span data-stu-id="df857-113">It is possible — when copying one value at a time — to allocate many small blocks of memory and cause memory to fragment.</span></span> 
    
- <span data-ttu-id="df857-114">Функция [ScCopyProps](sccopyprops.md) копирует значения свойств в пакетном режиме.</span><span class="sxs-lookup"><span data-stu-id="df857-114">The [ScCopyProps](sccopyprops.md) function copies property values in bulk.</span></span> <span data-ttu-id="df857-115">**ScCopyProps** можно скопировать значения свойств, которые были созданы из несвязанное блоки памяти.</span><span class="sxs-lookup"><span data-stu-id="df857-115">**ScCopyProps** can copy property values that have been built from disjointed blocks of memory.</span></span> <span data-ttu-id="df857-116">Возвращает новый массив свойство.</span><span class="sxs-lookup"><span data-stu-id="df857-116">It returns a new property array.</span></span> 
    
- <span data-ttu-id="df857-117">Если свойство массив, возвращенный **ScCopyProps** будут храниться на диске, используйте функцию [ScRelocProps](screlocprops.md) регулировка указатели.</span><span class="sxs-lookup"><span data-stu-id="df857-117">If the property array returned by **ScCopyProps** is to be stored on disk, use the [ScRelocProps](screlocprops.md) function to adjust the pointers.</span></span> <span data-ttu-id="df857-118">**ScRelocProps** должен быть вызван дважды; один раз, чтобы настроить адреса перед записью операции с данными и затем снова во время операции чтения.</span><span class="sxs-lookup"><span data-stu-id="df857-118">**ScRelocProps** should be called twice; once to adjust the addresses before writing the data operation and then again during the read operation.</span></span> <span data-ttu-id="df857-119">Функция **ScRelocProps** предполагается, что массива значение свойства сначала выделенная в за одну операцию.</span><span class="sxs-lookup"><span data-stu-id="df857-119">The **ScRelocProps** function assumes that the property value array was originally allocated in a single allocation.</span></span> 
    
<span data-ttu-id="df857-120">Функции интерфейса API, описано в предыдущей копии списка свойств в памяти, а не из одного объекта в другой объект.</span><span class="sxs-lookup"><span data-stu-id="df857-120">The API functions described in the preceding list copy properties in memory rather than from one object to another object.</span></span> <span data-ttu-id="df857-121">Эти функции поддерживаются в настоящее время, но может не поддерживаться в следующем выпуске.</span><span class="sxs-lookup"><span data-stu-id="df857-121">These functions are presently supported, but might not be supported in a future release.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="df857-122">См. также</span><span class="sxs-lookup"><span data-stu-id="df857-122">See also</span></span>



[<span data-ttu-id="df857-123">Обзор свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="df857-123">MAPI Property Overview</span></span>](mapi-property-overview.md)

