---
title: Функция BITAND
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251398
localization_priority: Normal
ms.assetid: c437de23-d2e0-469d-62e6-8eb8b8cfea5c
description: Возвращает 16-разрядный двоичное число, в котором каждый бит равен 1 только в том случае, если соответствующий бит в binarynumber1 и binarynumber2 — 1. В противном случае бит равен 0.
ms.openlocfilehash: 0b501bb383596e3f2f39ea14f2cb9eb4bf40b25b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813250"
---
# <a name="bitand-function"></a>Функция BITAND

Возвращает 16-разрядный двоичное число, в котором каждый бит равен 1 только в том случае, если соответствующий бит в binarynumber1 и binarynumber2 — 1. В противном случае бит равен 0. 
  
## <a name="syntax"></a>Синтаксис

BITAND (** *binarynumber1* **, ** *binarynumber2* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _двоичные Число1_ <br/> |Обязательный  <br/> |**Числовой** <br/> |Первый номер двоичные 16-разрядной.  <br/> |
| _двоичные число2_ <br/> |Обязательный  <br/> |**Числовой** <br/> |Второй 16-разрядное число двоичные.  <br/> |
   
## <a name="remarks"></a>Замечания

Эта функция используется для тестирования и изменения свойств фигуры, которые хранятся в виде битовой маски, например, текстовый формат фигуры.
  
## <a name="example"></a>Пример

BITAND(12,6)
  
Возвращает 4. 12 = 0... 01100. 6 = 0... 00110. Таким образом, BITAND(12,6) = 0... 00100.
  

