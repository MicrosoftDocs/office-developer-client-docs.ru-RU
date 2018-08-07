---
title: Функция REPT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027335
localization_priority: Normal
ms.assetid: 53362a32-ac27-42a3-ace1-c6184ab20b52
description: Повторяет текст заданное количество раз.
ms.openlocfilehash: 761f2f95824d5bdab4995b2867bfeac6be64bc12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814628"
---
# <a name="rept-function"></a>Функция REPT

Повторяет текст заданное количество раз. 
  
## <a name="syntax"></a>Синтаксис

Повтор (** *текст* **, ** *сколько_раз* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _text_ <br/> |Обязательный  <br/> |**Строка** <br/> | Текст, который необходимо повторить.  <br/> |
| _Сколько_раз_ <br/> |Обязательный  <br/> |**Число** <br/> |Положительное число, определяющее, сколько раз необходимо повторить текст.  <br/> |
   
## <a name="remarks"></a>Замечания

Если *сколько_раз* : 
  
- Нуль (0), то функция ПОВТОР возвращает «» (пустая строка).
    
- Не interger, оно сокращается.
    
## <a name="example"></a>Пример

Повтор (»\*«, 5) 
  
Возвращает \* \* \* \* \*. 
  

