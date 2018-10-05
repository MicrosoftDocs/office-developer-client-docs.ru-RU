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
ms.openlocfilehash: 7843a31094d2564f30000f21ee888e525f39f960
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397186"
---
# <a name="pidtagexchangeprofilesectionid-canonical-property"></a>Каноническое свойство PidTagExchangeProfileSectionId

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит динамически созданных GUID используется для определения учетной записи при использовании нескольких учетных записей сервера Microsoft Exchange.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_EMSMDB_SECTION_UID  <br/> |
|Идентификатор:  <br/> |0x3d150102  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Несколько учетных записей Exchange  <br/> |
   
## <a name="remarks"></a>Замечания

Microsoft Outlook 2010 и Microsoft Outlook 2013 поддерживает несколько учетных записей Exchange вместо одной одной учетной записи Exchange. Чтобы обеспечить несколько учетных записей Exchange, макет профилей MAPI был изменен. В Microsoft Office Outlook 2007 и более ранних версий профили содержащиеся раздела основных профиля, выделенного для параметров Exchange, такие как имя сервера, имя пользователя и файла автономной папки (OST). расположение. Эти параметры обнаружены с помощью уникального идентификатора, свойство **pbGlobalProfileSectionGuid** . Раздел, используемый для параметров Exchange называется глобального раздела профиля Exchange. Дополнительные сведения о глобальных профиля Exchange в Outlook 2007 [как открыть общий раздел профилей](https://support.microsoft.com/kb/188482)см.
  
Расположение раздела основных профиля больше не достаточно для учета нескольких учетных записей Exchange. Вместо этого для каждой учетной записи Exchange в профиле раздел существует, предназначенный для параметров для этой учетной записи. Уникальный идентификатор **emsmdbUID**определяется новый раздел, используемые для параметров Exchange.
  
В разделе профиля службы сообщений для учетной записи Exchange можно найти свойство, которое содержит идентификатор GUID, создаваемый динамически во время создания учетной записи. Идентификатор GUID хранится в свойстве **PidTagExchangeProfileSectionId** . Хранилищ сообщений и адресной книги контейнеры предоставляют свойство так, чтобы определить, какая учетная запись Exchange, он входит. Доступно в таблице служб сообщения, это свойство предоставляет каждой службы Exchange. 
  
Это свойство посредством вызова [IMAPIProp::GetProps](imapiprop-getprops.md) на **PidTagExchangeProfileSectionId** можно получить после запроса для каких-либо следующие интерфейсы: 
  
- [IMsgStore: IMAPIProp](imsgstoreimapiprop.md)
    
- [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
    
- [IABContainer : IMAPIContainer](iabcontainerimapicontainer.md)
    
Если объект не связан с сервером Exchange, вызов возвращает **MAPI_E_NOT_FOUND**.
  
Можно ограничить контейнеров в **PidTagExchangeProfileSectionId** при отображении в адресной книге. При наличии открытых контейнер, можно выполнить запрос **emsmdbUID** из нее. Это также следует отметить, что если получатель была выбрана в адресной книге Exchange, у получателя также установлена **PidTagExchangeProfileSectionId** в списке свойств. 
  
> [!NOTE]
> Идентификатор GUID во всей функции заголовки и примеры кода, называется **emsmdbUID**. 
  
Один из учетных записей Exchange отмечен как устаревшие учетные записи Exchange. Как правило это первую учетную запись, добавляемого к профилю. Каждого вызова, чтобы открыть **pbGlobalProfileSectionGuid** перенаправляется в глобальный раздел Exchange прежней версии. Вызовы объектной модели, которые взаимодействуют с учетной записью Exchange не прежних версий также взаимодействовать с учетной записью Exchange прежних версий. 
  
Служба Exchange прежних версий имеет свойство **PR_EMSMDB_LEGACY** (0x3D18000B) которого имеет значение **true** в таблице служб сообщения. 
  
Прежних версий **emsmdbUID** также записывается в раздел глобальный профиль Outlook профиля как **PidTagExchangeProfileSectionId**. Код, написанный для поддержки нескольких учетных записей Exchange для получения прежних версий **emsmdbUID** , так как он должны получить правильные **emsmdbUID**, в зависимости от того, с учетной записью, взаимодействует код не должен.
  
## <a name="see-also"></a>См. также



[Использование нескольких учетных записей Exchange](using-multiple-exchange-accounts.md)


[How To Open the Global Profile Section](https://support.microsoft.com/kb/188482)

