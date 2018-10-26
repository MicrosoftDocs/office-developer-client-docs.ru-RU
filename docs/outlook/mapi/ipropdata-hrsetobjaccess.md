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
ms.openlocfilehash: d7886d08c21e8fff9aceb3437ecb6bbbd970ed7b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591424"
---
# <a name="ipropdatahrsetobjaccess"></a><span data-ttu-id="464d2-103">IPropData::HrSetObjAccess</span><span class="sxs-lookup"><span data-stu-id="464d2-103">IPropData::HrSetObjAccess</span></span>

  
  
<span data-ttu-id="464d2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="464d2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="464d2-105">Задает уровень доступа для объекта.</span><span class="sxs-lookup"><span data-stu-id="464d2-105">Sets the access level for the object.</span></span>
  
```cpp
HRESULT HrSetObjAccess(
  ULONG ulAccess
);
```

## <a name="parameters"></a><span data-ttu-id="464d2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="464d2-106">Parameters</span></span>

 <span data-ttu-id="464d2-107">_ulAccess_</span><span class="sxs-lookup"><span data-stu-id="464d2-107">_ulAccess_</span></span>
  
> <span data-ttu-id="464d2-108">[in] Битовая маска флаги, задающее уровень доступа объекта.</span><span class="sxs-lookup"><span data-stu-id="464d2-108">[in] A bitmask of flags that specifies the object's access level.</span></span> <span data-ttu-id="464d2-109">Можно установить один из следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="464d2-109">One of the following flags can be set:</span></span>
    
<span data-ttu-id="464d2-110">IPROP_READONLY</span><span class="sxs-lookup"><span data-stu-id="464d2-110">IPROP_READONLY</span></span> 
  
> <span data-ttu-id="464d2-111">Задает объект уровень доступа только для чтения.</span><span class="sxs-lookup"><span data-stu-id="464d2-111">Sets the object's access level to read-only.</span></span> 
    
<span data-ttu-id="464d2-112">IPROP_READWRITE</span><span class="sxs-lookup"><span data-stu-id="464d2-112">IPROP_READWRITE</span></span> 
  
> <span data-ttu-id="464d2-113">Задает объект уровень доступа для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="464d2-113">Sets the object's access level to read/write.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="464d2-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="464d2-114">Return value</span></span>

<span data-ttu-id="464d2-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="464d2-115">S_OK</span></span> 
  
> <span data-ttu-id="464d2-116">Уровень доступа объекта был успешно установлен.</span><span class="sxs-lookup"><span data-stu-id="464d2-116">The object's access level was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="464d2-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="464d2-117">Remarks</span></span>

<span data-ttu-id="464d2-118">Метод **IPropData::HrSetObjAccess** можно задать уровень доступа для объекта целиком, а не для отдельных свойств.</span><span class="sxs-lookup"><span data-stu-id="464d2-118">The **IPropData::HrSetObjAccess** method sets the access level for an entire object, rather than for individual properties.</span></span> <span data-ttu-id="464d2-119">**HrSetObjAccess** можно использовать для изменения уровня доступа, указанные при создании объекта.</span><span class="sxs-lookup"><span data-stu-id="464d2-119">**HrSetObjAccess** can be used to change the access level established when the object was created.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="464d2-120">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="464d2-120">Notes to callers</span></span>

<span data-ttu-id="464d2-121">Чтобы задать уровень доступа к свойству, вызовите **HrSetObjAccess** с флагом IPROP_READWRITE, задавать в параметре _ulAccess_ , чтобы сделать объект изменяемым.</span><span class="sxs-lookup"><span data-stu-id="464d2-121">To set an access level on a property, first call **HrSetObjAccess** with the IPROP_READWRITE flag set in the  _ulAccess_ parameter to make the object modifiable.</span></span> <span data-ttu-id="464d2-122">Затем вызовите метод [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) , указав свойства конечного объекта в массиве указывает параметр _lpPropTagArray_ .</span><span class="sxs-lookup"><span data-stu-id="464d2-122">Then call the [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) method, specifying the target property in the array pointed to by the  _lpPropTagArray_ parameter.</span></span> 
  
<span data-ttu-id="464d2-123">Чтобы создать объект со свойствами, которые будут доступны только для чтения, чтобы клиенты, создайте объект чтения и записи, добавление необходимых свойств, а затем вызвать **HrSetObjAccess** для изменения объекта доступа только для чтения.</span><span class="sxs-lookup"><span data-stu-id="464d2-123">To create an object with properties that will be read-only to clients, create a read/write object, add the necessary properties, and then call **HrSetObjAccess** to change the object's access to read-only.</span></span> 
  
<span data-ttu-id="464d2-124">Можно также использовать **HrSetObjAccess** чтобы предотвратить создание нового свойства клиентов.</span><span class="sxs-lookup"><span data-stu-id="464d2-124">You can also use **HrSetObjAccess** to prevent clients from creating new properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="464d2-125">См. также</span><span class="sxs-lookup"><span data-stu-id="464d2-125">See also</span></span>



[<span data-ttu-id="464d2-126">IPropData::HrGetPropAccess</span><span class="sxs-lookup"><span data-stu-id="464d2-126">IPropData::HrGetPropAccess</span></span>](ipropdata-hrgetpropaccess.md)
  
[<span data-ttu-id="464d2-127">IPropData::HrSetPropAccess</span><span class="sxs-lookup"><span data-stu-id="464d2-127">IPropData::HrSetPropAccess</span></span>](ipropdata-hrsetpropaccess.md)
  
[<span data-ttu-id="464d2-128">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="464d2-128">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)

