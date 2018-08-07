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
ms.openlocfilehash: 66e318c3b7b772f2713b5c730590ce4a8ad5965b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808764"
---
# <a name="iattach--imapiprop"></a>IAttach : IMAPIProp

  
  
**Относится к**: Outlook 
  
Поддерживает и предоставляет доступ к свойствам вложений в сообщениях. Интерфейс **IAttach** не имеет уникальное методов свои собственные. Дополнительные сведения об использовании вложения можно [Вложений MAPI](mapi-attachments.md) и [Таблиц вложений](attachment-tables.md). 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapidefs.h  <br/> |
|Предоставляемые:  <br/> |Объекты вложения  <br/> |
|Реализованный:  <br/> |Поставщики хранилища сообщений  <br/> |
|Вызывается:  <br/> |Клиентские приложения  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IAttachment  <br/> |
|Тип указателя:  <br/> |LPATTACH  <br/> |
|Модель транзакций:  <br/> |В транзакции  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

Этот интерфейс не имеет каких-либо уникальных методов.
  
|**Обязательные свойства**|**Access**|
|:-----|:-----|
|**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md))  <br/> |Чтение и запись  <br/> |
|**PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md))  <br/> |Чтение и запись  <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

