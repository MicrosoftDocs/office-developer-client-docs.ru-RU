---
title: Каноническое свойство PidTagAddressBookChooseDirectoryAutomatically
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cecd0679-4bc2-4399-8f89-a4e17bb909a0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 41fdaf333084b7d567f4e67ae9fd2638a1731349
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359792"
---
# <a name="pidtagaddressbookchoosedirectoryautomatically-canonical-property"></a>Каноническое свойство PidTagAddressBookChooseDirectoryAutomatically

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Позволяет Microsoft Outlook 2010 и Microsoft Outlook 2013 выбрать наиболее подходящий глобальный список адресов (GAL) или папку контактов для текущего почтового ящика.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_АБ_ЧУСЕ_ДИРЕКТОРИ_АУТОМАТИКАЛЛИ  <br/> |
|Идентификатор:  <br/> |0x3D1C000B  <br/> |
|Тип свойства:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Адресная книга  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство соответствует параметру **выбрать автоматический** параметр в диалоговом окне Параметры адресной книги. Если это свойство существует в разделе profile ИИД_КАПОНЕ_ПРОФ и имеет значение **true**, диалоговое окно адресной книги больше не будет использоваться по умолчанию в контейнере, указанном в методе [сетдефаултдир](iaddrbook-setdefaultdir.md) , но выбирает адресную книгу, которую outlook 2010 или Outlook 2013 подсчитается подходящим для контекста, в котором отображается диалоговое окно. Обратите внимание, что это может привести к неудовлетворительному взаимодействию сторонних поставщиков адресных книг. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заГоловков

Мапитагс. h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
MAPIDEFS. h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[��������� MAPI](mapi-constants.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

