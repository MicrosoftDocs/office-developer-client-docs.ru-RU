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
ms.openlocfilehash: 6b0a8923ee5efe22584170ce9853698885527ee8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407664"
---
# <a name="imapiprop--iunknown"></a>IMAPIProp : IUnknown

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Позволяет клиентам, поставщикам услуг и MAPI работать с свойствами. Все объекты, поддерживают свойства, реализуют этот интерфейс.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Подвергается:  <br/> |Ни один объект не предоставляет этот интерфейс напрямую.  <br/> |
|Реализовано в:  <br/> |Поставщики услуг и MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения, поставщики услуг и MAPI  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IMAPIProp  <br/> |
|Тип указателя:  <br/> |LPMAPIPROP  <br/> |
|Модель транзакции:  <br/> |Абстрактный класс, никогда не реализованный  <br/> |
   
## <a name="vtable-order"></a>Заказ Vtable

|||
|:-----|:-----|
|[GetLastError](imapiprop-getlasterror.md) <br/> |Возвращает [структуру MAPIERROR, которая](mapierror.md) содержит сведения о предыдущей ошибке.  <br/> |
|[SaveChanges](imapiprop-savechanges.md) <br/> |Вносит постоянные изменения, внесенные в объект с момента последней операции сохранения.  <br/> |
|[GetProps](imapiprop-getprops.md) <br/> |Извлекает значение свойства одного или более свойств объекта.  <br/> |
|[GetPropList](imapiprop-getproplist.md) <br/> |Возвращает теги свойств для всех свойств.  <br/> |
|[OpenProperty](imapiprop-openproperty.md) <br/> |Возвращает указатель в интерфейс, который можно использовать для доступа к свойству.  <br/> |
|[SetProps](imapiprop-setprops.md) <br/> |Обновляет одно или несколько свойств.  <br/> |
|[DeleteProps](imapiprop-deleteprops.md) <br/> |Удаляет одно или несколько свойств из объекта.  <br/> |
|[CopyTo](imapiprop-copyto.md) <br/> |Копирует или перемещает все свойства, за исключением специально исключенных свойств.  <br/> |
|[CopyProps](imapiprop-copyprops.md) <br/> |Копирует или перемещает выбранные свойства.  <br/> |
|[GetNamesFromIDs](imapiprop-getnamesfromids.md) <br/> |Предоставляет имена свойств, соответствующие одному или более идентификаторам свойств.  <br/> |
|[GetIDsFromNames](imapiprop-getidsfromnames.md) <br/> |Предоставляет идентификаторы свойств, соответствующие одному или более имени свойств.  <br/> |
   
## <a name="remarks"></a>Примечания

 **IMAPIProp** — это базовый интерфейс для следующих интерфейсов: 
  
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

