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

**Область применения**: Outlook 2013 | Outlook 2016 
  
Сравнивает два значения свойств, как правило, строки или двоичные массивы, чтобы узнать, содержит ли одно другое. 
  
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

## <a name="parameters"></a>Parameters

_lpSPropValueDst_
  
> [in] Указатель на [структуру SPropValue,](spropvalue.md) определяющей значение свойства, которое может содержать строку поиска, указываемую параметром _lpSPropValueSrc._ 
    
_lpSPropValueSrc_
  
> [in] Указатель на **структуру SPropValue,** определяющей строку поиска, которую **ищет FPropContainsProp,** в значении свойства, на которое указывает параметр _lpSPropValueDst._ 
    
_ulFuzzyLevel_
  
> [in] Параметры, определяющие уровень точности, который необходимо использовать в сопоставлении. 

  - Нижние **16 битов** применяются к свойствам типа PT_BINARY и PT_STRING8. Они должны быть назначены как раз к одному из следующих значений:
      
    - FL_FULLSTRING. Строка поиска _lpSPropValueSrc_ должна быть равна значению свойства, установленного _lpSPropValueDst._
        
    - FL_PREFIX. Строка поиска  _lpSPropValueSrc_ должна отображаться в начале значения свойства, установленного  _lpSPropValueDst_. Эти два значения следует сравнить только с длиной строки поиска, обозначенной _lpSPropValueSrc._ 
        
    - FL_SUBSTRING. Строка поиска _lpSPropValueSrc_ должна содержаться в любом месте в значении свойства, идентифицированного _lpSPropValueDst._ 
      
  - Верхние **16 битов** применяются только к свойствам типа PT_STRING8. Они могут быть установлены к следующим значениям в любой комбинации:
    
    - FL_IGNORECASE. Сравнение должно быть выполнено без рассмотрения чувствительности к делу. 
        
    - FL_IGNORENONSPACE. Сравнение должно игнорировать неспаксированные символы, определенные Юникодом, такие как диакритические знаки. 
        
    - FL_LOOSE. Сравнение должно указывать совпадение по мере возможности, игнорируя чувствительность к делу и неспаные символы.
    
## <a name="return-value"></a>Возвращаемое значение

TRUE 
  
> Все параметры действительны, а строка поиска _lpSPropValueSrc_ содержится в значении _свойства lpSPropValueDst._ 
    
FALSE 
  
> Сравниваемые значения свойств не имеют типа PT_STRING8 или PT_BINARY, значения свойств имеют различные типы, или строка поиска _lpSPropValueSrc_ не содержится, как указано в значении свойства _lpSPropValueDst._ 
    
## <a name="remarks"></a>Примечания

Метод сравнения зависит от типов свойств, указанных в определениях [свойств SPropValue,](spropvalue.md) и эвристичного уровня нечетких уровней, указанных в параметре _ulFuzzyLevel._ Функции [FPropCompareProp](fpropcompareprop.md) и **FPropContainsProp** можно использовать для подготовки ограничений для создания таблицы. 
  
Верхние 16  _битов ulFuzzyLevel_ игнорируются для типа PT_BINARY. Если параметры  _в ulFuzzyLevel_ отсутствуют или недействительны, выполняется полное совпадение точных строк. Дополнительные сведения о сдерживании свойств см. в структуре [SContentRestriction.](scontentrestriction.md) 
  

