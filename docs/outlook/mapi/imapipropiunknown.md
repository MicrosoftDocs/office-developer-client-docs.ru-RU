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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Позволяет клиентам, поставщикам услуг и MAPI работать со свойствами. Этот интерфейс реализуется всеми объектами, которые поддерживаются свойствами.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Предоставлено:  <br/> |Ни один объект не предоставляет этот интерфейс напрямую.  <br/> |
|Реализовано в:  <br/> |Поставщики услуг и MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения, поставщики служб и MAPI  <br/> |
|Идентификатор интерфейса:  <br/> |Иид_имапипроп  <br/> |
|Тип указателя:  <br/> |ЛПМАПИПРОП  <br/> |
|Модель транзакции:  <br/> |Абстрактный класс, никогда не реализован  <br/> |
   
## <a name="vtable-order"></a>Заказ vtable

|||
|:-----|:-----|
|[GetLastError](imapiprop-getlasterror.md) <br/> |Возвращает структуру [мапиеррор](mapierror.md) , которая содержит сведения о предыдущем сообщении об ошибке.  <br/> |
|[SaveChanges](imapiprop-savechanges.md) <br/> |Делает неизменными все изменения, внесенные в объект с момента последнего выполнения операции сохранения.  <br/> |
|[GetProps](imapiprop-getprops.md) <br/> |Получает значение свойства одного или нескольких свойств объекта.  <br/> |
|[Жетпроплист](imapiprop-getproplist.md) <br/> |Возвращает теги свойств для всех свойств.  <br/> |
|[Опенпроперти](imapiprop-openproperty.md) <br/> |Возвращает указатель на интерфейс, который можно использовать для доступа к свойству.  <br/> |
|[SetProps](imapiprop-setprops.md) <br/> |Обновляет одно или несколько свойств.  <br/> |
|[Делетепропс](imapiprop-deleteprops.md) <br/> |Удаляет одно или несколько свойств объекта.  <br/> |
|[CopyTo](imapiprop-copyto.md) <br/> |Копирует или перемещает все свойства, кроме специально исключенных свойств.  <br/> |
|[Копипропс](imapiprop-copyprops.md) <br/> |Копирование или перемещение выбранных свойств.  <br/> |
|[Жетнамесфромидс](imapiprop-getnamesfromids.md) <br/> |Предоставляет имена свойств, которые соответствуют одному или нескольким идентификаторам свойств.  <br/> |
|[Жетидсфромнамес](imapiprop-getidsfromnames.md) <br/> |Предоставляет идентификаторы свойств, соответствующие одному или нескольким именам свойств.  <br/> |
   
## <a name="remarks"></a>Примечания

 **IMAPIProp** является базовым интерфейсом для следующих интерфейсов: 
  
- [Иаттач](iattachimapiprop.md)
    
- [Имаилусер](imailuserimapiprop.md)
    
- [IMAPIContainer](imapicontainerimapiprop.md)
    
- [Имапиформинфо](imapiforminfoimapiprop.md)
    
- [Имапистатус](imapistatusimapiprop.md)
    
- [IMessage](imessageimapiprop.md)
    
- [IMsgStore](imsgstoreimapiprop.md)
    
- [Ипрофсект](iprofsectimapiprop.md)
    
- [Ипропдата](ipropdataimapiprop.md)
    
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

