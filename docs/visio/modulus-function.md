---
title: Функция MODULUS
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251465
localization_priority: Normal
ms.assetid: cb6326a5-1bf8-b6a3-5c0d-d38c071353a5
description: Возвращает остаток (modulus), который приводит к разделению номера разделителем.
ms.openlocfilehash: f6b713b1b3a9d2afa85f49de9d451642a00d8dad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429273"
---
# <a name="modulus-function"></a>Функция MODULUS

Возвращает остаток (modulus), который приводит к разделению номера разделителем.
  
## <a name="syntax"></a>Синтаксис

НОМЕР MODULUS(** ***,* ** *divisor* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _число_ <br/> |Обязательный  <br/> |**Number** <br/> |Дивиденд.  <br/> |
| _divisor_ <br/> |Обязательный  <br/> |**Number** <br/> |Дивизор.  <br/> |
   
### <a name="return-value"></a>Возвращаемое значение

Номер
  
## <a name="remarks"></a>Примечания

Результат имеет тот же знак, что и дивизор. A #DIV/0! ошибка возвращается, если раздвиватель 0. 
  
Почти во всех ситуациях следует использовать функцию MODULUS, а не функцию MOD. 
  
## <a name="example-1"></a>Пример 1

MODULUS (5, 1.4)
  
Возвращает 0.8.
  
## <a name="example-2"></a>Пример 2

MODULUS(5, -1.4)
  
Возвращает -0.6.
  
## <a name="example-3"></a>Пример 3

MODULUS(-5, 1.4)
  
Возвращает 0.6.
  
## <a name="example-4"></a>Пример 4

MODULUS(-5, -1.4)
  
Возвращает -0.8.
  

