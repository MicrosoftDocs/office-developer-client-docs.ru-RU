---
title: IMAPIMessageSiteGetStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetStore
api_type:
- COM
ms.assetid: d1ca619e-8bdc-417b-aed6-23dd30e6eafa
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0c78574f213245a5c30ff589ade824e5c5bd84ee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410471"
---
# <a name="imapimessagesitegetstore"></a><span data-ttu-id="ababd-103">IMAPIMessageSite::GetStore</span><span class="sxs-lookup"><span data-stu-id="ababd-103">IMAPIMessageSite::GetStore</span></span>

  
  
<span data-ttu-id="ababd-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ababd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ababd-105">Возвращает хранилище сообщений, которое содержит текущее сообщение, если такое хранилище существует.</span><span class="sxs-lookup"><span data-stu-id="ababd-105">Returns the message store that contains the current message, if such a store exists.</span></span> <span data-ttu-id="ababd-106">Этот метод возвращает NULL в  _параметре ppStore_ для внедренных сообщений, которые хранятся в другом сообщении, а не непосредственно в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="ababd-106">This method will return NULL in the  _ppStore_ parameter for embedded messages, which are stored in another message instead of directly in a message store.</span></span> 
  
```cpp
HRESULT GetStore(
  LPMDB FAR * ppStore
);
```

## <a name="parameters"></a><span data-ttu-id="ababd-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ababd-107">Parameters</span></span>

 <span data-ttu-id="ababd-108">_ppStore_</span><span class="sxs-lookup"><span data-stu-id="ababd-108">_ppStore_</span></span>
  
> <span data-ttu-id="ababd-109">[out] Указатель на указатель на хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="ababd-109">[out] A pointer to a pointer to the message store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ababd-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ababd-110">Return value</span></span>

<span data-ttu-id="ababd-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="ababd-111">S_OK</span></span> 
  
> <span data-ttu-id="ababd-112">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="ababd-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="ababd-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="ababd-113">S_FALSE</span></span> 
  
> <span data-ttu-id="ababd-114">Хранилище, в которое входит сообщение, не существует.</span><span class="sxs-lookup"><span data-stu-id="ababd-114">There is no store that contains the message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ababd-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="ababd-115">Remarks</span></span>

<span data-ttu-id="ababd-116">Список интерфейсов, связанных с серверами форм, см. в списке [интерфейсов форм MAPI.](mapi-form-interfaces.md)</span><span class="sxs-lookup"><span data-stu-id="ababd-116">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ababd-117">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ababd-117">MFCMAPI reference</span></span>

<span data-ttu-id="ababd-118">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="ababd-118">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ababd-119">**Файл**</span><span class="sxs-lookup"><span data-stu-id="ababd-119">**File**</span></span>|<span data-ttu-id="ababd-120">**Функция**</span><span class="sxs-lookup"><span data-stu-id="ababd-120">**Function**</span></span>|<span data-ttu-id="ababd-121">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="ababd-121">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ababd-122">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="ababd-122">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="ababd-123">CMyMAPIFormViewer::GetStore</span><span class="sxs-lookup"><span data-stu-id="ababd-123">CMyMAPIFormViewer::GetStore</span></span>  <br/> |<span data-ttu-id="ababd-124">MFCMAPI использует метод **IMAPIMessageSite::GetStore** для получения кэшного указателя на указанное хранилище, если оно доступно.</span><span class="sxs-lookup"><span data-stu-id="ababd-124">MFCMAPI uses the **IMAPIMessageSite::GetStore** method to get the currently cached pointer to the specified store, if it is available.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ababd-125">См. также</span><span class="sxs-lookup"><span data-stu-id="ababd-125">See also</span></span>



[<span data-ttu-id="ababd-126">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ababd-126">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="ababd-127">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="ababd-127">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="ababd-128">Интерфейсы форм MAPI</span><span class="sxs-lookup"><span data-stu-id="ababd-128">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

