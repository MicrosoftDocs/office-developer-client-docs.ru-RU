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
description: Возвращает символ Юникод из номера.
ms.openlocfilehash: 81e76b72da35f79dee9ad6afbde51bc2e228483c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417583"
---
# <a name="unichar-function"></a>Функция UNICHAR

Возвращает символ Юникод из номера. 
  
## <a name="syntax"></a>Синтаксис

UNICHAR (** *номер* ** ) 
  
### <a name="parameters"></a>Параметры

|**Имя**|**Необходимость**|**Тип данных**|**Описание**|
|:-----|:-----|:-----|:-----|
| _число_ <br/> |Обязательный  <br/> |**Integer** <br/> |В системе от 1 до 65 535 (включительно) или функция возвращает ошибку.  <br/> |
   
## <a name="remarks"></a>Примечания

В результате строка является одним символом Юникод (два символа) в длину. 
  
## <a name="example"></a>Пример

UNICHAR (65) 
  
Возвращает букву A (Латинская буква A) 
  

