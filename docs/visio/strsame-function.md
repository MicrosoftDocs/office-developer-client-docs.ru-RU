---
title: Функция STRSAME
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251786
localization_priority: Normal
ms.assetid: d9fc2007-cc21-b20c-adee-be87cc356753
description: Определяет, одинаковы ли строки. Возвращает значение TRUE, если они совпадают с и значение FALSE, если они не.
ms.openlocfilehash: 5365ce6e679f708a47f4bcbdebbc4cabb13a2aee
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814944"
---
# <a name="strsame-function"></a>Функция STRSAME

Определяет, одинаковы ли строки. Возвращает значение TRUE, если они совпадают с и значение FALSE, если они не. 
  
## <a name="syntax"></a>Синтаксис

STRSAME (» ** *string1* ** «,» ** *string2* ** «, ** *ignoreCase* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _string1_ <br/> |Обязательный  <br/> |**Строка** <br/> |Первая строка для сравнения.  <br/> |
| _Строка string2_ <br/> |Обязательный  <br/> |**Строка** <br/> |Вторая строка для сравнения.  <br/> |
| _ignoreCase_ <br/> |Optional  <br/> |**Boolean** <br/> |Значение TRUE, следует ли игнорировать регистр и значение FALSE для сравнения регистр. Значение по умолчанию — FALSE.  <br/> |
   
### <a name="return-value"></a>������������ ��������

Логический
  
## <a name="remarks"></a>Замечания

Для сравнения строк из нескольких байтов или сравнений с использованием правил регистра для определенного языкового стандарта, используйте функцию STRSAMEEX.
  
## <a name="example-1"></a>Пример 1

STRSAME("CAT","dog")
  
Возвращает значение FALSE.
  
## <a name="example-2"></a>Пример 2

STRSAME("CAT","CAT")
  
Возвращает значение TRUE.
  
## <a name="example-3"></a>Пример 3

STRSAME («cat», «cat», значение TRUE)
  
Возвращает значение TRUE.
  
## <a name="example-4"></a>Пример 4

STRSAME("CAT","CAT")
  
Возвращает значение FALSE.
  
## <a name="example-5"></a>Пример 5

STRSAME (слово "кошка", "Кот", значение TRUE)
  
Возвращает значение TRUE.
  
## <a name="example-6"></a>В примере 6

STRSAME ("cät," кот", значение TRUE)
  
Возвращает значение FALSE.
  
## <a name="example-7"></a>Пример 7

STRSAME ("cät," CÄT", значение TRUE)
  
Возвращает значение TRUE.
  

