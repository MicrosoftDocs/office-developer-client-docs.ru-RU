---
title: ISocialSessionFindPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a86cb847-5d49-44b8-b2bc-0e35e70395b4
description: Получает строку, представляющую одного или нескольких пользователей, соответствующих параметру идентификатор пользователя.
ms.openlocfilehash: 0b7525f853f7d97a991e2996a4e715cc53756d4a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812737"
---
# <a name="isocialsessionfindperson"></a><span data-ttu-id="c2810-103">ISocialSession::FindPerson</span><span class="sxs-lookup"><span data-stu-id="c2810-103">ISocialSession::FindPerson</span></span>

<span data-ttu-id="c2810-104">Получает строку, представляющую одного или нескольких пользователей, соответствующих параметру _идентификатор пользователя_ .</span><span class="sxs-lookup"><span data-stu-id="c2810-104">Gets a string that represents one or more persons who match the  _userID_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall FindPerson([in] BSTR userId, [out, retval] BSTR* result);
```

## <a name="parameters"></a><span data-ttu-id="c2810-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="c2810-105">Parameters</span></span>

<span data-ttu-id="c2810-106">_userId_</span><span class="sxs-lookup"><span data-stu-id="c2810-106">_userId_</span></span>
  
> <span data-ttu-id="c2810-107">[in] Идентификатор пользователя социальных сетей, SMTP-адрес или отображаемое имя пользователя.</span><span class="sxs-lookup"><span data-stu-id="c2810-107">[in] A social network user ID, SMTP address, or display name of a person.</span></span>
    
<span data-ttu-id="c2810-108">_результат_</span><span class="sxs-lookup"><span data-stu-id="c2810-108">_result_</span></span>
  
> <span data-ttu-id="c2810-109">[out] XML-строка, которая представляет один или несколько пользователей, соответствующие данные идентификации, указанного с помощью параметра _идентификатор пользователя_ .</span><span class="sxs-lookup"><span data-stu-id="c2810-109">[out] An XML string that represents one or more persons who match the identification information specified by the  _userId_ parameter.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="c2810-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="c2810-110">Remarks</span></span>

<span data-ttu-id="c2810-111">Если один или несколько лиц соответствует запрос **FindPerson** , этот метод возвращает сведения для пользователей с помощью параметра _результатов_ .</span><span class="sxs-lookup"><span data-stu-id="c2810-111">If one or more persons match the **FindPerson** request, this method returns the information for those persons in the  _result_ parameter.</span></span> <span data-ttu-id="c2810-112">XML-строка _результат_ должен соответствовать требованиям определение схемы для **друзей**, определенных в схеме для расширений поставщика Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="c2810-112">The  _result_ XML string must comply with the schema definition for **friends**, as defined in the schema for Outlook Social Connector (OSC) provider extensibility.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c2810-113">См. также</span><span class="sxs-lookup"><span data-stu-id="c2810-113">See also</span></span>

- [<span data-ttu-id="c2810-114">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c2810-114">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

