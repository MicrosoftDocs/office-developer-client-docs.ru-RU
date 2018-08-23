---
title: IMAPIMessageSiteGetFormManager
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetFormManager
api_type:
- COM
ms.assetid: d48bd537-c562-4deb-8a4c-011208991054
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5e3a2224daace9be7f4504a693806ccb3cf4abbe
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570494"
---
# <a name="imapimessagesitegetformmanager"></a><span data-ttu-id="097a7-103">IMAPIMessageSite::GetFormManager</span><span class="sxs-lookup"><span data-stu-id="097a7-103">IMAPIMessageSite::GetFormManager</span></span>

  
  
<span data-ttu-id="097a7-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="097a7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="097a7-105">Возвращает интерфейс диспетчера формы, который сервера форм можно использовать для открытия другой сервер формы.</span><span class="sxs-lookup"><span data-stu-id="097a7-105">Returns a form manager interface, which a form server can use to open another form server.</span></span>
  
```cpp
HRESULT GetFormManager(
  LPMAPIFORMMGR FAR * ppFormMgr
);
```

## <a name="parameters"></a><span data-ttu-id="097a7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="097a7-106">Parameters</span></span>

 <span data-ttu-id="097a7-107">_ppFormMgr_</span><span class="sxs-lookup"><span data-stu-id="097a7-107">_ppFormMgr_</span></span>
  
> <span data-ttu-id="097a7-108">[out] Указатель на указатель на интерфейс диспетчера возвращенные формы.</span><span class="sxs-lookup"><span data-stu-id="097a7-108">[out] A pointer to a pointer to the returned form manager interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="097a7-109">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="097a7-109">Return value</span></span>

<span data-ttu-id="097a7-110">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="097a7-110">S_OK</span></span> 
  
> <span data-ttu-id="097a7-111">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="097a7-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="097a7-112">���������</span><span class="sxs-lookup"><span data-stu-id="097a7-112">Remarks</span></span>

<span data-ttu-id="097a7-113">Список интерфейсы, связанные с серверами формы в разделе [Интерфейсов формы MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="097a7-113">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="097a7-114">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="097a7-114">MFCMAPI reference</span></span>

<span data-ttu-id="097a7-115">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="097a7-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="097a7-116">**����**</span><span class="sxs-lookup"><span data-stu-id="097a7-116">**File**</span></span>|<span data-ttu-id="097a7-117">**�������**</span><span class="sxs-lookup"><span data-stu-id="097a7-117">**Function**</span></span>|<span data-ttu-id="097a7-118">**�����������**</span><span class="sxs-lookup"><span data-stu-id="097a7-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="097a7-119">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="097a7-119">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="097a7-120">CMyMAPIFormViewer::GetFormManager</span><span class="sxs-lookup"><span data-stu-id="097a7-120">CMyMAPIFormViewer::GetFormManager</span></span>  <br/> |<span data-ttu-id="097a7-121">Mfcmapi (en) использует метод **IMAPIMessageSite::GetFormManager** для вызова [MAPIOpenFormMgr](mapiopenformmgr.md) и возвращать результаты этого вызова.</span><span class="sxs-lookup"><span data-stu-id="097a7-121">MFCMAPI uses the **IMAPIMessageSite::GetFormManager** method to call [MAPIOpenFormMgr](mapiopenformmgr.md) and return the results of that call.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="097a7-122">См. также</span><span class="sxs-lookup"><span data-stu-id="097a7-122">See also</span></span>



[<span data-ttu-id="097a7-123">MAPIOpenFormMgr</span><span class="sxs-lookup"><span data-stu-id="097a7-123">MAPIOpenFormMgr</span></span>](mapiopenformmgr.md)
  
[<span data-ttu-id="097a7-124">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="097a7-124">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="097a7-125">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="097a7-125">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="097a7-126">Интерфейсы форм MAPI</span><span class="sxs-lookup"><span data-stu-id="097a7-126">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

