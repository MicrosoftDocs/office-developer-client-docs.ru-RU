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
# <a name="hrgetautodiscoverxml"></a>HrGetAutoDiscoverXML

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Возвращает поток XML, который представляет сведения, полученные из службы автоматического обнаружения сервера Microsoft Exchange 2007.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Экспортируется с помощью:  <br/> |olmapi32.dll  <br/> |
|Вызывающая сторона:  <br/> |Клиент  <br/> |
|Реализовано в:  <br/> |Outlook  <br/> |
   
```cpp
HRESULT HrGetAutoDiscoverXML( 
    __in_z const WCHAR *pwzAddress, 
    __in_opt_z const WCHAR *pwzPassword, 
    __in_opt HANDLE hCancelEvent, 
    __in_opt ULONG ulFlags, 
    __out IStream** ppXmlStream); 

```

## <a name="parameters"></a>Параметры

 _pwzAddress_
  
> [in] SmTP-адрес электронной почты учетной записи, для которой необходимо получить сведения об автоматическом обнаружении.
    
 _pwzPassword_
  
> [in] Необязательный пароль для учетной записи, указанной _pwzAddress._ Обратите внимание, что передача пароля не действует, если учетная запись, указанная  _pwzAddress,_ не требует пароля. 
    
 _hCancelEvent_
  
> [in] Unset Win32 event handle that is optional and can be used to cancel the operation. Чтобы отменить операцию, задав событие и передав его в качестве  _hCancelEvent;_ если **вы** не хотите отменять операцию, передав ее null. Обратите внимание, что передача значения, не представляюющего окне события, не оказывает влияния и игнорируется функцией. 
    
 _ulFlags_
  
> [in] Этот параметр не используется. Должно быть 0.
    
 _ppXmlStream_
  
> [out] Указатель на объект [IStream,](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) содержащий XML автооружения. Возвращает **null в** случае сбой операции автооружия. После завершения его необходимо освободить объект [IStream.](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) 
    
## <a name="return-values"></a>Возвращаемые значения

S_OK 
  
- Вызов функции успешно.
    
E_INVALIDARG 
  
-  _pwzAddress_ имеет **null** или не является допустимым SMTP-адресом, или _ppXmlStream_ — это **null-указатель** на [объект IStream.](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) 
    
MAPI_E_NOT_FOUND 
  
- Клиентский компьютер не подключен к сети, клиентский компьютер не подключен к серверу Microsoft Exchange 2007,  _pwzAddress_ не является учетной записью на сервере Exchange 2007 или  _pwzAddress_ — это учетная запись, которая не поддерживает службу автоматического обнаружения Exchange. 
    
MAPI_E_USER_CANCEL 
  
- Для отмены операции в  _hCancelEvent_ передан работка события. 
    
STRSAFE_E_INSUFFICIENT_BUFFER
  
- Значение, передаваемого  _в pwzAddress_ или  _pwzPassword,_ слишком длинное, чтобы оно переполнило внутренний буфер размером 256байт. 
    

