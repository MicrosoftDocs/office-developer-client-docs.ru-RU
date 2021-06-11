---
title: IMAPIMessageSiteGetSession
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetSession
api_type:
- COM
ms.assetid: c35d9e38-f4cf-4908-aaa1-a4263b58f7e8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e1ea68a7690a93915cd80ad5406c4d71d3a97400
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412690"
---
# <a name="imapimessagesitegetsession"></a><span data-ttu-id="fa2ed-103">IMAPIMessageSite::GetSession</span><span class="sxs-lookup"><span data-stu-id="fa2ed-103">IMAPIMessageSite::GetSession</span></span>

  
  
<span data-ttu-id="fa2ed-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa2ed-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa2ed-105">Возвращает сеанс MAPI, в котором было создано или открыто текущее сообщение.</span><span class="sxs-lookup"><span data-stu-id="fa2ed-105">Returns the MAPI session in which the current message was created or opened.</span></span>
  
```cpp
HRESULT GetSession(
  LPMAPISESSION FAR * ppSession
);
```

## <a name="parameters"></a><span data-ttu-id="fa2ed-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="fa2ed-106">Parameters</span></span>

 <span data-ttu-id="fa2ed-107">_ppSession_</span><span class="sxs-lookup"><span data-stu-id="fa2ed-107">_ppSession_</span></span>
  
> <span data-ttu-id="fa2ed-108">[вышел] Указатель на указатель на возвращаемом объекте сеанса.</span><span class="sxs-lookup"><span data-stu-id="fa2ed-108">[out] A pointer to a pointer to the returned session object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fa2ed-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fa2ed-109">Return value</span></span>

<span data-ttu-id="fa2ed-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="fa2ed-110">S_OK</span></span> 
  
> <span data-ttu-id="fa2ed-111">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="fa2ed-111">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="fa2ed-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="fa2ed-112">S_FALSE</span></span> 
  
> <span data-ttu-id="fa2ed-113">Для текущего сообщения сеанса не существует.</span><span class="sxs-lookup"><span data-stu-id="fa2ed-113">No session exists for the current message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fa2ed-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="fa2ed-114">Remarks</span></span>

<span data-ttu-id="fa2ed-115">Список интерфейсов, связанных с серверами форм, см. в перечне [интерфейсов форм MAPI.](mapi-form-interfaces.md)</span><span class="sxs-lookup"><span data-stu-id="fa2ed-115">For a list of interfaces that are related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="fa2ed-116">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="fa2ed-116">MFCMAPI reference</span></span>

<span data-ttu-id="fa2ed-117">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="fa2ed-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="fa2ed-118">**Файл**</span><span class="sxs-lookup"><span data-stu-id="fa2ed-118">**File**</span></span>|<span data-ttu-id="fa2ed-119">**Функция**</span><span class="sxs-lookup"><span data-stu-id="fa2ed-119">**Function**</span></span>|<span data-ttu-id="fa2ed-120">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="fa2ed-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fa2ed-121">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="fa2ed-121">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="fa2ed-122">CMyMAPIFormViewer::GetSession</span><span class="sxs-lookup"><span data-stu-id="fa2ed-122">CMyMAPIFormViewer::GetSession</span></span>  <br/> |<span data-ttu-id="fa2ed-123">MFCMAPI использует **метод IMAPIMessageSite::GetSession** для возврата кэшного указателя сеанса, если он доступен.</span><span class="sxs-lookup"><span data-stu-id="fa2ed-123">MFCMAPI uses the **IMAPIMessageSite::GetSession** method to return the currently cached session pointer, if it is available.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fa2ed-124">См. также</span><span class="sxs-lookup"><span data-stu-id="fa2ed-124">See also</span></span>



[<span data-ttu-id="fa2ed-125">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fa2ed-125">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="fa2ed-126">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="fa2ed-126">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

