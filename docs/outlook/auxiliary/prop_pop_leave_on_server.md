---
title: PROP_POP_LEAVE_ON_SERVER
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 22d7c1e8-48b9-4768-b4de-9a9f32a3aabb
description: Указывает, сохранение копий сообщений на сервере для учетной записи POP.
ms.openlocfilehash: 9f986ff60a5824ece0a8bb91619323b58ec8b87a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807947"
---
# <a name="proppopleaveonserver"></a>PROP_POP_LEAVE_ON_SERVER

Указывает, сохранение копий сообщений на сервере для учетной записи POP.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Идентификатор:  <br/> |0x1000  <br/> |
|Тип свойства:  <br/> |PT_DWORD  <br/> |
|Свойство tag:  <br/> |0x10000003  <br/> |
|Access:  <br/> |Только для чтения  <br/> |
   
## <a name="remarks"></a>Замечания

В следующей таблице приведены возможные значения. Для получения дополнительных сведений о константы видеть [константы (Управление учетными записями API)](constants-account-management-api.md) . 
  
|**Возможные значения**|**Описание**|
|:-----|:-----|
|**LEAVE_ON_SERVER** <br/> |Покидает копии сообщения на POP-сервер после загрузки сообщения с устройством.  <br/> |
|**REMOVE_AFTER** <br/> |Удаляет сообщение с POP-сервера после загрузки на устройство.  <br/> |
|**REMOVE_ON_NUKE** <br/> |Удаляет сообщение из POP-сервер только после пользователь удаляет сообщение из папки «Удаленные».  <br/> |
|**GET_REMOVE_AFTER_DAYS** ( _ul_)  <br/> |Получает количество дней, после которого сообщение будет удален из POP-сервера.  <br/> |
|**SET_REMOVE_AFTER_DAYS** ( _дней_)  <br/> |Задает число дней, после которого сообщение будет удален из POP-сервера.  <br/> |
   
## <a name="see-also"></a>См. также

- [Управление скачиванием сообщений для учетных записей POP3](managing-message-downloads-for-pop3-accounts.md) 
- [Constants (Account management API)](constants-account-management-api.md)

