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
# <a name="exchange_store_version_num"></a>EXCHANGE_STORE_VERSION_NUM

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Сохраняет сведения о версии для Microsoft Exchange Server учетных записей в профиле Microsoft Office Outlook подключены к.
  
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

 _wMajorVersion_
  
- Основной номер версии, который обычно приращен, когда выпуск содержит значительные новые функции и изменения в функциональных возможностях.
    
 _wMinorVersion_
  
- Незначительный номер версии, соответствующий определенному основному номеру версии и который, как правило, приращен, когда выпуск содержит незначительные новые функции или значительные исправления.
    
 _wBuild_
  
- Основной номер сборки, соответствующий определенным основным и незначительным номерам версий и обычно приращенный во внутреннем выпуске, который содержит новые функции или исправления. Это значение также приумножная, если выпуск является основной ветвью внутреннего кода или вехой, например кандидатом на выпуск.
    
 _wMinorBuild_
  
- Небольшой номер сборки, который обычно приращен во внутреннем выпуске, который содержит новые функции или исправления, соответствующие определенной крупной сборке, которая обозначает главную ветвь кода или веху.
    
## <a name="see-also"></a>См. также



[Сведения о дополнениях для MAPI](about-mapi-additions.md)
  
[Каноническое свойство PidTagProfileServerFullVersion](pidtagprofileserverfullversion-canonical-property.md)

