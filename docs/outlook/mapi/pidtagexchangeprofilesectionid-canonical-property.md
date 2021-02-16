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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит динамически генерируемый GUID, используемый для определения учетной записи при использовании нескольких Microsoft Exchange Server учетных записей.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_EMSMDB_SECTION_UID  <br/> |
|Идентификатор:  <br/> |0x3d150102  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Несколько учетных записей Exchange  <br/> |
   
## <a name="remarks"></a>Примечания

Microsoft Outlook 2010, русская версия Microsoft Outlook 2013 поддерживают несколько учетных записей Exchange вместо одной учетной записи Exchange. Для размещения нескольких учетных записей Exchange макет профиля MAPI был изменен. В Microsoft Office Outlook 2007 и более ранних, профили содержали фиксированный раздел профиля, выделенный для параметров Exchange, таких как имя сервера, имя пользователя и файл автономной папки (OST). расположение. Эти параметры были определены с помощью уникального идентификатора, **свойства pbGlobalProfileSectionGuid.** Раздел, используемый для параметров Exchange, называется разделом глобального профиля Exchange. 
  
Фиксированного расположения раздела профиля больше недостаточно для размещения нескольких учетных записей Exchange. Вместо этого для каждой учетной записи Exchange в профиле существует раздел, выделенный для параметров этой учетной записи. Новый раздел, используемый для параметров Exchange, определяется уникальным идентификатором **emsmdbUID.**
  
В разделе профиля службы сообщений для учетной записи Exchange можно найти свойство, которое содержит GUID, динамически генерируемый во время создания учетной записи. Этот GUID хранится в свойстве **PidTagExchangeProfileSectionId.** Хранилища сообщений и контейнеры адресной книги предоставляет свойство, определяя, к какой учетной записи Exchange они принадлежат. Доступно в таблице служб сообщений, каждая служба Exchange предоставляет это свойство. 
  
Это свойство можно получить с помощью вызова [IMAPIProp::GetProps](imapiprop-getprops.md) на **pidTagExchangeProfileSectionId** после запроса любого из следующих интерфейсов: 
  
- [IMsgStore: IMAPIProp](imsgstoreimapiprop.md)
    
- [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
    
- [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)
    
Если объект не связан с Exchange, вызов возвращает **MAPI_E_NOT_FOUND.**
  
При отображении адресной книги можно ограничить контейнеры **для PidTagExchangeProfileSectionId.** После открытия контейнера можно запросить у **него emsmdbUID.** Также стоит отметить, что если получатель был выбран из адресной книги Exchange, в списке свойств получателя также есть **pidTagExchangeProfileSectionId.** 
  
> [!NOTE]
> Во всех примерах кода и в заголовщиках функций этот GUID называется **emsmdbUID.** 
  
Одна из учетных записей Exchange помечена как устаревшая учетная запись Exchange. Обычно это первая учетная запись, добавленная в профиль. Каждый вызов для открытия **pbGlobalProfileSectionGuid** перенаправляется в глобальный раздел Exchange устаревшей учетной записи. Вызовы объектной модели, взаимодействующие с устаревшей учетной записью Exchange, также взаимодействуют с устаревшей учетной записью Exchange. 
  
Устаревшая служба Exchange имеет свойство **PR_EMSMDB_LEGACY** (0x3D18000B), которое имеет true **в** таблице служб сообщений. 
  
**Устаревшее emsmdbUID** также помещается в разделе глобального профиля Outlook профиля как **PidTagExchangeProfileSectionId.** Код, написанный для поддержки нескольких учетных записей Exchange, не должен извлекать устаревший **emsmdbUID,** так как он должен получать правильный **emsmdbUID** в зависимости от учетной записи, с помощью которых взаимодействует код.
  
## <a name="see-also"></a>См. также



[Использование нескольких учетных записей Exchange](using-multiple-exchange-accounts.md)


[How To Open the Global Profile Section](https://support.microsoft.com/kb/188482)

