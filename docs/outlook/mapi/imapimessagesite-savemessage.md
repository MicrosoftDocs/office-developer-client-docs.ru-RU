---
title: IMAPIMessageSiteSaveMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.SaveMessage
api_type:
- COM
ms.assetid: 94c44952-d297-4705-9778-90373dfa5ad6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ec85f7bdfc9d2d275bdb5ffe7ba0113ad4a35c3b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808982"
---
# <a name="imapimessagesitesavemessage"></a><span data-ttu-id="00894-103">IMAPIMessageSite::SaveMessage</span><span class="sxs-lookup"><span data-stu-id="00894-103">IMAPIMessageSite::SaveMessage</span></span>

  
  
<span data-ttu-id="00894-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="00894-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="00894-105">Запросы, которые сохранены текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="00894-105">Requests that the current message be saved.</span></span>
  
```cpp
HRESULT SaveMessage( void );
```

## <a name="parameters"></a><span data-ttu-id="00894-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="00894-106">Parameters</span></span>

<span data-ttu-id="00894-107">Нет.</span><span class="sxs-lookup"><span data-stu-id="00894-107">None.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="00894-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8">Return value</span></span>

<span data-ttu-id="00894-109">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="00894-109">S_OK</span></span> 
  
> <span data-ttu-id="00894-110">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="00894-110">The call succeeded and has returned the expected value or values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="00894-111">���������</span><span class="sxs-lookup"><span data-stu-id="00894-111">Remarks</span></span>

<span data-ttu-id="00894-112">Форм вызовите метод **IMAPIMessageSite::SaveMessage** для запроса сохранить сообщение.</span><span class="sxs-lookup"><span data-stu-id="00894-112">Forms call the **IMAPIMessageSite::SaveMessage** method to request that a message be saved.</span></span> 
  
<span data-ttu-id="00894-113">Список интерфейсы, связанные с серверами формы в разделе [Интерфейсов формы MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="00894-113">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="00894-114">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="00894-114">MFCMAPI reference</span></span>

<span data-ttu-id="00894-115">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="00894-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="00894-116">**����**</span><span class="sxs-lookup"><span data-stu-id="00894-116">**File**</span></span>|<span data-ttu-id="00894-117">**�������**</span><span class="sxs-lookup"><span data-stu-id="00894-117">**Function**</span></span>|<span data-ttu-id="00894-118">**�����������**</span><span class="sxs-lookup"><span data-stu-id="00894-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="00894-119">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="00894-119">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="00894-120">CMyMAPIFormViewer::SaveMessage</span><span class="sxs-lookup"><span data-stu-id="00894-120">CMyMAPIFormViewer::SaveMessage</span></span>  <br/> |<span data-ttu-id="00894-121">Mfcmapi (en) использует метод **IMAPIMessageSite::SaveMessage** для сохранения сообщения.</span><span class="sxs-lookup"><span data-stu-id="00894-121">MFCMAPI uses the **IMAPIMessageSite::SaveMessage** method to save the message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="00894-122">См. также</span><span class="sxs-lookup"><span data-stu-id="00894-122">See also</span></span>



[<span data-ttu-id="00894-123">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="00894-123">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="00894-124">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="00894-124">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="00894-125">Интерфейсы форм MAPI</span><span class="sxs-lookup"><span data-stu-id="00894-125">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

