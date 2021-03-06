---
title: Функция BITNOT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251399
localization_priority: Normal
ms.assetid: 7b6486bb-3618-3747-4b00-93bd55767c1c
description: Возвращает 16-битный двоичный номер, в котором каждый бит устанавливается до 1, только если соответствующий бит в двоичном номере — 0. В противном случае для бита установлено 0.
ms.openlocfilehash: 34ea6fd614feae8e3c8e97e34b7ff6c531f4c123
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438836"
---
# <a name="bitnot-function"></a>Функция BITNOT

Возвращает 16-битный двоичный номер, в котором каждый бит устанавливается до 1, только если соответствующий бит в двоичном номере — 0. В противном случае для бита установлено 0.
  
## <a name="syntax"></a>Синтаксис

BITNOT(** *двоичный номер* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _двоичный номер_ <br/> |Обязательный  <br/> |**Числовой** <br/> |16-битный двоичный номер.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

16-битная двоичная
  
## <a name="example"></a>Пример

BITNOT(6)
  
Возвращает 65529. 6 = 0...00110. Таким образом, BITNOT(6) = 1...11001.
  

