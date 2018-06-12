---
title: Функция ВЕЛИЧИНЫ
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251461
localization_priority: Normal
ms.assetid: 9f443687-9861-5f51-94c4-f056805f736b
description: Возвращает модуль, развитием — A, а чьи запуск — B, умноженное на соответствующие константы constantA и constantB.
ms.openlocfilehash: f4c428b8b381af58958dab66a71ddd0bcaf715c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814189"
---
# <a name="magnitude-function"></a>Функция ВЕЛИЧИНЫ

Возвращает модуль, развитием — _A_ , а чьи запуск — _B_, умноженное на соответствующие константы _constantA_ и _constantB_. 
  
## <a name="syntax"></a>Синтаксис

ВЕЛИЧИНА (** *constantA* **, ** *A* **, ** *constantB* **, ** *B* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _constantA_ <br/> |Обязательный  <br/> |**Число** <br/> |Константа, на который умножается увеличение.  <br/> |
| _A_ <br/> |Обязательный  <br/> |**Число** <br/> |Увеличение.  <br/> |
| _constantB_ <br/> |Обязательный  <br/> |**Число** <br/> |Константа, на который умножается запустить.  <br/> |
| _B_ <br/> |Обязательный  <br/> |**Число** <br/> |Запустить.  <br/> |
   
## <a name="remarks"></a>Замечания

ВЕЛИЧИНА рассчитывается по следующей формуле:
  
КОРЕНЬ ((constantA \* A) ^ 2 + (constantB \* Б) ^ 2)
  
## <a name="example"></a>Пример

ВЕЛИЧИНА (1, 3, 1, 4) 
  
Возвращает 5. 
  

