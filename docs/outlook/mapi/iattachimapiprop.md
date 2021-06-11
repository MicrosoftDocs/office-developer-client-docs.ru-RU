---
title: IAttach IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAttach
api_type:
- COM
ms.assetid: f47e20e1-2a30-4c9e-8ca6-e8c5e72f44a1
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2ef3bc973e12bd5630cc00b3c512b748d4a16e86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409092"
---
# <a name="iattach--imapiprop"></a>IAttach : IMAPIProp

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Поддерживает и предоставляет доступ к свойствам вложений в сообщениях. Интерфейс **IAttach** не имеет уникальных методов. Дополнительные сведения об использовании вложений см. в [таблице MAPI Attachments](mapi-attachments.md) and [Attachment Tables.](attachment-tables.md) 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Подвергается:  <br/> |Объекты вложения  <br/> |
|Реализовано в:  <br/> |Поставщики магазинов сообщений  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IAttachment  <br/> |
|Тип указателя:  <br/> |LPATTACH  <br/> |
|Модель транзакции:  <br/> |Transacted  <br/> |
   
## <a name="vtable-order"></a>Заказ Vtable

Этот интерфейс не имеет уникальных методов.
  
|**Обязательные свойства**|**Access**|
|:-----|:-----|
|**PR_OBJECT_TYPE** [(PidTagObjectType)](pidtagobjecttype-canonical-property.md)  <br/> |Только для чтения  <br/> |
|**PR_ATTACH_METHOD** [(PidTagAttachMethod)](pidtagattachmethod-canonical-property.md)  <br/> |Чтение и запись  <br/> |
|**PR_RENDERING_POSITION** [(PidTagRenderingPosition)](pidtagrenderingposition-canonical-property.md)  <br/> |Чтение и запись  <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

