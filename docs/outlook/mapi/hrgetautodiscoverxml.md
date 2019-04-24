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
# <a name="hrgetautodiscoverxml"></a><span data-ttu-id="4d817-103">HrGetAutoDiscoverXML</span><span class="sxs-lookup"><span data-stu-id="4d817-103">HrGetAutoDiscoverXML</span></span>

  
  
<span data-ttu-id="4d817-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d817-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4d817-105">Возвращает XML-поток, представляющий информацию, полученную из службы автоматического обнаружения сервера Microsoft Exchange 2007.</span><span class="sxs-lookup"><span data-stu-id="4d817-105">Returns an Extensible Markup Language (XML) stream that represents information retrieved from the auto-discovery service of a Microsoft Exchange 2007 server.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="4d817-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="4d817-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4d817-107">Экспортировано:</span><span class="sxs-lookup"><span data-stu-id="4d817-107">Exported by:</span></span>  <br/> |<span data-ttu-id="4d817-108">olmapi32. dll</span><span class="sxs-lookup"><span data-stu-id="4d817-108">olmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="4d817-109">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="4d817-109">Called by:</span></span>  <br/> |<span data-ttu-id="4d817-110">Клиент</span><span class="sxs-lookup"><span data-stu-id="4d817-110">Client</span></span>  <br/> |
|<span data-ttu-id="4d817-111">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="4d817-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="4d817-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="4d817-112">Outlook</span></span>  <br/> |
   
```cpp
HRESULT HrGetAutoDiscoverXML( 
    __in_z const WCHAR *pwzAddress, 
    __in_opt_z const WCHAR *pwzPassword, 
    __in_opt HANDLE hCancelEvent, 
    __in_opt ULONG ulFlags, 
    __out IStream** ppXmlStream); 

```

## <a name="parameters"></a><span data-ttu-id="4d817-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="4d817-113">Parameters</span></span>

 <span data-ttu-id="4d817-114">_Пвзаддресс_</span><span class="sxs-lookup"><span data-stu-id="4d817-114">_pwzAddress_</span></span>
  
> <span data-ttu-id="4d817-115">возврата SMTP-адрес электронной почты с завершающим нулем для учетной записи, для которой требуется получить сведения об автоматическом обнаружении.</span><span class="sxs-lookup"><span data-stu-id="4d817-115">[in] A null-terminated Simple Mail Transfer Protocol (SMTP) email address of the account for which you want to retrieve the auto-discovery information.</span></span>
    
 <span data-ttu-id="4d817-116">_Пвзпассворд_</span><span class="sxs-lookup"><span data-stu-id="4d817-116">_pwzPassword_</span></span>
  
> <span data-ttu-id="4d817-117">возврата Необязательный пароль для учетной записи, указанной в параметре _пвзаддресс_.</span><span class="sxs-lookup"><span data-stu-id="4d817-117">[in] An optional password for the account specified by  _pwzAddress_.</span></span> <span data-ttu-id="4d817-118">Обратите внимание на то, что передача любого пароля не действует, если учетная запись, указанная в _пвзаддресс_ , не требует пароля.</span><span class="sxs-lookup"><span data-stu-id="4d817-118">Note that passing any password has no effect if the account specified by  _pwzAddress_ does not require a password.</span></span> 
    
 <span data-ttu-id="4d817-119">_Хканцелевент_</span><span class="sxs-lookup"><span data-stu-id="4d817-119">_hCancelEvent_</span></span>
  
> <span data-ttu-id="4d817-120">возврата Необязательный дескриптор события Win32, который можно использовать для отмены операции.</span><span class="sxs-lookup"><span data-stu-id="4d817-120">[in] An unset Win32 event handle that is optional and can be used to cancel the operation.</span></span> <span data-ttu-id="4d817-121">Чтобы отменить операцию, задайте событие и передайте обработчик события как _хканцелевент_; Если не нужно отменять операцию, передается **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="4d817-121">To cancel the operation, set the event and pass the event handle as  _hCancelEvent_; pass **null** if you do not want to cancel the operation.</span></span> <span data-ttu-id="4d817-122">Обратите внимание, что передача значения, не представляющего дескриптор события, не оказывает влияния и игнорируется функцией.</span><span class="sxs-lookup"><span data-stu-id="4d817-122">Note that passing a value that does not represent an event handle has no effect and is ignored by the function.</span></span> 
    
 <span data-ttu-id="4d817-123">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4d817-123">_ulFlags_</span></span>
  
