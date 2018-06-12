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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: abf33e4167d836aeb88fdefb30ba05840e80ce63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808497"
---
# <a name="fpropcontainsprop"></a>FPropContainsProp

**Применимо к**: Outlook 
  
Сравнивает два значения свойств, обычно строк или двоичные массивы, если один содержит другое. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Mapiutil.h  <br/> |
|Реализованный:  <br/> |MAPI  <br/> |
|Вызывается:  <br/> |Клиентские приложения и поставщиков услуг  <br/> |
   
```cpp
BOOL FPropContainsProp(
  LPSPropValue lpSPropValueDst,
  LPSPropValue lpSPropValueSrc,
  ULONG ulFuzzyLevel
);
```

## <a name="parameters"></a>Parameters

_lpSPropValueDst_
  
> [in] Указатель на структуру [SPropValue](spropvalue.md) , определяющее значение свойства, которое может содержать строку поиска, на который указывает параметр _lpSPropValueSrc_ . 
    
_lpSPropValueSrc_
  
> [in] Указатель на структуру **SPropValue** определение строку поиска, поиск **FPropContainsProp** в значение свойства, на который указывает параметр _lpSPropValueDst_ . 
    
_ulFuzzyLevel_
  
> [in] Параметр параметры определение уровня привыкли использовать для сравнения. 

  - **Снижение 16-разрядный** относятся к свойств типа PT_BINARY и PT_STRING8. Они должны иметь значение только один из следующих значений:
      
    - FL_FULLSTRING: Строка поиска _lpSPropValueSrc_ должно быть равно значению свойства, определяемую средством _lpSPropValueDst_.
        
    - FL_PREFIX: Строка поиска _lpSPropValueSrc_ , которые должны встречаться в начале значение свойства, определяемую средством _lpSPropValueDst_. Только полностью заполняя длину строки поиска, указанный в параметре _lpSPropValueSrc_сравнения двух значений. 
        
    - FL_SUBSTRING: Строка поиска _lpSPropValueSrc_ должны быть включены в любом месте в значение свойства, определяемую средством _lpSPropValueDst_. 
      
  - **Верхний 16-разрядный** применяются только к свойств типа PT_STRING8. Они могут применяться следующие значения в любом сочетании:
    
    - FL_IGNORECASE: Необходимо выполнить сравнение без учета регистра. 
        
    - FL_IGNORENONSPACE: Сравнение следует игнорировать определенные Юникод непробельные символы, такие как диакритические знаки. 
        
    - FL_LOOSE: Сравнение следует указать соответствие по возможности без учета регистра знаков и непробельные символы.
    
## <a name="return-value"></a>������������ ��������

TRUE 
  
> Параметры доступны и строка поиска _lpSPropValueSrc_ содержится указанный в значение свойства _lpSPropValueDst_ . 
    
FALSE 
  
> Сравниваемые значения свойства не типа PT_STRING8 или PT_BINARY, значения свойств относятся к различным типам или не содержится строка поиска _lpSPropValueSrc_ , как указано в значение свойства _lpSPropValueDst_ . 
    
## <a name="remarks"></a>Замечания

Метод сравнения зависит от типы свойств, указанных в определениях свойство [SPropValue](spropvalue.md) и нечеткое уровня совет, заданного в параметре _ulFuzzyLevel_ . Функции [FPropCompareProp](fpropcompareprop.md) и **FPropContainsProp** можно использовать для подготовки ограничения для создания таблицы. 
  
Для типа свойства PT_BINARY верхнем 16 бит _ulFuzzyLevel_ игнорируются. Если в параметрах _ulFuzzyLevel_ отсутствует или недопустимо, выполняется точного совпадения строки full. Дополнительные сведения о вложенности свойство Просмотр структуры [SContentRestriction](scontentrestriction.md) . 
  

