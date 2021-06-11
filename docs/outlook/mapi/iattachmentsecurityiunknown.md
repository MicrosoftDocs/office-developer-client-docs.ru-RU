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
ms.openlocfilehash: a8464c8265ebc1754f7909be5413620e7f76db5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411416"
---
# <a name="iattachmentsecurity--iunknown"></a>IAttachmentSecurity : IUnknown

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Позволяет Microsoft Outlook 2010, русская версия и Microsoft Outlook 2013, чтобы узнать, считается ли вложение небезопасным и заблокировано для просмотра и индексации.
  
|||
|:-----|:-----|
|Идентификатор интерфейса:  <br/> |IID_IAttachmentSecurity  <br/> |
   
## <a name="vtable-order"></a>Заказ Vtable

|||
|:-----|:-----|
|[IAttachmentSecurity::IsAttachmentBlocked](iattachmentsecurity-isattachmentblocked.md) <br/> |Проверяет, блокируется ли указанное вложение Outlook 2010 или Outlook 2013 г. для просмотра и индексации.  <br/> |
   
## <a name="remarks"></a>Примечания

Outlook 2010 и Outlook 2013 года решения могут запрашивать этот интерфейс, чтобы узнать, заблокировано ли вложение. Вложения, заблокированные Outlook 2010 или Outlook 2013 г., различаются в зависимости от настройки Outlook 2010 или Outlook 2013 г. и политик, примененных администратором.
  
## <a name="see-also"></a>См. также



[Константы MAPI](mapi-constants.md)
  
[Проверка блокировки вложения](how-to-verify-an-attachment-is-blocked.md)

