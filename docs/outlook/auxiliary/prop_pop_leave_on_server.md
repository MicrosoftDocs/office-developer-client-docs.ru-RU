---
title: PROP_POP_LEAVE_ON_SERVER
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 22d7c1e8-48b9-4768-b4de-9a9f32a3aabb
description: Указывает, что копия сообщения на сервере остается на сервере для учетной записи POP.
ms.openlocfilehash: e1bbddea0f10c07d630676960d1b330f6055e137
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326490"
---
# <a name="proppopleaveonserver"></a>PROP_POP_LEAVE_ON_SERVER

Указывает, что копия сообщения на сервере остается на сервере для учетной записи POP.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Идентификатор:  <br/> |0x1000  <br/> |
|Тип свойства:  <br/> |ПТ_ДВОРД  <br/> |
|Тег свойства:  <br/> |0x10000003  <br/> |
|Обращения  <br/> |Только для чтения  <br/> |
   
## <a name="remarks"></a>Замечания

В приведенной ниже таблице перечислены возможные значения. Для [](constants-account-management-api.md) получения дополнительных сведений о константах см. 
  
|**Возможные значения**|**Описание**|
|:-----|:-----|
|**ЛЕАВЕ_ОН_СЕРВЕР** <br/> |Оставляет копию сообщения на сервере POP после загрузки сообщения на устройство.  <br/> |
|**РЕМОВЕ_АФТЕР** <br/> |Удаляет сообщение с сервера POP после его загрузки на устройство.  <br/> |
|**РЕМОВЕ_ОН_НУКЕ** <br/> |Удаляет сообщение с сервера POP только после того, как пользователь удалит сообщение из папки "Удаленные".  <br/> |
|**Жет_ремове_афтер_дайс** ( _UL_)  <br/> |Возвращает количество дней, по истечении которого сообщение будет удалено с сервера POP.  <br/> |
|**Сет_ремове_афтер_дайс** ( _дней_)  <br/> |Задает число дней, по истечении которого сообщение будет удалено с сервера POP.  <br/> |
   
## <a name="see-also"></a>См. также

- [Управление скачиванием сообщений для учетных записей POP3](managing-message-downloads-for-pop3-accounts.md) 
- [Constants (Account management API)](constants-account-management-api.md)

