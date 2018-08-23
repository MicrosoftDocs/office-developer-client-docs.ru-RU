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
ms.openlocfilehash: 490c834ee63c158b3f9c0e34f8de7f582c650bc4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584067"
---
# <a name="hrgetautodiscoverxml"></a><span data-ttu-id="30fc5-103">HrGetAutoDiscoverXML</span><span class="sxs-lookup"><span data-stu-id="30fc5-103">HrGetAutoDiscoverXML</span></span>

  
  
<span data-ttu-id="30fc5-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="30fc5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="30fc5-105">Возвращает поток языке (XML), который представляет данные, полученные из службы автоматического обнаружения сервера Microsoft Exchange 2007.</span><span class="sxs-lookup"><span data-stu-id="30fc5-105">Returns an Extensible Markup Language (XML) stream that represents information retrieved from the auto-discovery service of a Microsoft Exchange 2007 server.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="30fc5-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="30fc5-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="30fc5-107">Экспортировать с:</span><span class="sxs-lookup"><span data-stu-id="30fc5-107">Exported by:</span></span>  <br/> |<span data-ttu-id="30fc5-108">olmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="30fc5-108">olmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="30fc5-109">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="30fc5-109">Called by:</span></span>  <br/> |<span data-ttu-id="30fc5-110">Клиент</span><span class="sxs-lookup"><span data-stu-id="30fc5-110">Client</span></span>  <br/> |
|<span data-ttu-id="30fc5-111">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="30fc5-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="30fc5-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="30fc5-112">Outlook</span></span>  <br/> |
   
```cpp
HRESULT HrGetAutoDiscoverXML( 
    __in_z const WCHAR *pwzAddress, 
    __in_opt_z const WCHAR *pwzPassword, 
    __in_opt HANDLE hCancelEvent, 
    __in_opt ULONG ulFlags, 
    __out IStream** ppXmlStream); 

```

## <a name="parameters"></a><span data-ttu-id="30fc5-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="30fc5-113">Parameters</span></span>

 <span data-ttu-id="30fc5-114">_pwzAddress_</span><span class="sxs-lookup"><span data-stu-id="30fc5-114">_pwzAddress_</span></span>
  
> <span data-ttu-id="30fc5-115">[in] Символом null Simple Mail Transfer Protocol (SMTP) адрес электронной почты учетной записи, для которого требуется извлечь данные автоматического обнаружения.</span><span class="sxs-lookup"><span data-stu-id="30fc5-115">[in] A null-terminated Simple Mail Transfer Protocol (SMTP) email address of the account for which you want to retrieve the auto-discovery information.</span></span>
    
 <span data-ttu-id="30fc5-116">_pwzPassword_</span><span class="sxs-lookup"><span data-stu-id="30fc5-116">_pwzPassword_</span></span>
  
> <span data-ttu-id="30fc5-117">[in] Необязательный пароль для учетной записи, указанной с _pwzAddress_.</span><span class="sxs-lookup"><span data-stu-id="30fc5-117">[in] An optional password for the account specified by  _pwzAddress_.</span></span> <span data-ttu-id="30fc5-118">Обратите внимание, что передача любой пароль не оказывает влияния, если пароль учетной записи, указанной с _pwzAddress_ не требуется.</span><span class="sxs-lookup"><span data-stu-id="30fc5-118">Note that passing any password has no effect if the account specified by  _pwzAddress_ does not require a password.</span></span> 
    
 <span data-ttu-id="30fc5-119">_hCancelEvent_</span><span class="sxs-lookup"><span data-stu-id="30fc5-119">_hCancelEvent_</span></span>
  
> <span data-ttu-id="30fc5-120">[in] Удаление Win32 обработчика событий, который является необязательной и позволяет отменить операцию.</span><span class="sxs-lookup"><span data-stu-id="30fc5-120">[in] An unset Win32 event handle that is optional and can be used to cancel the operation.</span></span> <span data-ttu-id="30fc5-121">Чтобы отменить операцию установки события и передать как обработчик события в качестве _hCancelEvent_; Передайте **значение null** , если вы не хотите отменить операцию.</span><span class="sxs-lookup"><span data-stu-id="30fc5-121">To cancel the operation, set the event and pass the event handle as  _hCancelEvent_; pass **null** if you do not want to cancel the operation.</span></span> <span data-ttu-id="30fc5-122">Обратите внимание, что передача значения, которое не представляет обработчика событий не оказывает влияния и учитывается, с помощью функции.</span><span class="sxs-lookup"><span data-stu-id="30fc5-122">Note that passing a value that does not represent an event handle has no effect and is ignored by the function.</span></span> 
    
 <span data-ttu-id="30fc5-123">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="30fc5-123">_ulFlags_</span></span>
  
