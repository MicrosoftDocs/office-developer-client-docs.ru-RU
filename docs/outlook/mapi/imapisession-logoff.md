---
title: IMAPISessionLogoff
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.Logoff
api_type:
- COM
ms.assetid: 93e38f6c-4b67-4f2d-bc94-631efec86852
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 317c3702415ddf30038ccd0d40cdf0f19abc61f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338110"
---
# <a name="imapisessionlogoff"></a><span data-ttu-id="92e5d-103">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="92e5d-103">IMAPISession::Logoff</span></span>

  
  
<span data-ttu-id="92e5d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="92e5d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="92e5d-105">Завершает сеанс MAPI.</span><span class="sxs-lookup"><span data-stu-id="92e5d-105">Ends a MAPI session.</span></span>
  
```cpp
HRESULT Logoff(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG ulReserved
);
```

## <a name="parameters"></a><span data-ttu-id="92e5d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="92e5d-106">Parameters</span></span>

 <span data-ttu-id="92e5d-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="92e5d-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="92e5d-108">[in] Handle to the parent window of any dialog boxes or windows to be displayed.</span><span class="sxs-lookup"><span data-stu-id="92e5d-108">[in] A handle to the parent window of any dialog boxes or windows to be displayed.</span></span> <span data-ttu-id="92e5d-109">Этот параметр игнорируется, если MAPI_LOGOFF_UI флага не задан.</span><span class="sxs-lookup"><span data-stu-id="92e5d-109">This parameter is ignored if the MAPI_LOGOFF_UI flag is not set.</span></span>
    
 <span data-ttu-id="92e5d-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="92e5d-110">_ulFlags_</span></span>
  
> <span data-ttu-id="92e5d-111">[in] Битоваяmas флагов, которые контролируют операцию выйдите из системы.</span><span class="sxs-lookup"><span data-stu-id="92e5d-111">[in] A bitmask of flags that control the logoff operation.</span></span> <span data-ttu-id="92e5d-112">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="92e5d-112">The following flags can be set:</span></span>
    
<span data-ttu-id="92e5d-113">MAPI_LOGOFF_SHARED</span><span class="sxs-lookup"><span data-stu-id="92e5d-113">MAPI_LOGOFF_SHARED</span></span> 
  
> <span data-ttu-id="92e5d-114">Если этот сеанс является общим, все клиенты, которые вошли в систему с помощью общего сеанса, должны быть уведомлены о том, что происходит вход.</span><span class="sxs-lookup"><span data-stu-id="92e5d-114">If this session is shared, all clients that logged on by using the shared session should be notified of the logoff in progress.</span></span> <span data-ttu-id="92e5d-115">Клиенты должны выйти.</span><span class="sxs-lookup"><span data-stu-id="92e5d-115">The clients should log off.</span></span> <span data-ttu-id="92e5d-116">Любой клиент, использующий общий сеанс, может установить этот флаг.</span><span class="sxs-lookup"><span data-stu-id="92e5d-116">Any client that is using the shared session can set this flag.</span></span> <span data-ttu-id="92e5d-117">MAPI_LOGOFF_SHARED игнорируется, если текущий сеанс не является общим.</span><span class="sxs-lookup"><span data-stu-id="92e5d-117">MAPI_LOGOFF_SHARED is ignored if the current session is not shared.</span></span>
    
<span data-ttu-id="92e5d-118">MAPI_LOGOFF_UI</span><span class="sxs-lookup"><span data-stu-id="92e5d-118">MAPI_LOGOFF_UI</span></span> 
  
> <span data-ttu-id="92e5d-119">**Во время** операции можно отобразить диалоговое окно с запросом подтверждения.</span><span class="sxs-lookup"><span data-stu-id="92e5d-119">**Logoff** can display a dialog box during the operation, possibly prompting the user for confirmation.</span></span> 
    
 <span data-ttu-id="92e5d-120">_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="92e5d-120">_ulReserved_</span></span>
  
> <span data-ttu-id="92e5d-121">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="92e5d-121">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="92e5d-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="92e5d-122">Return value</span></span>

<span data-ttu-id="92e5d-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="92e5d-123">S_OK</span></span> 
  