> <span data-ttu-id="4d817-124">возврата Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="4d817-124">[in] This parameter is not used.</span></span> <span data-ttu-id="4d817-125">Значение должно быть равно 0.</span><span class="sxs-lookup"><span data-stu-id="4d817-125">It must be 0.</span></span>
    
 <span data-ttu-id="4d817-126">_Ппксмлстреам_</span><span class="sxs-lookup"><span data-stu-id="4d817-126">_ppXmlStream_</span></span>
  
> <span data-ttu-id="4d817-127">вышли Указатель на объект [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) , который содержит XML-код автообнаружения.</span><span class="sxs-lookup"><span data-stu-id="4d817-127">[out] A pointer to an [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object that contains the autodiscovery XML.</span></span> <span data-ttu-id="4d817-128">Возвращает **значение NULL** , если операция автообнаружения завершается с ошибкой.</span><span class="sxs-lookup"><span data-stu-id="4d817-128">Returns **null** if the autodiscovery operation fails.</span></span> <span data-ttu-id="4d817-129">После завершения работы с объектом [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) необходимо освободить его.</span><span class="sxs-lookup"><span data-stu-id="4d817-129">You must release the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object when you are finished with it.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="4d817-130">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="4d817-130">Return values</span></span>

<span data-ttu-id="4d817-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="4d817-131">S_OK</span></span> 
  
- <span data-ttu-id="4d817-132">Вызов функции выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="4d817-132">The function call is successful.</span></span>
    
<span data-ttu-id="4d817-133">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="4d817-133">E_INVALIDARG</span></span> 
  
-  <span data-ttu-id="4d817-134">_пвзаддресс_ имеет **значение NULL** или не является допустимым SMTP-адресом, или _ппксмлстреам_ является **нулевым** указателем на объект [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4d817-134">_pwzAddress_ is **null** or is not a valid SMTP address, or  _ppXmlStream_ is a **null** pointer to an [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) object.</span></span> 
    
<span data-ttu-id="4d817-135">МАПИ_Е_НОТ_ФАУНД</span><span class="sxs-lookup"><span data-stu-id="4d817-135">MAPI_E_NOT_FOUND</span></span> 
  
- <span data-ttu-id="4d817-136">Клиентский компьютер не подключен к сети, клиентский компьютер не подключен к серверу Microsoft Exchange 2007, _пвзаддресс_ не является учетной записью на сервере Exchange 2007, или _пвзаддресс_ — это учетная запись, которая не поддерживает Exchange Служба автоматического обнаружения.</span><span class="sxs-lookup"><span data-stu-id="4d817-136">Client computer is not connected to the network, client computer is not connected to a Microsoft Exchange 2007 server,  _pwzAddress_ is not an account on an Exchange 2007 server, or  _pwzAddress_ is an account that does not support Exchange auto-discovery service.</span></span> 
    
<span data-ttu-id="4d817-137">МАПИ_Е_УСЕР_КАНЦЕЛ</span><span class="sxs-lookup"><span data-stu-id="4d817-137">MAPI_E_USER_CANCEL</span></span> 
  
- <span data-ttu-id="4d817-138">Для отмены операции в _хканцелевент_ был передан дескриптор события.</span><span class="sxs-lookup"><span data-stu-id="4d817-138">An event handle has been passed to  _hCancelEvent_ to cancel the operation.</span></span> 
    
<span data-ttu-id="4d817-139">СТРСАФЕ_Е_ИНСУФФИЦИЕНТ_БУФФЕР</span><span class="sxs-lookup"><span data-stu-id="4d817-139">STRSAFE_E_INSUFFICIENT_BUFFER</span></span>
  
- <span data-ttu-id="4d817-140">Значение, переданное в _пвзаддресс_ или _пвзпассворд_ , имеет слишком большую длину, так как оно вызывает переполнение внутреннего буфера размером 256 байт.</span><span class="sxs-lookup"><span data-stu-id="4d817-140">The value passed to  _pwzAddress_ or  _pwzPassword_ is too long, such that it overflows the internal buffer of size 256 bytes.</span></span> 
    

