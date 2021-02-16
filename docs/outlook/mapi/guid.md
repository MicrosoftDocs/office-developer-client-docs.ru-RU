---
title: GUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.GUID
api_type:
- COM
ms.assetid: e3608c47-06be-4476-a6ef-060fac252387
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 12c50ab5936d7fffd364c276ba07ca69d3459ae7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421587"
---
# <a name="guid"></a><span data-ttu-id="6c477-103">GUID</span><span class="sxs-lookup"><span data-stu-id="6c477-103">GUID</span></span>

  
  
<span data-ttu-id="6c477-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6c477-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6c477-105">Описывает глобальный уникальный идентификатор (GUID).</span><span class="sxs-lookup"><span data-stu-id="6c477-105">Describes a globally unique identifier (GUID).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6c477-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="6c477-106">Header file:</span></span>  <br/> |<span data-ttu-id="6c477-107">Mapiguid.h</span><span class="sxs-lookup"><span data-stu-id="6c477-107">Mapiguid.h</span></span>  <br/> |
   
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a><span data-ttu-id="6c477-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="6c477-108">Members</span></span>

 <span data-ttu-id="6c477-109">**Data1**</span><span class="sxs-lookup"><span data-stu-id="6c477-109">**Data1**</span></span>
  
> <span data-ttu-id="6c477-110">Неподписаное длинное значение данных.</span><span class="sxs-lookup"><span data-stu-id="6c477-110">An unsigned long integer data value.</span></span>
    
 <span data-ttu-id="6c477-111">**Data2**</span><span class="sxs-lookup"><span data-stu-id="6c477-111">**Data2**</span></span>
  
> <span data-ttu-id="6c477-112">Неподписано короткое значение данных.</span><span class="sxs-lookup"><span data-stu-id="6c477-112">An unsigned short integer data value.</span></span>
    
 <span data-ttu-id="6c477-113">**Data3**</span><span class="sxs-lookup"><span data-stu-id="6c477-113">**Data3**</span></span>
  
> <span data-ttu-id="6c477-114">Неподписано короткое значение данных.</span><span class="sxs-lookup"><span data-stu-id="6c477-114">An unsigned short integer data value.</span></span>
    
 <span data-ttu-id="6c477-115">**Data4**</span><span class="sxs-lookup"><span data-stu-id="6c477-115">**Data4**</span></span>
  
> <span data-ttu-id="6c477-116">Массив неподписаных символов.</span><span class="sxs-lookup"><span data-stu-id="6c477-116">An array of unsigned characters.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6c477-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="6c477-117">Remarks</span></span>

 <span data-ttu-id="6c477-118">**Структуры GUID** используются в MAPI следующим образом:</span><span class="sxs-lookup"><span data-stu-id="6c477-118">**GUID** structures are used in MAPI as follows:</span></span> 
  
- <span data-ttu-id="6c477-119">В [структурах MAPIUID,](mapiuid.md) которые однозначно определяют поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="6c477-119">In the [MAPIUID](mapiuid.md) structures that uniquely identify service providers.</span></span> 
    
- <span data-ttu-id="6c477-120">Для идентификаторов интерфейса.</span><span class="sxs-lookup"><span data-stu-id="6c477-120">For interface identifiers.</span></span>
    
- <span data-ttu-id="6c477-121">В наборе свойств имена именуемого свойства.</span><span class="sxs-lookup"><span data-stu-id="6c477-121">In the property set names of named properties.</span></span> 
    
<span data-ttu-id="6c477-122">Поставщики хранения сообщений и адресных книг создают структуру **GUID** для использования в своей структуре **MAPIUID.**</span><span class="sxs-lookup"><span data-stu-id="6c477-122">Message store and address book providers generate a **GUID** structure to use in their **MAPIUID** structure.</span></span> <span data-ttu-id="6c477-123">Передав итоговые **данные MAPIUID** в [IMAPISupport::SetProviderUID,](imapisupport-setprovideruid.md)эти поставщики услуг сообщают MAPI о своем уникальном идентификаторе.</span><span class="sxs-lookup"><span data-stu-id="6c477-123">By passing the resulting **MAPIUID** to [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md), these service providers inform MAPI of their unique identifier.</span></span>
  
<span data-ttu-id="6c477-124">Кроме того, они используются в реализации удаленного вызова процедур (RPC) Майкрософт и языка описания объектов (ODL).</span><span class="sxs-lookup"><span data-stu-id="6c477-124">Also, they are used in the implementation of Microsoft Remote Procedure Call (RPC) and the Object Description Language (ODL).</span></span> <span data-ttu-id="6c477-125">Дополнительные сведения об этих вариантах использования см. в руководстве и справочнике по microsoft *RPC Programmer,* справочнике *по OLE Programmer* и *inside OLE*, *Second Edition.*</span><span class="sxs-lookup"><span data-stu-id="6c477-125">For more information about these uses, see the  *Microsoft RPC Programmer's Guide and Reference*, *OLE Programmer's Reference*  ,and  *Inside OLE*, *Second Edition*  .</span></span> 
  
<span data-ttu-id="6c477-126">Структура **GUID** определена в справочнике *win32 Programmer..*</span><span class="sxs-lookup"><span data-stu-id="6c477-126">The **GUID** structure is defined in the  *Win32 Programmer's Reference*  .</span></span> <span data-ttu-id="6c477-127">Определенные значения для структур **GUID,** используемых в MAPI, определяются в файле загона MAPI Mapiguid.h.</span><span class="sxs-lookup"><span data-stu-id="6c477-127">Specific values for **GUID** structures that are used within MAPI are defined in the MAPI header file Mapiguid.h.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6c477-128">См. также</span><span class="sxs-lookup"><span data-stu-id="6c477-128">See also</span></span>



[<span data-ttu-id="6c477-129">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="6c477-129">MAPIUID</span></span>](mapiuid.md)


[<span data-ttu-id="6c477-130">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="6c477-130">MAPI Structures</span></span>](mapi-structures.md)

