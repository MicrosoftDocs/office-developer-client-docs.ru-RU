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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает поток языка разметки extensible (XML), который представляет информацию, извлеченную из службы автоматического обнаружения сервера Microsoft Exchange 2007 г.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Экспортируемая по:  <br/> |olmapi32.dll  <br/> |
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

## <a name="parameters"></a>Parameters

 _pwzAddress_
  
> [in] Null-terminated Simple Mail Transfer Protocol (SMTP) email address of the account for which you want to retrieve the auto-discovery information.
    
 _pwzPassword_
  
> [in] Необязательный пароль для учетной записи, указанной _pwzAddress._ Обратите внимание, что передача любого пароля не влияет, если учетная запись, указанная  _pwzAddress,_ не требует пароля. 
    
 _hCancelEvent_
  
> [in] Необязательная ручка событий Win32, которая необязательна и может быть использована для отмены операции. Чтобы отменить операцию, установите событие и передай обработку события  _в качестве hCancelEvent;_ пропускать **null,** если не нужно отменять операцию. Обратите внимание, что передача значения, которое не представляет ручку события, не влияет и игнорируется функцией. 
    
 _ulFlags_
  
> [in] Этот параметр не используется. Должно быть 0.
    
 _ppXmlStream_
  
> [вышел] Указатель на [объект IStream,](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) содержащий XML автонаружения. Возвращает **null,** если операция автооткрытия не удалась. Вы должны освободить [объект IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) по его завершению. 
    
## <a name="return-values"></a>Возвращаемые значения

S_OK 
  
- Вызов функции является успешным.
    
E_INVALIDARG 
  
-  _pwzAddress_ является **null** или не является допустимым smTP-адресом, или _ppXmlStream_ является указателем **null** для [объекта IStream.](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) 
    
MAPI_E_NOT_FOUND 
  
- Клиентский компьютер не подключен к сети, клиентский компьютер не подключен к серверу Microsoft Exchange 2007 г., _pwzAddress_ не является учетной записью на сервере Exchange 2007 г., или _pwzAddress_ — это учетная запись, которая не поддерживает Exchange службу автоматического обнаружения. 
    
MAPI_E_USER_CANCEL 
  
- Для отмены операции в  _hCancelEvent_ была передана ручка события. 
    
STRSAFE_E_INSUFFICIENT_BUFFER
  
- Значение, переданное  _pwzAddress_ или  _pwzPassword,_ слишком длинное, поэтому оно переполнено внутренним буфером размером 256 bytes. 
    

