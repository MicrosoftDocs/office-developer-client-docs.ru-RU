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
ms.openlocfilehash: abaf8f665ea7add92a34c2e4d6fcbf9d5fc08d3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808979"
---
# <a name="imapimessagesitegetformmanager"></a><span data-ttu-id="51d9c-103">IMAPIMessageSite::GetFormManager</span><span class="sxs-lookup"><span data-stu-id="51d9c-103">IMAPIMessageSite::GetFormManager</span></span>

  
  
<span data-ttu-id="51d9c-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="51d9c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="51d9c-105">Возвращает интерфейс диспетчера формы, который сервера форм можно использовать для открытия другой сервер формы.</span><span class="sxs-lookup"><span data-stu-id="51d9c-105">Returns a form manager interface, which a form server can use to open another form server.</span></span>
  
```cpp
HRESULT GetFormManager(
  LPMAPIFORMMGR FAR * ppFormMgr
);
```

## <a name="parameters"></a><span data-ttu-id="51d9c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="51d9c-106">Parameters</span></span>

 <span data-ttu-id="51d9c-107">_ppFormMgr_</span><span class="sxs-lookup"><span data-stu-id="51d9c-107">_ppFormMgr_</span></span>
  
> <span data-ttu-id="51d9c-108">[out] Указатель на указатель на интерфейс диспетчера возвращенные формы.</span><span class="sxs-lookup"><span data-stu-id="51d9c-108">[out] A pointer to a pointer to the returned form manager interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="51d9c-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9">Return value</span></span>

<span data-ttu-id="51d9c-110">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="51d9c-110">S_OK</span></span> 
  
> <span data-ttu-id="51d9c-111">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="51d9c-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="51d9c-112">���������</span><span class="sxs-lookup"><span data-stu-id="51d9c-112">Remarks</span></span>

<span data-ttu-id="51d9c-113">Список интерфейсы, связанные с серверами формы в разделе [Интерфейсов формы MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="51d9c-113">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="51d9c-114">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="51d9c-114">MFCMAPI reference</span></span>

<span data-ttu-id="51d9c-115">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="51d9c-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="51d9c-116">**����**</span><span class="sxs-lookup"><span data-stu-id="51d9c-116">**File**</span></span>|<span data-ttu-id="51d9c-117">**�������**</span><span class="sxs-lookup"><span data-stu-id="51d9c-117">**Function**</span></span>|<span data-ttu-id="51d9c-118">**�����������**</span><span class="sxs-lookup"><span data-stu-id="51d9c-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="51d9c-119">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="51d9c-119">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="51d9c-120">CMyMAPIFormViewer::GetFormManager</span><span class="sxs-lookup"><span data-stu-id="51d9c-120">CMyMAPIFormViewer::GetFormManager</span></span>  <br/> |<span data-ttu-id="51d9c-121">Mfcmapi (en) использует метод **IMAPIMessageSite::GetFormManager** для вызова [MAPIOpenFormMgr](mapiopenformmgr.md) и возвращать результаты этого вызова.</span><span class="sxs-lookup"><span data-stu-id="51d9c-121">MFCMAPI uses the **IMAPIMessageSite::GetFormManager** method to call [MAPIOpenFormMgr](mapiopenformmgr.md) and return the results of that call.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="51d9c-122">См. также</span><span class="sxs-lookup"><span data-stu-id="51d9c-122">See also</span></span>



[<span data-ttu-id="51d9c-123">MAPIOpenFormMgr</span><span class="sxs-lookup"><span data-stu-id="51d9c-123">MAPIOpenFormMgr</span></span>](mapiopenformmgr.md)
  
[<span data-ttu-id="51d9c-124">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="51d9c-124">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="51d9c-125">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="51d9c-125">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="51d9c-126">Интерфейсы форм MAPI</span><span class="sxs-lookup"><span data-stu-id="51d9c-126">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

