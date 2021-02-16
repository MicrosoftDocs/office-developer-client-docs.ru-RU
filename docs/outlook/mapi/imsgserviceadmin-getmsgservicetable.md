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
ms.openlocfilehash: fcaebb96d4dca4e6bfbee7491dabeafcbd93a2eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410478"
---
# <a name="imsgserviceadmingetmsgservicetable"></a><span data-ttu-id="9e690-103">IMsgServiceAdmin::GetMsgServiceTable</span><span class="sxs-lookup"><span data-stu-id="9e690-103">IMsgServiceAdmin::GetMsgServiceTable</span></span>

  
  
<span data-ttu-id="9e690-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9e690-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9e690-105">Предоставляет доступ к таблице службы сообщений, списку служб сообщений в профиле.</span><span class="sxs-lookup"><span data-stu-id="9e690-105">Provides access to the message service table, a list of the message services in the profile.</span></span>
  
```cpp
HRESULT GetMsgServiceTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="9e690-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9e690-106">Parameters</span></span>

 <span data-ttu-id="9e690-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9e690-107">_ulFlags_</span></span>
  
> <span data-ttu-id="9e690-108">[in] Всегда NULL.</span><span class="sxs-lookup"><span data-stu-id="9e690-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="9e690-109">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="9e690-109">_lppTable_</span></span>
  
> <span data-ttu-id="9e690-110">[out] Указатель на указатель на таблицу службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="9e690-110">[out] A pointer to a pointer to the message service table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9e690-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9e690-111">Return value</span></span>

<span data-ttu-id="9e690-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="9e690-112">S_OK</span></span> 
  
> <span data-ttu-id="9e690-113">Таблица службы сообщений успешно возвращена.</span><span class="sxs-lookup"><span data-stu-id="9e690-113">The message service table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9e690-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="9e690-114">Remarks</span></span>

<span data-ttu-id="9e690-115">Метод **IMsgServiceAdmin::GetMsgServiceTable** предоставляет доступ к таблице службы сообщений, которая поддерживается MAPI и содержит список служб сообщений, установленных в данный момент в профиле сеанса.</span><span class="sxs-lookup"><span data-stu-id="9e690-115">The **IMsgServiceAdmin::GetMsgServiceTable** method provides access to the message service table, a table that MAPI maintains that lists the message services currently installed in the session profile.</span></span> <span data-ttu-id="9e690-116">Полный список столбцов в таблице службы сообщений см. в [таблице службы сообщений.](message-service-tables.md)</span><span class="sxs-lookup"><span data-stu-id="9e690-116">For a complete list of columns in the message service table, see [Message Service Table](message-service-tables.md).</span></span>
  
<span data-ttu-id="9e690-117">Таблица службы сообщений является статической.</span><span class="sxs-lookup"><span data-stu-id="9e690-117">The message service table is static.</span></span> <span data-ttu-id="9e690-118">После того как клиент получит доступ к нему, последующие добавления или удаления службы сообщений не повлияют на него.</span><span class="sxs-lookup"><span data-stu-id="9e690-118">After a client has been given access to it, subsequent message service additions or deletions will not affect it.</span></span> <span data-ttu-id="9e690-119">Если в текущем профиле нет служб сообщений, **GetMsgServiceTable** возвращает таблицу с нулем строк.</span><span class="sxs-lookup"><span data-stu-id="9e690-119">If there are no message services in the current profile, **GetMsgServiceTable** returns a table with zero rows.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9e690-120">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="9e690-120">MFCMAPI reference</span></span>

<span data-ttu-id="9e690-121">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="9e690-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9e690-122">**Файл**</span><span class="sxs-lookup"><span data-stu-id="9e690-122">**File**</span></span>|<span data-ttu-id="9e690-123">**Функция**</span><span class="sxs-lookup"><span data-stu-id="9e690-123">**Function**</span></span>|<span data-ttu-id="9e690-124">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="9e690-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9e690-125">MsgServiceTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="9e690-125">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="9e690-126">CMsgServiceTableDlg::OnRefreshView</span><span class="sxs-lookup"><span data-stu-id="9e690-126">CMsgServiceTableDlg::OnRefreshView</span></span>  <br/> |<span data-ttu-id="9e690-127">MFCMAPI использует метод **IMsgServiceAdmin::GetMsgServiceTable** для загрузки таблицы служб в профиле для отображения в представлении.</span><span class="sxs-lookup"><span data-stu-id="9e690-127">MFCMAPI uses the **IMsgServiceAdmin::GetMsgServiceTable** method to load the table of services in a profile to render in the view.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9e690-128">См. также</span><span class="sxs-lookup"><span data-stu-id="9e690-128">See also</span></span>



[<span data-ttu-id="9e690-129">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="9e690-129">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="9e690-130">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="9e690-130">IMsgServiceAdmin::DeleteMsgService</span></span>](imsgserviceadmin-deletemsgservice.md)
  
[<span data-ttu-id="9e690-131">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9e690-131">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="9e690-132">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="9e690-132">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

