---
title: Каноническое свойство PidTagMemberRights
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMemberRights
api_type:
- HeaderDef
ms.assetid: 3e526b93-1f64-41ea-b43c-5b03fe1c56ed
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: dcbf8a323f5178a5a2e39d0963dd19415ab835bd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342696"
---
# <a name="pidtagmemberrights-canonical-property"></a>Каноническое свойство PidTagMemberRights

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит набор битов, которые указали права этого члена в папке или почтовом ящике.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_MEMBER_RIGHTS  <br/> |
|Идентификатор:  <br/> |0x6673  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Управление доступом  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство используется интерфейсом [IExchangeModifyTable](iexchangemodifytableiunknown.md) для определения прав члена папки. Эти права могут отображаться и изменяться. Следующие значения являются правами, определенными для этого свойства. 
  
frightsReadAny
  
> Участник может читать любые сообщения.
    
frightsCreate
  
> Участник может создавать сообщения.
    
frightsEditOwned
  
> Участник может редактировать любые сообщения, которые принадлежат пользователю.
    
frightsDeleteOwned
  
> Участник может удалять любые сообщения, которые принадлежат пользователю.
    
frightsEditAny
  
> Участник может редактировать любое сообщение.
    
frightsDeleteAny
  
> Участник может удалить любое сообщение.
    
frightsCreateSubfolder
  
> Участник может создавать вложенные папки для папки.
    
frightsOwner
  
> У участника есть все предыдущие права на папку.
    
frightsContact
  
> Член может отображать ваше имя в качестве контакта в папке.
    
frightsVisible
  
> Член может видеть, что папка существует.
    
rightsNone
  
> У участника нет прав на папку.
    
rightsReadOnly
  
> Участник может читать любое сообщение в папке.
    
rightsReadWrite
  
> Участник может читать и записывать любые сообщения в папке.
    
rightsAll
  
> У участника есть все предыдущие права на папку.
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Обрабатывает операции с папками.
    
[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)
  
> Обрабатывает и получить списки разрешений папок, хранимые на сервере.
    
[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Указывает методы подключения и настройки почтовых ящиков в качестве делегатов, а также взаимодействия с элементами сообщений и календаря, когда они действуют от имени другого пользователя.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