> <span data-ttu-id="92e5d-124">Операция logoff прошла успешно.</span><span class="sxs-lookup"><span data-stu-id="92e5d-124">The logoff operation was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="92e5d-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="92e5d-125">Remarks</span></span>

<span data-ttu-id="92e5d-126">Метод **IMAPISession::Logoff** завершает сеанс MAPI.</span><span class="sxs-lookup"><span data-stu-id="92e5d-126">The **IMAPISession::Logoff** method ends a MAPI session.</span></span> <span data-ttu-id="92e5d-127">Когда **logoff** возвращается, ни один из методов, кроме [IUnknown::Release,](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) не может быть вызван.</span><span class="sxs-lookup"><span data-stu-id="92e5d-127">When **Logoff** returns, none of the methods except for [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) can be called.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="92e5d-128">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="92e5d-128">Notes to callers</span></span>

<span data-ttu-id="92e5d-129">Когда **logoff** возвращается, отпустите объект сеанса, вызывая его **метод IUnknown::Release.**</span><span class="sxs-lookup"><span data-stu-id="92e5d-129">When **Logoff** returns, release the session object by calling its **IUnknown::Release** method.</span></span> 
  
<span data-ttu-id="92e5d-130">Дополнительные сведения о завершении сеанса см. в под [вопросе "Завершение сеанса MAPI".](ending-a-mapi-session.md)</span><span class="sxs-lookup"><span data-stu-id="92e5d-130">For more information about ending a session, see [Ending a MAPI Session](ending-a-mapi-session.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="92e5d-131">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="92e5d-131">MFCMAPI reference</span></span>

<span data-ttu-id="92e5d-132">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="92e5d-132">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="92e5d-133">**Файл**</span><span class="sxs-lookup"><span data-stu-id="92e5d-133">**File**</span></span>|<span data-ttu-id="92e5d-134">**Функция**</span><span class="sxs-lookup"><span data-stu-id="92e5d-134">**Function**</span></span>|<span data-ttu-id="92e5d-135">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="92e5d-135">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="92e5d-136">MAPIObjects.cpp</span><span class="sxs-lookup"><span data-stu-id="92e5d-136">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="92e5d-137">CMapiObjects::Logoff</span><span class="sxs-lookup"><span data-stu-id="92e5d-137">CMapiObjects::Logoff</span></span>  <br/> |<span data-ttu-id="92e5d-138">MFCMAPI использует метод **IMAPISession::Logoff** для выхода из сеанса перед его освобождением.</span><span class="sxs-lookup"><span data-stu-id="92e5d-138">MFCMAPI uses the **IMAPISession::Logoff** method to log off from the session before releasing it.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="92e5d-139">Из-за быстрого завершения работы, введенного в Microsoft Office Outlook 2007 Пакет обновления 2, Microsoft Outlook 2010, русская версия и Microsoft Outlook 2013, клиенты никогда не должны передавать параметр **MAPI_LOGOFF_SHARED** [iMAPISession::Logoff](imapisession-logoff.md).</span><span class="sxs-lookup"><span data-stu-id="92e5d-139">Due to the fast shutdown behavior introduced in Microsoft Office Outlook 2007 Service Pack 2, Microsoft Outlook 2010, and Microsoft Outlook 2013, clients should never pass the **MAPI_LOGOFF_SHARED** parameter to [IMAPISession::Logoff](imapisession-logoff.md).</span></span> <span data-ttu-id="92e5d-140">Передача **MAPI_LOGOFF_SHARED** приведет к тому, что все клиенты MAPI начнут работу и произойдет непредвиденное поведение.</span><span class="sxs-lookup"><span data-stu-id="92e5d-140">Passing **MAPI_LOGOFF_SHARED** will cause all MAPI clients to begin shutdown and unexpected behavior will occur.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="92e5d-141">См. также</span><span class="sxs-lookup"><span data-stu-id="92e5d-141">See also</span></span>



[<span data-ttu-id="92e5d-142">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="92e5d-142">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="92e5d-143">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="92e5d-143">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="92e5d-144">Завершение сеанса MAPI</span><span class="sxs-lookup"><span data-stu-id="92e5d-144">Ending a MAPI Session</span></span>](ending-a-mapi-session.md)

