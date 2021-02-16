---
title: HrGetAutoDiscoverXML
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrGetAutoDiscoverXML
api_type:
- COM
ms.assetid: 03691187-7c65-620b-576f-6ebe62a80830
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 77f28654ffe0f6f459fde229bb7428f2c39e96c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347805"
---
# <a name="hrgetautodiscoverxml"></a><span data-ttu-id="f11d4-103">HrGetAutoDiscoverXML</span><span class="sxs-lookup"><span data-stu-id="f11d4-103">HrGetAutoDiscoverXML</span></span>

  
  
<span data-ttu-id="f11d4-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f11d4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f11d4-105">Возвращает поток XML, который представляет сведения, полученные из службы автоматического обнаружения сервера Microsoft Exchange 2007.</span><span class="sxs-lookup"><span data-stu-id="f11d4-105">Returns an Extensible Markup Language (XML) stream that represents information retrieved from the auto-discovery service of a Microsoft Exchange 2007 server.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f11d4-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="f11d4-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f11d4-107">Экспортируется с помощью:</span><span class="sxs-lookup"><span data-stu-id="f11d4-107">Exported by:</span></span>  <br/> |<span data-ttu-id="f11d4-108">olmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="f11d4-108">olmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="f11d4-109">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="f11d4-109">Called by:</span></span>  <br/> |<span data-ttu-id="f11d4-110">Клиент</span><span class="sxs-lookup"><span data-stu-id="f11d4-110">Client</span></span>  <br/> |
|<span data-ttu-id="f11d4-111">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="f11d4-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="f11d4-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="f11d4-112">Outlook</span></span>  <br/> |
   
```cpp
HRESULT HrGetAutoDiscoverXML( 
    __in_z const WCHAR *pwzAddress, 
    __in_opt_z const WCHAR *pwzPassword, 
    __in_opt HANDLE hCancelEvent, 
    __in_opt ULONG ulFlags, 
    __out IStream** ppXmlStream); 

```

## <a name="parameters"></a><span data-ttu-id="f11d4-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="f11d4-113">Parameters</span></span>

 <span data-ttu-id="f11d4-114">_pwzAddress_</span><span class="sxs-lookup"><span data-stu-id="f11d4-114">_pwzAddress_</span></span>
  
> <span data-ttu-id="f11d4-115">[in] SmTP-адрес электронной почты учетной записи, для которой необходимо получить сведения об автоматическом обнаружении.</span><span class="sxs-lookup"><span data-stu-id="f11d4-115">[in] A null-terminated Simple Mail Transfer Protocol (SMTP) email address of the account for which you want to retrieve the auto-discovery information.</span></span>
    
 <span data-ttu-id="f11d4-116">_pwzPassword_</span><span class="sxs-lookup"><span data-stu-id="f11d4-116">_pwzPassword_</span></span>
  
> <span data-ttu-id="f11d4-117">[in] Необязательный пароль для учетной записи, указанной _pwzAddress._</span><span class="sxs-lookup"><span data-stu-id="f11d4-117">[in] An optional password for the account specified by  _pwzAddress_.</span></span> <span data-ttu-id="f11d4-118">Обратите внимание, что передача пароля не действует, если учетная запись, указанная  _pwzAddress,_ не требует пароля.</span><span class="sxs-lookup"><span data-stu-id="f11d4-118">Note that passing any password has no effect if the account specified by  _pwzAddress_ does not require a password.</span></span> 
    
 <span data-ttu-id="f11d4-119">_hCancelEvent_</span><span class="sxs-lookup"><span data-stu-id="f11d4-119">_hCancelEvent_</span></span>
  
> <span data-ttu-id="f11d4-120">[in] Unset Win32 event handle that is optional and can be used to cancel the operation.</span><span class="sxs-lookup"><span data-stu-id="f11d4-120">[in] An unset Win32 event handle that is optional and can be used to cancel the operation.</span></span> <span data-ttu-id="f11d4-121">Чтобы отменить операцию, задав событие и передав его в качестве  _hCancelEvent;_ если **вы** не хотите отменять операцию, передав ее null.</span><span class="sxs-lookup"><span data-stu-id="f11d4-121">To cancel the operation, set the event and pass the event handle as  _hCancelEvent_; pass **null** if you do not want to cancel the operation.</span></span> <span data-ttu-id="f11d4-122">Обратите внимание, что передача значения, не представляюющего окне события, не оказывает влияния и игнорируется функцией.</span><span class="sxs-lookup"><span data-stu-id="f11d4-122">Note that passing a value that does not represent an event handle has no effect and is ignored by the function.</span></span> 
    
 <span data-ttu-id="f11d4-123">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f11d4-123">_ulFlags_</span></span>
  
