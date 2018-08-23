---
title: IMsgServiceAdminGetMsgServiceTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.GetMsgServiceTable
api_type:
- COM
ms.assetid: 064dd5ca-0108-4045-b17b-0bb29cb93346
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5d8e91490cc39c3f259d35a923bb3bcbb2bf6011
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568170"
---
# <a name="imsgserviceadmingetmsgservicetable"></a><span data-ttu-id="2f64f-103">IMsgServiceAdmin::GetMsgServiceTable</span><span class="sxs-lookup"><span data-stu-id="2f64f-103">IMsgServiceAdmin::GetMsgServiceTable</span></span>

  
  
<span data-ttu-id="2f64f-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2f64f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2f64f-105">Предоставляет доступ к таблице службы сообщений, список служб сообщения в профиле.</span><span class="sxs-lookup"><span data-stu-id="2f64f-105">Provides access to the message service table, a list of the message services in the profile.</span></span>
  
```cpp
HRESULT GetMsgServiceTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="2f64f-106">���������</span><span class="sxs-lookup"><span data-stu-id="2f64f-106">Parameters</span></span>

 <span data-ttu-id="2f64f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2f64f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="2f64f-108">[in] Всегда имеет значение NULL.</span><span class="sxs-lookup"><span data-stu-id="2f64f-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="2f64f-109">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="2f64f-109">_lppTable_</span></span>
  
> <span data-ttu-id="2f64f-110">[out] Указатель на указатель в таблице службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="2f64f-110">[out] A pointer to a pointer to the message service table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2f64f-111">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="2f64f-111">Return value</span></span>

<span data-ttu-id="2f64f-112">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="2f64f-112">S_OK</span></span> 
  
> <span data-ttu-id="2f64f-113">В таблице службы сообщение успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="2f64f-113">The message service table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2f64f-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="2f64f-114">Remarks</span></span>

<span data-ttu-id="2f64f-115">Метод **IMsgServiceAdmin::GetMsgServiceTable** предоставляет доступ к таблице службы сообщений, таблица, содержащая MAPI, в котором приведены службы сообщений, установленные в профиле сеанса.</span><span class="sxs-lookup"><span data-stu-id="2f64f-115">The **IMsgServiceAdmin::GetMsgServiceTable** method provides access to the message service table, a table that MAPI maintains that lists the message services currently installed in the session profile.</span></span> <span data-ttu-id="2f64f-116">Полный список столбцов в таблице служб сообщения в разделе [Таблицы службы сообщений](message-service-tables.md).</span><span class="sxs-lookup"><span data-stu-id="2f64f-116">For a complete list of columns in the message service table, see [Message Service Table](message-service-tables.md).</span></span>
  
<span data-ttu-id="2f64f-117">В таблице службы сообщения является статическим.</span><span class="sxs-lookup"><span data-stu-id="2f64f-117">The message service table is static.</span></span> <span data-ttu-id="2f64f-118">После клиента предоставлен доступ к нему, появившееся сообщение службы добавления или удаления не повлияет на его.</span><span class="sxs-lookup"><span data-stu-id="2f64f-118">After a client has been given access to it, subsequent message service additions or deletions will not affect it.</span></span> <span data-ttu-id="2f64f-119">Если в текущий профиль службы не сообщения, **GetMsgServiceTable** возвращает таблицу с нуля строк.</span><span class="sxs-lookup"><span data-stu-id="2f64f-119">If there are no message services in the current profile, **GetMsgServiceTable** returns a table with zero rows.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2f64f-120">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="2f64f-120">MFCMAPI reference</span></span>

<span data-ttu-id="2f64f-121">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="2f64f-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2f64f-122">**����**</span><span class="sxs-lookup"><span data-stu-id="2f64f-122">**File**</span></span>|<span data-ttu-id="2f64f-123">**�������**</span><span class="sxs-lookup"><span data-stu-id="2f64f-123">**Function**</span></span>|<span data-ttu-id="2f64f-124">**�����������**</span><span class="sxs-lookup"><span data-stu-id="2f64f-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2f64f-125">MsgServiceTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="2f64f-125">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="2f64f-126">CMsgServiceTableDlg::OnRefreshView</span><span class="sxs-lookup"><span data-stu-id="2f64f-126">CMsgServiceTableDlg::OnRefreshView</span></span>  <br/> |<span data-ttu-id="2f64f-127">Mfcmapi (en) использует метод **IMsgServiceAdmin::GetMsgServiceTable** для загрузки в таблице службы профиля для отображения в представлении.</span><span class="sxs-lookup"><span data-stu-id="2f64f-127">MFCMAPI uses the **IMsgServiceAdmin::GetMsgServiceTable** method to load the table of services in a profile to render in the view.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2f64f-128">См. также</span><span class="sxs-lookup"><span data-stu-id="2f64f-128">See also</span></span>



[<span data-ttu-id="2f64f-129">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="2f64f-129">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="2f64f-130">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="2f64f-130">IMsgServiceAdmin::DeleteMsgService</span></span>](imsgserviceadmin-deletemsgservice.md)
  
[<span data-ttu-id="2f64f-131">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2f64f-131">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="2f64f-132">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="2f64f-132">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

