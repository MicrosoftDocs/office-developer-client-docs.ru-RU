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
ms.openlocfilehash: d5d86af111bc778839a78f9b56ba7126e6c973d5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567379"
---
# <a name="imapimessagesitegetsession"></a><span data-ttu-id="80d2d-103">IMAPIMessageSite::GetSession</span><span class="sxs-lookup"><span data-stu-id="80d2d-103">IMAPIMessageSite::GetSession</span></span>

  
  
<span data-ttu-id="80d2d-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="80d2d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="80d2d-105">Возвращает сеанса MAPI, в которой была создана или открыта текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="80d2d-105">Returns the MAPI session in which the current message was created or opened.</span></span>
  
```cpp
HRESULT GetSession(
  LPMAPISESSION FAR * ppSession
);
```

## <a name="parameters"></a><span data-ttu-id="80d2d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="80d2d-106">Parameters</span></span>

 <span data-ttu-id="80d2d-107">_ppSession_</span><span class="sxs-lookup"><span data-stu-id="80d2d-107">_ppSession_</span></span>
  
> <span data-ttu-id="80d2d-108">[out] Указатель на указатель на объект возвращенные сеанса.</span><span class="sxs-lookup"><span data-stu-id="80d2d-108">[out] A pointer to a pointer to the returned session object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="80d2d-109">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="80d2d-109">Return value</span></span>

<span data-ttu-id="80d2d-110">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="80d2d-110">S_OK</span></span> 
  
> <span data-ttu-id="80d2d-111">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="80d2d-111">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="80d2d-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="80d2d-112">S_FALSE</span></span> 
  
> <span data-ttu-id="80d2d-113">Не существуют сеансы для текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="80d2d-113">No session exists for the current message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="80d2d-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="80d2d-114">Remarks</span></span>

<span data-ttu-id="80d2d-115">Список интерфейсов, которые связаны с серверами формы в разделе [Интерфейсов формы MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="80d2d-115">For a list of interfaces that are related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="80d2d-116">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="80d2d-116">MFCMAPI reference</span></span>

<span data-ttu-id="80d2d-117">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="80d2d-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="80d2d-118">**����**</span><span class="sxs-lookup"><span data-stu-id="80d2d-118">**File**</span></span>|<span data-ttu-id="80d2d-119">**�������**</span><span class="sxs-lookup"><span data-stu-id="80d2d-119">**Function**</span></span>|<span data-ttu-id="80d2d-120">**�����������**</span><span class="sxs-lookup"><span data-stu-id="80d2d-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="80d2d-121">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="80d2d-121">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="80d2d-122">CMyMAPIFormViewer::GetSession</span><span class="sxs-lookup"><span data-stu-id="80d2d-122">CMyMAPIFormViewer::GetSession</span></span>  <br/> |<span data-ttu-id="80d2d-123">Mfcmapi (en) использует метод **IMAPIMessageSite::GetSession** возвращает указатель в настоящее время кэширования сеанса, если она доступна.</span><span class="sxs-lookup"><span data-stu-id="80d2d-123">MFCMAPI uses the **IMAPIMessageSite::GetSession** method to return the currently cached session pointer, if it is available.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="80d2d-124">См. также</span><span class="sxs-lookup"><span data-stu-id="80d2d-124">See also</span></span>



[<span data-ttu-id="80d2d-125">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="80d2d-125">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="80d2d-126">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="80d2d-126">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

