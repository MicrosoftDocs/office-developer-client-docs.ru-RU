---
title: FtNegFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtNegFt
api_type:
- COM
ms.assetid: 639a408c-aed1-456b-9f75-9d6fb8dcb33b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: db208dad8697060e394b3ee037ea658cefbab669
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423386"
---
# <a name="ftnegft"></a>FtNegFt

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Вычисляет дополнение для двух неподписанного 64 — разрядного целого числа. 
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |Мапиутил. h  <br/> |
|Реализовано в:  <br/> |MAPI  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения и поставщики услуг  <br/> |
   
```cpp
FILETIME FtNegFt(
  FILETIME ft
);
```

## <a name="parameters"></a>Параметры

 _метр_
  
> возврата Структура [fileTime](filetime.md) , которая содержит неподписанное 64 — разрядное целое число, для которого вычисляется дополнение к двум. 
    
## <a name="return-value"></a>Возвращаемое значение

Функция **фтнегфт** возвращает структуру **fileTime** , которая содержит дополнение до двух элементов целого числа. Входной параметр остается неизменным. 
  

