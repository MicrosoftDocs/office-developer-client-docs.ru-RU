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
ms.openlocfilehash: 16e85eabc067bd82f5fb89c917afaf2831c75673
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439998"
---
# <a name="getattribimsgonistg"></a><span data-ttu-id="04b66-103">GetAttribIMsgOnIStg</span><span class="sxs-lookup"><span data-stu-id="04b66-103">GetAttribIMsgOnIStg</span></span>

  
  
<span data-ttu-id="04b66-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="04b66-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="04b66-105">Извлекает атрибуты свойств объекта [IMessage,](imessageimapiprop.md) предоставленного функцией [OpenIMsgOnIStg.](openimsgonistg.md)</span><span class="sxs-lookup"><span data-stu-id="04b66-105">Retrieves attributes of properties on an [IMessage](imessageimapiprop.md) object supplied by the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="04b66-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="04b66-106">Header file:</span></span>  <br/> |<span data-ttu-id="04b66-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="04b66-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="04b66-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="04b66-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="04b66-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="04b66-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="04b66-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="04b66-110">Called by:</span></span>  <br/> |<span data-ttu-id="04b66-111">Клиентские приложения и поставщики магазинов сообщений</span><span class="sxs-lookup"><span data-stu-id="04b66-111">Client applications and message store providers</span></span>  <br/> |
   
```cpp
HRESULT GetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTagArray,
  LPSPropAttrArray FAR * lppPropAttrArray
);
```

## <a name="parameters"></a><span data-ttu-id="04b66-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="04b66-112">Parameters</span></span>

 <span data-ttu-id="04b66-113">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="04b66-113">_lpObject_</span></span>
  
> <span data-ttu-id="04b66-114">[in] Указатель на **объект IMessage,** полученный из [функции OpenIMsgOnIStg.](openimsgonistg.md)</span><span class="sxs-lookup"><span data-stu-id="04b66-114">[in] Pointer to an **IMessage** object obtained from the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
    
 <span data-ttu-id="04b66-115">_lpPropTagArray_</span><span class="sxs-lookup"><span data-stu-id="04b66-115">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="04b66-116">[in] Указатель на [структуру SPropTagArray,](sproptagarray.md) содержащий массив тегов свойств, указывающих свойства, для которых необходимо получить атрибуты.</span><span class="sxs-lookup"><span data-stu-id="04b66-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags indicating the properties for which attributes are to be retrieved.</span></span> 
    
 <span data-ttu-id="04b66-117">_lppPropAttrArray_</span><span class="sxs-lookup"><span data-stu-id="04b66-117">_lppPropAttrArray_</span></span>
  
> <span data-ttu-id="04b66-118">[вышел] Указатель на указатель на возвращенную [структуру SPropAttrArray,](spropattrarray.md) которая содержит извлеченные атрибуты свойства.</span><span class="sxs-lookup"><span data-stu-id="04b66-118">[out] Pointer to a pointer to the returned [SPropAttrArray](spropattrarray.md) structure that contains the retrieved property attributes.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="04b66-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="04b66-119">Return value</span></span>

<span data-ttu-id="04b66-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="04b66-120">S_OK</span></span> 
  
> <span data-ttu-id="04b66-121">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="04b66-121">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="04b66-122">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="04b66-122">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="04b66-123">Вызов удался в целом, но один или несколько свойств не удалось получить доступ и были возвращены с типом свойства PT_ERROR.</span><span class="sxs-lookup"><span data-stu-id="04b66-123">The call succeeded overall, but one or more properties could not be accessed and were returned with a property type of PT_ERROR.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="04b66-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="04b66-124">Remarks</span></span>

<span data-ttu-id="04b66-125">Атрибуты свойств можно получить только для объектов свойств, то есть объектов, реализующих [интерфейс IMAPIProp : IUnknown.](imapipropiunknown.md)</span><span class="sxs-lookup"><span data-stu-id="04b66-125">Property attributes can only be accessed on property objects, that is, objects implementing the [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span></span> <span data-ttu-id="04b66-126">Чтобы сделать свойства MAPI доступными для структурированного объекта хранения OLE, [OpenIMsgOnIStg](openimsgonistg.md) создает [объект IMessage : IMAPIProp](imessageimapiprop.md) поверх объекта **IStorage** OLE.</span><span class="sxs-lookup"><span data-stu-id="04b66-126">To make MAPI properties available on an OLE structured storage object, [OpenIMsgOnIStg](openimsgonistg.md) builds an [IMessage : IMAPIProp](imessageimapiprop.md) object on top of the OLE **IStorage** object.</span></span> <span data-ttu-id="04b66-127">Атрибуты свойств таких объектов можно установить или изменить с [помощью SetAttribIMsgOnIStg](setattribimsgonistg.md) и получить с **помощью GetAttribIMsgOnIStg**.</span><span class="sxs-lookup"><span data-stu-id="04b66-127">The property attributes on such objects can be set or altered with [SetAttribIMsgOnIStg](setattribimsgonistg.md) and retrieved with **GetAttribIMsgOnIStg**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="04b66-128">**GetAttribIMsgOnIStg** и **SetAttribIMsgOnIStg** не работают на всех **объектах IMessage.**</span><span class="sxs-lookup"><span data-stu-id="04b66-128">**GetAttribIMsgOnIStg** and **SetAttribIMsgOnIStg** do not operate on all **IMessage** objects.</span></span> <span data-ttu-id="04b66-129">Они действительны только для объектов IMessage-on-IStorage, возвращенных **OpenIMsgOnIStg.**  </span><span class="sxs-lookup"><span data-stu-id="04b66-129">They are only valid for **IMessage**-on- **IStorage** objects returned by **OpenIMsgOnIStg**.</span></span> 
  
<span data-ttu-id="04b66-130">Количество и позиции атрибутов в параметре _lppPropAttrArray_ соответствуют числу и расположению тегов свойств в параметре _lpPropTagArray._</span><span class="sxs-lookup"><span data-stu-id="04b66-130">The number and positions of the attributes in the  _lppPropAttrArray_ parameter correspond to the number and positions of the property tags in the  _lpPropTagArray_ parameter.</span></span> 
  

