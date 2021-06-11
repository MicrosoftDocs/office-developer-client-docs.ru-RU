---
title: Каноническое свойство PidTagExchangeProfileSectionId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExchangeProfileSectionId
api_type:
- HeaderDef
ms.assetid: 4ad2f417-be8f-4fc8-9321-82097289074b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ce823159047410a8cea13b7eff5566cd8abaa5b9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316431"
---
# <a name="pidtagexchangeprofilesectionid-canonical-property"></a>Каноническое свойство PidTagExchangeProfileSectionId

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит динамически созданный GUID, используемый для определения учетной записи при использовании нескольких Microsoft Exchange Server учетных записей.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_EMSMDB_SECTION_UID  <br/> |
|Идентификатор:  <br/> |0x3d150102  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Несколько учетных записей Exchange  <br/> |
   
## <a name="remarks"></a>Примечания

Microsoft Outlook 2010, русская версия и Microsoft Outlook 2013 поддерживают несколько Exchange учетных записей вместо одной Exchange учетной записи. Для размещения нескольких Exchange учетных записей был изменен макет профиля MAPI. В Microsoft Office Outlook 2007 г. и ранее профили содержали фиксированный раздел профиля, посвященный Exchange параметров, таких как имя сервера, имя пользователя и автономный файл папки (.ost). расположение. Эти параметры были определены с помощью уникального **идентификатора, свойства pbGlobalProfileSectionGuid.** Раздел, используемый для Exchange параметров, называется разделом глобального Exchange профиля. 
  
Расположения фиксированного раздела профиля больше недостаточно для размещения нескольких Exchange учетных записей. Вместо этого для Exchange учетной записи в профиле существует раздел, посвященный настройкам этой учетной записи. Новый раздел, используемый для Exchange параметров, определяется уникальным идентификатором **emsmdbUID.**
  
В разделе профиль службы сообщений для учетной записи Exchange вы можете найти свойство, которое содержит GUID, динамически созданный на момент создания учетной записи. Этот GUID хранится в **свойстве PidTagExchangeProfileSectionId.** Хранилища сообщений и контейнеры адресной книги раскрывают свойство, чтобы определить, Exchange учетной записи, к которой они принадлежат. Доступные в таблице служб сообщений, каждая Exchange предоставляет это свойство. 
  
Это свойство можно получить с помощью вызова [в IMAPIProp::GetProps](imapiprop-getprops.md) на **PidTagExchangeProfileSectionId** после запроса на любой из следующих интерфейсов: 
  
- [IMsgStore: IMAPIProp](imsgstoreimapiprop.md)
    
- [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
    
- [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)
    
Если объект не связан с Exchange, вызов возвращается **MAPI_E_NOT_FOUND.**
  
Вы можете ограничить контейнеры **на PidTagExchangeProfileSectionId** при отображении адресной книги. После открытия контейнера можно запросить **у него emsmdbUID.** Также стоит отметить, что если получатель был выбран из Exchange адресной книги, получатель также имеет в списке свойств **PidTagExchangeProfileSectionId.** 
  
> [!NOTE]
> На всех примерах кода и в заголовке функций этот GUID известен как **emsmdbUID.** 
  
Одна из Exchange помечена как устаревшая Exchange учетная запись. Обычно это первая учетная запись, добавленная в профиль. Каждый вызов для открытия **pbGlobalProfileSectionGuid** перенаправляется Exchange глобальный раздел устаревшей учетной записи. Вызовы объектной модели, взаимодействующие с Exchange учетной записью, также взаимодействуют с Exchange учетной записью. 
  
Устаревшая Exchange имеет свойство **PR_EMSMDB_LEGACY** (0x3D18000B), которое установлено в таблице  служб сообщений. 
  
Устаревший **emsmdbUID** также штампуется в разделе глобального профиля Outlook профиля **как PidTagExchangeProfileSectionId**. Код, написанный для поддержки нескольких Exchange учетных записей, не должен получать устаревший **emsmdbUID,** так как он должен получать правильный **emsmdbUID,** в зависимости от учетной записи, с помощью которых взаимодействует код.
  
## <a name="see-also"></a>См. также



[Использование нескольких Exchange учетных записей](using-multiple-exchange-accounts.md)


[How To Open the Global Profile Section](https://support.microsoft.com/kb/188482)

