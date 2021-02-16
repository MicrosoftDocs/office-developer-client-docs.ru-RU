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
ms.openlocfilehash: cbdfba68490b1e756f277c6e552235368a86f310
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434118"
---
# <a name="iprofadmin--iunknown"></a>IProfAdmin : IUnknown

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Поддерживает администрирование профилей. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapix.h  <br/> |
|Выставим:  <br/> |Объект администрирования профилей  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IProfAdmin  <br/> |
|Тип указателя:  <br/> |LPPROFADMIN  <br/> |
   
## <a name="vtable-order"></a>Порядок ветвей

|||
|:-----|:-----|
|[GetLastError](iprofadmin-getlasterror.md) <br/> |Возвращает структуру [MAPIERROR, которая](mapierror.md) содержит сведения о предыдущей ошибке, которая произошла в объекте администрирования профиля.  <br/> |
|[GetProfileTable](iprofadmin-getprofiletable.md) <br/> |Предоставляет доступ к таблице профилей, которая содержит сведения обо всех доступных профилях.  <br/> |
|[CreateProfile](iprofadmin-createprofile.md) <br/> |Создает новый профиль.  <br/> |
|[DeleteProfile](iprofadmin-deleteprofile.md) <br/> |Удаляет профиль.  <br/> |
|[ChangeProfilePassword](iprofadmin-changeprofilepassword.md) <br/> |Устарело. Изменяет пароль для профиля.  <br/> |
|[CopyProfile](iprofadmin-copyprofile.md) <br/> |Копирует профиль.  <br/> |
|[RenameProfile](iprofadmin-renameprofile.md) <br/> |Назначает новое имя для профиля.  <br/> |
|[SetDefaultProfile](iprofadmin-setdefaultprofile.md) <br/> |Задает или очищает профиль клиента по умолчанию.  <br/> |
|[AdminServices](iprofadmin-adminservices.md) <br/> |Предоставляет доступ к объекту администрирования службы сообщений для внесения изменений в службы сообщений в профиле.  <br/> |
   
## <a name="see-also"></a>См. также



[Интерфейсы MAPI](mapi-interfaces.md)

