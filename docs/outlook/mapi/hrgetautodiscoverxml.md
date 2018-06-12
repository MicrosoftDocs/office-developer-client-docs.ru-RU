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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: da466fc9add8cbc385014782f31749d3b6522da9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808666"
---
# <a name="hrgetautodiscoverxml"></a>HrGetAutoDiscoverXML

  
  
**Применимо к**: Outlook 
  
Возвращает поток языке (XML), который представляет данные, полученные из службы автоматического обнаружения сервера Microsoft Exchange 2007.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Экспортировать с:  <br/> |olmapi32.dll  <br/> |
|Вызывается:  <br/> |Клиент  <br/> |
|Реализованный:  <br/> |Outlook  <br/> |
   
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
  
> [in] Символом null Simple Mail Transfer Protocol (SMTP) адрес электронной почты учетной записи, для которого требуется извлечь данные автоматического обнаружения.
    
 _pwzPassword_
  
> [in] Необязательный пароль для учетной записи, указанной с _pwzAddress_. Обратите внимание, что передача любой пароль не оказывает влияния, если пароль учетной записи, указанной с _pwzAddress_ не требуется. 
    
 _hCancelEvent_
  
> [in] Удаление Win32 обработчика событий, который является необязательной и позволяет отменить операцию. Чтобы отменить операцию установки события и передать как обработчик события в качестве _hCancelEvent_; Передайте **значение null** , если вы не хотите отменить операцию. Обратите внимание, что передача значения, которое не представляет обработчика событий не оказывает влияния и учитывается, с помощью функции. 
    
 _ulFlags_
  
> [in] Этот параметр не используется. Он должен иметь значение 0.
    
 _ppXmlStream_
  
> [out] Указатель на объект [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) , который содержит XML автоматического обнаружения. Возвращает **значение null** , если происходит сбой операции автоматического обнаружения. Необходимо удалить объект [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) после завершения с ним. 
    
## <a name="return-values"></a>Возвращаемые значения

ЗНАЧЕНИЕ S_OK 
  
- Вызов функции выполнен успешно.
    
E_INVALIDARG 
  
-  _pwzAddress_ имеет **значение null** или не является допустимым адресом SMTP, или _ppXmlStream_ имеет **значение null,** указателя на объект [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) . 
    
MAPI_E_NOT_FOUND 
  
- Клиентский компьютер не подключен к сети, клиентский компьютер не подключен к серверу Microsoft Exchange 2007, _pwzAddress_ не является учетную запись на сервере Exchange 2007 или _pwzAddress_ является учетной записью, которая не поддерживает Exchange Служба автообнаружения. 
    
MAPI_E_USER_CANCEL 
  
- Обработчика событий передается _hCancelEvent_ , чтобы отменить операцию. 
    
STRSAFE_E_INSUFFICIENT_BUFFER
  
- Значение, переданное в _pwzAddress_ или _pwzPassword_ слишком много времени, таким образом, чтобы превышает внутренний буфер размером 256 байт. 
    

