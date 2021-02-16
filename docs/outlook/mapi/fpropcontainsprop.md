---
title: FPropContainsProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FPropContainsProp
api_type:
- COM
ms.assetid: 43da5b59-7691-49aa-b83c-753d43bfd8fd
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ea56996ad56bb4ce93d103a75eba2c29e6059a87
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432634"
---
# <a name="fpropcontainsprop"></a>FPropContainsProp

**Относится к**: Outlook 2013 | Outlook 2016 
  
Сравнивает два значения свойств, как правило, строки или двоичные массивы, чтобы узнать, содержит ли один из них другой. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
BOOL FPropContainsProp(
  LPSPropValue lpSPropValueDst,
  LPSPropValue lpSPropValueSrc,
  ULONG ulFuzzyLevel
);
```

## <a name="parameters"></a>Параметры

_lpSPropValueDst_
  
> [in] Указатель на структуру [SPropValue,](spropvalue.md) определяющее значение свойства, которое может содержать строку поиска, на которую указывает параметр _lpSPropValueSrc._ 
    
_lpSPropValueSrc_
  
> [in] Указатель на **структуру SPropValue,** определяющей строку поиска, которую **ищет FPropContainsProp,** в значении свойства, на которое указывает параметр _lpSPropValueDst._ 
    
_ulFuzzyLevel_
  
> [in] Параметры, определяющие уровень точности, который будет применяться в сравнении. 

  - Нижние **16 битов** применяются к свойствам типа PT_BINARY и PT_STRING8. Для них должно быть установлено одно из следующих значений:
      
    - FL_FULLSTRING: строка поиска _lpSPropValueSrc_ должна быть равна значению свойства, _задаваемой lpSPropValueDst._
        
    - FL_PREFIX: строка поиска _lpSPropValueSrc_ должна отображаться в начале значения свойства, задаваемого _lpSPropValueDst._ Эти два значения следует сравнивать только с длиной строки поиска, задаваемой _lpSPropValueSrc._ 
        
    - FL_SUBSTRING: строка поиска _lpSPropValueSrc_ должна содержаться в любом месте значения свойства, задаваемом _lpSPropValueDst._ 
      
  - Верхние **16 битов** применяются только к свойствам типа PT_STRING8. В любом сочетании им можно установить следующие значения:
    
    - FL_IGNORECASE: сравнение должно быть выполнено без учета чувствительности к делу. 
        
    - FL_IGNORENONSPACE: сравнение должно игнорировать неспактические символы, определенные в Юникоде, например диакритические знаки. 
        
    - FL_LOOSE: сравнение должно указывать на соответствие, когда это возможно, игнорируя чувствительность к делу и символы, неспакинговые символы.
    
## <a name="return-value"></a>Возвращаемое значение

TRUE 
  
> Все параметры допустимы, а строка поиска _lpSPropValueSrc_ содержится, как указано в значении свойства _lpSPropValueDst._ 
    
FALSE 
  
> Сравниваемые значения свойств не имеют типа PT_STRING8 или PT_BINARY, значения свойств разных типов или строка поиска _lpSPropValueSrc_ не содержится, как указано в значении свойства _lpSPropValueDst._ 
    
## <a name="remarks"></a>Примечания

Метод сравнения зависит от типов свойств, указанных в определениях свойств [SPropValue,](spropvalue.md) и эвристичного эвристичного уровня нечеткого уровня, предоставленного в параметре _ulFuzzyLevel._ Функции [FPropCompareProp](fpropcompareprop.md) и **FPropContainsProp** можно использовать для подготовки ограничений для создания таблицы. 
  
Верхние 16 битов  _ulFuzzyLevel_ игнорируются для типа PT_BINARY. Если параметры  _в ulFuzzyLevel_ отсутствуют или недействительны, выполняется точное совпадение с полной строкой. Дополнительные сведения о реализации свойств см. в структуре [SContentRestriction.](scontentrestriction.md) 
  

