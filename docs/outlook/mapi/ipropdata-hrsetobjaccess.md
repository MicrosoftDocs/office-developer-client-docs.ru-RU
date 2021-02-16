---
title: IPropDataHrSetObjAccess
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrSetObjAccess
api_type:
- COM
ms.assetid: 01bd3235-22cc-4ff3-b2b6-341ce622128b
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 4e478c9e8978125a37691ee5bd97fa9f1cbce077
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425157"
---
# <a name="ipropdatahrsetobjaccess"></a><span data-ttu-id="4064e-103">IPropData::HrSetObjAccess</span><span class="sxs-lookup"><span data-stu-id="4064e-103">IPropData::HrSetObjAccess</span></span>

  
  
<span data-ttu-id="4064e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4064e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4064e-105">Задает уровень доступа для объекта.</span><span class="sxs-lookup"><span data-stu-id="4064e-105">Sets the access level for the object.</span></span>
  
```cpp
HRESULT HrSetObjAccess(
  ULONG ulAccess
);
```

## <a name="parameters"></a><span data-ttu-id="4064e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4064e-106">Parameters</span></span>

 <span data-ttu-id="4064e-107">_ulAccess_</span><span class="sxs-lookup"><span data-stu-id="4064e-107">_ulAccess_</span></span>
  
> <span data-ttu-id="4064e-108">[in] Битоваяmas флагов, которая указывает уровень доступа объекта.</span><span class="sxs-lookup"><span data-stu-id="4064e-108">[in] A bitmask of flags that specifies the object's access level.</span></span> <span data-ttu-id="4064e-109">Можно установить один из следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="4064e-109">One of the following flags can be set:</span></span>
    
<span data-ttu-id="4064e-110">IPROP_READONLY</span><span class="sxs-lookup"><span data-stu-id="4064e-110">IPROP_READONLY</span></span> 
  
> <span data-ttu-id="4064e-111">Устанавливает уровень доступа объекта только для чтения.</span><span class="sxs-lookup"><span data-stu-id="4064e-111">Sets the object's access level to read-only.</span></span> 
    
<span data-ttu-id="4064e-112">IPROP_READWRITE</span><span class="sxs-lookup"><span data-stu-id="4064e-112">IPROP_READWRITE</span></span> 
  
> <span data-ttu-id="4064e-113">Устанавливает уровень доступа объекта для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="4064e-113">Sets the object's access level to read/write.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4064e-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4064e-114">Return value</span></span>

<span data-ttu-id="4064e-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="4064e-115">S_OK</span></span> 
  
> <span data-ttu-id="4064e-116">Уровень доступа объекта успешно установлен.</span><span class="sxs-lookup"><span data-stu-id="4064e-116">The object's access level was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4064e-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="4064e-117">Remarks</span></span>

<span data-ttu-id="4064e-118">Метод **IPropData::HrSetObjAccess** задает уровень доступа для всего объекта, а не для отдельных свойств.</span><span class="sxs-lookup"><span data-stu-id="4064e-118">The **IPropData::HrSetObjAccess** method sets the access level for an entire object, rather than for individual properties.</span></span> <span data-ttu-id="4064e-119">**HrSetObjAccess можно** использовать для изменения уровня доступа, установленного при создания объекта.</span><span class="sxs-lookup"><span data-stu-id="4064e-119">**HrSetObjAccess** can be used to change the access level established when the object was created.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="4064e-120">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="4064e-120">Notes to callers</span></span>

<span data-ttu-id="4064e-121">Чтобы установить уровень доступа для свойства, сначала вызовите **HrSetObjAccess** с флагом IPROP_READWRITE, установленным в параметре  _ulAccess,_ чтобы сделать объект изменимым.</span><span class="sxs-lookup"><span data-stu-id="4064e-121">To set an access level on a property, first call **HrSetObjAccess** with the IPROP_READWRITE flag set in the  _ulAccess_ parameter to make the object modifiable.</span></span> <span data-ttu-id="4064e-122">Затем вызовите метод [IPropData::HrSetPropAccess,](ipropdata-hrsetpropaccess.md) указав целевое свойство в массиве, на который указывает параметр _lpPropTagArray._</span><span class="sxs-lookup"><span data-stu-id="4064e-122">Then call the [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) method, specifying the target property in the array pointed to by the  _lpPropTagArray_ parameter.</span></span> 
  
<span data-ttu-id="4064e-123">Чтобы создать объект со свойствами, которые будут доступны только для чтения клиентам, создайте объект для чтения и записи, добавьте необходимые свойства, а затем вызовите **HrSetObjAccess,** чтобы изменить доступ объекта на доступ только для чтения.</span><span class="sxs-lookup"><span data-stu-id="4064e-123">To create an object with properties that will be read-only to clients, create a read/write object, add the necessary properties, and then call **HrSetObjAccess** to change the object's access to read-only.</span></span> 
  
<span data-ttu-id="4064e-124">Вы также можете использовать **HrSetObjAccess,** чтобы запретить клиентам создавать новые свойства.</span><span class="sxs-lookup"><span data-stu-id="4064e-124">You can also use **HrSetObjAccess** to prevent clients from creating new properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4064e-125">См. также</span><span class="sxs-lookup"><span data-stu-id="4064e-125">See also</span></span>



[<span data-ttu-id="4064e-126">IPropData::HrGetPropAccess</span><span class="sxs-lookup"><span data-stu-id="4064e-126">IPropData::HrGetPropAccess</span></span>](ipropdata-hrgetpropaccess.md)
  
[<span data-ttu-id="4064e-127">IPropData::HrSetPropAccess</span><span class="sxs-lookup"><span data-stu-id="4064e-127">IPropData::HrSetPropAccess</span></span>](ipropdata-hrsetpropaccess.md)
  
[<span data-ttu-id="4064e-128">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="4064e-128">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)