> <span data-ttu-id="30fc5-124">[in] Этот параметр не используется.</span><span class="sxs-lookup"><span data-stu-id="30fc5-124">[in] This parameter is not used.</span></span> <span data-ttu-id="30fc5-125">Он должен иметь значение 0.</span><span class="sxs-lookup"><span data-stu-id="30fc5-125">It must be 0.</span></span>
    
 <span data-ttu-id="30fc5-126">_ppXmlStream_</span><span class="sxs-lookup"><span data-stu-id="30fc5-126">_ppXmlStream_</span></span>
  
> <span data-ttu-id="30fc5-127">[out] Указатель на объект [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) , который содержит XML автоматического обнаружения.</span><span class="sxs-lookup"><span data-stu-id="30fc5-127">[out] A pointer to an [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) object that contains the autodiscovery XML.</span></span> <span data-ttu-id="30fc5-128">Возвращает **значение null** , если происходит сбой операции автоматического обнаружения.</span><span class="sxs-lookup"><span data-stu-id="30fc5-128">Returns **null** if the autodiscovery operation fails.</span></span> <span data-ttu-id="30fc5-129">Необходимо удалить объект [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) после завершения с ним.</span><span class="sxs-lookup"><span data-stu-id="30fc5-129">You must release the [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) object when you are finished with it.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="30fc5-130">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="30fc5-130">Return values</span></span>

<span data-ttu-id="30fc5-131">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="30fc5-131">S_OK</span></span> 
  
- <span data-ttu-id="30fc5-132">Вызов функции выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="30fc5-132">The function call is successful.</span></span>
    
<span data-ttu-id="30fc5-133">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="30fc5-133">E_INVALIDARG</span></span> 
  
-  <span data-ttu-id="30fc5-134">_pwzAddress_ имеет **значение null** или не является допустимым адресом SMTP, или _ppXmlStream_ имеет **значение null,** указателя на объект [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="30fc5-134">_pwzAddress_ is **null** or is not a valid SMTP address, or  _ppXmlStream_ is a **null** pointer to an [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) object.</span></span> 
    
<span data-ttu-id="30fc5-135">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="30fc5-135">MAPI_E_NOT_FOUND</span></span> 
  
- <span data-ttu-id="30fc5-136">Клиентский компьютер не подключен к сети, клиентский компьютер не подключен к серверу Microsoft Exchange 2007, _pwzAddress_ не является учетную запись на сервере Exchange 2007 или _pwzAddress_ является учетной записью, которая не поддерживает Exchange Служба автообнаружения.</span><span class="sxs-lookup"><span data-stu-id="30fc5-136">Client computer is not connected to the network, client computer is not connected to a Microsoft Exchange 2007 server,  _pwzAddress_ is not an account on an Exchange 2007 server, or  _pwzAddress_ is an account that does not support Exchange auto-discovery service.</span></span> 
    
<span data-ttu-id="30fc5-137">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="30fc5-137">MAPI_E_USER_CANCEL</span></span> 
  
- <span data-ttu-id="30fc5-138">Обработчика событий передается _hCancelEvent_ , чтобы отменить операцию.</span><span class="sxs-lookup"><span data-stu-id="30fc5-138">An event handle has been passed to  _hCancelEvent_ to cancel the operation.</span></span> 
    
<span data-ttu-id="30fc5-139">STRSAFE_E_INSUFFICIENT_BUFFER</span><span class="sxs-lookup"><span data-stu-id="30fc5-139">STRSAFE_E_INSUFFICIENT_BUFFER</span></span>
  
- <span data-ttu-id="30fc5-140">Значение, переданное в _pwzAddress_ или _pwzPassword_ слишком много времени, таким образом, чтобы превышает внутренний буфер размером 256 байт.</span><span class="sxs-lookup"><span data-stu-id="30fc5-140">The value passed to  _pwzAddress_ or  _pwzPassword_ is too long, such that it overflows the internal buffer of size 256 bytes.</span></span> 
    

