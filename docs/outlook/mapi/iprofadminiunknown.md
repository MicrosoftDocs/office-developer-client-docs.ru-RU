---
title: IProfAdmin IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin
api_type:
- COM
ms.assetid: 274899cc-2894-4d99-84ec-f18121e856a0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 28dd45f29610b7ad56b4d3302715311569d497c4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577417"
---
# <a name="iprofadmin--iunknown"></a>IProfAdmin : IUnknown

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Поддерживает управления профилями. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapix.h  <br/> |
|Предоставляемые:  <br/> |Объект администрирования профилей  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IProfAdmin  <br/> |
|Тип указателя:  <br/> |LPPROFADMIN  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[GetLastError](iprofadmin-getlasterror.md) <br/> |Возвращает структуру [MAPIERROR](mapierror.md) , который содержит сведения о предыдущем ошибки, которые произошли в объект администрирования профилей.  <br/> |
|[GetProfileTable](iprofadmin-getprofiletable.md) <br/> |Предоставляет доступ к таблице профилей таблицу, содержащую сведения обо всех доступных профилей.  <br/> |
|[CreateProfile](iprofadmin-createprofile.md) <br/> |Создает новый профиль.  <br/> |
|[DeleteProfile](iprofadmin-deleteprofile.md) <br/> |Удаляет профиль.  <br/> |
|[ChangeProfilePassword](iprofadmin-changeprofilepassword.md) <br/> |Рекомендуется использовать. Изменение пароля для профиля.  <br/> |
|[CopyProfile](iprofadmin-copyprofile.md) <br/> |Копирует профиль.  <br/> |
|[RenameProfile](iprofadmin-renameprofile.md) <br/> |Назначает новое имя профиля.  <br/> |
|[SetDefaultProfile](iprofadmin-setdefaultprofile.md) <br/> |Устанавливает или удаляет профиль клиента по умолчанию.  <br/> |
|[AdminServices](iprofadmin-adminservices.md) <br/> |Предоставляет доступ к объекту администрирования службы сообщений для внесения изменений в службы сообщений в профиле.  <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

