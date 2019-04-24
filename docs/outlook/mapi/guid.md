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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299519"
---
# <a name="guid"></a><span data-ttu-id="9a5de-103">GUID</span><span class="sxs-lookup"><span data-stu-id="9a5de-103">GUID</span></span>

  
  
<span data-ttu-id="9a5de-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9a5de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9a5de-105">Описывает глобальный уникальный идентификатор (GUID).</span><span class="sxs-lookup"><span data-stu-id="9a5de-105">Describes a globally unique identifier (GUID).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9a5de-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="9a5de-106">Header file:</span></span>  <br/> |<span data-ttu-id="9a5de-107">Мапигуид. h</span><span class="sxs-lookup"><span data-stu-id="9a5de-107">Mapiguid.h</span></span>  <br/> |
   
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a><span data-ttu-id="9a5de-108">Members</span><span class="sxs-lookup"><span data-stu-id="9a5de-108">Members</span></span>

 <span data-ttu-id="9a5de-109">**Data1**</span><span class="sxs-lookup"><span data-stu-id="9a5de-109">**Data1**</span></span>
  
> <span data-ttu-id="9a5de-110">Длинное целое значение данных без знака.</span><span class="sxs-lookup"><span data-stu-id="9a5de-110">An unsigned long integer data value.</span></span>
    
 <span data-ttu-id="9a5de-111">**Data2**</span><span class="sxs-lookup"><span data-stu-id="9a5de-111">**Data2**</span></span>
  
> <span data-ttu-id="9a5de-112">Неподписанное короткое целое значение данных.</span><span class="sxs-lookup"><span data-stu-id="9a5de-112">An unsigned short integer data value.</span></span>
    
 <span data-ttu-id="9a5de-113">**Data3**</span><span class="sxs-lookup"><span data-stu-id="9a5de-113">**Data3**</span></span>
  
> <span data-ttu-id="9a5de-114">Неподписанное короткое целое значение данных.</span><span class="sxs-lookup"><span data-stu-id="9a5de-114">An unsigned short integer data value.</span></span>
    
 <span data-ttu-id="9a5de-115">**Data4**</span><span class="sxs-lookup"><span data-stu-id="9a5de-115">**Data4**</span></span>
  
> <span data-ttu-id="9a5de-116">Массив неподписанных символов.</span><span class="sxs-lookup"><span data-stu-id="9a5de-116">An array of unsigned characters.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9a5de-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="9a5de-117">Remarks</span></span>

 <span data-ttu-id="9a5de-118">Структуры **GUID** используются в MAPI следующим образом:</span><span class="sxs-lookup"><span data-stu-id="9a5de-118">**GUID** structures are used in MAPI as follows:</span></span> 
  
- <span data-ttu-id="9a5de-119">В структурах [мапиуид](mapiuid.md) , которые однозначно идентифицируют поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="9a5de-119">In the [MAPIUID](mapiuid.md) structures that uniquely identify service providers.</span></span> 
    
- <span data-ttu-id="9a5de-120">Для идентификаторов интерфейса.</span><span class="sxs-lookup"><span data-stu-id="9a5de-120">For interface identifiers.</span></span>
    
- <span data-ttu-id="9a5de-121">В поле Имя набора свойств именованных свойств.</span><span class="sxs-lookup"><span data-stu-id="9a5de-121">In the property set names of named properties.</span></span> 
    
<span data-ttu-id="9a5de-122">Поставщики хранилищ сообщений и адресных книг создают структуру **GUID** для использования в структуре **мапиуид** .</span><span class="sxs-lookup"><span data-stu-id="9a5de-122">Message store and address book providers generate a **GUID** structure to use in their **MAPIUID** structure.</span></span> <span data-ttu-id="9a5de-123">Передав полученный **мапиуид** в [Имаписуппорт:: сетпровидеруид](imapisupport-setprovideruid.md), эти поставщики услуг информируют MAPI об их уникальном идентификаторе.</span><span class="sxs-lookup"><span data-stu-id="9a5de-123">By passing the resulting **MAPIUID** to [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md), these service providers inform MAPI of their unique identifier.</span></span>
  
<span data-ttu-id="9a5de-124">Кроме того, они используются в реализации Microsoft Remote Procedure Call (RPC) и языка описания объектов (ODL).</span><span class="sxs-lookup"><span data-stu-id="9a5de-124">Also, they are used in the implementation of Microsoft Remote Procedure Call (RPC) and the Object Description Language (ODL).</span></span> <span data-ttu-id="9a5de-125">Для получения дополнительных сведений об этих возможностях ознакомьтесь с *руководством программиста по программированИю Microsoft RPC*, справочником по *OLE для программиста* , а также *в OLE*, *втором* выпуске.</span><span class="sxs-lookup"><span data-stu-id="9a5de-125">For more information about these uses, see the  *Microsoft RPC Programmer's Guide and Reference*, *OLE Programmer's Reference*  ,and  *Inside OLE*, *Second Edition*  .</span></span> 
  
<span data-ttu-id="9a5de-126">Структура **GUID** определена в справочнике *программиста Win32* .</span><span class="sxs-lookup"><span data-stu-id="9a5de-126">The **GUID** structure is defined in the  *Win32 Programmer's Reference*  .</span></span> <span data-ttu-id="9a5de-127">Конкретные значения для структур **GUID** , используемых в MAPI, определяются в файле заГоловков MAPI мапигуид. h.</span><span class="sxs-lookup"><span data-stu-id="9a5de-127">Specific values for **GUID** structures that are used within MAPI are defined in the MAPI header file Mapiguid.h.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9a5de-128">См. также</span><span class="sxs-lookup"><span data-stu-id="9a5de-128">See also</span></span>



[<span data-ttu-id="9a5de-129">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="9a5de-129">MAPIUID</span></span>](mapiuid.md)


[<span data-ttu-id="9a5de-130">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="9a5de-130">MAPI Structures</span></span>](mapi-structures.md)

