---
title: SMAPIVerb
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SMAPIVerb
api_type:
- COM
ms.assetid: 45066528-2447-4178-aaa3-7513ed0b3ba4
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3ef284a2c036abb9eac10ecf33de4adbf61f3c54
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410961"
---
# <a name="smapiverb"></a><span data-ttu-id="e8f77-103">SMAPIVerb</span><span class="sxs-lookup"><span data-stu-id="e8f77-103">SMAPIVerb</span></span>

  
  
<span data-ttu-id="e8f77-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e8f77-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e8f77-105">Описывает команду MAPI.</span><span class="sxs-lookup"><span data-stu-id="e8f77-105">Describes a MAPI verb.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e8f77-106">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="e8f77-106">Header file:</span></span>  <br/> |<span data-ttu-id="e8f77-107">Мапиформ. h</span><span class="sxs-lookup"><span data-stu-id="e8f77-107">Mapiform.h</span></span>  <br/> |
   
```cpp
typedef struct
{
  ULONG lVerb;
  LPSTR szVerbname;
  DWORD fuFlags;
  DWORD grfAttribs;
  ULONG ulFlags; /* Either 0 or MAPI_UNICODE */
} SMAPIVerb, FAR * LPMAPIVERB;

```

## <a name="members"></a><span data-ttu-id="e8f77-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="e8f77-108">Members</span></span>

 <span data-ttu-id="e8f77-109">**лверб**</span><span class="sxs-lookup"><span data-stu-id="e8f77-109">**lVerb**</span></span>
  
> <span data-ttu-id="e8f77-110">Код, представляющий команду, которая передается в [имапиформ::D оверб](imapiform-doverb.md).</span><span class="sxs-lookup"><span data-stu-id="e8f77-110">Code representing the verb that is passed to [IMAPIForm::DoVerb](imapiform-doverb.md).</span></span> <span data-ttu-id="e8f77-111">Стандартные команды определяются в файле заголовка Ексчформ. h.</span><span class="sxs-lookup"><span data-stu-id="e8f77-111">Standard verbs are defined in the header file Exchform.h.</span></span>
    
 <span data-ttu-id="e8f77-112">**сзвербнаме**</span><span class="sxs-lookup"><span data-stu-id="e8f77-112">**szVerbname**</span></span>
  
> <span data-ttu-id="e8f77-113">Отображаемое имя команды в том виде, в котором оно отображается в меню формы.</span><span class="sxs-lookup"><span data-stu-id="e8f77-113">Display name of the verb as it appears on the form menu.</span></span>
    
 <span data-ttu-id="e8f77-114">**фуфлагс**</span><span class="sxs-lookup"><span data-stu-id="e8f77-114">**fuFlags**</span></span>
  
> <span data-ttu-id="e8f77-115">Флаги для команды.</span><span class="sxs-lookup"><span data-stu-id="e8f77-115">Flags for the verb.</span></span>
    
 <span data-ttu-id="e8f77-116">**грфаттрибс**</span><span class="sxs-lookup"><span data-stu-id="e8f77-116">**grfAttribs**</span></span>
  
> <span data-ttu-id="e8f77-117">Атрибуты команды.</span><span class="sxs-lookup"><span data-stu-id="e8f77-117">Attributes of the verb.</span></span> 
    
 <span data-ttu-id="e8f77-118">**ulFlags**</span><span class="sxs-lookup"><span data-stu-id="e8f77-118">**ulFlags**</span></span>
  
> <span data-ttu-id="e8f77-119">Флаг, указывающий формат отображаемого имени команды.</span><span class="sxs-lookup"><span data-stu-id="e8f77-119">Flag indicating the format of the verb's display name.</span></span> <span data-ttu-id="e8f77-120">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="e8f77-120">The following flag can be set:</span></span>
    
<span data-ttu-id="e8f77-121">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e8f77-121">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="e8f77-122">Отображаемое имя в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="e8f77-122">The display name is in Unicode format.</span></span> <span data-ttu-id="e8f77-123">Если флаг MAPI_UNICODE не установлен, отображаемое имя отображается в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="e8f77-123">If the MAPI_UNICODE flag is not set, the display name is in ANSI format.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e8f77-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="e8f77-124">Remarks</span></span>

<span data-ttu-id="e8f77-125">Структура **смапиверб** передается в качестве параметра в следующих методах:</span><span class="sxs-lookup"><span data-stu-id="e8f77-125">The **SMAPIVerb** structure is passed as a parameter in the following methods:</span></span> 
  
- [<span data-ttu-id="e8f77-126">IMAPIFormContainer::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="e8f77-126">IMAPIFormContainer::ResolveMultipleMessageClasses</span></span>](imapiformcontainer-resolvemultiplemessageclasses.md)
    
- [<span data-ttu-id="e8f77-127">IMAPIFormMgr::ResolveMultipleMessageClasses</span><span class="sxs-lookup"><span data-stu-id="e8f77-127">IMAPIFormMgr::ResolveMultipleMessageClasses</span></span>](imapiformmgr-resolvemultiplemessageclasses.md)
    
## <a name="see-also"></a><span data-ttu-id="e8f77-128">См. также</span><span class="sxs-lookup"><span data-stu-id="e8f77-128">See also</span></span>



[<span data-ttu-id="e8f77-129">CbMessageClassArray</span><span class="sxs-lookup"><span data-stu-id="e8f77-129">CbMessageClassArray</span></span>](cbmessageclassarray.md)


[<span data-ttu-id="e8f77-130">Структуры MAPI</span><span class="sxs-lookup"><span data-stu-id="e8f77-130">MAPI Structures</span></span>](mapi-structures.md)

