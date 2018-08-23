---
title: CreateIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CreateIProp
api_type:
- COM
ms.assetid: 9bf68814-2564-433d-b762-3d2c83ca3c60
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8d6eb011e65ad44f4183eb5821697dcf2508032c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566882"
---
# <a name="createiprop"></a><span data-ttu-id="b8251-103">CreateIProp</span><span class="sxs-lookup"><span data-stu-id="b8251-103">CreateIProp</span></span>

  
  
<span data-ttu-id="b8251-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b8251-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b8251-105">Создает объект данных свойств, то есть, объект [IPropData](ipropdataimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="b8251-105">Creates a property data object, that is, an [IPropData](ipropdataimapiprop.md) object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b8251-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="b8251-106">Header file:</span></span>  <br/> |<span data-ttu-id="b8251-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="b8251-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="b8251-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="b8251-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b8251-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b8251-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b8251-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="b8251-110">Called by:</span></span>  <br/> |<span data-ttu-id="b8251-111">Клиентские приложения и поставщиков услуг</span><span class="sxs-lookup"><span data-stu-id="b8251-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE CreateIProp(
  LPCIID lpInterface,
  ALLOCATEBUFFER FAR * lpAllocateBuffer,
  ALLOCATEMORE FAR * lpAllocateMore,
  FREEBUFFER FAR * lpFreeBuffer,
  LPVOID lpvReserved,
  LPPROPDATA FAR * lppPropData
);
```

## <a name="parameters"></a><span data-ttu-id="b8251-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="b8251-112">Parameters</span></span>

 <span data-ttu-id="b8251-113">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="b8251-113">_lpInterface_</span></span>
  
> <span data-ttu-id="b8251-114">[in] Указатель на идентификатор интерфейса (ИД интерфейса) для объекта данных свойства.</span><span class="sxs-lookup"><span data-stu-id="b8251-114">[in] Pointer to an interface identifier (IID) for the property data object.</span></span> <span data-ttu-id="b8251-115">Допустимый идентификатор является IID_IMAPIPropData.</span><span class="sxs-lookup"><span data-stu-id="b8251-115">The valid interface identifier is IID_IMAPIPropData.</span></span> <span data-ttu-id="b8251-116">Указать значение NULL для параметра _lpInterface_ вызывает объект данных свойств, возвращенный с помощью параметра _lppPropData_ приведения стандартный интерфейс для объекта данных свойства.</span><span class="sxs-lookup"><span data-stu-id="b8251-116">Passing NULL in the  _lpInterface_ parameter also causes the property data object returned in the  _lppPropData_ parameter to be cast to the standard interface for a property data object.</span></span> 
    
 <span data-ttu-id="b8251-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="b8251-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="b8251-118">[in] Указатель на функцию [MAPIAllocateBuffer](mapiallocatebuffer.md) , которые будут использоваться для выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="b8251-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="b8251-119">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="b8251-119">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="b8251-120">[in] Указатель на функцию [MAPIAllocateMore](mapiallocatemore.md) , которые будут использоваться для выделения дополнительной памяти.</span><span class="sxs-lookup"><span data-stu-id="b8251-120">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="b8251-121">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="b8251-121">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="b8251-122">[in] Указатель на функцию [MAPIFreeBuffer](mapifreebuffer.md) , которые будут использоваться для свободного использования памяти.</span><span class="sxs-lookup"><span data-stu-id="b8251-122">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="b8251-123">_lpvReserved_</span><span class="sxs-lookup"><span data-stu-id="b8251-123">_lpvReserved_</span></span>
  
> <span data-ttu-id="b8251-124">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="b8251-124">[in] Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="b8251-125">_lppPropData_</span><span class="sxs-lookup"><span data-stu-id="b8251-125">_lppPropData_</span></span>
  
> <span data-ttu-id="b8251-126">[out] Указатель на указатель на объект данных возвращаемого свойства.</span><span class="sxs-lookup"><span data-stu-id="b8251-126">[out] Pointer to a pointer to the returned property data object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b8251-127">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="b8251-127">Return value</span></span>

<span data-ttu-id="b8251-128">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="b8251-128">S_OK</span></span> 
  
> <span data-ttu-id="b8251-129">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="b8251-129">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="b8251-130">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="b8251-130">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="b8251-131">Запрошенный интерфейс не поддерживается для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="b8251-131">The requested interface is not supported for this object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b8251-132">Замечания</span><span class="sxs-lookup"><span data-stu-id="b8251-132">Remarks</span></span>

<span data-ttu-id="b8251-133">Входные параметры _lpAllocateBuffer_, _lpAllocateMore_и _lpFreeBuffer_ пункты функции [MAPIFreeBuffer](mapifreebuffer.md) , [MAPIAllocateMore](mapiallocatemore.md)и [MAPIAllocateBuffer](mapiallocatebuffer.md)соответственно.</span><span class="sxs-lookup"><span data-stu-id="b8251-133">The  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ input parameters point to the [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) functions, respectively.</span></span> <span data-ttu-id="b8251-134">Клиентское приложение вызов **CreateIProp** передается в указатели функции MAPI только с именем; Поставщик службы передает указатели эти функции его полученным в его вызовы инициализации и получить с помощью вызова метода [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) .</span><span class="sxs-lookup"><span data-stu-id="b8251-134">A client application calling **CreateIProp** passes in pointers to the MAPI functions just named; a service provider passes the pointers to these functions it received in its initialization call or retrieved with a call to the [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) method.</span></span> 
  

