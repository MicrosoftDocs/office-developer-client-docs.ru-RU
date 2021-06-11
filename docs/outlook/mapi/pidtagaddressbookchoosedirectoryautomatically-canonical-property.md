---
title: PidTagAddressBookChooseDirectoryAutomatically Canonical Property
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cecd0679-4bc2-4399-8f89-a4e17bb909a0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 41fdaf333084b7d567f4e67ae9fd2638a1731349
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409666"
---
# <a name="pidtagaddressbookchoosedirectoryautomatically-canonical-property"></a>PidTagAddressBookChooseDirectoryAutomatically Canonical Property

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Позволяет Microsoft Outlook 2010, русская версия и Microsoft Outlook 2013 выбрать наиболее подходящий глобальный адресный список (GAL) или контактную папку для текущего почтового ящика.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY  <br/> |
|Идентификатор:  <br/> |0x3D1C000B  <br/> |
|Тип свойства:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Адресная книга  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство соответствует параметру **Выбор автоматически** в диалоговом диалоговом окте "Параметры адресной книги". Если это свойство существует в разделе IID_CAPONE_PROF профиля и задано значение **true,** диалоговое окно адресной книги больше не по умолчанию подходит для контейнера, указанного методом [SetDefaultDir,](iaddrbook-setdefaultdir.md) но выбирает адресную книгу, Outlook 2010 или Outlook 2013 г. для контекста, в котором диалоговое окно отображалось. Обратите внимание, что это может привести к плохому опыту сторонних поставщиков адресных книг. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовки

Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве связанных свойств.
    
Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[��������� MAPI](mapi-constants.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

