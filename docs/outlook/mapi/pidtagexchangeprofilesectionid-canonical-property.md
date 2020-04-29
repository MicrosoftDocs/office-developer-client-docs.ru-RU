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
  
Содержит динамически созданный идентификатор GUID, используемый для определения учетной записи при использовании нескольких учетных записей Microsoft Exchange Server.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_EMSMDB_SECTION_UID  <br/> |
|Идентификатор:  <br/> |0x3d150102  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Несколько учетных записей Exchange  <br/> |
   
## <a name="remarks"></a>Примечания

Microsoft Outlook 2010 и Microsoft Outlook 2013 поддерживают несколько учетных записей Exchange вместо одной учетной записи Exchange. Для поддержки нескольких учетных записей Exchange изменился макет профиля MAPI. В Microsoft Office Outlook 2007 и более ранних версий профили содержат раздел фиксированного профиля, выделенный для параметров Exchange, таких как имя сервера, имя пользователя и файл автономных папок (OST). расположение. Эти параметры были идентифицированы с помощью уникального идентификатора, свойства **пбглобалпрофилесектионгуид** . Раздел, используемый для параметров Exchange, называется разделом глобального профиля Exchange. 
  
Расположение раздела фиксированного профиля больше не является достаточным для размещения нескольких учетных записей Exchange. Вместо этого для каждой учетной записи Exchange в профиле существует раздел, выделенный для параметров этой учетной записи. Новый раздел, используемый для параметров Exchange, определяется уникальным идентификатором **емсмдбуид**.
  
В разделе профиль службы сообщений для учетной записи Exchange можно найти свойство, которое содержит GUID, динамически создаваемый во время создания учетной записи. Этот идентификатор GUID хранится в свойстве **PidTagExchangeProfileSectionId** . Хранилища сообщений и контейнеры адресных книг предоставляют свойство, определяющее учетную запись Exchange, к которой они относятся. Доступна в таблице Message Services, каждая служба Exchange предоставляет это свойство. 
  
Это свойство можно извлечь с помощью вызова метода [IMAPIProp::](imapiprop-getprops.md) PidTagExchangeProfileSectionId в **PidTagExchangeProfileSectionId** после запроса для любого из следующих интерфейсов: 
  
- [IMsgStore: IMAPIProp](imsgstoreimapiprop.md)
    
- [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
    
- [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)
    
Если объект не связан с Exchange, вызов возвращает **MAPI_E_NOT_FOUND**.
  
Вы можете ограничить контейнеры в **PidTagExchangeProfileSectionId** при отображении адресной книги. После открытия контейнера вы можете запросить **емсмдбуид** от него. Кроме того, следует отметить, что если получатель был выбран из адресной книги Exchange, у получателя также есть **PidTagExchangeProfileSectionId** в своем списке свойств. 
  
> [!NOTE]
> На протяжении всех примеров кода и заголовков функций этот идентификатор GUID называется **емсмдбуид**. 
  
Одна из учетных записей Exchange помечена как устаревшая учетная запись Exchange. Обычно это первая учетная запись, добавленная в профиль. Каждый вызов Open **пбглобалпрофилесектионгуид** перенаправляется в глобальный раздел Exchange устаревшей учетной записи. Вызовы объектной модели, взаимодействующие с неустаревшей учетной записью Exchange, также взаимодействуют с устаревшей учетной записью Exchange. 
  
Устаревшая служба Exchange имеет свойство **PR_EMSMDB_LEGACY** (0x3D18000B), для которого задано **значение true** в таблице службы сообщений. 
  
Устаревший **емсмдбуид** также помечаются в разделе глобального профиля Outlook профиля как **PidTagExchangeProfileSectionId**. Код, написанный для поддержки нескольких учетных записей Exchange, не должен извлекать устаревший **емсмдбуид** , так как он должен получить правильный **емсмдбуид**в зависимости от учетной записи, с которой взаимодействует код.
  
## <a name="see-also"></a>См. также



[Использование нескольких учетных записей Exchange](using-multiple-exchange-accounts.md)


[How To Open the Global Profile Section](https://support.microsoft.com/kb/188482)

