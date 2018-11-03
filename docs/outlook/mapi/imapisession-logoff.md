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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399650"
---
# <a name="imapisessionlogoff"></a><span data-ttu-id="32933-103">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="32933-103">IMAPISession::Logoff</span></span>

  
  
<span data-ttu-id="32933-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="32933-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="32933-105">Завершение сеанса MAPI.</span><span class="sxs-lookup"><span data-stu-id="32933-105">Ends a MAPI session.</span></span>
  
```cpp
HRESULT Logoff(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG ulReserved
);
```

## <a name="parameters"></a><span data-ttu-id="32933-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="32933-106">Parameters</span></span>

 <span data-ttu-id="32933-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="32933-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="32933-108">[in] Дескриптор родительского окна все диалоговые окна или окна для отображения.</span><span class="sxs-lookup"><span data-stu-id="32933-108">[in] A handle to the parent window of any dialog boxes or windows to be displayed.</span></span> <span data-ttu-id="32933-109">Этот параметр игнорируется, если флаг MAPI_LOGOFF_UI не установлен.</span><span class="sxs-lookup"><span data-stu-id="32933-109">This parameter is ignored if the MAPI_LOGOFF_UI flag is not set.</span></span>
    
 <span data-ttu-id="32933-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="32933-110">_ulFlags_</span></span>
  
> <span data-ttu-id="32933-111">[in] Битовая маска флаги, определяющие операции выхода из системы.</span><span class="sxs-lookup"><span data-stu-id="32933-111">[in] A bitmask of flags that control the logoff operation.</span></span> <span data-ttu-id="32933-112">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="32933-112">The following flags can be set:</span></span>
    
<span data-ttu-id="32933-113">MAPI_LOGOFF_SHARED</span><span class="sxs-lookup"><span data-stu-id="32933-113">MAPI_LOGOFF_SHARED</span></span> 
  
> <span data-ttu-id="32933-114">Если этот сеанс является общей, все клиенты, войти в систему с помощью общего сеанса уведомляться об выхода из системы в процессе выполнения.</span><span class="sxs-lookup"><span data-stu-id="32933-114">If this session is shared, all clients that logged on by using the shared session should be notified of the logoff in progress.</span></span> <span data-ttu-id="32933-115">Клиенты должны выйти из системы.</span><span class="sxs-lookup"><span data-stu-id="32933-115">The clients should log off.</span></span> <span data-ttu-id="32933-116">Каждый клиент, который использует совместный сеанс можно задать этот флаг.</span><span class="sxs-lookup"><span data-stu-id="32933-116">Any client that is using the shared session can set this flag.</span></span> <span data-ttu-id="32933-117">MAPI_LOGOFF_SHARED игнорируется, если не общий текущего сеанса.</span><span class="sxs-lookup"><span data-stu-id="32933-117">MAPI_LOGOFF_SHARED is ignored if the current session is not shared.</span></span>
    
<span data-ttu-id="32933-118">MAPI_LOGOFF_UI</span><span class="sxs-lookup"><span data-stu-id="32933-118">MAPI_LOGOFF_UI</span></span> 
  
> <span data-ttu-id="32933-119">**Выход из системы** может отображать диалоговое окно во время операции, возможно запросом на подтверждение.</span><span class="sxs-lookup"><span data-stu-id="32933-119">**Logoff** can display a dialog box during the operation, possibly prompting the user for confirmation.</span></span> 
    
 <span data-ttu-id="32933-120">_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="32933-120">_ulReserved_</span></span>
  
> <span data-ttu-id="32933-121">[in] ���������������; ������ ���� ����� ����.</span><span class="sxs-lookup"><span data-stu-id="32933-121">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="32933-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="32933-122">Return value</span></span>

<span data-ttu-id="32933-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="32933-123">S_OK</span></span> 
  
> <span data-ttu-id="32933-124">Выход из системы операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="32933-124">The logoff operation was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="32933-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="32933-125">Remarks</span></span>

<span data-ttu-id="32933-126">Метод **IMAPISession::Logoff** завершает сеанс MAPI.</span><span class="sxs-lookup"><span data-stu-id="32933-126">The **IMAPISession::Logoff** method ends a MAPI session.</span></span> <span data-ttu-id="32933-127">При возврате **выхода из системы** , ни один из методов, за исключением [функции IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) может быть вызван.</span><span class="sxs-lookup"><span data-stu-id="32933-127">When **Logoff** returns, none of the methods except for [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) can be called.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="32933-128">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="32933-128">Notes to callers</span></span>

<span data-ttu-id="32933-129">При возврате **выхода из системы** , release путем вызова метода **функции IUnknown::Release** объект сеанса.</span><span class="sxs-lookup"><span data-stu-id="32933-129">When **Logoff** returns, release the session object by calling its **IUnknown::Release** method.</span></span> 
  
<span data-ttu-id="32933-130">Дополнительные сведения о завершении сеанса можно [Завершение сеанса MAPI](ending-a-mapi-session.md).</span><span class="sxs-lookup"><span data-stu-id="32933-130">For more information about ending a session, see [Ending a MAPI Session](ending-a-mapi-session.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="32933-131">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="32933-131">MFCMAPI reference</span></span>

<span data-ttu-id="32933-132">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="32933-132">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="32933-133">**Файл**</span><span class="sxs-lookup"><span data-stu-id="32933-133">**File**</span></span>|<span data-ttu-id="32933-134">**Функция**</span><span class="sxs-lookup"><span data-stu-id="32933-134">**Function**</span></span>|<span data-ttu-id="32933-135">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="32933-135">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="32933-136">MAPIObjects.cpp</span><span class="sxs-lookup"><span data-stu-id="32933-136">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="32933-137">CMapiObjects::Logoff</span><span class="sxs-lookup"><span data-stu-id="32933-137">CMapiObjects::Logoff</span></span>  <br/> |<span data-ttu-id="32933-138">Mfcmapi (en) использует метод **IMAPISession::Logoff** для сеанса перед выпуском его.</span><span class="sxs-lookup"><span data-stu-id="32933-138">MFCMAPI uses the **IMAPISession::Logoff** method to log off from the session before releasing it.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="32933-139">Из-за быстрого завершения работы, введенные в пакет обновления 2 для Microsoft Office Outlook 2007, Microsoft Outlook 2010 и Microsoft Outlook 2013 клиенты никогда не следует передавать параметр **MAPI_LOGOFF_SHARED** в [IMAPISession::Logoff](imapisession-logoff.md).</span><span class="sxs-lookup"><span data-stu-id="32933-139">Due to the fast shutdown behavior introduced in Microsoft Office Outlook 2007 Service Pack 2, Microsoft Outlook 2010, and Microsoft Outlook 2013, clients should never pass the **MAPI_LOGOFF_SHARED** parameter to [IMAPISession::Logoff](imapisession-logoff.md).</span></span> <span data-ttu-id="32933-140">Передача **MAPI_LOGOFF_SHARED** вызывает все клиенты MAPI приступить к завершению работы и будет привести к возникновению проблем.</span><span class="sxs-lookup"><span data-stu-id="32933-140">Passing **MAPI_LOGOFF_SHARED** will cause all MAPI clients to begin shutdown and unexpected behavior will occur.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="32933-141">См. также</span><span class="sxs-lookup"><span data-stu-id="32933-141">See also</span></span>



[<span data-ttu-id="32933-142">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="32933-142">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="32933-143">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="32933-143">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="32933-144">Завершение сеанса MAPI</span><span class="sxs-lookup"><span data-stu-id="32933-144">Ending a MAPI Session</span></span>](ending-a-mapi-session.md)

