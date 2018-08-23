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
ms.openlocfilehash: ddb87af4b14be6d728bcceddb4d958ba49229ad4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579041"
---
# <a name="iaddrbookcreateoneoff"></a>IAddrBook::CreateOneOff

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Создает запись идентификатор указывает адрес.
  
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
  
> [in] Указатель на значение свойства **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) получателя. Параметр _lpszName_ может быть NULL. 
    
 _lpszAdrType_
  
> [in] Указатель на тип адреса получателя, например, ФАКС или SMTP. Параметр _lpszAdrType_ не может быть NULL. 
    
 _lpszAddress_
  
> [in] Указатель на адрес получателя. Параметр _lpszAddress_ не может быть NULL. 
    
 _ulFlags_
  
> [in] Битовая маска флаги, влияющей на одноразовых получателя. Можно задать следующие флажки:
    
MAPI_SEND_NO_RICH_INFO 
  
> Получатель не может обрабатывать сообщения Форматированный контент. Если значение MAPI_SEND_NO_RICH_INFO, MAPI свойству получателя **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) присваивается значение FALSE. Если MAPI_SEND_NO_RICH_INFO не задано, MAPI этому свойству значение TRUE, если адрес получателя обмена мгновенными сообщениями, на который указывает _lpszAddress_ интерпретируется быть адрес в Интернете. В этом случае MAPI задает **PR_SEND_RICH_INFO** значение FALSE. 
    
MAPI_UNICODE 
  
> Отображаемое имя, тип адреса и адрес находятся в формате Юникод. Если флаг MAPI_UNICODE не установлен, эти строки находятся в формате ANSI.
    
 _lpcbEntryID_
  
> [out] Указатель на число байтов в идентификатор записи, на который указывает параметр _lppEntryID_ . 
    
 _lppEntryID_
  
> [out] Указатель на указатель на идентификатор записи для одноразовых получателя.
    
## <a name="return-value"></a>������������ ��������

ЗНАЧЕНИЕ S_OK 
  
> Идентификатор единичных записей успешно создан.
    
## <a name="remarks"></a>Замечания

Клиенты вызовите метод **CreateOneOff** для создания записи идентификатора для одноразовых получателя — получателя, не принадлежащие ни контейнеры из любого из поставщиками в настоящее время загрузки адресной книги. Одноразовых получателей может иметь любой тип адреса, который поддерживается с помощью одного из поставщиками active адресной книги для сеанса. 
  
Получатели одноразовых обычно создаются с помощью шаблона для их адрес определенного типа. Поставщик адресной книги, поддерживающего тип адреса предоставляет шаблон. Пользователь из клиентского приложения вводит информацию в шаблон.
  
MAPI поддерживает знаков Юникод для отображаемое имя, тип адреса и параметры адреса из **CreateOneOff**.
  
Флаг MAPI_SEND_NO_RICH_INFO определяет, является ли форматированный текст в форматированный текст (RTF) отправляется вместе с каждого сообщения. Транспорта Neutral Encapsulation формата TNEF — формат, используемый для передачи форматированный текст, отправляемого большинство поставщиков транспорта, независимо от того, как получатель задает его свойство **PR_SEND_RICH_INFO** . Эта проблема не возникает для сообщений (en), которые работают с сообщениями электронной почты — это. Тем не менее так как TNEF обычно используется для отправки настраиваемых свойств для пользовательских классов сообщений, не поддерживает может вызвать проблемы для клиентов на основе форм или клиентов, которым требуется настраиваемых свойств MAPI. Дополнительные сведения можно [Отправлять сообщения с TNEF](sending-messages-with-tnef.md).
  
## <a name="mfcmapi-reference"></a>Справочник по mfcmapi (en)

������ ���� mfcmapi (en) ���������� � ������� ����.
  
|**����**|**�������**|**�����������**|
|:-----|:-----|:-----|
|Mapiabfunctions.cpp  <br/> |AddOneOffAddress  <br/> |Mfcmapi (en) использует метод **CreateOneOff** для создания идентификатор записи адреса, который не найден в любой адресной книги.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPISupport::CreateOneOff](imapisupport-createoneoff.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

