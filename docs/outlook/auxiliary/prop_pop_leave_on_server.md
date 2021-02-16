---
title: PROP_POP_LEAVE_ON_SERVER
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 22d7c1e8-48b9-4768-b4de-9a9f32a3aabb
description: Указывает, что копия сообщения на сервере будет оставлена для учетной записи POP.
ms.openlocfilehash: e1bbddea0f10c07d630676960d1b330f6055e137
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410947"
---
# <a name="prop_pop_leave_on_server"></a>PROP_POP_LEAVE_ON_SERVER

Указывает, что копия сообщения на сервере будет оставлена для учетной записи POP.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Идентификатор:  <br/> |0x1000  <br/> |
|Тип свойства:  <br/> |PT_DWORD  <br/> |
|Тег свойства:  <br/> |0x10000003  <br/> |
|Access:  <br/> |Только для чтения  <br/> |
   
## <a name="remarks"></a>Примечания

В следующей таблице перечислены возможные значения. Дополнительные сведения о константах см. в записях [Constants (API](constants-account-management-api.md) управления учетной записью). 
  
|**Возможные значения**|**Описание**|
|:-----|:-----|
|**LEAVE_ON_SERVER** <br/> |Оставляет копию сообщения на POP-сервере после загрузки сообщения на устройство.  <br/> |
|**REMOVE_AFTER** <br/> |Удаляет сообщение с POP-сервера после его загрузки на устройство.  <br/> |
|**REMOVE_ON_NUKE** <br/> |Удаляет сообщение с POP-сервера только после удаления сообщения из папки "Удаленные".  <br/> |
|**GET_REMOVE_AFTER_DAYS**( _ul)_  <br/> |Получает количество дней, по и после которых сообщение будет удалено с POP-сервера.  <br/> |
|**SET_REMOVE_AFTER_DAYS**( _дней)_  <br/> |Задает количество дней, по и после которых сообщение будет удалено с POP-сервера.  <br/> |
   
## <a name="see-also"></a>См. также

- [Управление скачиванием сообщений для учетных записей POP3](managing-message-downloads-for-pop3-accounts.md) 
- [Constants (Account management API)](constants-account-management-api.md)

