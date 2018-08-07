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
description: Возвращает символ Unicode из числа.
ms.openlocfilehash: 06f97717ee4d5965253b0da7cfd5c35faf0ca2f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815104"
---
# <a name="unichar-function"></a>Функция UNICHAR

Возвращает символ Unicode из числа. 
  
## <a name="syntax"></a>Синтаксис

UNICHAR (** *номер* **) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Обязательный или необязательный**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |Обязательный  <br/> |**Integer** <br/> |Целое число от 1 до 65 535 (включительно) или функцию возвращает ошибку.  <br/> |
   
## <a name="remarks"></a>Замечания

Результирующую строку — один символ Unicode (двух знаков) в длину. 
  
## <a name="example"></a>Пример

UNICHAR(65) 
  
Возвращает (прописная латинская буква A) 
  

