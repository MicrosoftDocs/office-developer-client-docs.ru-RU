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
description: Определяет, совпадают ли строки. Он возвращает значение TRUE, если они одинаковы, и значение FALSE в противном случае.
ms.openlocfilehash: 0f298c966ec7a3f1e23c89473fecc555ed950f79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428685"
---
# <a name="strsame-function"></a>Функция STRSAME

Определяет, совпадают ли строки. Он возвращает значение TRUE, если они одинаковы, и значение FALSE в противном случае. 
  
## <a name="syntax"></a>Синтаксис

STRSAME ("* * *строка_поиска* * *", "* * *строка2* * *", * * *ignoreCase* * *) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _строка1_ <br/> |Обязательный  <br/> |**String** <br/> |Первая сравниваемая строка.  <br/> |
| _строка2_ <br/> |Обязательный  <br/> |**String** <br/> |Вторая сравниваемая строка.  <br/> |
| _ignoreCase_ <br/> |Необязательный  <br/> |**Логический** <br/> |Значение TRUE, чтобы игнорировать регистр и значение FALSE, чтобы сравнить регистр. Значение по умолчанию — FALSE.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

Boolean
  
## <a name="remarks"></a>Примечания

Чтобы сравнить многобайтовые строки или выполнить сравнения с использованием правил для определенного языкового стандарта, используйте функцию STRSAMEEX.
  
## <a name="example-1"></a>Пример 1

STRSAME ("Cat", "собака")
  
Возвращает значение FALSE.
  
## <a name="example-2"></a>Пример 2

STRSAME ("Cat", "Cat")
  
Возвращает значение TRUE.
  
## <a name="example-3"></a>Пример 3

STRSAME ("Cat", "Cat", TRUE)
  
Возвращает значение TRUE.
  
## <a name="example-4"></a>Пример 4

STRSAME ("Cat", "CAT")
  
Возвращает значение FALSE.
  
## <a name="example-5"></a>Пример 5

STRSAME ("Cat", "CAT", TRUE)
  
Возвращает значение TRUE.
  
## <a name="example-6"></a>Пример 6

STRSAME ("кäт", "CAT", TRUE)
  
Возвращает значение FALSE.
  
## <a name="example-7"></a>Пример 7

STRSAME ("кäт", "КÄТ", TRUE)
  
Возвращает значение TRUE.
  

