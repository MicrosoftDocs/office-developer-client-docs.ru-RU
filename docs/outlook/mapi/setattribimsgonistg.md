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
# <a name="setattribimsgonistg"></a><span data-ttu-id="be2b5-103">SetAttribIMsgOnIStg</span><span class="sxs-lookup"><span data-stu-id="be2b5-103">SetAttribIMsgOnIStg</span></span>

  
  
<span data-ttu-id="be2b5-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="be2b5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="be2b5-105">Задает или изменяет атрибуты свойств объекта [iMessage](imessageimapiprop.md) , предоставляемого функцией [опенимсгонистг](openimsgonistg.md) .</span><span class="sxs-lookup"><span data-stu-id="be2b5-105">Sets or alters attributes of properties on an [IMessage](imessageimapiprop.md) object supplied by the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="be2b5-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="be2b5-106">Header file:</span></span>  <br/> |<span data-ttu-id="be2b5-107">IMessage. h</span><span class="sxs-lookup"><span data-stu-id="be2b5-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="be2b5-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="be2b5-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="be2b5-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="be2b5-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="be2b5-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="be2b5-110">Called by:</span></span>  <br/> |<span data-ttu-id="be2b5-111">Клиентские приложения и поставщики хранилищ сообщений</span><span class="sxs-lookup"><span data-stu-id="be2b5-111">Client applications and message store providers</span></span>  <br/> |
   
```cpp
HRESULT SetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTags,
  LPSPropAttrArray lpPropAttrs,
  LPSPropProblemArray FAR * lppPropProblems
);
```

## <a name="parameters"></a><span data-ttu-id="be2b5-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="be2b5-112">Parameters</span></span>

 <span data-ttu-id="be2b5-113">_Лпобжект_</span><span class="sxs-lookup"><span data-stu-id="be2b5-113">_lpObject_</span></span>
  
> <span data-ttu-id="be2b5-114">возврата Указатель на объект, для которого задаются атрибуты свойства.</span><span class="sxs-lookup"><span data-stu-id="be2b5-114">[in] Pointer to the object for which property attributes are being set.</span></span> 
    
 <span data-ttu-id="be2b5-115">_Лппроптагс_</span><span class="sxs-lookup"><span data-stu-id="be2b5-115">_lpPropTags_</span></span>
  
> <span data-ttu-id="be2b5-116">возврата Указатель на структуру [спроптагаррай](sproptagarray.md) , содержащую массив тегов свойств, указывающий свойства, для которых задаются атрибуты свойств.</span><span class="sxs-lookup"><span data-stu-id="be2b5-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure containing an array of property tags indicating the properties for which property attributes are being set.</span></span> 
    
 <span data-ttu-id="be2b5-117">_Лппропаттрс_</span><span class="sxs-lookup"><span data-stu-id="be2b5-117">_lpPropAttrs_</span></span>
  
> <span data-ttu-id="be2b5-118">возврата Указатель на структуру [спропаттраррай](spropattrarray.md) , в которой перечислены атрибуты свойств, которые требуется задать.</span><span class="sxs-lookup"><span data-stu-id="be2b5-118">[in] Pointer to an [SPropAttrArray](spropattrarray.md) structure listing the property attributes to set.</span></span> 
    
 <span data-ttu-id="be2b5-119">_Лпппроппроблемс_</span><span class="sxs-lookup"><span data-stu-id="be2b5-119">_lppPropProblems_</span></span>
  
> <span data-ttu-id="be2b5-120">вышли Указатель на возвращаемую структуру [спроппроблемаррай](spropproblemarray.md) , содержащую набор проблем свойств.</span><span class="sxs-lookup"><span data-stu-id="be2b5-120">[out] Pointer to the returned [SPropProblemArray](spropproblemarray.md) structure containing a set of property problems.</span></span> <span data-ttu-id="be2b5-121">Эта структура определяет проблемы, которые возникают, если **сетаттрибимсгонистг** удалось задать некоторые свойства, но не все.</span><span class="sxs-lookup"><span data-stu-id="be2b5-121">This structure identifies problems encountered if **SetAttribIMsgOnIStg** has been able to set some properties, but not all.</span></span> <span data-ttu-id="be2b5-122">Если в параметре _лпппроппроблемс_ передается указатель на значение null, то массив проблем свойств не возвращается, даже если не заданы некоторые свойства.</span><span class="sxs-lookup"><span data-stu-id="be2b5-122">If a pointer to NULL is passed in the  _lppPropProblems_ parameter, no property problem array is returned even if some properties were not set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="be2b5-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="be2b5-123">Return value</span></span>

