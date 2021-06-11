---
title: ISocialSessionFindPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a86cb847-5d49-44b8-b2bc-0e35e70395b4
description: Получает строку, представляюную одного или несколько лиц, которые соответствуют параметру userID.
ms.openlocfilehash: 1aa6478126e509c8d707d6a8d11b2c8428177bbd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434797"
---
# <a name="isocialsessionfindperson"></a><span data-ttu-id="64548-103">ISocialSession::FindPerson</span><span class="sxs-lookup"><span data-stu-id="64548-103">ISocialSession::FindPerson</span></span>

<span data-ttu-id="64548-104">Получает строку, представляюную одного или несколько лиц, которые соответствуют _параметру userID._</span><span class="sxs-lookup"><span data-stu-id="64548-104">Gets a string that represents one or more persons who match the  _userID_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall FindPerson([in] BSTR userId, [out, retval] BSTR* result);
```

## <a name="parameters"></a><span data-ttu-id="64548-105">Parameters</span><span class="sxs-lookup"><span data-stu-id="64548-105">Parameters</span></span>

<span data-ttu-id="64548-106">_userId_</span><span class="sxs-lookup"><span data-stu-id="64548-106">_userId_</span></span>
  
> <span data-ttu-id="64548-107">[in] ID пользователя социальной сети, SMTP-адрес или отображение имени пользователя.</span><span class="sxs-lookup"><span data-stu-id="64548-107">[in] A social network user ID, SMTP address, or display name of a person.</span></span>
    
<span data-ttu-id="64548-108">_result_</span><span class="sxs-lookup"><span data-stu-id="64548-108">_result_</span></span>
  
> <span data-ttu-id="64548-109">[вышел] Строка XML, которая представляет одного или несколько лиц, которые соответствуют данным идентификации, указанным _параметром userId._</span><span class="sxs-lookup"><span data-stu-id="64548-109">[out] An XML string that represents one or more persons who match the identification information specified by the  _userId_ parameter.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="64548-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="64548-110">Remarks</span></span>

<span data-ttu-id="64548-111">Если один или несколько лиц соответствуют запросу **FindPerson,** этот метод возвращает сведения для этих лиц в _параметре результат._</span><span class="sxs-lookup"><span data-stu-id="64548-111">If one or more persons match the **FindPerson** request, this method returns the information for those persons in the  _result_ parameter.</span></span> <span data-ttu-id="64548-112">_Строка_ XML должна соответствовать определению схемы для друзей, как определено в схеме для Outlook поставщика социальных соединителем (OSC). </span><span class="sxs-lookup"><span data-stu-id="64548-112">The  _result_ XML string must comply with the schema definition for **friends**, as defined in the schema for Outlook Social Connector (OSC) provider extensibility.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="64548-113">См. также</span><span class="sxs-lookup"><span data-stu-id="64548-113">See also</span></span>

- [<span data-ttu-id="64548-114">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="64548-114">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

