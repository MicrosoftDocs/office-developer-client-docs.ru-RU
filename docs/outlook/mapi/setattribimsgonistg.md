---
title: SetAttribIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SetAttribIMsgOnIStg
api_type:
- COM
ms.assetid: 683d0d00-1b93-445d-86ff-180a3e6d2323
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 852ce31ba5ab02ff8f05dee25c9b32acb73130ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428832"
---
# <a name="setattribimsgonistg"></a><span data-ttu-id="fa2d3-103">SetAttribIMsgOnIStg</span><span class="sxs-lookup"><span data-stu-id="fa2d3-103">SetAttribIMsgOnIStg</span></span>

  
  
<span data-ttu-id="fa2d3-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa2d3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa2d3-105">Задает или изменяет атрибуты свойств объекта [IMessage,](imessageimapiprop.md) предоставленного функцией [OpenIMsgOnIStg.](openimsgonistg.md)</span><span class="sxs-lookup"><span data-stu-id="fa2d3-105">Sets or alters attributes of properties on an [IMessage](imessageimapiprop.md) object supplied by the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fa2d3-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="fa2d3-106">Header file:</span></span>  <br/> |<span data-ttu-id="fa2d3-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="fa2d3-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="fa2d3-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="fa2d3-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="fa2d3-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="fa2d3-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="fa2d3-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="fa2d3-110">Called by:</span></span>  <br/> |<span data-ttu-id="fa2d3-111">Клиентские приложения и поставщики store сообщений</span><span class="sxs-lookup"><span data-stu-id="fa2d3-111">Client applications and message store providers</span></span>  <br/> |
   
```cpp
HRESULT SetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTags,
  LPSPropAttrArray lpPropAttrs,
  LPSPropProblemArray FAR * lppPropProblems
);
```

## <a name="parameters"></a><span data-ttu-id="fa2d3-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="fa2d3-112">Parameters</span></span>

 <span data-ttu-id="fa2d3-113">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="fa2d3-113">_lpObject_</span></span>
  
> <span data-ttu-id="fa2d3-114">[in] Указатель на объект, для которого устанавливаются атрибуты свойства.</span><span class="sxs-lookup"><span data-stu-id="fa2d3-114">[in] Pointer to the object for which property attributes are being set.</span></span> 
    
 <span data-ttu-id="fa2d3-115">_lpPropTags_</span><span class="sxs-lookup"><span data-stu-id="fa2d3-115">_lpPropTags_</span></span>
  
> <span data-ttu-id="fa2d3-116">[in] Указатель на структуру [SPropTagArray,](sproptagarray.md) содержащую массив тегов свойств, указывающих свойства, для которых устанавливаются атрибуты свойства.</span><span class="sxs-lookup"><span data-stu-id="fa2d3-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure containing an array of property tags indicating the properties for which property attributes are being set.</span></span> 
    
 <span data-ttu-id="fa2d3-117">_lpPropAttrs_</span><span class="sxs-lookup"><span data-stu-id="fa2d3-117">_lpPropAttrs_</span></span>
  
> <span data-ttu-id="fa2d3-118">[in] Указатель на [структуру SPropAttrArray](spropattrarray.md) со списком атрибутов свойств, которые необходимо установить.</span><span class="sxs-lookup"><span data-stu-id="fa2d3-118">[in] Pointer to an [SPropAttrArray](spropattrarray.md) structure listing the property attributes to set.</span></span> 
    
 <span data-ttu-id="fa2d3-119">_lppPropProblems_</span><span class="sxs-lookup"><span data-stu-id="fa2d3-119">_lppPropProblems_</span></span>
  
> <span data-ttu-id="fa2d3-120">[out] Указатель на возвращенную [структуру SPropProblemArray,](spropproblemarray.md) содержащую набор проблем со свойствами.</span><span class="sxs-lookup"><span data-stu-id="fa2d3-120">[out] Pointer to the returned [SPropProblemArray](spropproblemarray.md) structure containing a set of property problems.</span></span> <span data-ttu-id="fa2d3-121">Эта структура определяет проблемы, которые возникают, если **setAttribIMsgOnIStg** удалось установить некоторые свойства, но не все.</span><span class="sxs-lookup"><span data-stu-id="fa2d3-121">This structure identifies problems encountered if **SetAttribIMsgOnIStg** has been able to set some properties, but not all.</span></span> <span data-ttu-id="fa2d3-122">Если указатель на NULL передается в  _параметре lppPropProblems,_ массив проблем свойств не возвращается, даже если некоторые свойства не заданы.</span><span class="sxs-lookup"><span data-stu-id="fa2d3-122">If a pointer to NULL is passed in the  _lppPropProblems_ parameter, no property problem array is returned even if some properties were not set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="fa2d3-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fa2d3-123">Return value</span></span>

