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
# <a name="imsgserviceadmingetmsgservicetable"></a><span data-ttu-id="b6e72-103">IMsgServiceAdmin::GetMsgServiceTable</span><span class="sxs-lookup"><span data-stu-id="b6e72-103">IMsgServiceAdmin::GetMsgServiceTable</span></span>

  
  
<span data-ttu-id="b6e72-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b6e72-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b6e72-105">Предоставляет доступ к таблице службы сообщений, список служб сообщения в профиле.</span><span class="sxs-lookup"><span data-stu-id="b6e72-105">Provides access to the message service table, a list of the message services in the profile.</span></span>
  
```cpp
HRESULT GetMsgServiceTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="b6e72-106">���������</span><span class="sxs-lookup"><span data-stu-id="b6e72-106">Parameters</span></span>

 <span data-ttu-id="b6e72-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b6e72-107">_ulFlags_</span></span>
  
> <span data-ttu-id="b6e72-108">[in] Всегда имеет значение NULL.</span><span class="sxs-lookup"><span data-stu-id="b6e72-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="b6e72-109">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="b6e72-109">_lppTable_</span></span>
  
> <span data-ttu-id="b6e72-110">[out] Указатель на указатель в таблице службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="b6e72-110">[out] A pointer to a pointer to the message service table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b6e72-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b6e72-111">Return value</span></span>

<span data-ttu-id="b6e72-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="b6e72-112">S_OK</span></span> 
  
> <span data-ttu-id="b6e72-113">В таблице службы сообщение успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="b6e72-113">The message service table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b6e72-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="b6e72-114">Remarks</span></span>

<span data-ttu-id="b6e72-115">Метод **IMsgServiceAdmin::GetMsgServiceTable** предоставляет доступ к таблице службы сообщений, таблица, содержащая MAPI, в котором приведены службы сообщений, установленные в профиле сеанса.</span><span class="sxs-lookup"><span data-stu-id="b6e72-115">The **IMsgServiceAdmin::GetMsgServiceTable** method provides access to the message service table, a table that MAPI maintains that lists the message services currently installed in the session profile.</span></span> <span data-ttu-id="b6e72-116">Полный список столбцов в таблице служб сообщения в разделе [Таблицы службы сообщений](message-service-tables.md).</span><span class="sxs-lookup"><span data-stu-id="b6e72-116">For a complete list of columns in the message service table, see [Message Service Table](message-service-tables.md).</span></span>
  
<span data-ttu-id="b6e72-117">В таблице службы сообщения является статическим.</span><span class="sxs-lookup"><span data-stu-id="b6e72-117">The message service table is static.</span></span> <span data-ttu-id="b6e72-118">После клиента предоставлен доступ к нему, появившееся сообщение службы добавления или удаления не повлияет на его.</span><span class="sxs-lookup"><span data-stu-id="b6e72-118">After a client has been given access to it, subsequent message service additions or deletions will not affect it.</span></span> <span data-ttu-id="b6e72-119">Если в текущий профиль службы не сообщения, **GetMsgServiceTable** возвращает таблицу с нуля строк.</span><span class="sxs-lookup"><span data-stu-id="b6e72-119">If there are no message services in the current profile, **GetMsgServiceTable** returns a table with zero rows.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b6e72-120">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="b6e72-120">MFCMAPI reference</span></span>

<span data-ttu-id="b6e72-121">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="b6e72-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b6e72-122">**Файл**</span><span class="sxs-lookup"><span data-stu-id="b6e72-122">**File**</span></span>|<span data-ttu-id="b6e72-123">**Функция**</span><span class="sxs-lookup"><span data-stu-id="b6e72-123">**Function**</span></span>|<span data-ttu-id="b6e72-124">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="b6e72-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b6e72-125">MsgServiceTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="b6e72-125">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="b6e72-126">CMsgServiceTableDlg::OnRefreshView</span><span class="sxs-lookup"><span data-stu-id="b6e72-126">CMsgServiceTableDlg::OnRefreshView</span></span>  <br/> |<span data-ttu-id="b6e72-127">Mfcmapi (en) использует метод **IMsgServiceAdmin::GetMsgServiceTable** для загрузки в таблице службы профиля для отображения в представлении.</span><span class="sxs-lookup"><span data-stu-id="b6e72-127">MFCMAPI uses the **IMsgServiceAdmin::GetMsgServiceTable** method to load the table of services in a profile to render in the view.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b6e72-128">См. также</span><span class="sxs-lookup"><span data-stu-id="b6e72-128">See also</span></span>



[<span data-ttu-id="b6e72-129">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="b6e72-129">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="b6e72-130">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="b6e72-130">IMsgServiceAdmin::DeleteMsgService</span></span>](imsgserviceadmin-deletemsgservice.md)
  
[<span data-ttu-id="b6e72-131">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b6e72-131">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="b6e72-132">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="b6e72-132">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

