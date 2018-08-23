---
title: EXCHANGE_STORE_VERSION_NUM
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 88950eda-85ae-ad7a-46c6-0e1933d35e04
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 152afd68bea44f3485b2cc566f3f0d2768590704
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594476"
---
# <a name="exchangestoreversionnum"></a>EXCHANGE_STORE_VERSION_NUM

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Сохранение сведений о версии для Microsoft Exchange Server, подключенные учетные записи в профиле Microsoft Office Outlook.
  
## <a name="quick-info"></a>Краткие сведения

```cpp
typedef struct { 
    WORD wMajorVersion; 
    WORD wMinorVersion; 
    WORD wBuild; 
    WORD wMinorBuild; 
} EXCHANGE_STORE_VERSION_NUM; 

```

## <a name="members"></a>Members

 _wMajorVersion_
  
- Основной номер версии, который обычно увеличивается при выпуска содержит значительные новые функции и изменения в функциональных возможностях.
    
 _wMinorVersion_
  
- Дополнительный номер версии, который соответствует определенный основной номер версии и, как правило будет увеличен при выпуске незначительные новые функции и основные исправления.
    
 _wBuild_
  
- Основной номер построения, который соответствует определенного основной и дополнительный номер и, как правило будет увеличен в внутренний выпуск, который содержит новые функции или исправления. Это значение также увеличивается при выпуске основных внутреннего кода филиала или вехи, такие как версия-кандидат.
    
 _wMinorBuild_
  
- Номер дополнительный номер сборки, обычно увеличивается в внутренний выпуск, который содержит новые функции или исправляет, соответствующие определенным основных построения, который обозначает основных кода филиала или вехи.
    
## <a name="see-also"></a>См. также



[Сведения о дополнениях для MAPI](about-mapi-additions.md)
  
[Каноническое свойство PidTagProfileServerFullVersion](pidtagprofileserverfullversion-canonical-property.md)

