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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Создает идентификатор записи для разовый адрес.
  
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

## <a name="parameters"></a>Параметры

 _lpszName_
  
> [in] Указатель на значение свойства PR_DISPLAY_NAME **(** [PidTagDisplayName).](pidtagdisplayname-canonical-property.md) Параметр  _lpszName может_ иметь параметр NULL. 
    
 _lpszAdrType_
  
> [in] Указатель на тип адреса получателя, например ФАКС или SMTP. Параметр  _lpszAdrType не_ может быть NULL. 
    
 _lpszAddress_
  
> [in] Указатель на адрес получателя. Параметр  _lpszAddress не_ может иметь NULL. 
    
 _ulFlags_
  
> [in] Битоваяmas флагов, влияющих на одного получателя. Можно установить следующие флаги:
    
MAPI_SEND_NO_RICH_INFO 
  
> Получатель не может обрабатывать отформатированный контент сообщения. Если MAPI_SEND_NO_RICH_INFO задан, MAPI устанавливает для свойства **PR_SEND_RICH_INFO** получателя [(PidTagSendRichInfo)](pidtagsendrichinfo-canonical-property.md)false. Если MAPI_SEND_NO_RICH_INFO не заданная, MAPI устанавливает для этого свойства true, если адрес получателя сообщений, на который указывает  _lpszAddress,_ не интерпретируется как адрес Интернета. В этом случае MAPI **PR_SEND_RICH_INFO** false. 
    
MAPI_UNICODE 
  
> Отображаемого имени, типа адреса и адреса в формате Юникод. Если флаг MAPI_UNICODE не установлен, эти строки имеют формат ANSI.
    
 _lpcbEntryID_
  
> [out] Указатель на количество byte в идентификаторе записи, на который указывает параметр _lppEntryID._ 
    
 _lppEntryID_
  
> [out] Указатель на указатель на идентификатор записи для одного получателя.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Идентификатор однорахой записи успешно создан.
    
## <a name="remarks"></a>Примечания

Клиенты **вызывали метод CreateOneOff,** чтобы создать идентификатор записи для одного получателя — получателя, который не принадлежит ни к одному из контейнеров ни от одного из текущих загруженных поставщиков адресной книги. У разных получателей может быть любой адрес, поддерживаемый одним из активных поставщиков адресных книг для сеанса. 
  
Как правило, для разных получателей создается шаблон для конкретного типа адреса. Поставщик адресной книги, который поддерживает тип адреса, передает шаблон. Пользователь клиентского приложения вводит соответствующую информацию в шаблон.
  
MAPI поддерживает строки символов Юникода для отображаемого имени, типа адреса и параметров **адреса CreateOneOff.**
  
Флаг MAPI_SEND_NO_RICH_INFO контролирует, отправляется ли форматированный текст в формате RTF вместе с каждым сообщением. Формат TNEF ( формат, используемый для передачи форматного текста) отправляется большинством поставщиков транспорта независимо от того, как получатель задает PR_SEND_RICH_INFO.  Это не проблема для клиентов обмена сообщениями, которые работают с межличностными сообщениями. Однако, так как формат TNEF обычно используется для отправки настраиваемого свойства для настраиваемого класса сообщений, его поддержка может быть проблемой для клиентов на основе форм, которые требуют настраиваемые свойства MAPI. Дополнительные сведения [см. в теме "Отправка сообщений с помощью TNEF".](sending-messages-with-tnef.md)
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Mapiabfunctions.cpp  <br/> |AddOneOffAddress  <br/> |MFCMAPI использует метод **CreateOneOff** для создания ИД записи для адреса, который не найден ни в одной адресной книге.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPISupport::CreateOneOff](imapisupport-createoneoff.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

