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
ms.openlocfilehash: e8a0daa2afe2397f39b7f37a31ef718ba65a3350
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812267"
---
# <a name="setattribimsgonistg"></a><span data-ttu-id="1ebad-103">SetAttribIMsgOnIStg</span><span class="sxs-lookup"><span data-stu-id="1ebad-103">SetAttribIMsgOnIStg</span></span>

  
  
<span data-ttu-id="1ebad-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1ebad-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1ebad-105">Задает или изменяет атрибуты свойств в объект [IMessage](imessageimapiprop.md) функцию [OpenIMsgOnIStg](openimsgonistg.md) .</span><span class="sxs-lookup"><span data-stu-id="1ebad-105">Sets or alters attributes of properties on an [IMessage](imessageimapiprop.md) object supplied by the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1ebad-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="1ebad-106">Header file:</span></span>  <br/> |<span data-ttu-id="1ebad-107">IMessage.h</span><span class="sxs-lookup"><span data-stu-id="1ebad-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="1ebad-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="1ebad-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1ebad-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1ebad-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1ebad-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="1ebad-110">Called by:</span></span>  <br/> |<span data-ttu-id="1ebad-111">Поставщики удаленного хранилища клиентских приложений и сообщения</span><span class="sxs-lookup"><span data-stu-id="1ebad-111">Client applications and message store providers</span></span>  <br/> |
   
```cpp
HRESULT SetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTags,
  LPSPropAttrArray lpPropAttrs,
  LPSPropProblemArray FAR * lppPropProblems
);
```

## <a name="parameters"></a><span data-ttu-id="1ebad-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="1ebad-112">Parameters</span></span>

 <span data-ttu-id="1ebad-113">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="1ebad-113">_lpObject_</span></span>
  
> <span data-ttu-id="1ebad-114">[in] Указатель на объект, для которых свойство задаются атрибуты.</span><span class="sxs-lookup"><span data-stu-id="1ebad-114">[in] Pointer to the object for which property attributes are being set.</span></span> 
    
 <span data-ttu-id="1ebad-115">_lpPropTags_</span><span class="sxs-lookup"><span data-stu-id="1ebad-115">_lpPropTags_</span></span>
  
> <span data-ttu-id="1ebad-116">[in] Указатель на структуру [SPropTagArray](sproptagarray.md) , содержащий массив теги свойство, определяющее, какие свойства задаются атрибуты свойства.</span><span class="sxs-lookup"><span data-stu-id="1ebad-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure containing an array of property tags indicating the properties for which property attributes are being set.</span></span> 
    
 <span data-ttu-id="1ebad-117">_lpPropAttrs_</span><span class="sxs-lookup"><span data-stu-id="1ebad-117">_lpPropAttrs_</span></span>
  
> <span data-ttu-id="1ebad-118">[in] Указатель на структуру [SPropAttrArray](spropattrarray.md) атрибуты свойства для установки списков.</span><span class="sxs-lookup"><span data-stu-id="1ebad-118">[in] Pointer to an [SPropAttrArray](spropattrarray.md) structure listing the property attributes to set.</span></span> 
    
 <span data-ttu-id="1ebad-119">_lppPropProblems_</span><span class="sxs-lookup"><span data-stu-id="1ebad-119">_lppPropProblems_</span></span>
  
> <span data-ttu-id="1ebad-120">[out] Указатель на структуру [SPropProblemArray](spropproblemarray.md) возвращенные, содержащий набор свойств проблем.</span><span class="sxs-lookup"><span data-stu-id="1ebad-120">[out] Pointer to the returned [SPropProblemArray](spropproblemarray.md) structure containing a set of property problems.</span></span> <span data-ttu-id="1ebad-121">Эта структура определяет проблем, возникающих при **SetAttribIMsgOnIStg** была возможность установить некоторые свойства, но не все.</span><span class="sxs-lookup"><span data-stu-id="1ebad-121">This structure identifies problems encountered if **SetAttribIMsgOnIStg** has been able to set some properties, but not all.</span></span> <span data-ttu-id="1ebad-122">Если в параметре _lppPropProblems_ передается указатель на значение NULL, массив проблема не свойство возвращается даже в том случае, если не заданы некоторые свойства.</span><span class="sxs-lookup"><span data-stu-id="1ebad-122">If a pointer to NULL is passed in the  _lppPropProblems_ parameter, no property problem array is returned even if some properties were not set.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1ebad-123">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="1ebad-123">Return value</span></span>

