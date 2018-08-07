---
title: IPersistMessageGetClassID
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
ms.openlocfilehash: e0937eed2e8ca61bc18ee45ff20337267808ea70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809486"
---
# <a name="ipersistmessagegetclassid"></a><span data-ttu-id="77dde-103">IPersistMessage::GetClassID</span><span class="sxs-lookup"><span data-stu-id="77dde-103">IPersistMessage::GetClassID</span></span>

  
  
<span data-ttu-id="77dde-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="77dde-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="77dde-105">Возвращает идентификатор, представляющий сервера форм для управления формы.</span><span class="sxs-lookup"><span data-stu-id="77dde-105">Returns an identifier that represents the form server that can manage the form.</span></span> 
  
```cpp
HRESULT GetClassID(
  LPCLSID lpClassID
);
```

## <a name="parameters"></a><span data-ttu-id="77dde-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="77dde-106">Parameters</span></span>

 <span data-ttu-id="77dde-107">_lpClassID_</span><span class="sxs-lookup"><span data-stu-id="77dde-107">_lpClassID_</span></span>
  
> <span data-ttu-id="77dde-108">[in, out] Указатель на идентификатор класса (CLSID) формы.</span><span class="sxs-lookup"><span data-stu-id="77dde-108">[in, out] A pointer to the class identifier (CLSID) of the form.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="77dde-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9">Return value</span></span>

<span data-ttu-id="77dde-110">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="77dde-110">S_OK</span></span> 
  
> <span data-ttu-id="77dde-111">Идентификатор класса успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="77dde-111">The class identifier was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="77dde-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="77dde-112">Remarks</span></span>

<span data-ttu-id="77dde-113">Метод **IPersistMessge::GetClassID** задает содержимое параметра _lpClassID_ идентификатор класса сервера форм и возвращает значение S_OK.</span><span class="sxs-lookup"><span data-stu-id="77dde-113">The **IPersistMessge::GetClassID** method sets the contents of the  _lpClassID_ parameter to the form server's class identifier and returns S_OK.</span></span> <span data-ttu-id="77dde-114">Когда форма просмотра вызывает **GetClassID** и его пройдет успешно, формы переводится в состояние [не инициализировано](uninitialized-state.md) .</span><span class="sxs-lookup"><span data-stu-id="77dde-114">When a form viewer calls **GetClassID** and it returns successfully, the form is placed in the [Uninitialized](uninitialized-state.md) state.</span></span> 
  
<span data-ttu-id="77dde-115">Дополнительные сведения об использовании идентификаторов классов в структурированных объектов хранилища метод [IPersist::GetClassID](http://msdn.microsoft.com/library/921a3b86-a240-454e-9411-8d653e02b90e.aspx) см.</span><span class="sxs-lookup"><span data-stu-id="77dde-115">For more information about how class identifiers are used with structured storage objects, see the documentation for the [IPersist::GetClassID](http://msdn.microsoft.com/library/921a3b86-a240-454e-9411-8d653e02b90e.aspx) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="77dde-116">См. также</span><span class="sxs-lookup"><span data-stu-id="77dde-116">See also</span></span>



[<span data-ttu-id="77dde-117">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="77dde-117">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)

