---
title: Иперсистмессажежетклассид
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPersistMessage.GetClassID
api_type:
- COM
ms.assetid: 77eeb468-3432-4ccd-9c1e-1df9ce605193
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 3f0d98b8ffa13fe238fc0fcf8ff0ec76a3a284eb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309627"
---
# <a name="ipersistmessagegetclassid"></a><span data-ttu-id="3c873-103">IPersistMessage::GetClassID</span><span class="sxs-lookup"><span data-stu-id="3c873-103">IPersistMessage::GetClassID</span></span>

  
  
<span data-ttu-id="3c873-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3c873-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3c873-105">Возвращает идентификатор, представляющий сервер форм, который может управлять формой.</span><span class="sxs-lookup"><span data-stu-id="3c873-105">Returns an identifier that represents the form server that can manage the form.</span></span> 
  
```cpp
HRESULT GetClassID(
  LPCLSID lpClassID
);
```

## <a name="parameters"></a><span data-ttu-id="3c873-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3c873-106">Parameters</span></span>

 <span data-ttu-id="3c873-107">_Лпклассид_</span><span class="sxs-lookup"><span data-stu-id="3c873-107">_lpClassID_</span></span>
  
> <span data-ttu-id="3c873-108">[вход, выход] Указатель на идентификатор класса (CLSID) формы.</span><span class="sxs-lookup"><span data-stu-id="3c873-108">[in, out] A pointer to the class identifier (CLSID) of the form.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3c873-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3c873-109">Return value</span></span>

<span data-ttu-id="3c873-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="3c873-110">S_OK</span></span> 
  
> <span data-ttu-id="3c873-111">Идентификатор класса был успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="3c873-111">The class identifier was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3c873-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="3c873-112">Remarks</span></span>

<span data-ttu-id="3c873-113">Метод **иперсистмессже::** задает содержимое параметра _лпклассид_ в качестве идентификатора класса сервера форм и возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="3c873-113">The **IPersistMessge::GetClassID** method sets the contents of the  _lpClassID_ parameter to the form server's class identifier and returns S_OK.</span></span> <span data-ttu-id="3c873-114">Если средство просмотра форм вызывает \*\*\*\* метод вызовов вызовов вызовов вызовов вызовов вызовов вызовов вызовов вызовов вызовов вызовов вызовов [](uninitialized-state.md) вызовов вызовов вызовов вызовов вызовов вызовов вызовов вызовов вызовов вызовов вызовов вызовов вызовов вызовов вызовов вызовов.</span><span class="sxs-lookup"><span data-stu-id="3c873-114">When a form viewer calls **GetClassID** and it returns successfully, the form is placed in the [Uninitialized](uninitialized-state.md) state.</span></span> 
  
<span data-ttu-id="3c873-115">Дополнительные сведения о том, как идентификаторы класса используются с структурированными объектами хранения, представлены в документации по методу [иперсист::::](https://msdn.microsoft.com/library/921a3b86-a240-454e-9411-8d653e02b90e.aspx) .</span><span class="sxs-lookup"><span data-stu-id="3c873-115">For more information about how class identifiers are used with structured storage objects, see the documentation for the [IPersist::GetClassID](https://msdn.microsoft.com/library/921a3b86-a240-454e-9411-8d653e02b90e.aspx) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3c873-116">См. также</span><span class="sxs-lookup"><span data-stu-id="3c873-116">See also</span></span>



[<span data-ttu-id="3c873-117">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3c873-117">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

