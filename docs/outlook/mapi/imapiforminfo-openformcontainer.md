---
title: Имапиформинфупенформконтаинер
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.OpenFormContainer
api_type:
- COM
ms.assetid: 1d6eec99-59f9-4700-9b83-7f7f8787a9f8
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a76d0c554d7cf06aceeaa2925c199e45411b999d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342093"
---
# <a name="imapiforminfoopenformcontainer"></a><span data-ttu-id="e97fe-103">IMAPIFormInfo::OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="e97fe-103">IMAPIFormInfo::OpenFormContainer</span></span>

  
  
<span data-ttu-id="e97fe-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e97fe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e97fe-105">Возвращает указатель на контейнер формы, в котором установлена определенная форма.</span><span class="sxs-lookup"><span data-stu-id="e97fe-105">Returns a pointer to the form container in which a particular form is installed.</span></span>
  
```cpp
HRESULT OpenFormContainer(
  LPMAPIFORMCONTAINER FAR * ppformcontainer
);
```

## <a name="parameters"></a><span data-ttu-id="e97fe-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e97fe-106">Parameters</span></span>

 <span data-ttu-id="e97fe-107">_ппформконтаинер_</span><span class="sxs-lookup"><span data-stu-id="e97fe-107">_ppformcontainer_</span></span>
  
> <span data-ttu-id="e97fe-108">вышли Указатель на указатель на возвращенный объект контейнера формы.</span><span class="sxs-lookup"><span data-stu-id="e97fe-108">[out] A pointer to a pointer to the returned form container object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e97fe-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e97fe-109">Return value</span></span>

<span data-ttu-id="e97fe-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="e97fe-110">S_OK</span></span> 
  
> <span data-ttu-id="e97fe-111">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="e97fe-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e97fe-112">См. также</span><span class="sxs-lookup"><span data-stu-id="e97fe-112">See also</span></span>



[<span data-ttu-id="e97fe-113">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="e97fe-113">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)

