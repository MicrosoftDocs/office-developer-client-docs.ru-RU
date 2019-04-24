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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300471"
---
# <a name="getattribimsgonistg"></a><span data-ttu-id="0145f-103">GetAttribIMsgOnIStg</span><span class="sxs-lookup"><span data-stu-id="0145f-103">GetAttribIMsgOnIStg</span></span>

  
  
<span data-ttu-id="0145f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0145f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0145f-105">Получает атрибуты свойств объекта [iMessage](imessageimapiprop.md) , предоставляемого функцией [опенимсгонистг](openimsgonistg.md) .</span><span class="sxs-lookup"><span data-stu-id="0145f-105">Retrieves attributes of properties on an [IMessage](imessageimapiprop.md) object supplied by the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0145f-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="0145f-106">Header file:</span></span>  <br/> |<span data-ttu-id="0145f-107">IMessage. h</span><span class="sxs-lookup"><span data-stu-id="0145f-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="0145f-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="0145f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0145f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0145f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0145f-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="0145f-110">Called by:</span></span>  <br/> |<span data-ttu-id="0145f-111">Клиентские приложения и поставщики хранилищ сообщений</span><span class="sxs-lookup"><span data-stu-id="0145f-111">Client applications and message store providers</span></span>  <br/> |
   
```cpp
HRESULT GetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTagArray,
  LPSPropAttrArray FAR * lppPropAttrArray
);
```

## <a name="parameters"></a><span data-ttu-id="0145f-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="0145f-112">Parameters</span></span>

 <span data-ttu-id="0145f-113">_Лпобжект_</span><span class="sxs-lookup"><span data-stu-id="0145f-113">_lpObject_</span></span>
  
> <span data-ttu-id="0145f-114">возврата Указатель на объект **iMessage** , полученный из функции [опенимсгонистг](openimsgonistg.md) .</span><span class="sxs-lookup"><span data-stu-id="0145f-114">[in] Pointer to an **IMessage** object obtained from the [OpenIMsgOnIStg](openimsgonistg.md) function.</span></span> 
    
 <span data-ttu-id="0145f-115">_Лппроптагаррай_</span><span class="sxs-lookup"><span data-stu-id="0145f-115">_lpPropTagArray_</span></span>
  
> <span data-ttu-id="0145f-116">возврата Указатель на структуру [спроптагаррай](sproptagarray.md) , содержащую массив тегов свойств, указывающий свойства, для которых необходимо извлечь атрибуты.</span><span class="sxs-lookup"><span data-stu-id="0145f-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags indicating the properties for which attributes are to be retrieved.</span></span> 
    
 <span data-ttu-id="0145f-117">_Лпппропаттраррай_</span><span class="sxs-lookup"><span data-stu-id="0145f-117">_lppPropAttrArray_</span></span>
  
> <span data-ttu-id="0145f-118">вышли Указатель на указатель на возвращенную структуру [спропаттраррай](spropattrarray.md) , содержащую атрибуты извлеченных свойств.</span><span class="sxs-lookup"><span data-stu-id="0145f-118">[out] Pointer to a pointer to the returned [SPropAttrArray](spropattrarray.md) structure that contains the retrieved property attributes.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0145f-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0145f-119">Return value</span></span>

<span data-ttu-id="0145f-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="0145f-120">S_OK</span></span> 
  
> <span data-ttu-id="0145f-121">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="0145f-121">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="0145f-122">МАПИ_В_ЕРРОРС_РЕТУРНЕД</span><span class="sxs-lookup"><span data-stu-id="0145f-122">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="0145f-123">Вызов выполнен в целом, но не удалось получить доступ к одному или нескольким свойствам и они возвращались с типом свойства ПТ_ЕРРОР.</span><span class="sxs-lookup"><span data-stu-id="0145f-123">The call succeeded overall, but one or more properties could not be accessed and were returned with a property type of PT_ERROR.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0145f-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="0145f-124">Remarks</span></span>

<span data-ttu-id="0145f-125">Доступ к атрибутам свойств возможен только для объектов Property, то есть объектов, реализующих интерфейс [IMAPIProp: IUnknown](imapipropiunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="0145f-125">Property attributes can only be accessed on property objects, that is, objects implementing the [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span></span> <span data-ttu-id="0145f-126">Чтобы сделать свойства MAPI доступными в объекте структурированного хранилища OLE, [опенимсгонистг](openimsgonistg.md) создает объект [iMessage: IMAPIProp](imessageimapiprop.md) в начале объекта OLE **IStorage** .</span><span class="sxs-lookup"><span data-stu-id="0145f-126">To make MAPI properties available on an OLE structured storage object, [OpenIMsgOnIStg](openimsgonistg.md) builds an [IMessage : IMAPIProp](imessageimapiprop.md) object on top of the OLE **IStorage** object.</span></span> <span data-ttu-id="0145f-127">Атрибуты свойств таких объектов можно задавать или изменять с помощью [сетаттрибимсгонистг](setattribimsgonistg.md) и извлекаются с помощью **жетаттрибимсгонистг**.</span><span class="sxs-lookup"><span data-stu-id="0145f-127">The property attributes on such objects can be set or altered with [SetAttribIMsgOnIStg](setattribimsgonistg.md) and retrieved with **GetAttribIMsgOnIStg**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="0145f-128">**Жетаттрибимсгонистг** и **сетаттрибимсгонистг** не работают со всеми объектами **iMessage** .</span><span class="sxs-lookup"><span data-stu-id="0145f-128">**GetAttribIMsgOnIStg** and **SetAttribIMsgOnIStg** do not operate on all **IMessage** objects.</span></span> <span data-ttu-id="0145f-129">Они действительны только для объектов **iMessage**— On — **IStorage** , возвращаемых методом **опенимсгонистг**.</span><span class="sxs-lookup"><span data-stu-id="0145f-129">They are only valid for **IMessage**-on- **IStorage** objects returned by **OpenIMsgOnIStg**.</span></span> 
  
<span data-ttu-id="0145f-130">Число и позиции атрибутов в параметре _лпппропаттраррай_ соответствуют числу и положениям тегов свойств в параметре _лппроптагаррай_ .</span><span class="sxs-lookup"><span data-stu-id="0145f-130">The number and positions of the attributes in the  _lppPropAttrArray_ parameter correspond to the number and positions of the property tags in the  _lpPropTagArray_ parameter.</span></span> 
  

