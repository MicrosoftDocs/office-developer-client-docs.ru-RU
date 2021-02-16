---
title: Функция UNICHAR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60117
localization_priority: Normal
ms.assetid: 371a475d-50f7-6b4c-4b47-581cd778dcba
description: Возвращает символ Юникода из числа.
ms.openlocfilehash: 81e76b72da35f79dee9ad6afbde51bc2e228483c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417583"
---
# <a name="unichar-function"></a>Функция UNICHAR

Возвращает символ Юникода из числа. 
  
## <a name="syntax"></a>Синтаксис

UNICHAR (** *number* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _число_ <br/> |Обязательна  <br/> |64-разрядное целое число. <br/> |В качестве возвращаемой функцией функции может быть несколько часов от 1 до 65 535 (включительно).  <br/> |
   
## <a name="remarks"></a>Примечания

Итоговая строка имеет один символ Юникода (два символа) в длину. 
  
## <a name="example"></a>Пример

UNICHAR(65) 
  
Возвращает A (латинская буква A) 
  

