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
ms.openlocfilehash: d5d0f465ecdf4865ca86448448c56d54d5df4505
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808975"
---
# <a name="imapimessagesitegetsession"></a><span data-ttu-id="6ea0b-103">IMAPIMessageSite::GetSession</span><span class="sxs-lookup"><span data-stu-id="6ea0b-103">IMAPIMessageSite::GetSession</span></span>

  
  
<span data-ttu-id="6ea0b-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6ea0b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6ea0b-105">Возвращает сеанса MAPI, в которой была создана или открыта текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="6ea0b-105">Returns the MAPI session in which the current message was created or opened.</span></span>
  
```cpp
HRESULT GetSession(
  LPMAPISESSION FAR * ppSession
);
```

## <a name="parameters"></a><span data-ttu-id="6ea0b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6ea0b-106">Parameters</span></span>

 <span data-ttu-id="6ea0b-107">_ppSession_</span><span class="sxs-lookup"><span data-stu-id="6ea0b-107">_ppSession_</span></span>
  
> <span data-ttu-id="6ea0b-108">[out] Указатель на указатель на объект возвращенные сеанса.</span><span class="sxs-lookup"><span data-stu-id="6ea0b-108">[out] A pointer to a pointer to the returned session object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6ea0b-109">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="6ea0b-109">Return value</span></span>

<span data-ttu-id="6ea0b-110">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="6ea0b-110">S_OK</span></span> 
  
> <span data-ttu-id="6ea0b-111">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="6ea0b-111">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="6ea0b-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="6ea0b-112">S_FALSE</span></span> 
  
> <span data-ttu-id="6ea0b-113">Не существуют сеансы для текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="6ea0b-113">No session exists for the current message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6ea0b-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="6ea0b-114">Remarks</span></span>

<span data-ttu-id="6ea0b-115">Список интерфейсов, которые связаны с серверами формы в разделе [Интерфейсов формы MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="6ea0b-115">For a list of interfaces that are related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6ea0b-116">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="6ea0b-116">MFCMAPI reference</span></span>

<span data-ttu-id="6ea0b-117">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="6ea0b-117">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6ea0b-118">**����**</span><span class="sxs-lookup"><span data-stu-id="6ea0b-118">**File**</span></span>|<span data-ttu-id="6ea0b-119">**�������**</span><span class="sxs-lookup"><span data-stu-id="6ea0b-119">**Function**</span></span>|<span data-ttu-id="6ea0b-120">**�����������**</span><span class="sxs-lookup"><span data-stu-id="6ea0b-120">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6ea0b-121">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="6ea0b-121">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="6ea0b-122">CMyMAPIFormViewer::GetSession</span><span class="sxs-lookup"><span data-stu-id="6ea0b-122">CMyMAPIFormViewer::GetSession</span></span>  <br/> |<span data-ttu-id="6ea0b-123">Mfcmapi (en) использует метод **IMAPIMessageSite::GetSession** возвращает указатель в настоящее время кэширования сеанса, если она доступна.</span><span class="sxs-lookup"><span data-stu-id="6ea0b-123">MFCMAPI uses the **IMAPIMessageSite::GetSession** method to return the currently cached session pointer, if it is available.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6ea0b-124">См. также</span><span class="sxs-lookup"><span data-stu-id="6ea0b-124">See also</span></span>



[<span data-ttu-id="6ea0b-125">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6ea0b-125">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="6ea0b-126">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="6ea0b-126">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

