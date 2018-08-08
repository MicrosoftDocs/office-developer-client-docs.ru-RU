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
ms.openlocfilehash: 06cad6e80a2def1c1c3d692a80efeebe0e654a92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809512"
---
# <a name="ipropdatahrsetobjaccess"></a><span data-ttu-id="82de8-103">IPropData::HrSetObjAccess</span><span class="sxs-lookup"><span data-stu-id="82de8-103">IPropData::HrSetObjAccess</span></span>

  
  
<span data-ttu-id="82de8-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="82de8-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="82de8-105">Задает уровень доступа для объекта.</span><span class="sxs-lookup"><span data-stu-id="82de8-105">Sets the access level for the object.</span></span>
  
```cpp
HRESULT HrSetObjAccess(
  ULONG ulAccess
);
```

## <a name="parameters"></a><span data-ttu-id="82de8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="82de8-106">Parameters</span></span>

 <span data-ttu-id="82de8-107">_ulAccess_</span><span class="sxs-lookup"><span data-stu-id="82de8-107">_ulAccess_</span></span>
  
> <span data-ttu-id="82de8-108">[in] Битовая маска флаги, задающее уровень доступа объекта.</span><span class="sxs-lookup"><span data-stu-id="82de8-108">[in] A bitmask of flags that specifies the object's access level.</span></span> <span data-ttu-id="82de8-109">Можно установить один из следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="82de8-109">One of the following flags can be set:</span></span>
    
<span data-ttu-id="82de8-110">IPROP_READONLY</span><span class="sxs-lookup"><span data-stu-id="82de8-110">IPROP_READONLY</span></span> 
  
> <span data-ttu-id="82de8-111">Задает объект уровень доступа только для чтения.</span><span class="sxs-lookup"><span data-stu-id="82de8-111">Sets the object's access level to read-only.</span></span> 
    
<span data-ttu-id="82de8-112">IPROP_READWRITE</span><span class="sxs-lookup"><span data-stu-id="82de8-112">IPROP_READWRITE</span></span> 
  
> <span data-ttu-id="82de8-113">Задает объект уровень доступа для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="82de8-113">Sets the object's access level to read/write.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="82de8-114">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="82de8-114">Return value</span></span>

<span data-ttu-id="82de8-115">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="82de8-115">S_OK</span></span> 
  
> <span data-ttu-id="82de8-116">Уровень доступа объекта был успешно установлен.</span><span class="sxs-lookup"><span data-stu-id="82de8-116">The object's access level was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="82de8-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="82de8-117">Remarks</span></span>

<span data-ttu-id="82de8-118">Метод **IPropData::HrSetObjAccess** можно задать уровень доступа для объекта целиком, а не для отдельных свойств.</span><span class="sxs-lookup"><span data-stu-id="82de8-118">The **IPropData::HrSetObjAccess** method sets the access level for an entire object, rather than for individual properties.</span></span> <span data-ttu-id="82de8-119">**HrSetObjAccess** можно использовать для изменения уровня доступа, указанные при создании объекта.</span><span class="sxs-lookup"><span data-stu-id="82de8-119">**HrSetObjAccess** can be used to change the access level established when the object was created.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="82de8-120">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="82de8-120">Notes to callers</span></span>

<span data-ttu-id="82de8-121">Чтобы задать уровень доступа к свойству, вызовите **HrSetObjAccess** с флагом IPROP_READWRITE, задавать в параметре _ulAccess_ , чтобы сделать объект изменяемым.</span><span class="sxs-lookup"><span data-stu-id="82de8-121">To set an access level on a property, first call **HrSetObjAccess** with the IPROP_READWRITE flag set in the  _ulAccess_ parameter to make the object modifiable.</span></span> <span data-ttu-id="82de8-122">Затем вызовите метод [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) , указав свойства конечного объекта в массиве указывает параметр _lpPropTagArray_ .</span><span class="sxs-lookup"><span data-stu-id="82de8-122">Then call the [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) method, specifying the target property in the array pointed to by the  _lpPropTagArray_ parameter.</span></span> 
  
<span data-ttu-id="82de8-123">Чтобы создать объект со свойствами, которые будут доступны только для чтения, чтобы клиенты, создайте объект чтения и записи, добавление необходимых свойств, а затем вызвать **HrSetObjAccess** для изменения объекта доступа только для чтения.</span><span class="sxs-lookup"><span data-stu-id="82de8-123">To create an object with properties that will be read-only to clients, create a read/write object, add the necessary properties, and then call **HrSetObjAccess** to change the object's access to read-only.</span></span> 
  
<span data-ttu-id="82de8-124">Можно также использовать **HrSetObjAccess** чтобы предотвратить создание нового свойства клиентов.</span><span class="sxs-lookup"><span data-stu-id="82de8-124">You can also use **HrSetObjAccess** to prevent clients from creating new properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="82de8-125">См. также</span><span class="sxs-lookup"><span data-stu-id="82de8-125">See also</span></span>



[<span data-ttu-id="82de8-126">IPropData::HrGetPropAccess</span><span class="sxs-lookup"><span data-stu-id="82de8-126">IPropData::HrGetPropAccess</span></span>](ipropdata-hrgetpropaccess.md)
  
[<span data-ttu-id="82de8-127">IPropData::HrSetPropAccess</span><span class="sxs-lookup"><span data-stu-id="82de8-127">IPropData::HrSetPropAccess</span></span>](ipropdata-hrsetpropaccess.md)
  
[<span data-ttu-id="82de8-128">IPropData : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="82de8-128">IPropData : IMAPIProp</span></span>](ipropdataimapiprop.md)

