---
title: Функция CHAR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251406
localization_priority: Normal
ms.assetid: 0803d5d3-d804-5ffe-604d-661b35d1fc01
description: Возвращает символ ANSI для номера.
ms.openlocfilehash: 6f1c459892331ec30ad93bbc860fcd038e8f4732
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418192"
---
# <a name="char-function"></a>Функция CHAR

Возвращает символ ANSI для номера.
  
## <a name="syntax"></a>Синтаксис

CHAR(** *номер* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _число_ <br/> |Обязательный  <br/> |**Number** <br/> |Номер, символ ANSI которого вы хотите получить.  <br/> |
   
## <a name="remarks"></a>Примечания

В результате строка — это один символ в длину. Параметр  _номера_ должен быть не более 1 и 255 (включительно), либо функция возвращает ошибку. 
  
## <a name="example"></a>Пример

CHAR (9) 
  
Возвращает символ вкладки. 
  