<span data-ttu-id="1ebad-124">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="1ebad-124">S_OK</span></span> 
  
> <span data-ttu-id="1ebad-125">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="1ebad-125">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="1ebad-126">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="1ebad-126">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="1ebad-127">Вызов завершился успешно в целом, но одно или несколько свойств не удается получить доступ к и были возвращены с типом свойства PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="1ebad-127">The call succeeded overall, but one or more properties could not be accessed and were returned with a property type of PT_ERROR.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1ebad-128">Замечания</span><span class="sxs-lookup"><span data-stu-id="1ebad-128">Remarks</span></span>

<span data-ttu-id="1ebad-129">Свойство атрибуты осуществляется только на свойство объекты, то есть, реализация [IMAPIProp: IUnknown](imapipropiunknown.md) интерфейса.</span><span class="sxs-lookup"><span data-stu-id="1ebad-129">Property attributes can only be accessed on property objects, that is, objects implementing the [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span></span> <span data-ttu-id="1ebad-130">Чтобы сделать свойства MAPI на объект структурированного хранилища OLE, обеспечивающая [OpenIMsgOnIStg](openimsgonistg.md) [IMessage: IMAPIProp](imessageimapiprop.md) объекта поверх объекта OLE **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="1ebad-130">To make MAPI properties available on an OLE structured storage object, [OpenIMsgOnIStg](openimsgonistg.md) builds an [IMessage : IMAPIProp](imessageimapiprop.md) object on top of the OLE **IStorage** object.</span></span> <span data-ttu-id="1ebad-131">Атрибуты свойств для таких объектов можно задать или изменены с помощью **SetAttribIMsgOnIStg** и получены с [GetAttribIMsgOnIStg](getattribimsgonistg.md).</span><span class="sxs-lookup"><span data-stu-id="1ebad-131">The property attributes on such objects can be set or altered with **SetAttribIMsgOnIStg** and retrieved with [GetAttribIMsgOnIStg](getattribimsgonistg.md).</span></span> 
  
 <span data-ttu-id="1ebad-132">**Примечание** **GetAttribIMsgOnIStg** и **SetAttribIMsgOnIStg** работают на все объекты **IMessage** .</span><span class="sxs-lookup"><span data-stu-id="1ebad-132">**Note** **GetAttribIMsgOnIStg** and **SetAttribIMsgOnIStg** do not operate on all **IMessage** objects.</span></span> <span data-ttu-id="1ebad-133">Они действительны только для **IMessage**- on - **IStorage** объекты, возвращаемые **OpenIMsgOnIStg**.</span><span class="sxs-lookup"><span data-stu-id="1ebad-133">They are only valid for **IMessage**-on- **IStorage** objects returned by **OpenIMsgOnIStg**.</span></span> 
  
<span data-ttu-id="1ebad-134">В параметре _lpPropAttrs_ номер и положение атрибутов должны соответствовать номер и положение тегов свойств, переданной в параметре _lpPropTags_ .</span><span class="sxs-lookup"><span data-stu-id="1ebad-134">In the  _lpPropAttrs_ parameter, the number and position of the attributes must match the number and position of the property tags passed in the  _lpPropTags_ parameter.</span></span> 
  
<span data-ttu-id="1ebad-135">Функция **SetAttribIMsgOnIStg** используется для сделать свойства сообщений доступно только для чтения, при необходимости в схеме **IMessage** .</span><span class="sxs-lookup"><span data-stu-id="1ebad-135">The **SetAttribIMsgOnIStg** function is used to make message properties read-only when required by the **IMessage** schema.</span></span> <span data-ttu-id="1ebad-136">Пример поставщика хранилища сообщений использует его для этой цели.</span><span class="sxs-lookup"><span data-stu-id="1ebad-136">The sample message store provider uses it for this purpose.</span></span> <span data-ttu-id="1ebad-137">[Дополнительные сведения см.](mapi-messages.md)</span><span class="sxs-lookup"><span data-stu-id="1ebad-137">For more information, see [Messages](mapi-messages.md).</span></span> 
  