<span data-ttu-id="fa2d3-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="fa2d3-124">S_OK</span></span> 
  
> <span data-ttu-id="fa2d3-125">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="fa2d3-125">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="fa2d3-126">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="fa2d3-126">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="fa2d3-127">Вызов в целом был успешным, но не удалось получить доступ к одному или более свойствам, и он был возвращен с типом свойства PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="fa2d3-127">The call succeeded overall, but one or more properties could not be accessed and were returned with a property type of PT_ERROR.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fa2d3-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="fa2d3-128">Remarks</span></span>

<span data-ttu-id="fa2d3-129">Доступ к атрибутам свойств можно получить только для объектов свойств, то есть объектов, реализующих [интерфейс IMAPIProp : IUnknown.](imapipropiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="fa2d3-129">Property attributes can only be accessed on property objects, that is, objects implementing the [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span></span> <span data-ttu-id="fa2d3-130">Чтобы сделать свойства MAPI доступными для объекта OLE структурированного хранилища, [OpenIMsgOnIStg](openimsgonistg.md) создает объект [IMessage : IMAPIProp](imessageimapiprop.md) поверх объекта OLE **IStorage.**</span><span class="sxs-lookup"><span data-stu-id="fa2d3-130">To make MAPI properties available on an OLE structured storage object, [OpenIMsgOnIStg](openimsgonistg.md) builds an [IMessage : IMAPIProp](imessageimapiprop.md) object on top of the OLE **IStorage** object.</span></span> <span data-ttu-id="fa2d3-131">Атрибуты свойств для таких объектов можно установить или изменить с помощью **SetAttribIMsgOnIStg** и получить с помощью [GetAttribIMsgOnIStg.](getattribimsgonistg.md)</span><span class="sxs-lookup"><span data-stu-id="fa2d3-131">The property attributes on such objects can be set or altered with **SetAttribIMsgOnIStg** and retrieved with [GetAttribIMsgOnIStg](getattribimsgonistg.md).</span></span> 
  
 <span data-ttu-id="fa2d3-132">**Обратите** внимание, что **getAttribIMsgOnIStg** и **SetAttribIMsgOnIStg** работают не на всех **объектах IMessage.**</span><span class="sxs-lookup"><span data-stu-id="fa2d3-132">**Note** **GetAttribIMsgOnIStg** and **SetAttribIMsgOnIStg** do not operate on all **IMessage** objects.</span></span> <span data-ttu-id="fa2d3-133">Они действительны только для **объектов IMessage**-on-IStorage, возвращенных **OpenIMsgOnIStg.** </span><span class="sxs-lookup"><span data-stu-id="fa2d3-133">They are only valid for **IMessage**-on- **IStorage** objects returned by **OpenIMsgOnIStg**.</span></span> 
  
<span data-ttu-id="fa2d3-134">В параметре _lpPropAttrs_ число и положение атрибутов должны совпадать с числом и положением тегов свойств, переданных в _параметре lpPropTags._</span><span class="sxs-lookup"><span data-stu-id="fa2d3-134">In the  _lpPropAttrs_ parameter, the number and position of the attributes must match the number and position of the property tags passed in the  _lpPropTags_ parameter.</span></span> 
  
<span data-ttu-id="fa2d3-135">Функция **SetAttribIMsgOnIStg** используется для того, чтобы свойства сообщений были только для чтения, если этого требует схема **IMessage.**</span><span class="sxs-lookup"><span data-stu-id="fa2d3-135">The **SetAttribIMsgOnIStg** function is used to make message properties read-only when required by the **IMessage** schema.</span></span> <span data-ttu-id="fa2d3-136">Для этой цели используется пример поставщика store сообщений.</span><span class="sxs-lookup"><span data-stu-id="fa2d3-136">The sample message store provider uses it for this purpose.</span></span> <span data-ttu-id="fa2d3-137">Дополнительные сведения см. [в сообщении.](mapi-messages.md)</span><span class="sxs-lookup"><span data-stu-id="fa2d3-137">For more information, see [Messages](mapi-messages.md).</span></span> 
  

