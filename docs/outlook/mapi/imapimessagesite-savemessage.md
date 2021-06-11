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
ms.openlocfilehash: 938eaa6c1a39d24157d5d690c42b435af6192cb6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417107"
---
# <a name="imapimessagesitesavemessage"></a><span data-ttu-id="734a8-103">IMAPIMessageSite::SaveMessage</span><span class="sxs-lookup"><span data-stu-id="734a8-103">IMAPIMessageSite::SaveMessage</span></span>

  
  
<span data-ttu-id="734a8-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="734a8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="734a8-105">Запрашивает, чтобы текущее сообщение было сохранено.</span><span class="sxs-lookup"><span data-stu-id="734a8-105">Requests that the current message be saved.</span></span>
  
```cpp
HRESULT SaveMessage( void );
```

## <a name="parameters"></a><span data-ttu-id="734a8-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="734a8-106">Parameters</span></span>

<span data-ttu-id="734a8-107">Нет.</span><span class="sxs-lookup"><span data-stu-id="734a8-107">None.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="734a8-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="734a8-108">Return value</span></span>

<span data-ttu-id="734a8-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="734a8-109">S_OK</span></span> 
  
> <span data-ttu-id="734a8-110">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="734a8-110">The call succeeded and has returned the expected value or values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="734a8-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="734a8-111">Remarks</span></span>

<span data-ttu-id="734a8-112">Формы называют **метод IMAPIMessageSite::SaveMessage,** чтобы попросить сохранить сообщение.</span><span class="sxs-lookup"><span data-stu-id="734a8-112">Forms call the **IMAPIMessageSite::SaveMessage** method to request that a message be saved.</span></span> 
  
<span data-ttu-id="734a8-113">Список интерфейсов, связанных с серверами форм, см. в [перечне интерфейсов форм MAPI.](mapi-form-interfaces.md)</span><span class="sxs-lookup"><span data-stu-id="734a8-113">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="734a8-114">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="734a8-114">MFCMAPI reference</span></span>

<span data-ttu-id="734a8-115">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="734a8-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="734a8-116">**Файл**</span><span class="sxs-lookup"><span data-stu-id="734a8-116">**File**</span></span>|<span data-ttu-id="734a8-117">**Функция**</span><span class="sxs-lookup"><span data-stu-id="734a8-117">**Function**</span></span>|<span data-ttu-id="734a8-118">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="734a8-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="734a8-119">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="734a8-119">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="734a8-120">CMyMAPIFormViewer::SaveMessage</span><span class="sxs-lookup"><span data-stu-id="734a8-120">CMyMAPIFormViewer::SaveMessage</span></span>  <br/> |<span data-ttu-id="734a8-121">MFCMAPI использует **метод IMAPIMessageSite::SaveMessage** для сохранения сообщения.</span><span class="sxs-lookup"><span data-stu-id="734a8-121">MFCMAPI uses the **IMAPIMessageSite::SaveMessage** method to save the message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="734a8-122">См. также</span><span class="sxs-lookup"><span data-stu-id="734a8-122">See also</span></span>



[<span data-ttu-id="734a8-123">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="734a8-123">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="734a8-124">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="734a8-124">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="734a8-125">Интерфейсы форм MAPI</span><span class="sxs-lookup"><span data-stu-id="734a8-125">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

