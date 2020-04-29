---
title: имаписессионлогофф
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
# <a name="imapisessionlogoff"></a><span data-ttu-id="e6b2f-103">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="e6b2f-103">IMAPISession::Logoff</span></span>

  
  
<span data-ttu-id="e6b2f-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e6b2f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e6b2f-105">Завершает сеанс MAPI.</span><span class="sxs-lookup"><span data-stu-id="e6b2f-105">Ends a MAPI session.</span></span>
  
```cpp
HRESULT Logoff(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG ulReserved
);
```

## <a name="parameters"></a><span data-ttu-id="e6b2f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e6b2f-106">Parameters</span></span>

 <span data-ttu-id="e6b2f-107">_улуипарам_</span><span class="sxs-lookup"><span data-stu-id="e6b2f-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="e6b2f-108">возврата Дескриптор родительского окна всех диалоговых окон и окон, которые должны отображаться.</span><span class="sxs-lookup"><span data-stu-id="e6b2f-108">[in] A handle to the parent window of any dialog boxes or windows to be displayed.</span></span> <span data-ttu-id="e6b2f-109">Этот параметр игнорируется, если не установлен флаг MAPI_LOGOFF_UI.</span><span class="sxs-lookup"><span data-stu-id="e6b2f-109">This parameter is ignored if the MAPI_LOGOFF_UI flag is not set.</span></span>
    
 <span data-ttu-id="e6b2f-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e6b2f-110">_ulFlags_</span></span>
  
> <span data-ttu-id="e6b2f-111">возврата Битовая маска флагов, которые контролируют операцию выхода.</span><span class="sxs-lookup"><span data-stu-id="e6b2f-111">[in] A bitmask of flags that control the logoff operation.</span></span> <span data-ttu-id="e6b2f-112">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="e6b2f-112">The following flags can be set:</span></span>
    
<span data-ttu-id="e6b2f-113">MAPI_LOGOFF_SHARED</span><span class="sxs-lookup"><span data-stu-id="e6b2f-113">MAPI_LOGOFF_SHARED</span></span> 
  
> <span data-ttu-id="e6b2f-114">Если этот сеанс является общим, все клиенты, выполнившие вход с использованием общего сеанса, должны получать уведомления о выходе из системы.</span><span class="sxs-lookup"><span data-stu-id="e6b2f-114">If this session is shared, all clients that logged on by using the shared session should be notified of the logoff in progress.</span></span> <span data-ttu-id="e6b2f-115">Клиенты должны выйти из системы.</span><span class="sxs-lookup"><span data-stu-id="e6b2f-115">The clients should log off.</span></span> <span data-ttu-id="e6b2f-116">Этот флаг может устанавливать любой клиент, использующий общий сеанс.</span><span class="sxs-lookup"><span data-stu-id="e6b2f-116">Any client that is using the shared session can set this flag.</span></span> <span data-ttu-id="e6b2f-117">MAPI_LOGOFF_SHARED игнорируется, если текущий сеанс не является общим.</span><span class="sxs-lookup"><span data-stu-id="e6b2f-117">MAPI_LOGOFF_SHARED is ignored if the current session is not shared.</span></span>
    
<span data-ttu-id="e6b2f-118">MAPI_LOGOFF_UI</span><span class="sxs-lookup"><span data-stu-id="e6b2f-118">MAPI_LOGOFF_UI</span></span> 
  
> <span data-ttu-id="e6b2f-119">При **выходе из системы** во время операции выводится диалоговое окно, которое может запрашивать подтверждение у пользователя.</span><span class="sxs-lookup"><span data-stu-id="e6b2f-119">**Logoff** can display a dialog box during the operation, possibly prompting the user for confirmation.</span></span> 
    
 <span data-ttu-id="e6b2f-120">_улресервед_</span><span class="sxs-lookup"><span data-stu-id="e6b2f-120">_ulReserved_</span></span>
  
> <span data-ttu-id="e6b2f-121">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="e6b2f-121">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e6b2f-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e6b2f-122">Return value</span></span>

<span data-ttu-id="e6b2f-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="e6b2f-123">S_OK</span></span> 
  
