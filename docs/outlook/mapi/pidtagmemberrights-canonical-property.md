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
ms.openlocfilehash: 2ffc6973d2670402ec8095120eea3db02f529d0a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811355"
---
# <a name="pidtagmemberrights-canonical-property"></a>Каноническое свойство PidTagMemberRights

  
  
**Относится к**: Outlook 
  
Содержит набор битов, указанных правами этот член в папке или почтового ящика.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_MEMBER_RIGHTS  <br/> |
|Идентификатор:  <br/> |0x6673  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Управление доступом  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство используется интерфейс [IExchangeModifyTable](iexchangemodifytableiunknown.md) для определения прав элемента в папке. Эти права можно отображения и изменения. Права, определенные для этого свойства являются следующие значения. 
  
frightsReadAny
  
> Член могут читать все сообщения.
    
frightsCreate
  
> Член можно создавать сообщения.
    
frightsEditOwned
  
> Участник может изменять все сообщения, принадлежащие пользователю.
    
frightsDeleteOwned
  
> Член можно удалить все сообщения, принадлежащие пользователю.
    
frightsEditAny
  
> Участник может изменять любые сообщения.
    
frightsDeleteAny
  
> Член можно удалить все сообщения.
    
frightsCreateSubfolder
  
> Член можно создать вложенные папки.
    
frightsOwner
  
> Элемент имеет все перечисленные выше права на папку.
    
frightsContact
  
> Элемент может иметь свое имя контакта в общей папке.
    
frightsVisible
  
> Член можно увидеть, что папка существует.
    
rightsNone
  
> Член не имеет права на папку.
    
rightsReadOnly
  
> Член могут читать все сообщения в папке.
    
rightsReadWrite
  
> Член могут выполнять чтение и запись для всех сообщений в папке.
    
rightsAll
  
> Элемент имеет все перечисленные выше права на папку.
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Обрабатывает операции папки.
    
[[MS-OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)
  
> Обрабатывает извлечения списков разрешений папки, которые хранятся на сервере.
    
[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Указывает методы для подключений и настройки почтовых ящиков как делегаты и взаимодействия с элементами календаря и сообщения, когда они действовать от имени другого пользователя.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств указано, что связанными свойствами.
    
## <a name="see-also"></a>См. также



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

