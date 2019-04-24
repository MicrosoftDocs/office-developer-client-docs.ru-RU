---
title: Каноническое свойство PidTagReceivedRepresentingSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceivedRepresentingSearchKey
api_type:
- COM
ms.assetid: 234c797c-4a3c-4e05-be22-2a2fa377871f
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bcf310138e4b43b1cc36a177194f721c401caba6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356821"
---
# <a name="pidtagreceivedrepresentingsearchkey-canonical-property"></a>Каноническое свойство PidTagReceivedRepresentingSearchKey

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит ключ поиска для пользователя обмена сообщениями, представленного принимающим пользователем.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_РКВД_РЕПРЕСЕНТИНГ_СЕАРЧ_КЭЙ  <br/> |
|Идентификатор:  <br/> |0x0052  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Address  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство является одним из свойств адреса пользователя обмена сообщениями, представленного принимающим пользователем. Он должен быть задан входящим поставщиком транспорта, который также отвечает за авторизацию или проверку делегата. Если пользователя обмена сообщениями нет, это свойство должно быть задано для ключа поиска, который хранится в свойстве **пр_рецеивед_би_сеарч_кэй** ([PidTagReceivedBySearchKey](pidtagreceivedbysearchkey-canonical-property.md)).
  
Клиентское приложение, отвечающее на сообщение, полученное от имени другого клиента, должно копировать это свойство из полученного сообщения в свойство **пр_сент_репресентинг_сеарч_кэй** ([PidTagSentRepresentingSearchKey](pidtagsentrepresentingsearchkey-canonical-property.md)) для ответа.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для объектов сообщений электронной почты.
    
[[MS — ОКСКФКСИКС]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Обрабатывает порядок и потоки для передачи данных между клиентом и сервером.
    
[[MS — ОКСЦИКАЛ]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Преобразование между IETF RFC2445, RFC2446 и RFC2447, а объекты встреч и собраний.
    
[[MS — ОКСОДЛГТ]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Задает методы для подключения и настройки почтовых ящиков в качестве делегатов и взаимодействия с объектами Message и Calendar, когда они действуют от имени другого пользователя.
    
[[MS — ОКСТНЕФ]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Кодирует и декодирует объекты сообщений и вложений в эффективное потоковое представление.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagSearchKey](pidtagsearchkey-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

