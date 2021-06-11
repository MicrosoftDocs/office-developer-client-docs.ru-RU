---
title: IAddrBookCreateOneOff
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.CreateOneOff
api_type:
- COM
ms.assetid: bcacfbdf-edff-4810-a985-e6d2c9271901
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 980ac82c6f7fcb5771a6013b3fb033b0bdfd05e0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427383"
---
# <a name="iaddrbookcreateoneoff"></a>IAddrBook::CreateOneOff

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Создает идентификатор записи для разового адреса.
  
```cpp
HRESULT CreateOneOff(
  LPSTR lpszName,
  LPSTR lpszAdrType,
  LPSTR lpszAddress,
  ULONG ulFlags,
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Parameters

 _lpszName_
  
> [in] Указатель на значение свойства PR_DISPLAY_NAME  [(PidTagDisplayName).](pidtagdisplayname-canonical-property.md) Параметр  _lpszName может_ быть NULL. 
    
 _lpszAdrType_
  
> [in] Указатель на тип адреса получателя, например ФАКС или SMTP. Параметр  _lpszAdrType_ не может быть NULL. 
    
 _lpszAddress_
  
> [in] Указатель на адрес получателя. Параметр  _lpszAddress не_ может быть NULL. 
    
 _ulFlags_
  
> [in] Битмашка флагов, которая влияет на разовую получатель. Можно установить следующие флаги:
    
MAPI_SEND_NO_RICH_INFO 
  
> Получатель не может обрабатывать отформатированный контент сообщения. Если MAPI_SEND_NO_RICH_INFO установлено, MAPI задает свойство  [PR_SEND_RICH_INFO (PidTagSendRichInfo)](pidtagsendrichinfo-canonical-property.md)false. Если MAPI_SEND_NO_RICH_INFO не установлено, MAPI задает это свойство true, если адрес обмена сообщениями получателя, на который указывает  _lpszAddress,_ не интерпретируется как интернет-адрес. В этом случае MAPI задает **PR_SEND_RICH_INFO** false. 
    
MAPI_UNICODE 
  
> Имя отображения, тип адреса и адрес находятся в формате Unicode. Если флаг MAPI_UNICODE не установлен, эти строки находятся в формате ANSI.
    
 _lpcbEntryID_
  
> [вышел] Указатель на количество byte в идентификаторе входа, на который указывает параметр _lppEntryID._ 
    
 _lppEntryID_
  
> [вышел] Указатель на указатель на идентификатор записи для разового получателя.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Идентификатор одноавтной записи был создан успешно.
    
## <a name="remarks"></a>Примечания

Клиенты звонят по методу **CreateOneOff** для создания идентификатора входа для разового получателя — получателя, который не принадлежит ни одному из контейнеров от любого из загруженных в настоящее время поставщиков адресных книг. У разных получателей может быть любой адрес, поддерживаемый одним из активных поставщиков адресных книг для сеанса. 
  
Разовые получатели обычно создаются с шаблоном для определенного типа адресов. Поставщик адресной книги, который поддерживает тип адресов, поставляет шаблон. Пользователь клиентского приложения вводит соответствующую информацию в шаблон.
  
MAPI поддерживает строки символов Юникод для параметров отображения, типа адреса **и адреса CreateOneOff.**
  
Флаг MAPI_SEND_NO_RICH_INFO, отправляется ли форматированный текст в формате Rich Text Format (RTF) вместе с каждым сообщением. Формат транспортной нейтральной инкапсуляции (TNEF) — формат, используемый для передачи форматного текста, отправляется большинством поставщиков транспорта независимо от того, как получатель задает **PR_SEND_RICH_INFO** свойству. Это не проблема для клиентов обмена сообщениями, которые работают с межличностными сообщениями. Однако, поскольку TNEF обычно используется для отправки настраиваемого свойства для настраиваемого класса сообщений, его поддержка может быть проблемой для клиентов или клиентов на основе форм, которые требуют настраиваемые свойства MAPI. Дополнительные сведения см. в [рублях Отправка сообщений с помощью TNEF.](sending-messages-with-tnef.md)
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Mapiabfunctions.cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI использует **метод CreateOneOff** для создания ID записи для адреса, не найденного ни в одной адресной книге.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPISupport::CreateOneOff](imapisupport-createoneoff.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

