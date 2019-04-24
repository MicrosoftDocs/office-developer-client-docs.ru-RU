---
title: Имапиконтаинержетконтентстабле
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.GetContentsTable
api_type:
- COM
ms.assetid: 88c7a666-875d-473a-b126-dbbb7009f7d9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 28315c5a09eba32816a0b63513cb98d1c30a96bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349289"
---
# <a name="imapicontainergetcontentstable"></a>IMAPIContainer::GetContentsTable

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Возвращает указатель на таблицу содержимого контейнера.
  
```cpp
HRESULT GetContentsTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Параметры

 _ulFlags_
  
> возврата Битовая маска флагов, которые управляют способом возвращения таблицы содержимого. Можно задать следующие флаги:
    
МАПИ_АССОЦИАТЕД 
  
> Вместо стандартной таблицы содержимого следует возвратить связанную таблицу содержимого контейнера. Этот флаг используется только для папок. Сообщения, включенные в связанную таблицу содержимого, были созданы с помощью флага МАПИ_АССОЦИАТЕД, установленного в вызове метода [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) . Клиенты обычно используют связанную таблицу содержимого для получения форм, представлений и других скрытых сообщений. 
    
АКЛТАБЛЕ_ФРИБУСИ
  
> Предоставляет доступ к правам Фригхтсфрибусисимпле и Фригхтсфрибусидетаилед в **пр_мембер_ригхтс**.
    
МАПИ_ДЕФЕРРЕД_ЕРРОРС 
  
> **Жетконтентстабле** может успешно вернуть, возможно, перед тем, как таблица стала доступна вызывающему объекту. Если таблица недоступна, выполнение последующих вызовов таблицы может вызвать ошибку. 
    
MAPI_UNICODE 
  
> ЗаПрашивает возврат столбцов, содержащих строковые данные, в формате Юникод. Если флаг МАПИ_УНИКОДЕ не установлен, строки должны быть возвращены в формате ANSI. 
    
SHOW_SOFT_DELETES
  
> Показывает элементы, которые в настоящее время помечены как обратимо удаленные — то есть они находятся на стадии хранения удаленных элементов.
    
 _Лпптабле_
  
> вышли Указатель на указатель на таблицу содержимого.
    
## <a name="return-value"></a>Возвращаемое значение

S_OK 
  
> Таблица содержимого успешно получена.
    
МАПИ_Е_БАД_ЧАРВИДС 
  
> Установлен либо флаг МАПИ_УНИКОДЕ, либо реализация не поддерживает Юникод, или МАПИ_УНИКОДЕ не задано, а реализация поддерживает только Юникод.
    
МАПИ_Е_НО_СУППОРТ 
  
> Контейнер не имеет содержимого и не может предоставить таблицу содержимого.
    
## <a name="remarks"></a>Примечания

Метод **IMAPIContainer:: жетконтентстабле** возвращает указатель на таблицу содержимого контейнера. Таблица содержимого содержит сводную информацию об объектах в контейнере. 
  
Таблицы содержимого содержат продолжительные наборы столбцов. Полный список обязательных и необязательных столбцов в таблицах содержимого представлен в [](contents-tables.md)статье оглавления. 
  
Некоторые контейнеры могут не иметь содержимого. Эти контейнеры возвращают МАПИ_Е_НО_СУППОРТ из реализации **жетконтентстабле**.
  
## <a name="notes-to-implementers"></a>Примечания для исполнителей

Если вы поддерживаете таблицу содержимого для контейнера, необходимо также выполнить следующие действия:
  
- Поддерживает вызовы метода контейнера [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) для открытия свойства **пр_контаинер_контентс** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)).
    
- Возвращает **пр_контаинер_контентс** в ответ на вызов объекта контейнера 
    
    [IMAPIProp:: PROPS](imapiprop-getprops.md) и [IMAPIProp:: жетпроплист](imapiprop-getproplist.md) методы. 
    
Реализация этого метода В удаленном поставщике транспорта должна возвращать указатель на метод [IMAPITable: IUnknown](imapitableiunknown.md) в параметре _пптабле_ , переданном в метод **жетконтентстабле** . Если у поставщика транспорта есть существующая таблица содержимого, достаточно возвратить указатель на него. В противном случае этот метод должен создать новый объект [IMAPITable: IUnknown](imapitableiunknown.md) , заполнить таблицу заголовками сообщений (если они доступны) и возвратить указатель на новую таблицу. Метод [итабледата:: хржетвиев](itabledata-hrgetview.md) полезен для создания возвращаемого значения и сохранения указателя таблицы в параметре _пптабле_ . Таблица Contents должна поддерживать по крайней мере следующие столбцы свойств: 
  
- **Пр_ентрид** ([PidTagEntryID](pidtagentryid-canonical-property.md))
    
- **Пр_сендер_наме** ([PidTagSenderName](pidtagsendername-canonical-property.md))
    
- **Пр_сент_репресентинг_наме** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))
    
- **Пр_дисплай_то** ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))
    
- **Пр_субжект** ([PidTagSubject](pidtagsubject-canonical-property.md))
    
- **Пр_мессаже_класс** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))
    
- **Пр_мессаже_флагс** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))
    
- **Пр_мессаже_сизе** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))
    
- **Пр_приорити** ([PidTagPriority](pidtagpriority-canonical-property.md))
    
- **Пр_импортанце** ([PidTagImportance](pidtagimportance-canonical-property.md))
    
- **Пр_сенситивити** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))
    
- **Пр_мессаже_деливери_тиме** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))
    
- **Пр_мсг_статус** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))
    
- **Пр_мессаже_довнлоад_тиме** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))
    
- **Пр_хасаттач** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))
    
- **Пр_обжект_типе** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))
    
- **Пр_инстанце_кэй** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))
    
- **Пр_нормализед_субжект** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))
    
## <a name="notes-to-callers"></a>Примечания для вызывающих методов

Столбцы таблицы строковых и двоичных содержимого можно усечь. Как правило, поставщики возвращают 255 символов. Так как вы не можете заранее узнать, содержит ли таблица усеченные столбцы, предположим, что столбец усекается, если длина столбца составляет 255 или 510 байт. Вы всегда можете получить полное значение сокращенного столбца (при необходимости) непосредственно из объекта, используя его идентификатор записи, чтобы открыть его, а затем вызвать метод **IMAPIProp::** /PROPS. 
  
В зависимости от реализации поставщика, ограничения и операции сортировки могут применяться ко всей строке или к усеченной версии этой строки.
  
## <a name="mfcmapi-reference"></a>Справочные материалы по MFCMAPI

Пример кода MFCMAPI указан в приведенной ниже таблице.
  
|**Файл**|**Функция**|**Примечание**|
|:-----|:-----|:-----|
|Контентстабледиалог. cpp  <br/> |Кконтентстабледлг:: Кконтентстабледлг  <br/> |Класс **кконтентстабледлг** использует **жетконтентстабле** для получения записей в таблице содержимого.  <br/> |
   
## <a name="see-also"></a>См. также



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPITable : IUnknown](imapitableiunknown.md)
  
[Каноническое свойство PidTagContainerContents](pidtagcontainercontents-canonical-property.md)
  
[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)


[Mfcmapi (en) � �������� ������� ����](mfcmapi-as-a-code-sample.md)