> <span data-ttu-id="e6b2f-124">Операция выхода выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="e6b2f-124">The logoff operation was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e6b2f-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="e6b2f-125">Remarks</span></span>

<span data-ttu-id="e6b2f-126">Метод **IMAPISession:: logoff** ЗАВЕРШАЕТ сеанс MAPI.</span><span class="sxs-lookup"><span data-stu-id="e6b2f-126">The **IMAPISession::Logoff** method ends a MAPI session.</span></span> <span data-ttu-id="e6b2f-127">При возвращении после **выхода** ни один из методов, кроме [IUnknown::](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) , не может быть вызван.</span><span class="sxs-lookup"><span data-stu-id="e6b2f-127">When **Logoff** returns, none of the methods except for [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) can be called.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="e6b2f-128">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="e6b2f-128">Notes to callers</span></span>

<span data-ttu-id="e6b2f-129">При **выходе из системы** выпустите объект Session, вызвав его метод **IUnknown:: Release** .</span><span class="sxs-lookup"><span data-stu-id="e6b2f-129">When **Logoff** returns, release the session object by calling its **IUnknown::Release** method.</span></span> 
  
<span data-ttu-id="e6b2f-130">Для получения дополнительных сведений о завершении сеанса обратитесь [к разделу завершение сеанса MAPI](ending-a-mapi-session.md).</span><span class="sxs-lookup"><span data-stu-id="e6b2f-130">For more information about ending a session, see [Ending a MAPI Session](ending-a-mapi-session.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="e6b2f-131">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e6b2f-131">MFCMAPI reference</span></span>

<span data-ttu-id="e6b2f-132">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="e6b2f-132">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e6b2f-133">**Файл**</span><span class="sxs-lookup"><span data-stu-id="e6b2f-133">**File**</span></span>|<span data-ttu-id="e6b2f-134">**Функция**</span><span class="sxs-lookup"><span data-stu-id="e6b2f-134">**Function**</span></span>|<span data-ttu-id="e6b2f-135">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="e6b2f-135">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e6b2f-136">Мапиобжектс. cpp</span><span class="sxs-lookup"><span data-stu-id="e6b2f-136">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="e6b2f-137">Кмапиобжектс:: выход</span><span class="sxs-lookup"><span data-stu-id="e6b2f-137">CMapiObjects::Logoff</span></span>  <br/> |<span data-ttu-id="e6b2f-138">MFCMAPI использует метод **IMAPISession:: logoff** для выхода из сеанса перед его освобождением.</span><span class="sxs-lookup"><span data-stu-id="e6b2f-138">MFCMAPI uses the **IMAPISession::Logoff** method to log off from the session before releasing it.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="e6b2f-139">Из-за возможности быстрого завершения работы, появившегося в Microsoft Office Outlook 2007 с пакетом обновления 2, Microsoft Outlook 2010 и Microsoft Outlook 2013, клиенты никогда не должны передавать параметр **MAPI_LOGOFF_SHARED** в [IMAPISession:: LOGOFF](imapisession-logoff.md).</span><span class="sxs-lookup"><span data-stu-id="e6b2f-139">Due to the fast shutdown behavior introduced in Microsoft Office Outlook 2007 Service Pack 2, Microsoft Outlook 2010, and Microsoft Outlook 2013, clients should never pass the **MAPI_LOGOFF_SHARED** parameter to [IMAPISession::Logoff](imapisession-logoff.md).</span></span> <span data-ttu-id="e6b2f-140">Передача **MAPI_LOGOFF_SHARED** приведет к тому, что все клиенты MAPI начнут завершать работу и произойдет неожиданное поведение.</span><span class="sxs-lookup"><span data-stu-id="e6b2f-140">Passing **MAPI_LOGOFF_SHARED** will cause all MAPI clients to begin shutdown and unexpected behavior will occur.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e6b2f-141">См. также</span><span class="sxs-lookup"><span data-stu-id="e6b2f-141">See also</span></span>



[<span data-ttu-id="e6b2f-142">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e6b2f-142">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="e6b2f-143">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="e6b2f-143">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="e6b2f-144">Завершение сеанса MAPI</span><span class="sxs-lookup"><span data-stu-id="e6b2f-144">Ending a MAPI Session</span></span>](ending-a-mapi-session.md)

