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
ms.openlocfilehash: 1f4e6c49ca1c537f78ccce708c4a0b00f81ad7e4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567932"
---
# <a name="imapimessagesitegetstore"></a><span data-ttu-id="34506-103">IMAPIMessageSite::GetStore</span><span class="sxs-lookup"><span data-stu-id="34506-103">IMAPIMessageSite::GetStore</span></span>

  
  
<span data-ttu-id="34506-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="34506-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="34506-105">Если такие хранилища возвращает хранилище сообщение, содержащее текущее сообщение.</span><span class="sxs-lookup"><span data-stu-id="34506-105">Returns the message store that contains the current message, if such a store exists.</span></span> <span data-ttu-id="34506-106">Этот метод возвращает значение NULL в параметре _ppStore_ для внедренных сообщений, которые хранятся в другое сообщение, а не непосредственно в хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="34506-106">This method will return NULL in the  _ppStore_ parameter for embedded messages, which are stored in another message instead of directly in a message store.</span></span> 
  
```cpp
HRESULT GetStore(
  LPMDB FAR * ppStore
);
```

## <a name="parameters"></a><span data-ttu-id="34506-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="34506-107">Parameters</span></span>

 <span data-ttu-id="34506-108">_ppStore_</span><span class="sxs-lookup"><span data-stu-id="34506-108">_ppStore_</span></span>
  
> <span data-ttu-id="34506-109">[out] Указатель на указатель на хранилище сообщений.</span><span class="sxs-lookup"><span data-stu-id="34506-109">[out] A pointer to a pointer to the message store.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="34506-110">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="34506-110">Return value</span></span>

<span data-ttu-id="34506-111">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="34506-111">S_OK</span></span> 
  
> <span data-ttu-id="34506-112">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="34506-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="34506-113">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="34506-113">S_FALSE</span></span> 
  
> <span data-ttu-id="34506-114">Нет без хранилища, содержащий сообщение.</span><span class="sxs-lookup"><span data-stu-id="34506-114">There is no store that contains the message.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="34506-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="34506-115">Remarks</span></span>

<span data-ttu-id="34506-116">Список интерфейсы, связанные с серверами формы в разделе [Интерфейсов формы MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="34506-116">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="34506-117">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="34506-117">MFCMAPI reference</span></span>

<span data-ttu-id="34506-118">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="34506-118">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="34506-119">**����**</span><span class="sxs-lookup"><span data-stu-id="34506-119">**File**</span></span>|<span data-ttu-id="34506-120">**�������**</span><span class="sxs-lookup"><span data-stu-id="34506-120">**Function**</span></span>|<span data-ttu-id="34506-121">**�����������**</span><span class="sxs-lookup"><span data-stu-id="34506-121">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="34506-122">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="34506-122">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="34506-123">CMyMAPIFormViewer::GetStore</span><span class="sxs-lookup"><span data-stu-id="34506-123">CMyMAPIFormViewer::GetStore</span></span>  <br/> |<span data-ttu-id="34506-124">Mfcmapi (en) использует метод **IMAPIMessageSite::GetStore** для получения указатель в настоящее время кэширования для заданного хранилища, если она доступна.</span><span class="sxs-lookup"><span data-stu-id="34506-124">MFCMAPI uses the **IMAPIMessageSite::GetStore** method to get the currently cached pointer to the specified store, if it is available.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="34506-125">См. также</span><span class="sxs-lookup"><span data-stu-id="34506-125">See also</span></span>



[<span data-ttu-id="34506-126">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="34506-126">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="34506-127">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="34506-127">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="34506-128">Интерфейсы форм MAPI</span><span class="sxs-lookup"><span data-stu-id="34506-128">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

