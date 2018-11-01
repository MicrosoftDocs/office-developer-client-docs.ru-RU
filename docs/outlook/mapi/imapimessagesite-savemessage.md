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
ms.openlocfilehash: 9fa7c7226c4ddb5acf5c6b73f55c46829d959eef
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572307"
---
# <a name="imapimessagesitesavemessage"></a><span data-ttu-id="80b6b-103">IMAPIMessageSite::SaveMessage</span><span class="sxs-lookup"><span data-stu-id="80b6b-103">IMAPIMessageSite::SaveMessage</span></span>

  
  
<span data-ttu-id="80b6b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="80b6b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="80b6b-105">Запросы, которые сохранены текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="80b6b-105">Requests that the current message be saved.</span></span>
  
```cpp
HRESULT SaveMessage( void );
```

## <a name="parameters"></a><span data-ttu-id="80b6b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="80b6b-106">Parameters</span></span>

<span data-ttu-id="80b6b-107">Нет.</span><span class="sxs-lookup"><span data-stu-id="80b6b-107">None.</span></span>
  
## <a name="return-value"></a><span data-ttu-id="80b6b-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="80b6b-108">Return value</span></span>

<span data-ttu-id="80b6b-109">S_OK</span><span class="sxs-lookup"><span data-stu-id="80b6b-109">S_OK</span></span> 
  
> <span data-ttu-id="80b6b-110">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="80b6b-110">The call succeeded and has returned the expected value or values.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="80b6b-111">���������</span><span class="sxs-lookup"><span data-stu-id="80b6b-111">Remarks</span></span>

<span data-ttu-id="80b6b-112">Форм вызовите метод **IMAPIMessageSite::SaveMessage** для запроса сохранить сообщение.</span><span class="sxs-lookup"><span data-stu-id="80b6b-112">Forms call the **IMAPIMessageSite::SaveMessage** method to request that a message be saved.</span></span> 
  
<span data-ttu-id="80b6b-113">Список интерфейсы, связанные с серверами формы в разделе [Интерфейсов формы MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="80b6b-113">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="80b6b-114">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="80b6b-114">MFCMAPI reference</span></span>

<span data-ttu-id="80b6b-115">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="80b6b-115">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="80b6b-116">**Файл**</span><span class="sxs-lookup"><span data-stu-id="80b6b-116">**File**</span></span>|<span data-ttu-id="80b6b-117">**Функция**</span><span class="sxs-lookup"><span data-stu-id="80b6b-117">**Function**</span></span>|<span data-ttu-id="80b6b-118">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="80b6b-118">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="80b6b-119">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="80b6b-119">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="80b6b-120">CMyMAPIFormViewer::SaveMessage</span><span class="sxs-lookup"><span data-stu-id="80b6b-120">CMyMAPIFormViewer::SaveMessage</span></span>  <br/> |<span data-ttu-id="80b6b-121">Mfcmapi (en) использует метод **IMAPIMessageSite::SaveMessage** для сохранения сообщения.</span><span class="sxs-lookup"><span data-stu-id="80b6b-121">MFCMAPI uses the **IMAPIMessageSite::SaveMessage** method to save the message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="80b6b-122">См. также</span><span class="sxs-lookup"><span data-stu-id="80b6b-122">See also</span></span>



[<span data-ttu-id="80b6b-123">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="80b6b-123">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="80b6b-124">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="80b6b-124">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="80b6b-125">Интерфейсы формы MAPI</span><span class="sxs-lookup"><span data-stu-id="80b6b-125">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

