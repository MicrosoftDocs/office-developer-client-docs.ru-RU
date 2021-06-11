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
# <a name="imsgserviceadmingetmsgservicetable"></a><span data-ttu-id="6fcef-103">IMsgServiceAdmin::GetMsgServiceTable</span><span class="sxs-lookup"><span data-stu-id="6fcef-103">IMsgServiceAdmin::GetMsgServiceTable</span></span>

  
  
<span data-ttu-id="6fcef-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6fcef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6fcef-105">Предоставляет доступ к таблице служб сообщений, списку служб сообщений в профиле.</span><span class="sxs-lookup"><span data-stu-id="6fcef-105">Provides access to the message service table, a list of the message services in the profile.</span></span>
  
```cpp
HRESULT GetMsgServiceTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="6fcef-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="6fcef-106">Parameters</span></span>

 <span data-ttu-id="6fcef-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6fcef-107">_ulFlags_</span></span>
  
> <span data-ttu-id="6fcef-108">[in] Всегда NULL.</span><span class="sxs-lookup"><span data-stu-id="6fcef-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="6fcef-109">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="6fcef-109">_lppTable_</span></span>
  
> <span data-ttu-id="6fcef-110">[вышел] Указатель на указатель на таблице службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="6fcef-110">[out] A pointer to a pointer to the message service table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6fcef-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6fcef-111">Return value</span></span>

<span data-ttu-id="6fcef-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="6fcef-112">S_OK</span></span> 
  
> <span data-ttu-id="6fcef-113">Таблица службы сообщений была успешно возвращена.</span><span class="sxs-lookup"><span data-stu-id="6fcef-113">The message service table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6fcef-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="6fcef-114">Remarks</span></span>

<span data-ttu-id="6fcef-115">Метод **IMsgServiceAdmin::GetMsgServiceTable** предоставляет доступ к таблице службы сообщений, которая поддерживает MAPI, которая содержит списки служб сообщений, установленных в профиле сеанса.</span><span class="sxs-lookup"><span data-stu-id="6fcef-115">The **IMsgServiceAdmin::GetMsgServiceTable** method provides access to the message service table, a table that MAPI maintains that lists the message services currently installed in the session profile.</span></span> <span data-ttu-id="6fcef-116">Полный список столбцов в таблице службы сообщений см. в [таблице службы сообщений.](message-service-tables.md)</span><span class="sxs-lookup"><span data-stu-id="6fcef-116">For a complete list of columns in the message service table, see [Message Service Table](message-service-tables.md).</span></span>
  
<span data-ttu-id="6fcef-117">Таблица службы сообщений статична.</span><span class="sxs-lookup"><span data-stu-id="6fcef-117">The message service table is static.</span></span> <span data-ttu-id="6fcef-118">После получения клиентом доступа к нему последующие добавления или удаления службы сообщений не повлияют на него.</span><span class="sxs-lookup"><span data-stu-id="6fcef-118">After a client has been given access to it, subsequent message service additions or deletions will not affect it.</span></span> <span data-ttu-id="6fcef-119">Если в текущем профиле нет служб сообщений, **GetMsgServiceTable** возвращает таблицу с нулевыми строками.</span><span class="sxs-lookup"><span data-stu-id="6fcef-119">If there are no message services in the current profile, **GetMsgServiceTable** returns a table with zero rows.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6fcef-120">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="6fcef-120">MFCMAPI reference</span></span>

<span data-ttu-id="6fcef-121">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="6fcef-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6fcef-122">**Файл**</span><span class="sxs-lookup"><span data-stu-id="6fcef-122">**File**</span></span>|<span data-ttu-id="6fcef-123">**Функция**</span><span class="sxs-lookup"><span data-stu-id="6fcef-123">**Function**</span></span>|<span data-ttu-id="6fcef-124">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="6fcef-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6fcef-125">MsgServiceTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="6fcef-125">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="6fcef-126">CMsgServiceTableDlg::OnRefreshView</span><span class="sxs-lookup"><span data-stu-id="6fcef-126">CMsgServiceTableDlg::OnRefreshView</span></span>  <br/> |<span data-ttu-id="6fcef-127">MFCMAPI использует **метод IMsgServiceAdmin::GetMsgServiceTable** для загрузки таблицы служб в профиле для отображения в представлении.</span><span class="sxs-lookup"><span data-stu-id="6fcef-127">MFCMAPI uses the **IMsgServiceAdmin::GetMsgServiceTable** method to load the table of services in a profile to render in the view.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6fcef-128">См. также</span><span class="sxs-lookup"><span data-stu-id="6fcef-128">See also</span></span>



[<span data-ttu-id="6fcef-129">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="6fcef-129">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="6fcef-130">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="6fcef-130">IMsgServiceAdmin::DeleteMsgService</span></span>](imsgserviceadmin-deletemsgservice.md)
  
[<span data-ttu-id="6fcef-131">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6fcef-131">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="6fcef-132">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="6fcef-132">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

