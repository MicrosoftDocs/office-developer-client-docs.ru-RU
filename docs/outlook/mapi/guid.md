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
ms.openlocfilehash: 94bafdf0ca84fa31a7df2f022265d5d5d1a99a37
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577697"
---
# <a name="guid"></a><span data-ttu-id="1ee09-103">GUID</span><span class="sxs-lookup"><span data-stu-id="1ee09-103">GUID</span></span>

  
  
<span data-ttu-id="1ee09-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1ee09-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1ee09-105">Описывает глобальный уникальный идентификатор (GUID).</span><span class="sxs-lookup"><span data-stu-id="1ee09-105">Describes a globally unique identifier (GUID).</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1ee09-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="1ee09-106">Header file:</span></span>  <br/> |<span data-ttu-id="1ee09-107">Mapiguid.h</span><span class="sxs-lookup"><span data-stu-id="1ee09-107">Mapiguid.h</span></span>  <br/> |
   
```cpp
typedef struct _GUID
{
  unsigned long Data1;
  unsigned short Data2;
  unsigned short Data3;
  unsigned char Data4[8];
} GUID;

```

## <a name="members"></a><span data-ttu-id="1ee09-108">Members</span><span class="sxs-lookup"><span data-stu-id="1ee09-108">Members</span></span>

 <span data-ttu-id="1ee09-109">**Бд1**</span><span class="sxs-lookup"><span data-stu-id="1ee09-109">**Data1**</span></span>
  
> <span data-ttu-id="1ee09-110">Длинное целое значение данных.</span><span class="sxs-lookup"><span data-stu-id="1ee09-110">An unsigned long integer data value.</span></span>
    
 <span data-ttu-id="1ee09-111">**Бд2**</span><span class="sxs-lookup"><span data-stu-id="1ee09-111">**Data2**</span></span>
  
> <span data-ttu-id="1ee09-112">Целое число без знака короткий данных.</span><span class="sxs-lookup"><span data-stu-id="1ee09-112">An unsigned short integer data value.</span></span>
    
 <span data-ttu-id="1ee09-113">**Data3**</span><span class="sxs-lookup"><span data-stu-id="1ee09-113">**Data3**</span></span>
  
> <span data-ttu-id="1ee09-114">Целое число без знака короткий данных.</span><span class="sxs-lookup"><span data-stu-id="1ee09-114">An unsigned short integer data value.</span></span>
    
 <span data-ttu-id="1ee09-115">**Data4 при**</span><span class="sxs-lookup"><span data-stu-id="1ee09-115">**Data4**</span></span>
  
> <span data-ttu-id="1ee09-116">Массив неподписанных символов.</span><span class="sxs-lookup"><span data-stu-id="1ee09-116">An array of unsigned characters.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1ee09-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="1ee09-117">Remarks</span></span>

 <span data-ttu-id="1ee09-118">**Идентификатор GUID** структуры используются в MAPI следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1ee09-118">**GUID** structures are used in MAPI as follows:</span></span> 
  
- <span data-ttu-id="1ee09-119">В структуре [MAPIUID](mapiuid.md) , которые однозначно идентифицируют поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="1ee09-119">In the [MAPIUID](mapiuid.md) structures that uniquely identify service providers.</span></span> 
    
- <span data-ttu-id="1ee09-120">Для идентификаторов интерфейса.</span><span class="sxs-lookup"><span data-stu-id="1ee09-120">For interface identifiers.</span></span>
    
- <span data-ttu-id="1ee09-121">В свойстве задайте имена именованных свойств.</span><span class="sxs-lookup"><span data-stu-id="1ee09-121">In the property set names of named properties.</span></span> 
    
<span data-ttu-id="1ee09-122">Хранение сообщений и адресной книги поставщиков создания структуры **идентификатор GUID** для использования в их **MAPIUID** структуры.</span><span class="sxs-lookup"><span data-stu-id="1ee09-122">Message store and address book providers generate a **GUID** structure to use in their **MAPIUID** structure.</span></span> <span data-ttu-id="1ee09-123">Путем передачи итоговый **MAPIUID** [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md), поставщики услуг Проинформируйте MAPI их уникальный идентификатор.</span><span class="sxs-lookup"><span data-stu-id="1ee09-123">By passing the resulting **MAPIUID** to [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md), these service providers inform MAPI of their unique identifier.</span></span>
  
<span data-ttu-id="1ee09-124">Кроме того они используются в реализации Microsoft удаленного вызова процедур (RPC) и язык описания объектов (ODL).</span><span class="sxs-lookup"><span data-stu-id="1ee09-124">Also, they are used in the implementation of Microsoft Remote Procedure Call (RPC) and the Object Description Language (ODL).</span></span> <span data-ttu-id="1ee09-125">Дополнительные сведения об этих использует иллюстрация *Руководство программиста Microsoft RPC и ссылка*, *OLE Справочник программиста* и *Внутри OLE*, *Второе издание* .</span><span class="sxs-lookup"><span data-stu-id="1ee09-125">For more information about these uses, see the  *Microsoft RPC Programmer's Guide and Reference*, *OLE Programmer's Reference*  ,and  *Inside OLE*, *Second Edition*  .</span></span> 
  
<span data-ttu-id="1ee09-126">Структура **GUID** определяется в *Справочник программиста Win32* .</span><span class="sxs-lookup"><span data-stu-id="1ee09-126">The **GUID** structure is defined in the  *Win32 Programmer's Reference*  .</span></span> <span data-ttu-id="1ee09-127">Определенные значения **GUID** структуры, используемые в рамках MAPI определяются в файле заголовка MAPI Mapiguid.h.</span><span class="sxs-lookup"><span data-stu-id="1ee09-127">Specific values for **GUID** structures that are used within MAPI are defined in the MAPI header file Mapiguid.h.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1ee09-128">См. также</span><span class="sxs-lookup"><span data-stu-id="1ee09-128">See also</span></span>



[<span data-ttu-id="1ee09-129">MAPIUID</span><span class="sxs-lookup"><span data-stu-id="1ee09-129">MAPIUID</span></span>](mapiuid.md)


[<span data-ttu-id="1ee09-130">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="1ee09-130">MAPI Structures</span></span>](mapi-structures.md)

