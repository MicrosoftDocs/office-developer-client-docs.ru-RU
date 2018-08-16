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
ms.openlocfilehash: 48dfced07a8fd78a1af22679759effbd3c6da343
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810810"
---
# <a name="pidtagaddressbookchoosedirectoryautomatically-canonical-property"></a>Каноническое свойство PidTagAddressBookChooseDirectoryAutomatically

  
  
**Относится к**: Outlook 
  
Позволяет выбрать наиболее подходящую глобальном списке адресов (GAL) или папку "Контакты" для текущего почтового ящика Microsoft Outlook 2010 и Microsoft Outlook 2013.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY  <br/> |
|Идентификатор:  <br/> |0x3D1C000B  <br/> |
|Тип свойства:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Адресная книга  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство соответствует параметру **автоматически выбирать** в диалоговом окне параметры адресной книги. Когда это свойство в разделе профилей IID_CAPONE_PROF существует и имеет значение **true**, в адресной книге диалоговое окно больше не по умолчанию контейнер, указанный с помощью метода [SetDefaultDir](iaddrbook-setdefaultdir.md) , но выбирает к адресной книге, Outlook 2010 или Outlook 2013 рассматривает контексту, в котором диалоговое окно отображается. Обратите внимание на то, что это может привести к низкого уровня качества для поставщиками сторонних производителей адресной книги. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

Mapitags.h
  
> Содержит определения свойств указано, что связанными свойствами.
    
Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[��������� MAPI](mapi-constants.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)
