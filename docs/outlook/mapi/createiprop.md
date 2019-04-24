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
ms.openlocfilehash: e318d7a709a09e67ebf423db0263985523d2fc28
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32333035"
---
# <a name="createiprop"></a><span data-ttu-id="4cea6-103">CreateIProp</span><span class="sxs-lookup"><span data-stu-id="4cea6-103">CreateIProp</span></span>

  
  
<span data-ttu-id="4cea6-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4cea6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4cea6-105">Создает объект данных свойства, то есть объект [ипропдата](ipropdataimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="4cea6-105">Creates a property data object, that is, an [IPropData](ipropdataimapiprop.md) object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4cea6-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="4cea6-106">Header file:</span></span>  <br/> |<span data-ttu-id="4cea6-107">Мапиутил. h</span><span class="sxs-lookup"><span data-stu-id="4cea6-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="4cea6-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="4cea6-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="4cea6-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="4cea6-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="4cea6-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="4cea6-110">Called by:</span></span>  <br/> |<span data-ttu-id="4cea6-111">Клиентские приложения и поставщики услуг</span><span class="sxs-lookup"><span data-stu-id="4cea6-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="4cea6-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="4cea6-112">Parameters</span></span>

 <span data-ttu-id="4cea6-113">_Лпинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="4cea6-113">_lpInterface_</span></span>
  
> <span data-ttu-id="4cea6-114">возврата Указатель на идентификатор интерфейса (IID) для объекта данных свойства.</span><span class="sxs-lookup"><span data-stu-id="4cea6-114">[in] Pointer to an interface identifier (IID) for the property data object.</span></span> <span data-ttu-id="4cea6-115">Допустимый идентификатор интерфейса — Иид_имапипропдата.</span><span class="sxs-lookup"><span data-stu-id="4cea6-115">The valid interface identifier is IID_IMAPIPropData.</span></span> <span data-ttu-id="4cea6-116">При передаче значения NULL в параметре _лпинтерфаце_ объект данных свойства, возвращаемый в параметре _лпппропдата_ , будет приведен к стандартному интерфейсу для объекта данных свойства.</span><span class="sxs-lookup"><span data-stu-id="4cea6-116">Passing NULL in the  _lpInterface_ parameter also causes the property data object returned in the  _lppPropData_ parameter to be cast to the standard interface for a property data object.</span></span> 
    
 <span data-ttu-id="4cea6-117">_Лпаллокатебуффер_</span><span class="sxs-lookup"><span data-stu-id="4cea6-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="4cea6-118">возврата Указатель на функцию [мапиаллокатебуффер](mapiallocatebuffer.md) , которая будет использоваться для выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="4cea6-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="4cea6-119">_Лпаллокатеморе_</span><span class="sxs-lookup"><span data-stu-id="4cea6-119">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="4cea6-120">возврата Указатель на функцию [мапиаллокатеморе](mapiallocatemore.md) , которая будет использоваться для выделения дополнительной памяти.</span><span class="sxs-lookup"><span data-stu-id="4cea6-120">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="4cea6-121">_Лпфрибуффер_</span><span class="sxs-lookup"><span data-stu-id="4cea6-121">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="4cea6-122">возврата Указатель на функцию [мапифрибуффер](mapifreebuffer.md) , который будет использоваться для освобождения памяти.</span><span class="sxs-lookup"><span data-stu-id="4cea6-122">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="4cea6-123">_Лпвресервед_</span><span class="sxs-lookup"><span data-stu-id="4cea6-123">_lpvReserved_</span></span>
  
> <span data-ttu-id="4cea6-124">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="4cea6-124">[in] Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="4cea6-125">_Лпппропдата_</span><span class="sxs-lookup"><span data-stu-id="4cea6-125">_lppPropData_</span></span>
  
> <span data-ttu-id="4cea6-126">вышли Указатель на указатель на объект данных возвращаемого свойства.</span><span class="sxs-lookup"><span data-stu-id="4cea6-126">[out] Pointer to a pointer to the returned property data object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4cea6-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4cea6-127">Return value</span></span>

<span data-ttu-id="4cea6-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="4cea6-128">S_OK</span></span> 
  
> <span data-ttu-id="4cea6-129">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="4cea6-129">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="4cea6-130">МАПИ_Е_ИНТЕРФАЦЕ_НОТ_СУППОРТЕД</span><span class="sxs-lookup"><span data-stu-id="4cea6-130">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="4cea6-131">Запрошенный интерфейс не поддерживается для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="4cea6-131">The requested interface is not supported for this object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4cea6-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4cea6-132">Remarks</span></span>

<span data-ttu-id="4cea6-133">Входные параметры _лпаллокатебуффер_, _лпаллокатеморе_и _Лпфрибуффер_ заменяют функции [мапиаллокатебуффер](mapiallocatebuffer.md), [мапиаллокатеморе](mapiallocatemore.md)и [MAPIFreeBuffer](mapifreebuffer.md) соответственно.</span><span class="sxs-lookup"><span data-stu-id="4cea6-133">The  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ input parameters point to the [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) functions, respectively.</span></span> <span data-ttu-id="4cea6-134">Клиентское приложение, вызывающее **креатеипроп** , передает указатели на функции MAPI только с именем; поставщик услуг передает указатели на эти функции, которые она получала при вызове инициализации, или извлекаются с помощью вызова метода [имаписуппорт:: жетмемаллокраутинес](imapisupport-getmemallocroutines.md) .</span><span class="sxs-lookup"><span data-stu-id="4cea6-134">A client application calling **CreateIProp** passes in pointers to the MAPI functions just named; a service provider passes the pointers to these functions it received in its initialization call or retrieved with a call to the [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) method.</span></span> 
  

