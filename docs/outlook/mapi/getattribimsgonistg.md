---
title: GetAttribIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.GetAttribIMsgOnIStg
api_type:
- COM
ms.assetid: bb27b28a-b2bd-4d4a-b0bb-0692f3de8e16
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9e17e8ef7df33ffa248eec4195c00c77d0c49f94
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587770"
---
# <a name="getattribimsgonistg"></a><span data-ttu-id="6c94d-103">GetAttribIMsgOnIStg</span><span class="sxs-lookup"><span data-stu-id="6c94d-103">GetAttribIMsgOnIStg</span></span>

  
  
<span data-ttu-id="6c94d-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c94d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c94d-105">Извлекает атрибуты свойств в объект [IMessage](imessageimapiprop.md) функцию [OpenIMsgOnIStg](openimsgonistg.md) .</span><span class="sxs-lookup"><span data-stu-id="6c94d-105">Retrieves attributes of properties on an [IMessage](imessageimapiprop.md) object supplied by the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6c94d-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="6c94d-106">Header file:</span></span>  <br/> |<span data-ttu-id="6c94d-107">IMessage.h</span><span class="sxs-lookup"><span data-stu-id="6c94d-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="6c94d-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="6c94d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="6c94d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="6c94d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="6c94d-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="6c94d-110">Called by:</span></span>  <br/> |<span data-ttu-id="6c94d-111">Поставщики удаленного хранилища клиентских приложений и сообщения</span><span class="sxs-lookup"><span data-stu-id="6c94d-111">Client applications and message store providers</span></span>  <br/> |
   
```cpp
HRESULT GetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTagArray,
  LPSPropAttrArray FAR * lppPropAttrArray
);
```

## <a name="parameters"></a><span data-ttu-id="6c94d-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="6c94d-112">Parameters</span></span>

 <span data-ttu-id="6c94d-113">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="6c94d-113">_lpObject_</span></span>
  
> <span data-ttu-id="6c94d-114">[in] Указатель на объект **IMessage** , полученный из функции [OpenIMsgOnIStg](openimsgonistg.md) .</span><span class="sxs-lookup"><span data-stu-id="6c94d-114">[in] Pointer to an **IMessage** object obtained from the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
    
 <span data-ttu-id="6c94d-115">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="6c94d-115">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="6c94d-116">[in] Указатель на структуру [SPropTagArray](sproptagarray.md) , который содержит массив свойств, для которых должны получить атрибуты тегов свойств.</span><span class="sxs-lookup"><span data-stu-id="6c94d-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags indicating the properties for which attributes are to be retrieved.</span></span> 
    
 <span data-ttu-id="6c94d-117">_lppPropAttrArray_</span><span class="sxs-lookup"><span data-stu-id="6c94d-117">_lppPropAttrArray_</span></span>
  
> <span data-ttu-id="6c94d-118">[out] Указатель на указатель на структуру возвращенные [SPropAttrArray](spropattrarray.md) , который содержит атрибуты, извлеченное свойство.</span><span class="sxs-lookup"><span data-stu-id="6c94d-118">[out] Pointer to a pointer to the returned [SPropAttrArray](spropattrarray.md) structure that contains the retrieved property attributes.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6c94d-119">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="6c94d-119">Return value</span></span>

<span data-ttu-id="6c94d-120">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="6c94d-120">S_OK</span></span> 
  
> <span data-ttu-id="6c94d-121">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="6c94d-121">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="6c94d-122">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="6c94d-122">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="6c94d-123">Вызов завершился успешно в целом, но одно или несколько свойств не удается получить доступ к и были возвращены с типом свойства PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="6c94d-123">The call succeeded overall, but one or more properties could not be accessed and were returned with a property type of PT_ERROR.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6c94d-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="6c94d-124">Remarks</span></span>

<span data-ttu-id="6c94d-125">Свойство атрибуты осуществляется только на свойство объекты, то есть, реализация [IMAPIProp: IUnknown](imapipropiunknown.md) интерфейса.</span><span class="sxs-lookup"><span data-stu-id="6c94d-125">Property attributes can only be accessed on property objects, that is, objects implementing the [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span></span> <span data-ttu-id="6c94d-126">Чтобы сделать свойства MAPI на объект структурированного хранилища OLE, обеспечивающая [OpenIMsgOnIStg](openimsgonistg.md) [IMessage: IMAPIProp](imessageimapiprop.md) объекта поверх объекта OLE **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="6c94d-126">To make MAPI properties available on an OLE structured storage object, [OpenIMsgOnIStg](openimsgonistg.md) builds an [IMessage : IMAPIProp](imessageimapiprop.md) object on top of the OLE **IStorage** object.</span></span> <span data-ttu-id="6c94d-127">Атрибуты свойств для таких объектов можно задать или изменены с помощью [SetAttribIMsgOnIStg](setattribimsgonistg.md) и получены с **GetAttribIMsgOnIStg**.</span><span class="sxs-lookup"><span data-stu-id="6c94d-127">The property attributes on such objects can be set or altered with [SetAttribIMsgOnIStg](setattribimsgonistg.md) and retrieved with **GetAttribIMsgOnIStg**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6c94d-128">**GetAttribIMsgOnIStg** и **SetAttribIMsgOnIStg** работают на все объекты **IMessage** .</span><span class="sxs-lookup"><span data-stu-id="6c94d-128">**GetAttribIMsgOnIStg** and **SetAttribIMsgOnIStg** do not operate on all **IMessage** objects.</span></span> <span data-ttu-id="6c94d-129">Они действительны только для **IMessage**- on - **IStorage** объекты, возвращаемые **OpenIMsgOnIStg**.</span><span class="sxs-lookup"><span data-stu-id="6c94d-129">They are only valid for **IMessage**-on- **IStorage** objects returned by **OpenIMsgOnIStg**.</span></span> 
  
<span data-ttu-id="6c94d-130">Количество и положения атрибуты с помощью параметра _lppPropAttrArray_ соответствуют номер и положения тегов свойств с помощью параметра _lpPropTagArray_ .</span><span class="sxs-lookup"><span data-stu-id="6c94d-130">The number and positions of the attributes in the  _lppPropAttrArray_ parameter correspond to the number and positions of the property tags in the  _lpPropTagArray_ parameter.</span></span> 
  

