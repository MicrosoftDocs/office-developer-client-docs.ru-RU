---
title: IMAPIProp IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp
api_type:
- COM
ms.assetid: 3c9e4e05-cd3a-4b56-9dff-879e33ff6fd5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a397ac9110429911755552298ffe244343d54a8a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583731"
---
# <a name="imapiprop--iunknown"></a>IMAPIProp : IUnknown

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Включает клиентов, поставщиков услуг и MAPI, для работы со свойствами. Все объекты, которые поддерживают свойства реализовать этот интерфейс.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Предоставляемые:  <br/> |Объект не предоставляет этот интерфейс напрямую.  <br/> |
|Реализованный:  <br/> |Поставщиков услуг и MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения, поставщиков услуг и MAPI  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIProp  <br/> |
|Тип указателя:  <br/> |LPMAPIPROP  <br/> |
|Модель транзакций:  <br/> |Абстрактный класс, никогда не реализовано  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[GetLastError](imapiprop-getlasterror.md) <br/> |Возвращает структуру [MAPIERROR](mapierror.md) , который содержит сведения о предыдущем ошибки.  <br/> |
|[SaveChanges](imapiprop-savechanges.md) <br/> |Выполняет постоянное все изменения, внесенные в объект с момента последней операции сохранения.  <br/> |
|[GetProps](imapiprop-getprops.md) <br/> |Получает значение свойства из одного или нескольких свойств объекта.  <br/> |
|[GetPropList](imapiprop-getproplist.md) <br/> |Возвращает свойство теги для всех свойств.  <br/> |
|[OpenProperty](imapiprop-openproperty.md) <br/> |Возвращает указатель на интерфейс, который можно использовать для доступа к свойству.  <br/> |
|[SetProps](imapiprop-setprops.md) <br/> |Обновление одного или нескольких свойств.  <br/> |
|[DeleteProps](imapiprop-deleteprops.md) <br/> |Удаляет одно или несколько свойств объекта.  <br/> |
|[CopyTo](imapiprop-copyto.md) <br/> |Копирует или переносит все свойства, за исключением специально исключенные свойства.  <br/> |
|[CopyProps](imapiprop-copyprops.md) <br/> |Копирование или Перемещение выбранных свойств.  <br/> |
|[GetNamesFromIDs](imapiprop-getnamesfromids.md) <br/> |Содержит имена свойств, которые соответствуют один или несколько идентификаторов свойств.  <br/> |
|[GetIDsFromNames](imapiprop-getidsfromnames.md) <br/> |Предоставляет свойство идентификаторы, соответствующие имена одного или нескольких свойств.  <br/> |
   
## <a name="remarks"></a>Замечания

 **IMAPIProp** — это основной интерфейс для следующие интерфейсы: 
  
- [IAttach](iattachimapiprop.md)
    
- [IMailUser](imailuserimapiprop.md)
    
- [IMAPIContainer](imapicontainerimapiprop.md)
    
- [IMAPIFormInfo](imapiforminfoimapiprop.md)
    
- [IMAPIStatus](imapistatusimapiprop.md)
    
- [IMessage](imessageimapiprop.md)
    
- [IMsgStore](imsgstoreimapiprop.md)
    
- [IProfSect](iprofsectimapiprop.md)
    
- [IPropData](ipropdataimapiprop.md)
    
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

