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
ms.openlocfilehash: 00d92f8e2ec3af766d5b241d1a911be304b346d6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808394"
---
# <a name="exchangestoreversionnum"></a>EXCHANGE_STORE_VERSION_NUM

  
  
**Относится к**: Outlook 
  
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