<span data-ttu-id="be2b5-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="be2b5-124">S_OK</span></span> 
  
> <span data-ttu-id="be2b5-125">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="be2b5-125">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="be2b5-126">МАПИ_В_ЕРРОРС_РЕТУРНЕД</span><span class="sxs-lookup"><span data-stu-id="be2b5-126">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="be2b5-127">Вызов выполнен в целом, но не удалось получить доступ к одному или нескольким свойствам и они возвращались с типом свойства ПТ_ЕРРОР.</span><span class="sxs-lookup"><span data-stu-id="be2b5-127">The call succeeded overall, but one or more properties could not be accessed and were returned with a property type of PT_ERROR.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="be2b5-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="be2b5-128">Remarks</span></span>

<span data-ttu-id="be2b5-129">Доступ к атрибутам свойств возможен только для объектов Property, то есть объектов, реализующих интерфейс [IMAPIProp: IUnknown](imapipropiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="be2b5-129">Property attributes can only be accessed on property objects, that is, objects implementing the [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span></span> <span data-ttu-id="be2b5-130">Чтобы сделать свойства MAPI доступными в объекте структурированного хранилища OLE, [опенимсгонистг](openimsgonistg.md) создает объект [iMessage: IMAPIProp](imessageimapiprop.md) в начале объекта OLE **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="be2b5-130">To make MAPI properties available on an OLE structured storage object, [OpenIMsgOnIStg](openimsgonistg.md) builds an [IMessage : IMAPIProp](imessageimapiprop.md) object on top of the OLE **IStorage** object.</span></span> <span data-ttu-id="be2b5-131">Атрибуты свойств таких объектов можно задавать или изменять с помощью **сетаттрибимсгонистг** и извлекаются с помощью [жетаттрибимсгонистг](getattribimsgonistg.md).</span><span class="sxs-lookup"><span data-stu-id="be2b5-131">The property attributes on such objects can be set or altered with **SetAttribIMsgOnIStg** and retrieved with [GetAttribIMsgOnIStg](getattribimsgonistg.md).</span></span> 
  
 <span data-ttu-id="be2b5-132">**Note (Примечание** ) **Жетаттрибимсгонистг** и **сетаттрибимсгонистг** не работают со всеми объектами **iMessage** .</span><span class="sxs-lookup"><span data-stu-id="be2b5-132">**Note** **GetAttribIMsgOnIStg** and **SetAttribIMsgOnIStg** do not operate on all **IMessage** objects.</span></span> <span data-ttu-id="be2b5-133">Они действительны только для объектов **iMessage**— On — **IStorage** , возвращаемых методом **опенимсгонистг**.</span><span class="sxs-lookup"><span data-stu-id="be2b5-133">They are only valid for **IMessage**-on- **IStorage** objects returned by **OpenIMsgOnIStg**.</span></span> 
  
<span data-ttu-id="be2b5-134">В параметре _лппропаттрс_ число и положение атрибутов должны быть соответствующими количеству и положению тегов свойств, переданных в параметре _лппроптагс_ .</span><span class="sxs-lookup"><span data-stu-id="be2b5-134">In the  _lpPropAttrs_ parameter, the number and position of the attributes must match the number and position of the property tags passed in the  _lpPropTags_ parameter.</span></span> 
  
<span data-ttu-id="be2b5-135">Функция **сетаттрибимсгонистг** используется, чтобы сделать свойства сообщения доступными только для чтения, если это требуется для схемы **iMessage** .</span><span class="sxs-lookup"><span data-stu-id="be2b5-135">The **SetAttribIMsgOnIStg** function is used to make message properties read-only when required by the **IMessage** schema.</span></span> <span data-ttu-id="be2b5-136">Для этой цели в качестве примера используется поставщик хранилища сообщений.</span><span class="sxs-lookup"><span data-stu-id="be2b5-136">The sample message store provider uses it for this purpose.</span></span> <span data-ttu-id="be2b5-137">Более подробную информацию можно [](mapi-messages.md)узнать в статье messages.</span><span class="sxs-lookup"><span data-stu-id="be2b5-137">For more information, see [Messages](mapi-messages.md).</span></span> 
  

