---
title: имсгсервицеадминжетмсгсервицетабле
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
# <a name="imsgserviceadmingetmsgservicetable"></a><span data-ttu-id="3ec41-103">IMsgServiceAdmin::GetMsgServiceTable</span><span class="sxs-lookup"><span data-stu-id="3ec41-103">IMsgServiceAdmin::GetMsgServiceTable</span></span>

  
  
<span data-ttu-id="3ec41-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3ec41-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3ec41-105">Предоставляет доступ к таблице службы сообщений, списку служб сообщений в профиле.</span><span class="sxs-lookup"><span data-stu-id="3ec41-105">Provides access to the message service table, a list of the message services in the profile.</span></span>
  
```cpp
HRESULT GetMsgServiceTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="3ec41-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3ec41-106">Parameters</span></span>

 <span data-ttu-id="3ec41-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3ec41-107">_ulFlags_</span></span>
  
> <span data-ttu-id="3ec41-108">возврата Всегда имеет значение NULL.</span><span class="sxs-lookup"><span data-stu-id="3ec41-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="3ec41-109">_лпптабле_</span><span class="sxs-lookup"><span data-stu-id="3ec41-109">_lppTable_</span></span>
  
> <span data-ttu-id="3ec41-110">вышли Указатель на указатель на таблицу службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="3ec41-110">[out] A pointer to a pointer to the message service table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3ec41-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3ec41-111">Return value</span></span>

<span data-ttu-id="3ec41-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="3ec41-112">S_OK</span></span> 
  
> <span data-ttu-id="3ec41-113">Таблица службы сообщений успешно возвращена.</span><span class="sxs-lookup"><span data-stu-id="3ec41-113">The message service table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3ec41-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="3ec41-114">Remarks</span></span>

<span data-ttu-id="3ec41-115">Метод **имсгсервицеадмин:: жетмсгсервицетабле** предоставляет доступ к таблице службы сообщений, таблице, которую поддерживает MAPI, в которой перечислены службы сообщений, установленные в профиле сеанса.</span><span class="sxs-lookup"><span data-stu-id="3ec41-115">The **IMsgServiceAdmin::GetMsgServiceTable** method provides access to the message service table, a table that MAPI maintains that lists the message services currently installed in the session profile.</span></span> <span data-ttu-id="3ec41-116">Полный список столбцов таблицы служба сообщений приведен в разделе [Таблица службы сообщений](message-service-tables.md).</span><span class="sxs-lookup"><span data-stu-id="3ec41-116">For a complete list of columns in the message service table, see [Message Service Table](message-service-tables.md).</span></span>
  
<span data-ttu-id="3ec41-117">Таблица службы сообщений является статической.</span><span class="sxs-lookup"><span data-stu-id="3ec41-117">The message service table is static.</span></span> <span data-ttu-id="3ec41-118">После того как клиенту будет предоставлен доступ к нему, последующие добавления и удаления службы сообщений не повлияют на нее.</span><span class="sxs-lookup"><span data-stu-id="3ec41-118">After a client has been given access to it, subsequent message service additions or deletions will not affect it.</span></span> <span data-ttu-id="3ec41-119">Если в текущем профиле нет служб сообщений, **жетмсгсервицетабле** возвращает таблицу с нулевыми строками.</span><span class="sxs-lookup"><span data-stu-id="3ec41-119">If there are no message services in the current profile, **GetMsgServiceTable** returns a table with zero rows.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3ec41-120">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="3ec41-120">MFCMAPI reference</span></span>

<span data-ttu-id="3ec41-121">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="3ec41-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3ec41-122">**Файл**</span><span class="sxs-lookup"><span data-stu-id="3ec41-122">**File**</span></span>|<span data-ttu-id="3ec41-123">**Функция**</span><span class="sxs-lookup"><span data-stu-id="3ec41-123">**Function**</span></span>|<span data-ttu-id="3ec41-124">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="3ec41-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3ec41-125">Мсгсервицетабледлг. cpp</span><span class="sxs-lookup"><span data-stu-id="3ec41-125">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="3ec41-126">Кмсгсервицетабледлг:: Онрефрешвиев</span><span class="sxs-lookup"><span data-stu-id="3ec41-126">CMsgServiceTableDlg::OnRefreshView</span></span>  <br/> |<span data-ttu-id="3ec41-127">MFCMAPI использует метод **имсгсервицеадмин:: жетмсгсервицетабле** для загрузки таблицы служб в профиле для отображения в представлении.</span><span class="sxs-lookup"><span data-stu-id="3ec41-127">MFCMAPI uses the **IMsgServiceAdmin::GetMsgServiceTable** method to load the table of services in a profile to render in the view.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3ec41-128">См. также</span><span class="sxs-lookup"><span data-stu-id="3ec41-128">See also</span></span>



[<span data-ttu-id="3ec41-129">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="3ec41-129">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="3ec41-130">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="3ec41-130">IMsgServiceAdmin::DeleteMsgService</span></span>](imsgserviceadmin-deletemsgservice.md)
  
[<span data-ttu-id="3ec41-131">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3ec41-131">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="3ec41-132">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="3ec41-132">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

