---
title: IAttachmentSecurity IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAttachmentSecurity
api_type:
- COM
ms.assetid: 69609f73-5884-9e2b-ab78-a2e0ece3a1d1
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f182610f9cf4874cc18c409960e1f8b23f853d4f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574828"
---
# <a name="iattachmentsecurity--iunknown"></a>IAttachmentSecurity : IUnknown

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Позволяет Microsoft Outlook 2010 и Microsoft Outlook 2013 решения узнать, если вложение считается небезопасные и заблокированные для просмотра и индексирования.
  
|||
|:-----|:-----|
|Идентификатор интерфейса:  <br/> |IID_IAttachmentSecurity  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md) <br/> |Проверяет, если указанное вложение не заблокирован по Outlook 2010 или Outlook 2013 для просмотра и индексирования.  <br/> |
   
## <a name="remarks"></a>Замечания

Решения для Outlook 2010 и Outlook 2013 можно запросить этот интерфейс, чтобы увидеть, если вложения блокируется. Вложения, которые блокируются по Outlook 2010 или Outlook 2013 различаться в зависимости от того, как был настроен Outlook 2010 или Outlook 2013 и политики, примененные администратора.
  
## <a name="see-also"></a>См. также



[��������� MAPI](mapi-constants.md)
  
[Проверка блокировки вложения](how-to-verify-an-attachment-is-blocked.md)