> <span data-ttu-id="f11d4-124">[in] Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="f11d4-124">[in] This parameter is not used.</span></span> <span data-ttu-id="f11d4-125">Должно быть 0.</span><span class="sxs-lookup"><span data-stu-id="f11d4-125">It must be 0.</span></span>
    
 <span data-ttu-id="f11d4-126">_ppXmlStream_</span><span class="sxs-lookup"><span data-stu-id="f11d4-126">_ppXmlStream_</span></span>
  
> <span data-ttu-id="f11d4-127">[out] Указатель на объект [IStream,](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) содержащий XML автооружения.</span><span class="sxs-lookup"><span data-stu-id="f11d4-127">[out] A pointer to an [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object that contains the autodiscovery XML.</span></span> <span data-ttu-id="f11d4-128">Возвращает **null в** случае сбой операции автооружия.</span><span class="sxs-lookup"><span data-stu-id="f11d4-128">Returns **null** if the autodiscovery operation fails.</span></span> <span data-ttu-id="f11d4-129">После завершения его необходимо освободить объект [IStream.](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f11d4-129">You must release the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object when you are finished with it.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="f11d4-130">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="f11d4-130">Return values</span></span>

<span data-ttu-id="f11d4-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="f11d4-131">S_OK</span></span> 
  
- <span data-ttu-id="f11d4-132">Вызов функции успешно.</span><span class="sxs-lookup"><span data-stu-id="f11d4-132">The function call is successful.</span></span>
    
<span data-ttu-id="f11d4-133">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="f11d4-133">E_INVALIDARG</span></span> 
  
-  <span data-ttu-id="f11d4-134">_pwzAddress_ имеет **null** или не является допустимым SMTP-адресом, или _ppXmlStream_ — это **null-указатель** на [объект IStream.](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f11d4-134">_pwzAddress_ is **null** or is not a valid SMTP address, or  _ppXmlStream_ is a **null** pointer to an [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object.</span></span> 
    
<span data-ttu-id="f11d4-135">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="f11d4-135">MAPI_E_NOT_FOUND</span></span> 
  
- <span data-ttu-id="f11d4-136">Клиентский компьютер не подключен к сети, клиентский компьютер не подключен к серверу Microsoft Exchange 2007,  _pwzAddress_ не является учетной записью на сервере Exchange 2007 или  _pwzAddress_ — это учетная запись, которая не поддерживает службу автоматического обнаружения Exchange.</span><span class="sxs-lookup"><span data-stu-id="f11d4-136">Client computer is not connected to the network, client computer is not connected to a Microsoft Exchange 2007 server,  _pwzAddress_ is not an account on an Exchange 2007 server, or  _pwzAddress_ is an account that does not support Exchange auto-discovery service.</span></span> 
    
<span data-ttu-id="f11d4-137">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="f11d4-137">MAPI_E_USER_CANCEL</span></span> 
  
- <span data-ttu-id="f11d4-138">Для отмены операции в  _hCancelEvent_ передан работка события.</span><span class="sxs-lookup"><span data-stu-id="f11d4-138">An event handle has been passed to  _hCancelEvent_ to cancel the operation.</span></span> 
    
<span data-ttu-id="f11d4-139">STRSAFE_E_INSUFFICIENT_BUFFER</span><span class="sxs-lookup"><span data-stu-id="f11d4-139">STRSAFE_E_INSUFFICIENT_BUFFER</span></span>
  
- <span data-ttu-id="f11d4-140">Значение, передаваемого  _в pwzAddress_ или  _pwzPassword,_ слишком длинное, чтобы оно переполнило внутренний буфер размером 256байт.</span><span class="sxs-lookup"><span data-stu-id="f11d4-140">The value passed to  _pwzAddress_ or  _pwzPassword_ is too long, such that it overflows the internal buffer of size 256 bytes.</span></span> 
    

