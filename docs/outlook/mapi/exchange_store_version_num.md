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
ms.openlocfilehash: bf60b12a6e4575d3504a112aa2b54fb8c4ae23c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433726"
---
# <a name="exchangestoreversionnum"></a>EXCHANGE_STORE_VERSION_NUM

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Хранит сведения о версии для сервера Microsoft Exchange, к которому подключены учетные записи в профиле Microsoft Office Outlook.
  
## <a name="quick-info"></a>Краткие сведения

```cpp
typedef struct { 
    WORD wMajorVersion; 
    WORD wMinorVersion; 
    WORD wBuild; 
    WORD wMinorBuild; 
} EXCHANGE_STORE_VERSION_NUM; 

```

## <a name="members"></a>Элементы

 _Вмажорверсион_
  
- Основной номер версии, который обычно увеличивается, когда выпуск содержит существенные новые функции и изменения в функциональных возможностях.
    
 _Вминорверсион_
  
- Дополнительный номер версии, соответствующий определенному основному номеру версии, который обычно увеличивается, если выпуск содержит незначительные новые функции или существенные исправления.
    
 _Вбуилд_
  
- Основной номер сборки, соответствующий определенным основным и дополнительным номерам версий, который обычно увеличивается во внутреннем выпуске, содержащем новые функции или исправления. Это значение также увеличивается, когда выпуск является основной внутренней ветвью кода или вехой, например версией-кандидатом.
    
 _Вминорбуилд_
  
- Дополнительный номер сборки, который обычно увеличивается во внутреннем выпуске, в котором содержатся новые функции или исправления, соответствующие определенному основному построению, которое обозначает основную ветвь кода или веху.
    
## <a name="see-also"></a>См. также



[Сведения о дополнениях для MAPI](about-mapi-additions.md)
  
[Каноническое свойство PidTagProfileServerFullVersion](pidtagprofileserverfullversion-canonical-property.md)

